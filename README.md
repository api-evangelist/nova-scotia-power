# Nova Scotia Power (nova-scotia-power)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Nova Scotia Power Incorporated (NSPI) is the investor-owned, vertically integrated regulated electric utility serving roughly half a million customers across Nova Scotia, Canada. A subsidiary of Halifax-based Emera Inc., it owns generation, transmission and distribution and is regulated by the Nova Scotia Energy and Regulatory Boards Tribunal (formerly the NSUARB). It sits at the retail end of the value chain as a franchise monopoly rather than a competitor in an open market — Nova Scotia has no wholesale market equivalent to IESO or AESO. Its API posture is the sharpest mandate-versus-implementation split in Canadian energy: section 4F of the Electricity Act, added by Bill 145 (SNS 2022, c. 12), legally required NSPI to implement the NAESB ESPI standard and be certified by the Green Button Alliance to BOTH "Connect My Data" and "Download My Data" on or before April 1, 2023. As of July 2026 the Green Button Alliance lists NSPI as certified to ESPI v3.3 for Download My Data only, with Connect My Data certification still "planned", and NSPI's own site states the Green Button Marketplace "is currently closed" to third-party applications. There is no developer portal, no published OpenAPI, no OAuth registration and no documented consumer data API — greenbutton.nspower.ca is live but every path redirects to a SAML customer login. By contrast NSPI is genuinely open on market and system data: its OASIS site publishes hourly net energy flow reports as anonymously downloadable CSV going back to 2012. Open market data, closed consumer data, and a statutory mandate whose API half is three years past its deadline.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/nova-scotia-power/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/nova-scotia-power/refs/heads/main/apis.yml)

## Tags

- Energy
- Canada
- Utilities
- Electricity
- Energy Retailer
- Green Button
- Smart Metering
- Grid
- Renewables
- Solar
- EV Charging
- Energy Markets
- Regulation

## Timestamps

- **Created:** 2026-07-27
- **Modified:** 2026-07-27

## APIs

No public, documented API is published by Nova Scotia Power.

This is recorded as an empty `apis[]` rather than filled with anything approximate. See
[review.yml](review.yml) for every URL probed and its HTTP status.

## Mandate

| | |
| --- | --- |
| **Regime** | `other` — Nova Scotia Electricity Act s. 4F, added by Bill 145 (SNS 2022, c. 12). A province-level, standard-specific Green Button mandate independent of Ontario's. |
| **Status** | `designated-not-live` |
| **Standard** | NAESB ESPI (Green Button) v3.3 |
| **Required by law** | Green Button Alliance certification to **both** Connect My Data and Download My Data, on or before **April 1, 2023** |
| **Certified today** | Download My Data only. Connect My Data "planned". |

Section 4F(5) of the Act reads:

> Nova Scotia Power Incorporated shall implement the NAESB ESPI standard and ensure that
> its implementation of the requirements set out in this Section is certified by the Green
> Button Alliance to its "Connect My Data" and "Download My Data" standards on or before
> April 1, 2023, unless granted an extension by the Board

Connect My Data is the half of Green Button that is an actual API — the authorization flow
that lets a customer grant a third-party application access to their interval data. It is
not certified, and Nova Scotia Power's own Innovation page states:

> Green Button Marketplace is currently closed. If you are a Third-Party application
> provider and wish to have your application registered and approved to be offered, please
> continue to check here for updates.

The linked third-party registration form returns HTTP 404.

## Consumer data vs market data

| | |
| --- | --- |
| **Consumer data API** | **No.** Download My Data is a file download behind SAML SSO at `greenbutton.nspower.ca` / `myaccount.nspower.ca`. No third party can obtain a customer's usage data programmatically. |
| **Open market data** | **Yes**, as bulk files. `oasis.nspower.ca` publishes hourly net energy flow reports (NS–NB interconnection, Onslow South) as CSV and HTM from 2012 through 2025, anonymously, with no login and no licence click-through. Verified: 2025 NS–NB tie CSV, HTTP 200, 253,453 bytes. |

## Access and auth

- **Access gate:** `customer-account-required`
- **Auth:** SAML 2.0 SSO via `accounts.nspower.ca`, hosted on LoginRadius. Every path on
  `greenbutton.nspower.ca` 302s to the SAML IdP.
- **OIDC discovery:** `https://accounts.nspower.ca/.well-known/openid-configuration` → HTTP 404
- **OAuth2 / API keys / mTLS:** none published
- **Self-serve signup:** none. **Sandbox:** none.

## Properties

- [Website](https://www.nspower.ca/)
- [About](https://www.nspower.ca/about-us/who-we-are)
- [Green Button](https://www.nspower.ca/cleanandgreen/innovation)
- [Green Button Portal](https://greenbutton.nspower.ca/) — SAML login wall
- [Authentication](https://accounts.nspower.ca/)
- [Customer Portal](https://myaccount.nspower.ca/)
- [OASIS Open Data](https://oasis.nspower.ca/)
- [OASIS Monthly Reports](https://www.nspower.ca/oasis/monthly-reports)
- [OASIS System Reports and Messages](https://www.nspower.ca/oasis/system-reports-messages)
- [Distribution Hosting Capacity](https://www.nspower.ca/oasis/distribution-hosting-capacity)
- [Regulatory Initiatives](https://www.nspower.ca/about-us/regulations/regulatory-initiatives)
- [Legal](https://www.nspower.ca/legal)
- [Privacy Statement](https://www.nspower.ca/privacy-statement)
- [Outage Map](https://outagemap.nspower.ca/)

## Artifacts

Nothing here is a harvested provider artifact, because Nova Scotia Power publishes none.
Each file below records what was probed and what was found, so the absence is documented
rather than assumed.

- [authentication/](authentication/nova-scotia-power-authentication.yml) — SAML 2.0 SSO via
  LoginRadius; no OAuth2, no API keys, no mTLS, no client registration. Every OIDC/OAuth
  discovery path 404s.
- [conformance/](conformance/nova-scotia-power-conformance.yml) — Green Button DMD certified
  to ESPI v3.3 (verified against the Green Button Alliance); CMD not certified. Standards
  asserted with evidence, absences recorded rather than omitted.
- [conventions/](conventions/nova-scotia-power-conventions.yml) — cross-cutting semantics for
  the bulk-file surface, plus the two undocumented vendor endpoints observed (KUBRA outage
  JSON, Sitefinity OData 401) and deliberately not listed as APIs.
- [lifecycle/](lifecycle/nova-scotia-power-lifecycle.yml) — the statutory timeline: mandate,
  deadline, partial certification, and 3 years 3 months outstanding.
- [well-known/](well-known/nova-scotia-power-well-known.yml) — every `/.well-known/` and spec
  path probed on six hosts. No discovery document exists; a `200` on the redirecting hosts is
  a landing page, not a document.
- [packages/](packages/nova-scotia-power-packages.yml) — eight registries and five GitHub org
  candidates searched. No first-party client library, no GitHub organization.
- [security/](security/nova-scotia-power-domain-security.yml) — TLS/HSTS/DNSSEC/CAA/SPF/DMARC
  probe across seven hosts. TLS 1.3 everywhere, DMARC p=reject, no DNSSEC, no CAA.
- [llms/](llms/nova-scotia-power-llms.txt) — generated llms.txt for agents.

The outage map is wired as `OutageMap`, not `StatusPage`: it is a KUBRA-hosted consumer
outage widget, not an API service-status surface.

## Maintainers

- Kin Lane — kin@apievangelist.com
