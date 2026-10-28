# SOC Investigation: Failed Windows Logon Attempts

## 1. Objective
Investigate Windows Security Event ID 4625 records to understand failed authentication attempts and assess whether further investigation is required.

## 2. Environment
- Operating system: Windows
- Tool: Windows Event Viewer
- Log source: Windows Logs → Security
- Event investigated: 4625 — An account failed to log on

## 3. Initial Findings
- Ten Event ID 4625 events were observed in the filtered results.
- The events occurred across October 26–28, 2026.
- Logon Type 2 was observed, indicating an interactive logon attempt.
- The failure description indicated an unknown username or incorrect password.
- The source address displayed was 127.0.0.1, the loopback address.

## 4. Analysis
These records confirm that failed logon events occurred. However, the available evidence does not establish that a brute-force attack took place.

The loopback address indicates local-host addressing, but does not independently identify the process responsible. Further analysis should examine the timestamps, target accounts, process information, and related events.

## 5. Recommended Next Steps
1. Review the detailed fields of each relevant event.
2. Compare failed logons by account and time.
3. Check for successful logons near suspicious failures.
4. Investigate repeated patterns before classifying the activity as malicious.
5. Apply appropriate account protections and monitoring if a genuine threat is identified.

## 6. Conclusion
The initial investigation identified failed Windows logon events requiring contextual analysis. No confirmed brute-force attack can be concluded from the evidence collected so far.

## 7. Evidence
Screenshots of the Event Viewer results should be added to the project's screenshots folder after reviewing them for sensitive information.

**Analyst:** Diya Kelvin Powei
