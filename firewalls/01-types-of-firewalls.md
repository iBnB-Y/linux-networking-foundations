
# Types of Firewalls: Stateless vs Stateful

Firewalls control network traffic by applying rules.  
The way they make decisions defines their type.

---

## 1. Stateless Firewall

A stateless firewall examines **each packet independently**.

### How it works
Looks only at:
   Source IP
   Destination IP
   Port
   Protocol
 Does NOT remember previous packets

### Example
Rule:
"Allow traffic on port 80"

If a packet matches port 80 → ALLOW 
If not → BLOCK

The firewall does not know:
 If this packet is part of an existing connection
 If it is legitimate or malicious

### Pros
 Fast
 Simple
 Low resource usage

### Cons
 Less secure
 Cannot track connections
 Vulnerable to spoofing attacks

### Real-world use
 Basic network devices
 Very simple filtering systems

---

## 2. Stateful Firewall

A stateful firewall **tracks the state of connections**.

### How it works
 Remembers:
   Connection start
   Connection state
   Connection end
 Allows return traffic automatically

### Example
You visit a website:
1. Outgoing request → allowed
2. Incoming response → allowed automatically

No need for separate rules.

### Pros
 Much more secure
 Understands real connections
 Blocks unexpected packets

### Cons
 Slightly more resource usage
 More complex

---

## 3. Which one does Linux use?

Linux firewalls are **stateful by default**.

They use:
 Connection tracking (conntrack)
 Kernel-level inspection

This makes Linux firewalls suitable for:
 Servers
 Cloud infrastructure
 DevOps environments

---

## Key takeaway

Stateless firewalls check packets. 
Stateful firewalls understand conversations.

Modern systems rely on **stateful firewalls**.
