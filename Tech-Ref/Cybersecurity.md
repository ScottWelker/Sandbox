[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref)

[[_TOC_]]

---
# Introduction

## Reference
1. [DoubleOctopus: Security Wiki](https://doubleoctopus.com/security-wiki/)
   - [Threats and Tools](https://doubleoctopus.com/security-wiki/threats-and-tools/#security-wiki-content)
1. [How the red team engagement really went down (Video)](https://www.linkedin.com/posts/cschipper_how-the-red-team-engagement-really-went-down-activity-6923080523158286336-S6-N?utm_source=linkedin_share&utm_medium=member_desktop_web).

## Terms

<details><summary>Click to exapnd/hide Terms.</summary>

|:seedling: [Wiki Gardening](/Tech-Ref/Wiki/Wiki-Gardening) |
|:-|
| Consider breaking the table's contents out to child pages. |

| Term | Definition | Notes |
|:-|:-|:-|
| Beacon <span id="beacon"/>| Malware beaconing is one of the first network-related indications of a botnet or a peer-to-peer (P2P) malware infection. A botnet is a network of computers infected with malicious software that’s being controlled by a remote malicious party without the owner’s knowledge.<br/><br/>P2P infections indicate malware that is laterally moving to infect one system after another. After malware infects a vulnerable host, it quickly scans the host environment and initiates a command and control ([C2](#c2)) channel with its creator (i.e. the intruder).<br/><br/>The compromised host then initiates regular interval malware beaconing calls out to the [C2](#c2) infrastructure to await further installation or to begin data exfiltration. | [Beacon](https://www.blumira.com/glossary/beacon/) |
| C2 <span id="c2"/>| Command and control (C2) is often used by attackers to retain communications with compromised systems within a target network.<br/><br/>They then issue commands and controls to compromised systems (as simple as a timed [beacon](#beacon), or as involved as remote control or data mining). It's usually the compromised system/host that initiates communication from inside a network to a command and control server on the public internet. Establishing a command and control link is often the primary objective of malware. | [Optiv: What is C2](https://www.optiv.com/cybersecurity-dictionary/c2-command-and-control) |
| Cobalt Strike <span id="cobalt-strike"/>| Cobalt Strike is a paid penetration testing product that allows an attacker to deploy an agent named '[Beacon](#beacon)' on the victim machine. [Beacon](#beacon) includes a wealth of functionality to the attacker, including, but not limited to command execution, key logging, file transfer, SOCKS proxying, privilege escalation, mimikatz, port scanning and lateral movement. [Beacon](#beacon) is in-memory/file-less, in that it consists of stageless or multi-stage shellcode that once loaded by exploiting a vulnerability or executing a shellcode loader, will reflectively load itself into the memory of a process without touching the disk. It supports [C2](#c2) and staging over HTTP, HTTPS, DNS, SMB named pipes as well as forward and reverse TCP; [Beacons](#beacon) can be daisy-chained. Cobalt Strike comes with a toolkit for developing shellcode loaders, called Artifact Kit. <br/><br/>The [Beacon](#beacon) implant has become popular amongst targeted attackers and criminal users as it is well written, stable, and highly customizable.| [MalPedia: Cobalt Strike](https://malpedia.caad.fkie.fraunhofer.de/details/win.cobalt_strike) |
| Defender <span id="Defender"/>| Microsoft Defender for Identity cloud service helps protect your enterprise hybrid environments from multiple types of advanced targeted cyber attacks and insider threats. |[Microsoft Defender for Identity documentation](https://docs.microsoft.com/en-us/defender-for-identity/) |
| EDR (Endpoint detection and response) <span id="edr"/>| Endpoint detection and response (EDR), also known as endpoint threat detection and response (ETDR), is an integrated endpoint security solution that combines real-time continuous monitoring and collection of endpoint data with rules-based automated response and analysis capabilities. The term was suggested by Anton Chuvakin at Gartner to describe emerging security systems that detect and investigate suspicious activities on hosts and endpoints, employing a high degree of automation to enable security teams to quickly identify and respond to threats. | [McAfee: What Is Endpoint Detection and Response (EDR)](https://www.mcafee.com/enterprise/en-us/security-awareness/endpoint/what-is-endpoint-detection-and-response.html) |
| Mimikatz <span id="Mimikatz"/>| Mimikatz is a credential dumping open source program used to obtain account login and password information, normally in the form of a hash or a clear text password, from an operating system or software. Credentials can then be used to perform lateral movement and access restricted information. | [Mimikatz](https://doubleoctopus.com/security-wiki/threats-and-tools/mimikatz/) |
| Process Hacker  <span id="process-hacker"/>| A free, powerful, multi-purpose tool that helps you monitor system resources, debug software and detect malware. | [Process Hacker](https://processhacker.sourceforge.io) |
| Security Operations Center (SOC)  <span id=""/>| A Security Operation Center (SOC) is a centralized function within an organization employing people, processes, and technology to continuously monitor and improve an organization's security posture while preventing, detecting, analyzing, and responding to cybersecurity incidents. | [McAfee: What Is a Security Operations Center (SOC)?](https://www.mcafee.com/enterprise/en-us/security-awareness/operations/what-is-soc.html) |
|  <span id=""/>| | |

</details>

---
# Topics
1. [Authentication](/Tech-Ref/Software-Development/IAM-\(Identity-&-Access-Management\)/Authentication).
1. [Cloud DevOps Security (CDS)](/Glossary/CDS-\(Cloud-DevOps-Security\)).
1. [Identity & Access Management (IAM)](/Tech-Ref/Software-Development/IAM-\(Identity-&-Access-Management\)).
1. [Information Security & Governance Team (Slalom)](/Slalom-LLC/Slalom-Consulting/Information-Security-&-Governance-Team).
1. [Security Assertion Markup Language (SAML)](/Tech-Ref/Software-Development/IAM-\(Identity-&-Access-Management\)/Authentication/SAML-\(Security-Assertion-Markup-Language\)).
