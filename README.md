# Nova Scotia Power (nova-scotia-power)

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

## Maintainers

- Kin Lane — kin@apievangelist.com
