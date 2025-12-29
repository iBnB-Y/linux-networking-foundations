
# SELinux Modes

SELinux operates in three distinct modes that determine how security policies are applied on a Linux system.

---

## 1. Enforcing Mode

Enforcing mode is the default and most secure SELinux mode.

- Security policies are actively enforced
- Unauthorized access attempts are blocked
- All policy violations are logged

This mode is recommended for production systems.

---

## 2. Permissive Mode

Permissive mode is used mainly for troubleshooting and learning.

- SELinux does not block actions
- Policy violations are logged
- System functionality is not interrupted

Permissive mode allows administrators to analyze what SELinux would block without enforcing restrictions.

---

## 3. Disabled Mode

Disabled mode turns SELinux off completely.

- No security policies are enforced
- No access violations are logged
- System loses an important security layer

Disabling SELinux is not recommended for production environments.

---

## Checking and Changing SELinux Mode

Check current mode:

