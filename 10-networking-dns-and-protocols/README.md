# 10. Networking, DNS & Protocols – Practical Guide & Lab

This section explores foundational networking concepts, key protocols, DNS mechanisms, and their relevance for modern workplace security in a Microsoft 365 environment. The goal is to deepen understanding of underlying traffic flows, detect threats, and apply this knowledge to SOC operations.

---

## 1. Networking Fundamentals
  
### 1.1. OSI Model
The OSI model defines seven layers of network communication:

- Physical – cables, bits, voltage
- Data Link – frames, MAC addresses, switches
- Network – packets, IP routing
- Transport – TCP/UDP, ports, sockets
- Session – sessions, control ports
- Presentation – encryption, encoding
- Application – applications/protocols like HTTP, DNS

Understanding OSI helps SOC analysts interpret where threats live—e.g., ARP spoofing at Layer 2, DNS tunneling at Layer 7.

---

### 1.2. TCP/IP Model

The TCP/IP model simplifies traffic into four layers: Link → Internet → Transport → Application. Compared to OSI, it aligns more closely with real-world traffic flows, especially in cloud environments.

---

### 1.3. Packets, Frames, Ports & Sockets

- Frame: a unit of data at Layer 2 (Ethernet).
- Packet: a unit at Layer 3 (IP).
- Port: a numeric endpoint at Layer 4 (TCP/UDP).
- Socket: combination of IP address + port that identifies a communication endpoint. For example: 192.168.1.10:443 is a socket using TCP port 443. For SOC investigations, identifying ports and sockets helps isolate attacker-traffic paths.

---

### 1.4. Subnets, VLANs & Routing Basics

- Subnet: logical network segment (e.g., 10.0.0.0/24).
- VLAN: virtual LAN for segmenting broadcast domains.
- Routing: determines how packets move between subnets/VLANs, often through gateways.
In modern workplace security, segmentation (via VLANs) limits lateral movement and routing ensures traffic flows to inspection points.

---

## 2. Core Network Protocols

- TCP vs UDP
  - TCP: connection-oriented, reliable, ordered (e.g., HTTP, HTTPS, SMB).
  - UDP: connectionless, faster but not guaranteed (e.g., DNS, VoIP). SOC use-cases: monitoring unexpected UDP traffic (DNS over unconventional ports) or abnormal TCP flags (SYN flood, port scan).

- ICMP & ARP
  - ARP: resolves IP ↔ MAC in LAN. Attack vector: ARP spoofing/poisoning.
  - ICMP: echo requests, redirects used for network diagnostics but also can be exploited for reconnaissance.

- DHCP: Dynamically assigns IP addresses to endpoints. Attack vectors include rogue DHCP servers or lease hijacking.

- DNS: Critical protocol for domain name resolution. Types: A, AAAA, MX, TXT, CNAME, SRV. Attack vectors: DNS tunneling, exfiltration, spoofing, malicious domain registration.

- HTTP / HTTPS: Core web protocols: HTTP unencrypted, HTTPS encrypted (TLS). SOC relevance: malicious web apps, insecure TLS versions, traffic inspection points.

- SMTP / IMAP / POP: Email protocols. Secure workplace uses SMTPS / IMAPS. Threat vectors: phishing, credential theft, spam injection.

---

## 3. DNS Deep Dive

- Query types: recursive vs iterative.
- Record types: A/AAAA, MX, CNAME, TXT, SRV.
- DNSSEC: adds authenticity via digital signatures.
- Relevance to M365: MX and Autodiscover records for Exchange Online, SPF/DKIM/DMARC (TXT) for email security.
- Detection: Look for suspicious TXT records, atypical DNS tunneling domains, large volumes of NXDOMAIN responses.

---

## 4. Protocol Use Cases in Modern Workplace

- M365 services rely on TCP/443, TCP/80 for connectivity; Teams may use UDP for media.
- DNS: endpoints must resolve *.office365.com, Autodiscover, Graph API, etc.
- Zero Trust design: use segmentation (VLANs) and enforce routing through inspection points.
- Endpoint connectivity: device → corporate network → firewall → internet/cloud service.

---

## 5. Security & Threat Detection

- DNS tunneling: attacker encodes data in DNS queries over port 53.
- Domain impersonation: look for one-character differences in domain names.
- TCP flag anomalies: e.g., SYN/ACK without previous SYN, unusual ports.
- ARP poisoning / MITM: attackers intercept LAN traffic using ARP spoofing.
- TLS inspection: weak TLS versions (SSL 3.0, TLS 1.0/1.1) indicate outdated encryption.

---

## 8. Summary & Key Takeaways

Networking and protocol knowledge underpins modern workplace security. For SOC engineers:

- Understanding traffic flows enables effective hunting and detection.
- DNS is a high-value telemetry source for email and cloud service threat detection.
- Segmentation, routing and protocol awareness reduce attack surfaces.
- Even in cloud-first environments such as M365, foundational networking is critical.
