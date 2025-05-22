Incident report analysis
Instructions
As you continue through this course, you may use this template to record your findings after completing an activity or to take notes on what you've learned about a specific tool or concept. You can also use this chart as a way to practice applying the NIST framework to different situations you encounter.

Summary
A distributed denial of service (DDoS) attack using ICMP flooding disrupted the company's internal network for two hours. The attack exploited an unconfigured firewall, allowing malicious traffic to overwhelm network resources. This incident led to immediate containment measures and long-term security improvements, including firewall rules, monitoring tools, and an IDS/IPS system.


Identify
Goal: Understand organizational risks to systems, assets, data, and capabilities.

Actions Taken and Needed:
* Conducted a post-incident audit to identify the firewall misconfiguration that allowed the ICMP flood.
* Performed a risk assessment on external-facing network components.
* Began scheduling regular vulnerability scans and penetration tests.
* Reviewed access privileges and configurations across routers, switches, and firewalls.
* Mapped all network assets and data flows to uncover unknown exposure points.

Tools/Processes to Implement:
* Asset inventory tools (e.g., Lansweeper, OpenVAS)
* Network diagrams & data flow mapping
* Security audit checklists (aligned with CIS Controls)

Protect
Goal: Develop and implement safeguards to ensure delivery of critical services.

Actions Taken and Needed:
* Implemented a firewall rule to rate-limit incoming ICMP packets.
* Set up source IP address verification to prevent spoofed packets.
* Defined and enforced a firewall configuration change policy.
* Trained IT staff on secure configuration and hardening practices.
* Updated the company's network security policy to define ICMP filtering.

Tools/Processes to Implement:
* Firewall with advanced rule customization (e.g., pfSense, Cisco ASA)
* Endpoint hardening scripts
* Employee training sessions on network and device security

Detect
Goal: Identify cybersecurity events in a timely manner.

Actions Taken or Needed:
* Deployed network monitoring software to detect unusual traffic patterns.
* Installed an Intrusion Detection/Prevention System (IDS/IPS) to flag and block malicious ICMP behavior.
* Set up alerts for unusual ICMP packet volume or spikes.
* Defined baseline traffic patterns to differentiate normal vs. abnormal behavior.

Tools/Processes to Implement:
* IDS/IPS (e.g., Snort, Suricata, Zeek)
* SIEM system (e.g., Splunk)
* Network flow analysis tools (e.g., ntopng)

Respond
Goal: Take action regarding a detected cybersecurity incident.

Actions Taken or Needed:
* Immediately blocked all ICMP packets during the attack to stop the flood.
* Took non-critical systems offline and prioritized restoration of essential services.
* Performed a root cause analysis to confirm the entry point.
* Documented the response process for future reference.
* Communicated with stakeholders during the incident to maintain transparency.

Tools/Processes to Implement:
* Incident Response Plan (IRP)
* DDoS mitigation playbook
* Communication templates for internal/external stakeholders

Recover
Goal: Restore normal operations and reduce impact from future events.

Actions Taken or Needed:
* Restored full network functionality after critical services were brought online.
* Conducted a lessons-learned meeting and updated recovery procedures.
* Reviewed and improved incident recovery policies based on response effectiveness.
* Enhanced the Business Continuity and Disaster Recovery Plan (BC/DR).

Tools/Processes to Implement:
* Backup verification tools
* DR runbooks
* Recovery time objectives (RTO) and recovery point objectives (RPO) testing


Reflections/Notes:
* Misconfigurations are a common threat vector; automated auditing of firewall and router configs should be standard.
* ICMP flooding is often overlooked because ICMP is not usually seen as dangerous; it needs more attention in firewall rules.
* This attack highlighted the importance of a layered defense strategy: firewall rules alone are not enough—active monitoring and IDS are essential.
* Future improvements could include DDoS mitigation services (Cloudflare, AWS Shield) for scalable protection.
* Staff training and simulations of incident scenarios can enhance readiness and reduce response time.

