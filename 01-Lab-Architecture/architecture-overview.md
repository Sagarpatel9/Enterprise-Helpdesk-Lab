# Lab Architecture Overview

## Purpose of This Lab

This lab was built to simulate a small enterprise IT Help Desk environment. The goal was to replicate how tickets are created, assigned, escalated, investigated, and resolved in a structured workflow.

Rather than only practicing commands, this lab focuses on understanding the relationship between systems, users, and support roles.

---

## Environment Components

### 1. Ubuntu Server (Ticketing System)

- Operating System: Ubuntu Server
- Services: Apache, MySQL, PHP (LAMP stack)
- Application: osTicket

The Ubuntu server hosts the osTicket platform, which acts as the central ticket management system. All users and IT staff interact through this web-based system.

---

### 2. Windows Workstation (Client Machine)

- Operating System: Windows 11 VM
- Hosted in: VMware Fusion
- Used for:
  - User account management
  - Network troubleshooting
  - Command-line diagnostics

This VM simulates an employee workstation within a company environment.

---

### 3. Roles Simulated

To make the lab realistic, I simulated multiple roles:

- End User (Sarah)
- Tier 1 IT Support
- Tier 2 Network Engineer

This allowed me to demonstrate escalation workflow and internal documentation practices.

---

## Network Layout

The Windows workstation and Ubuntu server are connected within the same virtual network environment using VMware NAT networking.

Communication flow:

User → Ticket Submission → osTicket (Ubuntu Server)
IT Support → Windows Workstation Troubleshooting
Network Team → Configuration-Level Adjustments

---

## Workflow Model

The lab follows a structured support model:

1. Ticket intake
2. Tier 1 triage
3. Escalation when necessary
4. Investigation
5. Resolution
6. Validation
7. Ticket closure

This mirrors how real IT support teams operate in enterprise environments.

---

## Key Design Principles

- Clear separation of roles
- Documentation at every stage
- Escalation based on issue type
- Validation before resolution
- Structured troubleshooting methodology

---

## Summary

This architecture provides a realistic environment to practice IT support responsibilities, ticket lifecycle management, and layered troubleshooting techniques in a controlled lab setting.
