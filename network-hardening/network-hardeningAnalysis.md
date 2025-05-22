Security risk assessment report 

Part 1: Select up to three hardening tools and methods to implement
1. Password Policies
2. Firewall Maintenance
3. MultiFactor Authentication(MFA)
4. Network Access Privileges 



Part 2: Explain your recommendations
1. Password Policies
The organization currently allows employees to share passwords, and the admin account still uses a defgault password. This presents a major risk-shared or default credentials make it significantly easier for attackers to compromise multiple systems at once. 
By implementing strict password policies, we can require:
* Unique passwords for every user
* Secure password storage using salting and hashing
* Use of long passphrases or complex password standards
* Regular training on password best practices
This reduces the risk of brute force attacks, credential stuffing, and internal misuse.

2. Network Access Privileges
Currently, all employees have access to all systems and data, regardless of their role. This violates the principle of least privilege, increasing the damage that can be caused if any account is compromised. 
Implementing role-based access control (RBAC) ensures:
* Employees only have access to the systems and the data they need
* Admin-level access is restricted to authorized personnel only
* Monitoring and audtiting of access rights becomes simpler
This limits internal threats and makes it harder for attackers to escalate privileges.

3. Firewall Maintenance
Firewalls are in place but currently lack traffic filtering rules, meaning malicious traffic can potentially enter or exit the network unchallenged.
Firewall Maintenance involves:
* Defining inbound/outbound rules
* Blocking unused or vulnerable ports
* Logging and alerting on suspicious activity
* Regularly updating rule sets based on emerging threats
Maintaining firewalls proactively protects the network from DDoS attacks, malware communication, unauthorized access, and data exfiltration.

4. MultiFactor Authentication (MFA)
The absence of MFA exposes all user accounts to risks from stolen or guessed passwords. MFA introduces a second layer of verification, which significantly improves account security. 
Common MFA methods include:
* One-time passwords (OTP) via SMS or email
* Authenticator apps (e.g, Google Authenticator)
* Biometric Verification (e.g., fingerprint or facial recognition)
* Hardware tokens (e.g., YubiKeys)
Implementing MFA across critical systems-especially administrative access, email, and remote connections - greatly reduces the risk of unauthorized access, even if a password is compromised. 

