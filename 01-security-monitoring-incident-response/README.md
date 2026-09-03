# Project 01 — Security Monitoring & Incident Response (Blue Team)

## Objective
Simulated a SOC analyst investigation: analyze system logs, detect a live
intrusion, build detection logic, and produce an incident response report.

## Scenario
Given two log sources (`auth.log`, `syslog.log`) from a Linux web server,
the task was to distinguish normal baseline activity from an active
compromise, and document the full incident lifecycle.

## Methodology
1. Established baseline behavior (routine cron jobs, known-user SSH sessions)
   before hunting for anomalies.
2. Correlated `auth.log` and `syslog.log` by timestamp to reconstruct a
   single, continuous attack timeline across both sources.
3. Wrote detection rules for each stage of the attack, each with a trigger
   condition, real log evidence, and justification.
4. Classified each finding by severity (Medium/High) with reasoning tied to
   actual system impact, not assumption.
5. Mapped the full incident lifecycle: Detection → Alert → Investigation →
   Response → Recovery → Closure.

## Key Findings
- **Brute-force SSH attack** from a single external IP against multiple
  usernames, succeeding after ~30 minutes.
- **Privilege escalation** via a newly created backdoor account granted
  passwordless (`NOPASSWD:ALL`) sudo access.
- **Persistence via C2 beacon** — a cron job calling out to an external
  server every 10 minutes to fetch and execute remote code.
- **Anti-forensics** — attacker wiped shell history immediately after
  privileged actions.

## Skills Demonstrated
`Log analysis` `Log correlation` `Detection engineering` `Incident
classification` `SOC incident workflow` `Linux auth/syslog forensics`

## Tools Used
VS Code (Log File Highlighter extension), `grep`, `less`, Linux terminal

---
*Note: Raw log files and the original case brief are confidential to the
Cryptonic Area internship program and are not published here.*
