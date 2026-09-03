# Project 03 — OSINT Investigation & Intelligence Gathering

## Objective
Perform Open Source Intelligence (OSINT) reconnaissance on a target website
using only publicly available tools, and produce a professional intelligence
report.

## Scenario
Given a single target URL, the task was to gather domain, hosting, and
technical footprint information, then assess it for security-relevant
observations.

## Methodology
1. Gathered domain, WHOIS, IP, DNS/nameserver, hosting, and SSL certificate
   data using public domain-intelligence tools.
2. Inspected the live site directly for technology stack indicators
   (framework, CDN usage) and metadata.
3. Cross-referenced findings against a third-party trust/reputation check.
4. Documented every finding with its source and reasoning — no claim
   without a citable origin.

## Key Findings
- Site infrastructure fully fronted by **Cloudflare**, masking the true
  origin server from direct reconnaissance.
- **WHOIS privacy protection** enabled — registrant identity not publicly
  attributable through domain records alone.
- SSL certificate is **Domain Validated (DV)** only — confirms domain
  control, not business identity.
- Site operates as an **affiliate/marketing redirect** rather than handling
  transactions directly — meaning real financial risk sits with an
  undisclosed third-party destination, not the domain investigated.

## Skills Demonstrated
`OSINT methodology` `Domain/DNS reconnaissance` `Security posture assessment`
`Source-backed reporting`

## Tools Used
Domain intelligence lookup tools, direct site inspection, public trust/
reputation checkers

---
*Note: Findings reflect information publicly available at the time of
investigation and may change if the target's infrastructure changes.*
