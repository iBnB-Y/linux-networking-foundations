
# UDP Ports

UDP ports identify services that use fast,
connectionless communication.

## Common UDP Ports
 53  – DNS
 67/68 – DHCP
 123 – NTP
 5060 – SIP

## How UDP Ports Work
UDP uses ports to deliver packets to the
correct application without establishing
a connection.

UDP ports are independent from TCP ports.

## Practical Commands

### List listening UDP ports
```bash
ss -uln
