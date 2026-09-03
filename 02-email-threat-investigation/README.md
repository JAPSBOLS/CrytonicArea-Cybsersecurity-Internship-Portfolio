# Project 02 — Email Threat Investigation & Analysis

## Objective
Investigate a mailbox of 13 recovered emails (legitimate and malicious mixed
together) following a suspected fraud attempt, and produce a professional
threat investigation report.

## Scenario
Emails recovered from a finance executive's mailbox after unusual activity
was flagged. Each email needed individual header, content, and link/
attachment analysis to determine legitimacy.

## Methodology
For every email, evaluated:
- Sender address vs. display name, and Reply-To/Return-Path consistency
- SPF/DKIM/DMARC authentication results
- Domain legitimacy (lookalike/typosquat detection)
- Embedded link destinations vs. displayed text
- Attachment type and risk (e.g. macro-enabled documents, archives)
- Social engineering tactics used (urgency, authority, secrecy, greed)

## Key Findings
- **5 of 13 emails** were verified safe (internal domains, clean auth, no
  manipulation tactics).
- **6 of 13 emails** were confirmed malicious, including: a credential-
  harvesting fake IT alert, a CEO wire-transfer fraud (BEC) attempt, a
  typosquatted fake Microsoft security alert, a gift-card fraud impersonating
  a CFO, an advance-fee lottery scam, and a macro-malware invoice attachment.
- **2 emails** were flagged suspicious despite passing authentication — the
  common thread was a **Reply-To address that didn't match the From domain**,
  which would silently route any reply to an attacker instead of the real sender.

## Skills Demonstrated
`Email header forensics` `Phishing/BEC detection` `IOC extraction`
`Social engineering pattern recognition` `Risk classification`

## Tools & Concepts Used
SPF/DKIM/DMARC analysis, OSINT verification concepts (VirusTotal, urlscan.io,
MXToolbox)

---
*Note: Original email case file is confidential to the Cryptonic Area
internship program and is not published here.*
