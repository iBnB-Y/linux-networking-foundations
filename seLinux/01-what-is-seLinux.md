
# What is SELinux?

SELinux (Security-Enhanced Linux) is a kernel-level security system that controls
what processes are allowed to do, even if normal Linux permissions allow it.

---

## The problem with normal Linux permissions

Traditional Linux security uses:
- Users
- Groups
- File permissions (rwx)

Once a process is allowed to run, Linux permissions cannot limit its behavior.

If a service is compromised, an attacker can abuse the permissions of that service.

---

## What SELinux solves

SELinux adds Mandatory Access Control (MAC).

This means:
- Even if permissions allow an action
- Even if the user is correct
- Even if the process is running normally

SELinux can still block the action.

---

## Simple example

Apache is allowed to read web files:
- `/var/www/html/index.html` → allowed
- `/etc/shadow` → blocked by SELinux

This prevents damage after compromise.

---

## One-sentence definition

SELinux limits what a process can do even after it is compromised.

---

## Why SELinux matters

 Reduces attack impact
 Protects servers and containers
 Used by Fedora, RHEL, Rocky, Alma
 Critical for DevOps and DevSecOps
