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
