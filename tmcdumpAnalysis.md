Security incident report

Section 1: Identify the network protocol involved in the incident
DNS (Domain Name System) used to resolve domain names to IP addresses.
TCP/IP (Transmission Control Protocol/ Internet Protocol) used to establish reliable connections to web servers.
HTTP (Hyper Text Transfer Protocol) used for communication between the user's browser and both the original and malicious websites. 





Section 2: Document the incident
YummyRecipesForMe.com was compromised via a brute force attack executed by a former employee. The attacker repeatedly entered known default admin passwords until they successfully gained access to the administrative control panel of the website. There were no mechanisms in place to limit login attempts, making the brute force attack feasible.

Once access was gained, the attacker modified the website's source code by embedding malicious JavaScript. This script prompted users to download and run an executable file disguised as a browser update. Upon execution, the script redirected the user’s browser from the legitimate site (yummyrecipesforme.com) to a spoofed malicious site (greatrecipesforme.com).

The attacker then changed the admin password to lock out legitimate access. Hours later, multiple customers reported slow computer performance and suspicious download prompts after visiting the site. In response, the site owner attempted to log in but was denied access, leading to a security investigation.

Investigation & Evidence:

A sandboxed environment was created to safely replicate the incident.

Tcpdump was used to capture packet data during website access.

DNS and HTTP logs confirmed:

Initial DNS request to yummyrecipesforme.com

HTTP request and download of a suspicious file

Secondary DNS request and HTTP connection to greatrecipesforme.com

The file was found to contain malware, including a redirect function and potential spyware.

Impact:

Unauthorized access to the web server

Malicious redirection of customer traffic

Potential data compromise on customer machines

Loss of administrative control over the website





Section 3: Recommend one remediation for brute force attacks
To reduce the risk of brute force attacks in the future, it is recommended that the organization implement a login attempt limit policy. After a defined number of failed login attempts (e.g., 5), the account should be temporarily locked, require a CAPTCHA, or alert administrators.

Why this is effective:
It prevents rapid password guessing by increasing time and effort for each attempt.

It allows early detection of potential brute force activity.

It reduces the window of opportunity for attackers using automated tools.

It protects admin accounts from unauthorized access.

Optional Additional Measures:

Enforce strong password policies.

Implement multi-factor authentication (MFA).

Monitor and log all admin access attempts.

Disable or change all default credentials before deployment.



