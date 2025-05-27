You are part of the security team at Rhetorical Hospital and arrive to work one morning. On the ground of the parking lot, you find a USB stick with the hospital's logo printed on it. There’s no one else around who might have dropped it, so you decide to pick it up out of curiosity.

You bring the USB drive back to your office where the team has virtualization software installed on a workstation. Virtualization software can be used for this very purpose because it’s one of the only ways to safely investigate an unfamiliar USB stick. The  software works by running a simulated instance of the computer on the same workstation. This simulation isn’t connected to other files or networks, so the USB drive can’t affect other systems if it happens to be infected with malicious software.

Parking lot USB exercise


Contents
The USB contains both personal and professional files, including documents like shift schedules, resumes, new hire letters, and budget trackers — many of which may contain personally identifiable information (PII) such as names, job titles, and financial data. Mixing personal files (like “Wedding list” and “Dog pics”) with sensitive work documents introduces a serious security risk and violates best practices for data separation. It is unsafe to store personal and work files on the same device, especially unencrypted and publicly accessible.

Attacker mindset
An attacker could use resume or HR documents to identify employees and target them with phishing or social engineering attacks. Shift schedules and organizational charts provide insight into staff availability and roles, which can be exploited to plan insider threats or impersonation attacks. Additionally, personal documents and photos could be used to impersonate Jorge or manipulate individuals in his personal or professional circle, potentially granting attackers deeper access into the hospital’s systems.

Risk analysis
Malicious USBs can contain malware such as keyloggers, rootkits, or backdoors that auto-execute when plugged into a system. If an unsuspecting employee inserted this USB into a company machine, the entire hospital network could be compromised. To mitigate these risks, organizations should enforce technical controls like disabling USB ports or requiring virtual sandbox environments for inspection. Operational controls include staff training on USB baiting and reporting unknown devices. Managerial controls include strict policies separating personal and professional storage and enforcing encryption for removable media.


