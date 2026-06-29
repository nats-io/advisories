## NATS Advisories

#### 2026-06

* [Security Note 2026-16](CVE/secnote-2026-16.txt)
  + nats-server: Route API Auth Bypass
  + `GHSA-38x3-76xf-cq45`
  + _2026-06-29_

* [Security Note 2026-17](CVE/secnote-2026-17.txt)
  + nats-server: Subscribe Authz Bypass via Wildcard-Overlap
  + `GHSA-wh7g-5m82-pmhr`
  + _2026-06-29_

* [Security Note 2026-18](CVE/secnote-2026-18.txt)
  + nats-server: Queue Subscribe Authz Bypass
  + `GHSA-jx8g-9g95-6322`
  + _2026-06-29_

* [Security Note 2026-19](CVE/secnote-2026-19.txt)
  + nats-server: Pre-auth server crash via double INFO in leafnode handshake: incomplete fix for CVE-2026-29785 and CVE-2026-33218
  + `GHSA-3g5q-cfh2-cq67`
  + _2026-06-29_

* [Security Note 2026-20](CVE/secnote-2026-20.txt)
  + nats-server: Incomplete fix for CVE-2026-33249: Leaf node connections bypass Nats-Trace-Dest permission check
  + `GHSA-p3j5-5hrq-p75h`
  + _2026-06-29_

* [Security Note 2026-21](CVE/secnote-2026-21.txt)
  + nats-server: MQTT subscribe ACL bypass via $MQTT.deliver.pubrel prefix (incomplete fix for CVE-2026-33217)
  + `GHSA-4g68-3pwx-5vfj`
  + _2026-06-29_

* [Security Note 2026-22](CVE/secnote-2026-22.txt)
  + nats-server: MQTT SUBSCRIBE Protocol Injection via Leaf Node/Route Forwarding allows arbitrary NATS command injection
  + `GHSA-qrcv-3558-gj4f`
  + _2026-06-29_

* [Security Note 2026-23](CVE/secnote-2026-23.txt)
  + nats-server: Pre-auth panic and server hang via malformed JWT issuer (missing Ed25519 length check in nkeys)
  + `GHSA-g33f-6538-grxh`
  + _2026-06-29_

* [Security Note 2026-24](CVE/secnote-2026-24.txt)
  + nats-server: `no_auth_user` pre-CONNECT fast path bypasses user connection restrictions
  + `GHSA-hmmp-q8cx-v964`
  + _2026-06-29_

* [Security Note 2026-25](CVE/secnote-2026-25.txt)
  + nats-server: MQTT partial CONNECT packets can exhaust pre-auth memory
  + `GHSA-r72h-j7qq-v6qg`
  + _2026-06-29_

* [Security Note 2026-26](CVE/secnote-2026-26.txt)
  + nats-server: MQTT retained and QoS replay bypass subscribe deny filters
  + `GHSA-7qmq-8cc4-hxwg`
  + _2026-06-29_

* [Security Note 2026-27](CVE/secnote-2026-27.txt)
  + nats-server: MQTT-over-WebSocket Path Can Crash WebSocket-Only JetStream Servers Before MQTT Is Enabled
  + `GHSA-p957-7v2w-g93g`
  + _2026-06-29_

* [Security Note 2026-28](CVE/secnote-2026-28.txt)
  + nats-server: Remote crash via integer overflow in Connz pagination
  + `GHSA-q59r-vq66-pxc2`
  + _2026-06-29_

----------------------------------------

#### 2026-03

* [Security Note 2026-05](CVE/secnote-2026-05.txt)
  + nats-server: MQTT plaintext password disclosure
  + `CVE-2026-33216` ; `GHSA-v722-jcv5-w7mc`
  + _2026-03-24_

* [Security Note 2026-06](CVE/secnote-2026-06.txt)
  + nats-server: MQTT hijacking via Client ID
  + `CVE-2026-33215` ; `GHSA-fcjp-h8cc-6879`
  + _2026-03-24_

* [Security Note 2026-07](CVE/secnote-2026-07.txt)
  + nats-server: MQTT ACLs ineffective
  + `CVE-2026-33217` ; `GHSA-jxxm-27vp-c3m5`
  + _2026-03-24_

* [Security Note 2026-08](CVE/secnote-2026-08.txt)
  + nats-server: Leafnode spoofing of Nats-Request-Info identity information
  + `CVE-2026-33246` ; `GHSA-55h8-8g96-x4hj`
  + _2026-03-24_

* [Security Note 2026-09](CVE/secnote-2026-09.txt)
  + nats-server: Internal identity header Nats-Request-Info spoofable
  + `CVE-2026-33223` ; `GHSA-pwx7-fx9r-hr4h`
  + _2026-03-24_

* [Security Note 2026-10](CVE/secnote-2026-10.txt)
  + nats-server: Pre-auth server panic in leafnode handling
  + `CVE-2026-33218` ; `GHSA-vprv-35vv-q339`
  + _2026-03-24_

* [Security Note 2026-11](CVE/secnote-2026-11.txt)
  + nats-server: WebSockets pre-auth DoS
  + `CVE-2026-33219` ; `GHSA-8r68-gvr4-jh7j`
  + _2026-03-24_

* [Security Note 2026-12](CVE/secnote-2026-12.txt)
  + nats-server: JetStream: Stream restore endpoint auth bypass
  + `CVE-2026-33222` ; `GHSA-9983-vrx2-fg9c`
  + _2026-03-24_

* [Security Note 2026-13](CVE/secnote-2026-13.txt)
  + nats-server: mTLS DN-based identity auth bypass for some DN patterns
  + `CVE-2026-33248` ; `GHSA-3f24-pcvm-5jqc`
  + _2026-03-24_

* [Security Note 2026-14](CVE/secnote-2026-14.txt)
  + nats-server: credentials via command-line argv exposed to monitoring
  + `CVE-2026-33247` ; `GHSA-x6g4-f6q3-fqvv`
  + _2026-03-24_

* [Security Note 2026-15](CVE/secnote-2026-15.txt)
  + nats-server: Message tracing can be redirected to arbitrary subject
  + `CVE-2026-33249` ; `GHSA-8m2x-3m6q-6w8j`
  + _2026-03-24_

----------------------------------------

#### Older

* [Security Note 2026-04](CVE/secnote-2026-04.txt)
  + nats-server leafnodes pre-auth server panic
  + `CVE-2026-29785` ; `GHSA-52jh-2xxh-pwh6`
  + _2026-03-09_
* [Security Note 2026-03](CVE/secnote-2026-03.txt)
  + nats-server WebSockets pre-auth remote server crash
  + `CVE-2026-27889` ; `GHSA-pq2q-rcw4-3hr6`
  + _2026-03-09_
* [Security Note 2026-02](CVE/secnote-2026-02.txt)
  + nats-server websockets pre-auth memory DoS
  + `CVE-2026-27571` ; `GHSA-qrvq-68c2-7grw`
  + _2026-02-23_
* [Security Note 2026-01](CVE/secnote-2026-01.txt)
  + Golang TLS bug affecting rare configurations
  + `CVE-2025-68121` (Golang)
  + _2026-02-04_
* [Security Note 2025-01](CVE/secnote-2025-01.txt)
  + `CVE-2025-30215`; `GHSA-fhg8-qxh5-7q3w`; `GO-2025-3600`
  + _2025-04-08_
* [Security Note 2023-02](CVE/secnote-2023-02.txt) (aka CVE-2023-46129)
  + nkeys: xkeys Seal encryption used fixed key for all encryption
  + `CVE-2023-46129`; `GHSA-mr45-rx8q-wcm9`
  + _2023-10-26_
* [Security Note 2023-01](CVE/secnote-2023-01.txt)
  + Adding accounts for just the system account adds auth bypass
  + `CVE-2023-47090`; `GHSA-fr2g-9hjm-wr23`; `GO-2023-2133`
  + _2023-10-12_
* [CVE-2022-42708](CVE/CVE-2022-42708.txt)
  + Server panic from inappropriate JetStream replica count
  + _2022-10-10_
* [CVE-2022-42709](CVE/CVE-2022-42709.txt)
  + Server panic from Account import loops, similar to [CVE-2020-28466](CVE/CVE-2020-28466.txt)
  + _2022-10-10_
* [CVE-2022-29946](CVE/CVE-2022-29946.txt)
  + Negative user permissions not enforced in one scenario
  + _2022-05-04_
* [CVE-2022-28357](CVE/CVE-2022-28357.txt)
  + Arbitrary file write from the privileged system account
  + _2022-04-18_
* [CVE-2022-26652](CVE/CVE-2022-26652.txt)
  + Arbitrary file write by JetStream-enabled users
  + _2022-03-09_
* [CVE-2022-24450](CVE/CVE-2022-24450.txt)
  + Unconstrained account assumption by authenticated clients (CRITICAL)
  + _2022-02-07_
* [CVE-2021-32026](CVE/CVE-2021-32026.txt)
  + TLS missing ciphersuite settings when CLI flags used (v.low severity)
  + _2021-05-04_
* [CVE-2021-3127](CVE/CVE-2021-3127.txt)
  + Import token permissions checking not enforced
  + _2021-03-15_
* [CVE-2020-28466](CVE/CVE-2020-28466.txt)
  + Account service import loop caused nats-server DoS
  + NATS server upgrade required to avoid Denial-of-Service
  + _2021-03-15_
  + See also: [CVE-2022-42709](CVE/CVE-2022-42709.txt)
* [CVE-2020-26521](CVE/CVE-2020-26521.txt)
  + Nil deref in JWT library, causing Go panic
  + NATS server upgrade required to avoid Denial-of-Service
  + _2020-11-02_
* [CVE-2020-26892](CVE/CVE-2020-26892.txt)
  + Incorrect credential expiration handling via JWT library
  + API fixes needed by library users
  + NATS server upgrade required for expiration to work
  + _2020-11-02_
* [CVE-2020-26149](CVE/CVE-2020-26149.txt)
  + Information disclosure in JS client libraries
  + [MITRE](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-26149)
  + _2020-09-29_

## Exposure Statements

* [log4j CVE-2021-44228](statements/log4j)
  + aka Log4Shell, aka LogJam
  + Statement for security teams about the exposure of the NATS ecosystem
