# 🛡️ Eagle Shield Pro
**Private Digital Architects | Serving the DFW Metroplex**

At Eagle Shield Pro, we believe your digital perimeter should be as secure as your physical one. We architect enterprise-grade networks and deploy 100% offline, on-premise AI systems that ensure absolute privacy.

---

## ⚙️ Our Tech Stack & Focus Areas
* **Networking:** Ubiquiti UniFi, Zero-Trust Architecture, VLAN Segmentation, Enterprise Firewalls.
* **Private AI (Eagle Shield Core):** Apple Silicon, Local LLMs, Retrieval-Augmented Generation (RAG), Edge Inference.
* **Security:** Air-gapped deployments, IoT isolation, Military-grade diagnostics.

---

## 🏗️ The Executive Home Network Baseline
*A Zero-Trust Architecture Guide for High-Net-Worth Individuals & Remote Executives.*

Standard ISP hardware is designed for basic connectivity, not enterprise security. When a home network handles sensitive corporate data, legal documents, or financial records, the physical architecture must be upgraded. Below are the baseline requirements we deploy for our clients across North Texas.

### 1. Gateway & Routing (The Perimeter)
The standard ISP modem/router combo must be bypassed and replaced with an Enterprise-Grade Gateway (e.g., Ubiquiti UniFi Dream Machine Pro/SE).
- [x] **Disable UPnP (Universal Plug and Play):** UPnP is a massive security vulnerability that allows devices to open firewall ports without user permission. 
- [x] **Intrusion Prevention System (IPS):** Enable Deep Packet Inspection (DPI) to actively monitor and block malicious traffic entering the network.
- [x] **Custom DNS:** Route traffic through secure, encrypted DNS providers (e.g., Cloudflare 1.1.1.2 or NextDNS) to block known malware and phishing domains.

### 2. Network Segmentation (Digital Walls)
A flat network means a compromised smart lightbulb can access a CEO's laptop. We enforce strict VLAN (Virtual Local Area Network) segmentation.
- [x] **VLAN 1 (Management):** Strictly for network infrastructure (switches, access points).
- [x] **VLAN 2 (Trusted/Corporate):** Only trusted devices (work laptops, secure phones, Eagle Shield Core AI).
- [x] **VLAN 3 (IoT/Smart Home):** Smart TVs, cameras, thermostats, and appliances. *Rule: Devices here cannot initiate contact with the Trusted VLAN.*
- [x] **VLAN 4 (Guest):** Client isolation enabled. Guests only get access to the internet, not local devices.

### 3. Sovereign AI Infrastructure (Air-Gapped Processing)
For clients utilizing our **Eagle Shield Core** (Local LLMs running on Apple Silicon for analyzing private documents):
- [x] **Local Subnet Isolation:** The Private AI server must reside on the Trusted VLAN.
- [x] **No Inbound WAN Access:** The AI server must never be exposed to the public internet via port forwarding. Remote access is handled via a secure, encrypted VPN tunnel.
- [x] **Zero Cloud Telemetry:** Ensure the OS and local AI models have telemetry and data-sharing strictly disabled. 

### 4. Wireless Security (The Airspace)
- [x] **WPA3 Encryption:** Enforce WPA3 for all modern Trusted devices.
- [x] **Hidden SSIDs for Infrastructure:** Hide the Wi-Fi broadcast for critical infrastructure networks.
- [x] **Fast Roaming (802.11r):** Enable zero-handoff roaming across multiple enterprise access points to ensure VoIP/video calls never drop in large estates.

---

## 🛠️ Open Source & Tools
We believe in building on solid foundations. We actively use, fork, and support open-source tools that enable local, private intelligence. 
* Check out our pinned repositories to see the tools we use for right-sizing LLMs to physical hardware and managing secure deployments.

---

## 🌐 Connect With Us
Need to upgrade your physical network to support secure, private intelligence? 

* **Book a Health Check:** [eagleshieldpro.com](https://eagleshieldpro.com)
* **LinkedIn:** [Eagle Shield Pro](https://www.linkedin.com/company/eagle-shield-pro/)
* **Contact:** hello@eagleshieldpro.com
