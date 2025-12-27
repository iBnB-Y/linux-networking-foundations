
# Types of Firewalls: Stateless vs Stateful

A firewall controls network traffic by allowing or blocking connections based on rules.  
The way it makes these decisions determines its type.

---

## 1. Stateless Firewall

**Definition:**  
A stateless firewall examines each packet independently, without remembering previous packets.

**How it works:**
- Checks source IP, destination IP, port, protocol
- Does not track connection state

**Analogy:**  
Security guard checks every visitor but forgets who already entered.

**Pros:**
- Fast
- Simple
- Low memory usage

**Cons:**
- Less secure
- Cannot track ongoing connections
- Vulnerable to spoofing

**Example:**  
Rule: “Allow traffic on port 80”  
Every packet on port 80 → allowed  
Other packets → blocked  

---

## 2. Stateful Firewall

**Definition:**  
A stateful firewall tracks the state of connections, knowing if a packet is part of an existing session.

**How it works:**
- Maintains a connection table
- Automatically allows return traffic of established connections

**Analogy:**  
Security guard remembers who came in and blocks unexpected visitors.

**Pros:**
- More secure
- Tracks real connection flows
- Blocks unexpected/malicious packets

**Cons:**
- Slightly higher resource usage
- More complex

**Example:**  
You visit a website:
1. Outgoing request → allowed
2. Server reply → automatically allowed

---

## 3. Key Differences

| Feature | Stateless | Stateful |
|---------|-----------|----------|
| Packet tracking | ❌ No | ✅ Yes |
| Connection awareness | ❌ None | ✅ Tracks sessions |
| Security | ⚠️ Basic | ✅ Strong |
| Resource usage | Low | Medium |
| Complexity | Simple | More complex |
| Use case | Basic routers | Modern Linux servers, cloud |

---

## 4. Linux perspective

 Linux firewalls (iptables, nftables, ufw, firewalld) are **stateful by default**
 Use **connection tracking** (conntrack)
 Secure servers and cloud infrastructure efficiently

---

## 5. Security principle

> Always use stateful firewalls: allow only required traffic, block everything unexpected.
