Data leak worksheet


Incident summary: A sales manager shared access to a folder of internal-only documents with their team during a meeting. The folder contained files associated with a new product that has not been publicly announced. It also included customer analytics and promotional materials. After the meeting, the manager did not revoke access to the internal folder, but warned the team to wait for approval before sharing the promotional materials with others.

During a video call with a business partner, a member of the sales team forgot the warning from their manager. The sales representative intended to share a link to the promotional materials so that the business partner could circulate the materials to their customers. However, the sales representative accidentally shared a link to the internal folder instead. Later, the business partner posted the link on their company's social media page assuming that it was the promotional materials.

Control
Least privilege
Issue(s)
What factors contributed to the information leak?
Overprovisioned Access:
The manager shared entire folder access instead of specific files.


The folder contained multiple document types with differing sensitivity levels.


Failure to Revoke Access:


After the meeting, access was not revoked, violating the just-in-time principle of access control.


No Granular Sharing Controls:


There were no file-level restrictions, allowing users to forward the entire folder.


Poor User Training and Awareness:


The sales rep did not recall the manager’s instruction.


There was a lack of automated safeguards (e.g., warning on sharing internal folders).


Inadequate Technical Controls:


The system did not enforce internal-only restrictions or detect the link being shared externally.


Review
What does NIST SP 800-53: AC-6 address?
Users are granted the minimum access necessary to perform their duties.


Access is limited in terms of time, scope, and function.


Controls ensure access is reviewed, revoked when no longer needed, and aligned with the principle of "need to know."


Systems enforce role-based access controls (RBAC) and temporary permissions where appropriate.


Recommendation(s)
How might the principle of least privilege be improved at the company?
1. Implement Role-Based Access Control (RBAC)
Sales reps should only access approved promotional materials — not strategic plans or customer data.


2. Use Time-Limited Access (Just-in-Time Permissions)
Automatically revoke shared access after a defined time (e.g., after the meeting).


3. Restrict External Sharing by Default
Internal folders should be flagged as confidential and cannot be shared externally unless explicitly approved.


4. File-Level Access Controls
Share specific files, not whole folders, and set view-only or download restrictions.


5. Audit Logs and Alerting
Monitor when links to sensitive files are generated and shared.


Alert admins if internal files are shared outside the domain.


6. User Training and Confirmation Prompts
Conduct regular data handling training for all employees.


Add confirmation dialogs when sharing sensitive documents externally, e.g., “This file is marked internal. Are you sure?”


Justification
How might these improvements address the issues?

RBAC
Ensures employees only access what their role needs, reducing exposure.


Time-limited Access
Prevents access persisting after it’s no longer necessary.


External Sharing Restrictions
Stops internal data from being shared outside by mistake.


File-Level Permissions
Limits scope of access, reducing chance of leaking unrelated sensitive info.


Audit Logs/Alerts
Enables real-time detection and response to unauthorized sharing.


Training & Prompts
Reinforces awareness and introduces friction before mistakes are made.





