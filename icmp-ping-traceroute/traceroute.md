
# Traceroute

Traceroute is a network diagnostic tool used to discover
the path packets take to a destination.

## How It Works
Traceroute sends packets with increasing TTL values.
Each router that drops the packet responds with an
ICMP Time Exceeded message.

## Protocols Used
 UDP (Linux default)
 ICMP (Windows / -I flag)
 TCP (-T flag)

## Common Uses
 Identify routing paths
 Locate network delays
 Troubleshoot connectivity issues
