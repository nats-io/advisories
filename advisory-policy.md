---
title: NATS Project Security Advisory Policy
---

NATS Project Security Advisory Policy
=====================================

Broadly speaking, the NATS Project aims to make it easy for administrators to
keep track of any known security issues, using appropriate ecosystem
identifiers (such as CVE numbers) and posting both here and to appropriate
fora when there are public statements to be made.

If we know, before a fix is committed to public git, that a fix is for a
security-impacting issue, then at our discretion we will usually hold the fix
until the release is available, so that fixed code is available in compiled
forms as soon as possible.


### Languages

The primary development language of the core parts of NATS is
[Go](https://go.dev/), a type-safe compiled language with protections against
buffer overflows and many other sources of security issues.  The
[nats-server](https://github.com/nats-io/nats-server) is written in Go and
uses Go stdlib for SSL/TLS.

Client libraries are available for a broad variety of languages, with
differing security properties.


### NATS with untrusted users

Running a NATS service which is exposed to untrusted users presents a
heightened risk.

Any remote execution flaw or equivalent seriousness, or
denial-of-service by unauthenticated users, will lead to prompt releases
by the NATS maintainers.

Fixes for denial of service issues with no threat of remote execution,
when limited to those signed into an account, are likely to just be committed
to the main development branch with no special attention.  Note that a
server configuration which permits anonymous users is still using an account:
the authentication is a no-op but happens.

Those who are running services which allow untrusted users are encouraged to
build regularly from git.

None of this restriction applies to any failure mode beyond denial of service.
Issues which break account isolation boundaries for data access will
most definitely trigger our CVE process.


### Malicious servers

A server which has passed any identity checks which might exist is considered
inside a NATS client's trust boundary, but only partially within a Leafnode
server's trust boundary.

Note that a NATS client is generally processing messages from a server and
taking actions upon those messages, and has to be trusting the server to some
extent.  The majority of interactions which go wrong through bugs in the code
are Robustness issues and **not regarded as security issues**.

What does this mean?

#### For NATS clients:

 1. If you use plaintext (no TLS) then all bets are off: you are susceptible
    to the usual man-in-the-middle interceptions.
 2. If you don't hard-require TLS, then the standard NATS protocol is an
    upgrade-existing-connection STARTTLS-style protocol and subject to the
    usual downgrade attacks of such protocols.  You should hard-require TLS.
    Using a `tls://` URL scheme for specifying servers should accomplish this.
 3. If the NATS client library fails to correctly verify some aspect of the
    TLS certificate or goes wrong in the TLS handshake, that is a security
    issue in the NATS client library: it failed to ensure that it could trust
    the remote peer, when given all the data needed to do so.
 4. If the peer has a valid TLS certificate and the NATS client library
    correctly validates it, then the server is now trusted: it sends us
    messages, we act upon them.  If we crash or otherwise do something
    unexpected then this is a Robustness issue, not a Security issue.

If you have told a NATS client to talk to a malicious server, and the NATS
client has verified it is talking to a malicious server, then that is your
problem.  If you told a NATS client to talk to a safe server, and provided it
with the information that TLS must be used, then it is the NATS client's
security responsibility to ensure it is talking to the correct safe server.

#### For a NATS server as a leafnode

All the policy statements regarding a NATS client applies, but we go a little
further.  While a malicious Hub server might be able to cause us to crash, or
spin CPU or any number of other things, it **must not be able to cross our
account boundaries**.

A NATS Server offers namespaces and account boundaries.  It is expected to be
robust to all peers, whether clients connecting or a Hub server to which it is
connecting as a Leafnode.  A malicious server can cause us to crash and that
will be fixed as a Robustness issue.  But if it can cross account boundaries
then that _is_ a Security issue.

