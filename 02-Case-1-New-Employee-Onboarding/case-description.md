# Case 1 – Password Reset Workflow

## Scenario

The user (Sarah) reported that she was unable to log into her Windows workstation after forgetting her password.

This is one of the most common help desk requests in real environments, so I used this case to simulate a realistic Tier 1 support workflow.

---

## Ticket Intake

Sarah submitted a ticket through the osTicket portal explaining that she could not log in.

As the assigned IT technician, I reviewed the ticket and added an internal note documenting the issue before taking any action. Maintaining documentation at every stage is important for accountability and audit purposes.

---

## Identity Verification

Before resetting the password, I documented that the user's identity was verified.

In a real organization, this step could involve:
- Confirming employee ID
- Verifying department information
- Performing a callback verification

Even in a lab environment, I included this step to reflect proper security practice.

---

## Technical Resolution

After verification, I logged into the Windows system using an administrative account and reset the password using the command line:

```net user sarah.johnson NewTemporaryPass123!```

The system confirmed:
"The command completed successfully."

This method is commonly used by help desk technicians for local account password resets.

---

## Validation

After resetting the password:
- The user was able to log in successfully.
- I documented the resolution in the ticket.
- The ticket status was changed to **Resolved**.

---

## Key Takeaways

- Password resets should always include identity verification.
- Command-line administration is often faster and more efficient than GUI tools.
- Proper documentation strengthens accountability.
- Even simple issues should follow structured workflow.
