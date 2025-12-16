
# OSI Model (Open Systems Interconnection)

The OSI model explains how data moves from one computer to another over a network.
It is a conceptual model with 7 layers, each responsible for a specific task.

---

## Layer 7 – Application
**What it does:** 
Provides network services to user applications.

**Examples:** 
HTTP, HTTPS, FTP, SSH, DNS

**Linux tools:** 
curl, ssh, wget

**Security Insight:** 
Most attacks happen here (SQLi, XSS, auth bypass).

---

## Layer 6 – Presentation
**What it does:** 
Formats, encrypts, and compresses data.

**Examples:** 
TLS/SSL, encryption, encoding

**Security Insight:** 
Weak encryption or misconfigured TLS exposes data.

---

## Layer 5 – Session
**What it does:** 
Manages sessions between two systems.

**Examples:** 
Session cookies, authentication sessions

**Security Insight:** 
Session hijacking and fixation attacks target this layer.

---

## Layer 4 – Transport
**What it does:** 
Controls how data is delivered (reliability and ports).

**Protocols:** 
TCP, UDP

**Linux tools:** 
ss, netstat

**Security Insight:** 
Port scanning and DoS attacks operate here.

---

## Layer 3 – Network
**What it does:** 
Routes packets between networks.

**Protocols:** 
IP, ICMP

**Linux tools:** 
ip route, traceroute

**Security Insight:** 
IP spoofing and routing misconfigurations occur here.

---

## Layer 2 – Data Link
**What it does:** 
Handles MAC addressing and local network delivery.

**Protocols:** 
Ethernet, ARP

**Linux tools:** 
ip link, arp

**Security Insight:** 
ARP spoofing attacks happen at this layer.

---

## Layer 1 – Physical
**What it does:** 
Transmits raw bits over physical media.

**Examples:** 
Cables, Wi-Fi signals, NICs

**Security Insight:** 
Physical access = total compromise.

---

## Key Takeaway
Understanding the OSI model helps map:
- Attacks → where they happen
- Defenses → where to apply controls
- Tools → what layer they operate on

