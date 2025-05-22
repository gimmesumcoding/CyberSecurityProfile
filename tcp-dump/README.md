# TCPDump Network Analysis - Malware Redirection Investigation

## Scope
Analyze suspicious DNS and HTTP traffic related to a brute force attack and malware redirection using Tcpdump logs.

## Summary
A former employee compromised the YummyRecipesForMe.com website using a brute force attack. Once inside the admin panel, they embedded JavaScript to trick visitors into downloading an executable. This file redirected users to a fake website that hosted malware.

This investigation used Tcpdump logs to trace DNS and HTTP requests/responses that confirmed the presence of malicious activity, including browser redirection to greatrecipesforme.com.

## Included Files
- `tmcdumpScope.md`: Details of the simulated incident, attacker method, and observable behavior.
- `tmcdumpAnalysis.md`: Full analysis of protocols, attack vector, infection method, and recommendations.
- `tmcdumpTrafficLog.md`: Captured network traffic showing DNS resolution and HTTP requests to both legitimate and malicious domains.

## Key Findings
- DNS and HTTP traffic logs showed a redirect to a malicious website after the user downloaded and ran a fake update.
- The attacker exploited a default admin password and changed it after gaining access.
- There were no brute force protection mechanisms in place.
- Recommended remediation includes limiting login attempts and implementing MFA.
