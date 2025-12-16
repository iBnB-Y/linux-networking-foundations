
# Linux Network Interfaces

## What is a network interface?
A network interface is how a Linux system connects to a network (Wi-Fi, Ethernet, virtual).

## How I checked my interfaces
Command used:
ip a

## What I observed
- Interfaces have names like wlp0s20f3 or eth0
- An interface can be UP or DOWN
- IP addresses are assigned to interfaces

## Security Insight
If an interface is down, the system cannot send or receive network traffic.
Disabling unused interfaces reduces attack surface.

