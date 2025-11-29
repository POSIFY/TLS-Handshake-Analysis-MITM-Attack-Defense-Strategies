# TLS Handshake Analysis MITM Attack-Defense Strategies

### Project Description

This repository documents my findings and observations as I explore Man-in-the-Middle (MITM) attacks and defense strategies, including methodology, underlying technologies, and tools used during MITM and session hijacking simulations.

I've always been fascinated by how systems communicate. Through this research, I’ve come to understand that data is most vulnerable while in transit, as it may pass through compromised networks, rogue access points, untrusted devices, or attacker-controlled infrastructure.
The goal of this project is to help individuals and organizations gain a clearer understanding of how MITM attacks operate — and more importantly — how to better protect transmitted data from unauthorized access.

### Scope of Work

1. TLS handshake observation and analysis
2. MITM attack simulation in a controlled lab environment
3. Session hijacking techniques and prevention
4. Defensive strategies, detection methods, and mitigation approaches
5. Tools, methodologies, and explanations provided at point of use

### Lab Environment & Tools
* Windows OS
* Linux OS
* Ettercap
* Wireshark
* Additional tools will be noted where applied
**Note**: All labs and installations required for this project have already been completed. A detailed installation and lab setup guide will be linked in future updates. For now, this repository is intended for review and observation.
If your own lab environment includes the tools listed above, you may follow along with caution.

### Ethical Notice
* All activities were conducted strictly in a lab environment
* No unapproved or unauthorized targets were used at any point
* This research is intended solely for educational and cybersecurity awareness purposes

**Unauthorized use of the information provided is strictly prohibited. Always ensure proper authorization before conducting any security testing.**

**How Can an Adversary Capture Your Network Traffic Remotely?**
You might be wondering how a threat actor could intercept your network traffic without having direct access to your internal network. In real-world attack scenarios, cybercriminals often exploit weaknesses in wireless authentication using techniques such as rogue access point (AP) deployment.

An attacker could set up a malicious AP designed to mimic a legitimate one by:
* Broadcasting a similar or identical SSID (network name)
* Configuring authentication to be open or weak, encouraging automatic connection
* Exploiting device behavior where systems connect to previously known or stronger signal networks without user intervention

Once a victim connects to this rogue AP, their traffic is routed through an attacker-controlled network, which can allow:

* Traffic interception and packet inspection
* TLS downgrade or manipulation attempts
* Credential harvesting
* Session hijacking or redirection attacks
* Possible funneling into further exploitation tools

Why Strong Authentication Matters

In enterprise and even private environments, relying on simple WPA/WPA2-PSK is not enough. To prevent rogue AP-based attacks and unauthorized access, two-way authentication mechanisms should be enforced, such as:

| Authentication Type | Protection Mechanism | Best Use Case |
|--------------------|----------------------|---------------|
| **EAP (Extensible Authentication Protocol)** | Mutual verification of client and network using certificates or credentials | Enterprise networks |
| **PEAP (Protected EAP)** | Uses TLS tunnel to secure EAP negotiation | Enterprise Wi-Fi, authentication servers |

These protocols verify both endpoints — ensuring the client is legitimate and the network is trustworthy before communication is allowed. That eliminates the chances of a device unknowingly connecting to a spoofed network.
