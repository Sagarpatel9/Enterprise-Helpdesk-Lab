# Enterprise Help Desk Lab (osTicket)

## Project Overview

This project is a hands-on simulation of a small enterprise IT Help Desk environment.

I built this lab to better understand how real IT support teams operate — from ticket intake to escalation and final resolution. The environment includes an Ubuntu Server running osTicket and a Windows workstation VM where I performed real troubleshooting tasks.

The goal of this project was not just to “fix issues,” but to follow structured workflow, documentation, and escalation procedures similar to what would happen in a real organization.

---

## Lab Environment

- **Ticketing System:** osTicket (hosted on Ubuntu Server)
- **Server Stack:** Apache, MySQL, PHP (LAMP)
- **Client System:** Windows VM (VMware Fusion)
- **Roles Simulated:**
  - End User (Sarah)
  - Tier 1 IT Support
  - Tier 2 Network Engineer

---

## Repository Structure

- `01-Lab-Architecture/` – Environment design and workflow overview  
- `02-Case-1-New-Employee-Onboarding/` – Account creation workflow  
- `03-Case-2-Password-Reset/` – Password reset procedure  
- `04-Case-3-Account-Investigation/` – Authentication investigation & escalation  
- `05-Case-4-DNS-Misconfiguration/` – Network troubleshooting case  
- `06-Lessons-Learned/` – Professional skills and reflections  

---

## Simulated Incident Cases

### Case 1 – New Employee Onboarding
Simulated an HR request to provision a workstation account for a new employee. Created the account using the Windows CLI, assigned appropriate group membership, validated the configuration, and documented the full ticket lifecycle.

### Case 2 – Password Reset
Handled a common login issue where a user forgot their password. Followed identity verification steps and reset credentials using the `net user` command before resolving the ticket.

### Case 3 – Account Investigation
Investigated repeated authentication failures before resetting credentials. Escalated the ticket to Tier 2 for log review, documented findings, and followed structured workflow before resolution.

### Case 4 – DNS Misconfiguration
User could reach external IP addresses but could not load websites. Diagnosed DNS misconfiguration using `ipconfig`, `ping`, and `nslookup`, escalated to the Network Team, corrected DNS settings, validated the fix, and closed the ticket.

---

## Skills Demonstrated

- IT Service Management (ITSM) ticket lifecycle handling  
- Tier 1 and Tier 2 escalation workflow  
- Windows user administration via command line  
- Structured network troubleshooting methodology  
- Root cause identification and validation testing  
- Clear and professional technical documentation  

---

## Why I Built This

I created this lab to gain practical experience beyond theory. Instead of only learning commands, I focused on understanding how IT teams document, escalate, investigate, and resolve real-world issues in a structured way.

This project reflects how I approach problem-solving: methodical, documented, and focused on root cause.

---

**Author:**  
Sagarkumar Patel
