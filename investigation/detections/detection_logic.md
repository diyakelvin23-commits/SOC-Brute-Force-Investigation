# Detection Logic: Windows Failed Logons

## Objective
Identify patterns of failed Windows authentication attempts that may indicate password guessing or brute-force activity.

## Event of Interest
- Event ID: 4625
- Meaning: An account failed to log on.

## Detection Approach
1. Collect Event ID 4625 records.
2. Group events by target account, source address, and time window.
3. Flag repeated failures within a short period for investigation.
4. Check for a successful logon (Event ID 4624) near the failures.
5. Review account, logon type, source address, and process details before making a conclusion.

## Example Detection Rule
Flag an account for investigation when 5 or more failed logons occur within 5 minutes.

This is an initial example threshold, not a universal security standard. Tune it to the environment to reduce false positives.

## Limitations
A high number of failed logons does not prove malicious activity. Mistyped passwords, scheduled tasks, and misconfigured applications can generate failures. Event ID 4625 should be correlated with other evidence.

## Response Recommendations
- Validate the affected account and source.
- Check for nearby successful logons.
- Review endpoint and authentication logs.
- Escalate when evidence supports suspicious activity.
- Follow organisational procedures before disabling accounts or blocking sources.
