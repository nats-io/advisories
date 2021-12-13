Apache Log4j 2 Java library
===========================

_2021-12-13_

Regarding `CVE-2021-44228`, aka “Log4Shell”, aka “LogJam”, a
security-impacting bug of text re-interpolation over untrusted data in the
Log4j v2 library:

* The NATS service is written in Go
* NATS client libraries are written in a variety of languages, but the core ecosystem is written in Go
* The direct client library for Java,
  [nats.java](https://github.com/nats-io/nats.java),
  does not use or reference log4j; but like any code which logs in Java, the
  developer using the library can use injection to setup log4j as the logging
  framework.
  + By the very design of code injection as a development pattern, this is
    outside of the control of the NATS Maintainers and all we can do is
    acknowledge that "someone might have done that".
* One repository, the
  [nats-jms-bridge](https://github.com/nats-io/nats-jms-bridge),
  contains an admin console which transitively depends upon log4j; this admin
  console is for privileged access.
  + The admin console is not built by default with any particular version of
    log4j, but the integration test script would set up a classpath which
    contained a vulnerable version.  This has been
    [fixed in PR/290](https://github.com/nats-io/nats-jms-bridge/pull/290).
* The NATS components will log data in various error scenarios, or when debug
  or trace level logging is enabled; the escaping used is to protect against
  string rendering attacks such as newlines leading to log-line injection, and
  would not sanitize most exploit strings for CVE-2021-44228.
  As such, the NATS server, like most service software not written in Java,
  can be a pass-through vector for log-strings containing a malicious payload:
  the expected contract of logging systems is that this should be safe.
  + Anyone using log-processing software written in a language targeting the
    JVM should be examining that software for expose.
  + The NATS maintainers consider this to be outside of our scope of
    responsibility.  We will continue to log as appropriate, redacting secrets
    and protecting line-based logs against newline injections, but not
    otherwise filtering.
