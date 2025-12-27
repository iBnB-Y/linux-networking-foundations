
# How Linux Enforces Firewall Rules

Linux firewalls operate at the **kernel level**, making them fast and secure.

---

## 1. netfilter – the core engine

At the heart of Linux firewalls is a kernel framework called:

**netfilter**

netfilter:

Intercepts network packets
Decides what happens to them
Enforces firewall rules

User tools do NOT block traffic themselves — the kernel does.

---

## 2. Packet flow inside Linux

When a packet enters a Linux system:

1. Packet arrives at network interface
2. netfilter checks rules
3. Decision is made:
    ACCEPT
    DROP
    REJECT

This happens **before applications see the packet**.

---

## 3. Firewall rule chains (conceptual)

Packets pass through logical checkpoints:
 INPUT (incoming to the system)
 OUTPUT (leaving the system)
 FORWARD (passing through the system)

Rules are checked **top to bottom**.

First match wins.

---

## 4. Tools that control netfilter

Linux provides multiple tools to manage firewall rules:

 iptables (legacy)
 nftables (modern)
 ufw (Ubuntu / Kali frontend)
 firewalld (Fedora / RHEL frontend)

All of them talk to **netfilter**.

---

## 5. Why kernel-level firewalls matter

Because enforcement happens in the kernel:
 Very fast
 Hard to bypass
 Independent of applications

Even if an app is compromised, firewall rules still apply.

---

## Security insight

Linux firewall rules are **not programs**. 
They are **kernel policies**.

This is why Linux is trusted for:
 Servers
 Cloud platforms
 Containers

