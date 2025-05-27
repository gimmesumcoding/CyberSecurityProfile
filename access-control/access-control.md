Recently, a deposit was made from the business to an unknown bank account. The finance manager says they didn’t make a mistake. Fortunately, they were able to stop the payment. The owner has asked you to investigate what happened to prevent any future incidents.

To do this, you’ll need to do some accounting on the incident to better understand what happened. First, you will review the access log of the incident. Next, you will take notes that can help you identify a possible threat actor. Then, you will spot issues with the access controls that were exploited by the user. Finally, you will recommend mitigations that can improve the business' access controls and reduce the likelihood that this incident reoccurs.

Event Type: Information
Event Source: AdsmEmployeeService
Event Category: None
Event ID: 1227
Date: 10/03/2023
Time: 8:29:57 AM
User: Legal\Administrator
Computer: Up2-NoGud
IP: 152.207.255.255
Description:
Payroll event added. FAUX_BANK



Note(s)
Issue(s)
Recommendation(s)
Authorization /authentication
Objective: List 1-2 pieces of information that can help identify the threat:


The action was performed by a user with Administrator-level access in the Legal department.


The event was logged on a device named "Up2-NoGud", which is potentially not assigned to anyone in the employee directory.


The IP address is suspicious (might be external or unregistered in the internal systems).


The FAUX_BANK detail strongly suggests this was a malicious or fake account entry.


Objective: Based on your notes, list 1-2 authorization issues:


The Legal/Administrator account appears to still be active, but the corresponding employee may no longer work at the company or shouldn't have access to payroll systems.


Employees share cloud resources, meaning no role-based access control (RBAC) is in place, making it easy for anyone with shared credentials to abuse access.


The naming of the machine ("Up2-NoGud") could indicate an unauthorized or rogue device on the network.


No audit or access revocation policy appears to be enforced for departed users.


Objective: Make at least 1 recommendation that could prevent this kind of incident:


Implement Role-Based Access Control (RBAC):


Grant access strictly based on job function. For example, only HR or Payroll staff should have access to payroll functions—not Legal Admins.


Enforce Least Privilege and Audit Access Regularly:


Conduct quarterly access reviews to ensure only current employees have access to critical systems.


Revoke accounts and permissions immediately when employees leave or change roles.


Enable Multi-Factor Authentication (MFA):


All administrative and sensitive systems should require a second layer of verification to prevent misuse of credentials.


Implement Device Whitelisting & Logging:


Only authorized devices should be able to access company systems.


Keep logs of device IDs and perform anomaly detection on suspicious names (e.g., “Up2-NoGud”).


Train Staff & Monitor Usage:


Conduct routine training on cybersecurity hygiene.


Set up alerts for high-risk actions (e.g., new bank account additions).




