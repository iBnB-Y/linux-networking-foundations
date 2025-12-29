
# SELinux vs Firewall

SELinux and firewalls are both security mechanisms, but they solve
different problems and operate at different levels of the system.

They are complementary, not replacements for each other.

---

## What a Firewall Does

A firewall controls **network traffic**.

It decides:
- What traffic can enter the system (incoming)
- What traffic can leave the system (outgoing)
- Based on IPs, ports, protocols, and direction

### Firewall focus
- Network-level security
- External threats
- Packet filtering

### Example
- Allow SSH on port 22
- Block all other incoming connections

---

## What SELinux Does

SELinux controls **process behavior** inside the system.

It decides:
- What a process can access
- What files it can read or write
- What actions it can perform

Even if:
- File permissions allow it
- The user is correct
- The process is running normally

SELinux can still block the action.

---

## Simple Analogy

- Firewall = Security gate at the entrance
- SELinux = Guards inside the building

The firewall stops unwanted visitors.
SELinux limits damage if someone gets inside.

---

## Key Differences

| Feature | Firewall | SELinux |
|------|--------|---------|
| Controls | Network traffic | Process actions |
| Level | Network | Kernel / process |
| Protects against | External attacks | Internal damage |
| Based on | IPs, ports, protocols | Labels and policies |
| Works after compromise | ❌ No | ✅ Yes |

---

## How They Work Together

Best practice is to use **both**:

1. Firewall blocks unwanted network access
2. SELinux restricts compromised services
3. Combined defense reduces attack impact

This is known as **defense in depth**.

---

## DevOps and Security Perspective

- Firewalls protect infrastructure
- SELinux protects services
- Fedora / RHEL enable SELinux by default
- Disabling SELinux weakens server security

---

## Key takeaway

Firewalls protect the system from the outside. 
SELinux protects the system from the inside.

Both are essential for secure Linux systems.
