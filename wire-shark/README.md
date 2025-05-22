# Wireshark Analysis - Brute Force & Malware Redirect

## Scope
Investigate suspicious HTTP traffic from a compromised website using Wireshark logs.

## Summary
A brute force attack allowed a former employee to inject JavaScript into the site, prompting users to download a malware executable that redirected traffic to a malicious clone.

## Included Files
- `WireShark incident-report.md`: Detailed security analysis
- `wire-sharklog.csv`: Captured network traffic log from Wireshark

## Key Findings
- DNS and HTTP logs confirmed malware redirection
- Default credentials were used and admin access was compromised
