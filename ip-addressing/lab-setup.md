
# Lab 1: SSH Setup (Real Machine)

## Goal
Install and prepare an SSH server on a Linux machine connected to the same Wi‑Fi network.

---

## Lab Environment
 Client: Kali / Ubuntu / Parrot (your laptop)
 Server: Ubuntu Server or another Linux machine / VM
 Network: Same router (private IP: 192.168.x.x)

---

## Step 1: Install SSH server (SERVER MACHINE)

```bash
sudo apt update
sudo apt install openssh-server -y
