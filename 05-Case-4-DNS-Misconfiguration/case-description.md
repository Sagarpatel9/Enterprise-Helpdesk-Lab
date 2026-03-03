# Case 4 – DNS Misconfiguration

## Scenario

The user reported that websites were not loading, even though the workstation appeared connected to the network.

This type of issue is common in real environments and requires layered troubleshooting rather than guessing the cause.

---

## Initial Troubleshooting (Tier 1)

I began by performing basic network diagnostics on the Windows workstation.

First, I checked the IP configuration:

```ipconfig```

The system showed:
- A valid IPv4 address
- A valid default gateway
- A DNS server configured

Next, I tested internet connectivity using:

```ping 8.8.8.8```

The ping was successful, confirming that the system had internet connectivity at the network layer.

However, when I tested DNS resolution using:

```nslookup google.com```

The request failed and timed out.

This indicated that the issue was not general connectivity, but specifically a DNS resolution problem.

At this point, I escalated the ticket to the Network Team.

---

## Investigation (Tier 2)

The Network Team reviewed the workstation's network configuration and identified that the DNS server had been manually set to:

10.10.10.10

This was not a valid resolver in the environment.

---

## Resolution

The DNS settings were corrected to:

- 8.8.8.8
- 8.8.4.4

After updating the configuration, I validated the fix using:

```nslookup google.com```
```ping google.com```


Both commands returned successful results, confirming that DNS resolution and hostname connectivity were restored.

---

## Lessons from This Case

- Troubleshooting should follow a layered approach.
- Successful IP connectivity does not guarantee DNS functionality.
- Escalation to Tier 2 is appropriate when configuration-level issues are identified.
- Validation testing is critical before closing a ticket.

