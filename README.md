# Enterprise Help Desk Lab (osTicket)

## Project Overview

A hands-on simulation of a small enterprise IT help desk environment built to demonstrate real-world ticket lifecycle management, escalation procedures, and Windows system administration. The lab runs osTicket on an Ubuntu Server (LAMP stack) with a Windows 11 VM as the client workstation.

---

## Lab Environment

| Component | Details |
|-----------|---------|
| Ticketing System | osTicket (self-hosted) |
| Server OS | Ubuntu Server (Apache, MySQL, PHP) |
| Client OS | Windows 11 VM (VMware Fusion) |
| Virtualization | VMware Fusion |
| Network | Internal host-only network (192.168.14.x) |

**Roles simulated:** End User · IT Head (Tier 1 Lead) · IT Person (Tier 1) · Net Engineer (Tier 2)

---

## Tools & Commands Used

`net user` · `net localgroup` · `ipconfig /all` · `ipconfig /flushdns` · `ping` · `nslookup` · Windows Event Viewer (Event ID 4625, 4624) · osTicket admin panel · Ubuntu terminal · Apache/MySQL/PHP configuration

---

## Repository Structure
```
01-Lab-Architecture/        # Environment design and network diagram
02-Case-1-New-Employee/     # Account provisioning workflow
03-Case-2-Password-Reset/   # Password reset procedure
04-Case-3-Investigation/    # Authentication investigation & escalation
05-Case-4-DNS/              # DNS misconfiguration & network fix
06-Lessons-Learned/         # Reflections and skills summary
```

---

## Simulated Cases

### Case 1 — New Employee Onboarding

HR submitted a ticket to provision a workstation account for a new hire. Created the local Windows account via `net user`, assigned group membership with `net localgroup`, validated login from the user's perspective, and closed the ticket with full documentation.

**Skills shown:** User provisioning, CLI account management, ticket documentation

---

### Case 2 — Password Reset

User reported being locked out of their workstation. Followed identity verification steps before resetting credentials using `net user`. Communicated the temporary password and required an immediate change on first login.

**Skills shown:** Account management, secure credential handling, SLA-aware ticket resolution

---

### Case 3 — Account Investigation & Escalation *(most complex)*

User reported repeated "invalid credentials" errors with login delays. Rather than immediately resetting the password, I escalated to Tier 2 to rule out brute-force activity first. The Net Engineer reviewed Windows Security logs in Event Viewer, filtered on **Event ID 4625** (failed logon), examined the EventData fields (TargetUserName, FailureReason, source IP), and confirmed no external attack indicators. Password was reset only after clearance.

**Skills shown:** Security-aware escalation, Event Viewer log analysis, multi-tier ticket workflow, root cause investigation before action

> ⚠️ **Note:** Plaintext passwords visible in CMD screenshots are for lab documentation purposes only. In a production environment, credentials would be delivered through a secure out-of-band channel and never captured in screenshots or logs.

---

### Case 4 — DNS Misconfiguration

User could ping external IP addresses but could not load any websites. Diagnosed as a DNS resolution failure using `ipconfig /all` and `nslookup`. Escalated to the Network Team, corrected the DNS server settings, flushed the DNS cache with `ipconfig /flushdns`, validated the fix end-to-end, and closed the ticket.

**Skills shown:** Systematic network troubleshooting, DNS diagnosis, escalation and validation workflow

---

## Skills Demonstrated

- Full ITSM ticket lifecycle: intake → triage → escalation → resolution → closure
- Tier 1 / Tier 2 escalation with documented handoff
- Windows local user administration via command line
- Windows Event Viewer log analysis (Security log, Event ID 4625)
- DNS and network troubleshooting methodology
- Professional internal notes and customer-facing communication
- Ubuntu Server administration and LAMP stack setup

---

## Why I Built This

Most IT labs stop at "I installed the software." I wanted to simulate how IT teams actually operate — with structured ticket workflows, documented escalation decisions, and investigation before action. Case 3 in particular reflects how a security-conscious technician should handle repeated login failures: escalate first, investigate logs, then resolve.

---

**Author:** Sagarkumar Patel
| [GitHub](https://github.com/Sagarpatel9) | [LinkedIn](https://linkedin.com/in/sagar-patel-48612a311/)
