
# Lab 2: SSH Connection Test

## Goal
Connect from a client machine to the SSH server and confirm remote control.

---

## Step 1: Scan SSH port (attacker mindset)

From CLIENT machine:

```bash
nmap -p 22 192.168.1.X
