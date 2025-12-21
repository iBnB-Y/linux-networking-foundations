
# NAT vs Bridged Networking (SSH)

## Why This Matters
SSH requires network reachability. NAT hides services; Bridged exposes them.

---

## NAT Mode
 VM hidden behind host
 IP example: 10.0.2.15
 Host cannot SSH into VM
 Suitable for internet-only access

Test:
ping 10.0.2.15
ssh user@10.0.2.15

Result: ❌ Fails

---

## Bridged Mode
 VM appears as a real LAN device
 IP example: 192.168.1.120
 Host can SSH into VM

Test:
ping 192.168.1.120
ssh user@192.168.1.120

Result: ✅ Works

---

## Security Implication
 Bridged exposes SSH on LAN
 Use SSH keys
 Disable password authentication
