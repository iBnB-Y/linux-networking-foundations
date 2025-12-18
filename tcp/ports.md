
# TCP Ports

TCP ports identify services that use reliable,
connection-oriented communication.

## Common TCP Ports
 22  – SSH
 80  – HTTP
 443 – HTTPS
 25  – SMTP
 3306 – MySQL

## How TCP Ports Work
A TCP connection is uniquely identified by:
 Source IP
 Source Port
 Destination IP
 Destination Port

Clients use ephemeral ports, while servers listen
on well-known ports.

## Practical Commands

### List listening TCP ports
```bash
ss -tln
