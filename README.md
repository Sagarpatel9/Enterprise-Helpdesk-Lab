# Enterprise Help Desk Lab (osTicket)

## Project Overview

This project is a hands-on simulation of a small enterprise IT Help Desk environment.

I built this lab to better understand how real IT support teams operate — from ticket intake to escalation and final resolution. The environment includes an Ubuntu Server running osTicket and a Windows workstation VM where I performed real troubleshooting tasks.

The goal of this project was not just to “fix issues,” but to follow proper workflow, documentation, and escalation procedures similar to what would happen in a real organization.

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

## What This Lab Demonstrates

This project focuses on practical IT support skills, including:

- Handling ticket intake and documentation
- Performing layered troubleshooting
- Distinguishing between network connectivity and DNS issues
- Resetting user accounts using the Windows CLI
- Escalating tickets between support tiers
- Validating fixes before closing tickets
- Communicating clearly in ticket responses

---

## Simulated Incident Cases

### Case 1 – Password Reset
Simulated a common login issue where a user forgot their password. Followed identity verification steps and reset credentials using the `net user` command.

### Case 2 – Account Access Investigation
Investigated repeated login failures before resetting credentials. Demonstrated escalation workflow and documentation discipline.

### Case 3 – DNS Misconfiguration
User could reach external IP addresses but could not load websites. Diagnosed DNS misconfiguration using `ipconfig`, `ping`, and `nslookup`, escalated to the Network Team, corrected DNS settings, and validated the fix.

---

## Skills Developed

- IT Service Management (ITSM) workflow
- Tier 1 and Tier 2 escalation process
- Windows user administration via command line
- Network troubleshooting methodology (OSI-layer thinking)
- Clear technical documentation
- Professional ticket communication

---

## Why I Built This

I created this lab to gain practical experience beyond theory. Instead of only learning commands, I focused on understanding how IT teams document, escalate, investigate, and resolve real-world issues in a structured way.

This project reflects how I approach problem-solving: methodical, documented, and focused on root cause.

---

**Author:**  
Sagarkumar Patel  
