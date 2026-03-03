# Case 3 – Account Access Investigation

## Scenario

The user reported repeated authentication failures and was unable to log in. Instead of immediately resetting the password, I treated this as a potential security-related issue.

In real environments, multiple failed login attempts can sometimes indicate user error — but they can also suggest possible unauthorized access attempts.

---

## Initial Triage (Tier 1)

After reviewing the ticket, I documented the issue and avoided immediately resetting the password.

Instead, I escalated the ticket to the Network Team (Tier 2) to review login activity before taking action.

This reflects proper escalation practice rather than assuming every issue is simply a forgotten password.

---

## Investigation (Tier 2)

The Network Team reviewed the system logs to look for patterns such as:

- Multiple failed login attempts
- Suspicious timing patterns
- Unusual behavior that might indicate brute-force attempts

After reviewing the logs, no signs of malicious activity were found. The failed attempts appeared consistent with normal user error.

The findings were documented internally.

---

## Resolution

Once the investigation cleared the account as safe:

- The ticket was reassigned back to IT Support.
- The password was reset using the Windows CLI.
- The user was instructed to change the temporary password upon login.

---

## Lessons from This Case

- Not all login issues should be treated as routine resets.
- Escalation is important when security concerns are possible.
- Clear internal documentation helps teams collaborate effectively.
- Even minor incidents can demonstrate structured response workflow.

