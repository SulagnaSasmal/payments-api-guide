# PayPlus REST API — Developer Reference

**A documentation portfolio project by Sulagna Sasmal — Senior Technical Writer | Documentation Architect**

[![Live Site](https://img.shields.io/badge/Live%20Site-sulagnasasmal.github.io-E8A84C?style=flat-square&logo=githubpages&logoColor=black)](https://sulagnasasmal.github.io/payments-api-guide/)
[![GitHub Repo](https://img.shields.io/badge/GitHub-payments--api--guide-181717?style=flat-square&logo=github)](https://github.com/SulagnaSasmal/payments-api-guide)

---

## About This Project

This is a fully authored developer API reference for a fictional enterprise payment hub REST API — **PayPlus REST API v2.1**. It demonstrates developer-facing API documentation for a regulated FinTech product covering all major US payment rails.

**Documentation style:** Developer API reference (Stripe / Plaid-inspired HTML structure)
**Audience:** Integration developers, core banking engineers, fintech teams
**Companion project:** [PayPlus Admin Guide](../payplus-admin-guide/) — the system administration documentation for the same platform

---

## What's Documented

| Section | Description |
|---|---|
| [Overview & Authentication](index.html) | API overview, OAuth 2.0 client credentials, API key auth, request/response format, rate limiting, environments, versioning |
| [ACH Payments](ach.html) | Initiate ACH credit/debit (PPD, CCD, CTX, WEB, TEL, IAT), submit batch files, get payment status, retrieve return details (R01–R85), initiate reversals |
| [Instant Payments — RTP / FedNow](instant.html) | Initiate real-time credit transfers (synchronous API response), get status, send Request for Payment (RfP), RfP status, rail auto-selection logic |
| [Wire Transfers — Fedwire / SWIFT](wire.html) | Initiate Fedwire (ISO 20022 pacs.008) and SWIFT transfers, get wire status, request payment recall (camt.056), recall status |
| [Webhooks](webhooks.html) | Register endpoints, HMAC-SHA256 signature verification, event reference (payment.settled, payment.returned, compliance.hold, rfp.fulfilled, etc.), retry logic, payload examples |
| [Error Codes](errors.html) | HTTP status codes, error response format, validation errors, auth errors, payment business rule errors, ACH return codes (R01–R85), ISO 20022 return codes, OFAC/compliance errors |

---

## Documentation Approach

This guide demonstrates:

- **Authentic API documentation depth** — not a capabilities overview. Documents request parameters (required/optional), response schemas, payment lifecycle states, idempotency handling, synchronous vs. asynchronous patterns, and webhook delivery.
- **Regulatory compliance context** — ISO 20022 pacs.008/pacs.009 message fields, BSA Travel Rule field requirements, OFAC compliance workflow, ACH return codes with re-presentment eligibility.
- **Developer-facing style** — code examples (JSON request/response), HTTP method badges, parameter tables, error handling guidance, and implementation patterns. Structured for developers integrating PayPlus into core banking or payment orchestration systems.
- **Dual-rail instant payment design** — documents the RTP vs. FedNow auto-selection logic, synchronous API response pattern for instant payments, and irrevocability handling.

---

## Companion Documentation

This project is part of a payments documentation suite:

- **[PayPlus Admin Guide](https://sulagnasasmal.github.io/payplus-admin-guide/)** — System administration, installation, user management, connector configuration, workflow engine, compliance configuration, and troubleshooting for the PayPlus Enterprise payment hub.
- **[US Payments Hub](https://sulagnasasmal.github.io/us-payments-hub/)** — Operations and compliance reference covering all 6 US payment rails (ACH, Fedwire, SWIFT, RTP, FedNow, Card Networks).

---

## Background

This project draws on real-world experience:

- **Fundtech India (2008–2010):** Documented CashIn and Global CASHplus — enterprise payment hub systems that are direct predecessors of Finastra GlobalPAYplus. The API structure here reflects that class of payment hub integration pattern.
- **NICE Actimize (2017–present):** API documentation for financial crime prevention platforms with complex integration requirements — informing the compliance webhook and error handling sections.

---

## Author

**Sulagna Sasmal**
Senior Specialist Technical Writer | Documentation Architect
19+ years in FinTech, enterprise SaaS, and financial systems documentation
[Portfolio](https://sulagnasasmal.github.io/sulagnasasmal-site/) · [GitHub](https://github.com/SulagnaSasmal) · [US Payments Hub](https://sulagnasasmal.github.io/us-payments-hub/)
