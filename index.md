## NATS Advisories

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
