# Meridian Protocol
**Web Preservation, Mirroring, and DNS Failover**
`draft-darley-meridian-protocol-01`

---

## Background

This protocol is introduced in [Field Note #8 — The Stack That Should Have Been Networked](https://propertools.be/fieldwork/field-note-8-the-stack-that-should-have-been-networked/).

---

## Problem

The web has no native mechanism for author-authorized preservation, verifiable mirroring, or continuity at canonical URLs after origin failure. When a domain lapses, a server is decommissioned, or an author dies, content disappears from its canonical URLs without recourse.

Meridian proposes three minimal, composable pieces to address this:

- A **signed site manifest format** — a cryptographically verifiable asset graph authored and signed by the site owner
- A **delta-synchronisation mechanism** — so authorised mirrors stay current with minimal bandwidth
- A **new DNS resource record type (MIRROR RR)** — supporting automatic failover to live mirrors when an origin becomes unavailable

```
Author → Manifest → Mirrors
                        ↓
                 DNS (MIRROR RR)
                        ↓
                     Clients
```

It does not reinvent WARC, IPFS, WebSub, or DNSSEC. It composes them. It adds what they do not provide: prospective author consent, signed asset integrity, and URL continuity after origin failure.

---

## Current Draft

[`draft-darley-meridian-protocol-01.txt`](./draft-darley-meridian-protocol-01.txt)

- **Intended status:** Proposed Standard
- **Expires:** 2026-09-27

---

## Status

This is an early-stage Internet-Draft. The protocol is stable enough for discussion and early prototyping, but not yet suitable for production deployment. It has been shared with members of the IETF community and is being developed in the open.

Critical feedback is welcome. We do not claim completion, sufficiency, or perfection. If you see a way to do something more elegantly, say so.

We are trying to build the system that would have deserved Bill's trust.

---

## Getting Involved

We are actively seeking:

- **Co-authors** — particularly those with experience in DNS, web archival, digital preservation, or infrastructure standards
- **Implementers** — anyone interested in building prototype implementations of the manifest format, delta-sync, or MIRROR RR
- **Mirror operators** — organisations willing to operate authorised mirrors as the protocol matures
- **Reviewers** — DNS, web archival, security, and standards perspectives all welcome

To contribute:

1. Read the draft
2. Open an issue to raise a question, flag a problem, or propose a change
3. See [CONTRIBUTING.md](./CONTRIBUTING.md) for contribution guidelines
4. Or contact the author directly at [trey@propertools.be](mailto:trey@propertools.be)

More information at [propertools.be/commons/](https://propertools.be/commons/)

---

## Dedication

This protocol is dedicated to the memory of **William Dana Atkinson** (1951–2025), creator of HyperCard, who demonstrated that ordinary people could author rich, navigable hypermedia systems and who gave his creation to the world without reservation. The network layer Bill wished he had built is long overdue.

And to the memory of **Aaron Swartz** (1986–2013), who believed that knowledge on the web should be free and permanent, and paid for that belief.

---

## License

The Meridian Protocol specification text is subject to the IETF Trust's legal provisions per BCP 78, as stated in the document itself.

This repository — including the README, CONTRIBUTING guide, and any supporting materials — is licensed under the [MIT License](./LICENSE).

Implementations of the protocol are not subject to any license from this repository. You are free to implement Meridian in any language, under any license, without restriction.

---

*Trey Darley · Proper Tools SRL · Brussels*
