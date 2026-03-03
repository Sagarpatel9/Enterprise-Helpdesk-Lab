# Case 1 – New Employee Onboarding

## Scenario

HR submitted a request to create a workstation account for a new employee, Sarah Johnson, who was joining the Marketing department. The account needed to be created with standard user permissions so she could log in on her first day.

This case simulates a typical Tier 1 Help Desk onboarding task.

---

## Ticket Intake

A ticket was created in osTicket with the following request:

- Create Windows local user account
- Assign appropriate group membership
- Confirm account functionality

The ticket was assigned to IT Support.

---

## Actions Taken

### 1. Account Creation

Using an elevated Command Prompt in the Windows VM, I created the user account:

```net user sarah.johnson TempPass123! /add```


### 2. Group Assignment

The account was added to the standard Users group:

```net localgroup Users sarah.johnson /add```


### 3. Verification

To confirm successful creation, I ran:

```net user sarah.johnson```


The system confirmed:
- Account is active
- Password is set
- Proper group membership applied

---

## Resolution

The ticket was updated with documentation of the actions performed.

The temporary password was communicated securely, and the user was instructed to change it upon first login.

The ticket was then marked as **Resolved**.

---

## What This Demonstrates

- Understanding of Windows local user management
- Proper ticket lifecycle handling
- Clear technical documentation
- Command-line administrative capability
- Professional onboarding workflow

This case reflects a standard entry-level Help Desk responsibility in an enterprise environment.
