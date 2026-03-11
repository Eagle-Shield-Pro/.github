# 🛡️ The Executive Home Network Baseline
**A Zero-Trust Architecture Guide for High-Net-Worth Individuals & Remote Executives**

*Maintained by the architects at [Eagle Shield Pro](https://eagleshieldpro.com).*

Standard ISP hardware (like those provided by AT&T, Spectrum, or Comcast) is designed for basic connectivity, not enterprise security. When a home network handles sensitive corporate data, legal documents, or financial records, the physical network architecture must be upgraded to a Zero-Trust standard.

This repository outlines the baseline requirements we deploy for our clients across the Dallas-Fort Worth Metroplex.

## 1. Gateway & Routing (The Perimeter)
The standard ISP modem/router combo must be bypassed (placed in IP Passthrough or Bridge Mode) and replaced with an Enterprise-Grade Gateway (e.g., Ubiquiti UniFi Dream Machine Pro/SE).
- [x] **Disable UPnP (Universal Plug and Play):** UPnP is a massive security vulnerability that allows devices to open firewall ports without user permission. It must be disabled at the gateway level.
- [x] **Intrusion Prevention System (IPS):** Enable Deep Packet Inspection (DPI) to actively monitor and block malicious traffic entering the network.
- [x] **Custom DNS:** Route traffic through secure, encrypted DNS providers (e.g., Cloudflare 1.1.1.2 or NextDNS) to block known malware and phishing domains at the network level.

## 2. Network Segmentation (Digital Walls)
A flat network (where all devices share the same IP range) means a compromised smart lightbulb can access a CEO's laptop. We enforce strict VLAN (Virtual Local Area Network) segmentation.
- [x] **VLAN 1 (Management):** Strictly for network infrastructure (switches, access points).
- [x] **VLAN 2 (Trusted/Corporate):** Only trusted devices (work laptops, secure phones, Eagle Shield Core AI).
- [x] **VLAN 3 (IoT/Smart Home):** All smart TVs, cameras, thermostats, and appliances. *Rule: Devices here cannot initiate contact with the Trusted VLAN.*
- [x] **VLAN 4 (Guest):** Client isolation enabled. Guests only get access to the internet, not local devices.

## 3. Sovereign AI Infrastructure (Air-Gapped Processing)
For clients utilizing our **Eagle Shield Core** (Local LLMs running on Apple Silicon for analyzing private documents):
- [x] **Local Subnet Isolation:** The Private AI server must reside on the Trusted VLAN.
- [x] **No Inbound WAN Access:** The AI server must never be exposed to the public internet via port forwarding. All remote access must be handled via a secure, encrypted VPN tunnel (e.g., WireGuard or Teleport).
- [x] **Zero Cloud Telemetry:** Ensure the OS and local AI models (via Ollama/MLX) have telemetry and data-sharing strictly disabled. 

## 4. Wireless Security (The Airspace)
- [x] **WPA3 Encryption:** Enforce WPA3 for all modern Trusted devices.
- [x] **Hidden SSIDs for Infrastructure:** Hide the Wi-Fi broadcast for critical infrastructure networks.
- [x] **Fast Roaming (802.11r):** Enable zero-handoff roaming across multiple enterprise access points to ensure VoIP and video calls never drop while walking through large estates (6,000+ sq ft).

---

### 🦅 About Eagle Shield Pro
We are Private Digital Architects serving the DFW Metroplex. We replace vulnerable consumer hardware with bank-grade infrastructure and deploy 100% offline Sovereign AI systems. 

Need to upgrade your physical network to support secure, private intelligence? 
**[Book a Network Health Check here](https://eagleshieldpro.com)**.
