
# DHCP (Dynamic Host Configuration Protocol)

## Introduction
DHCP automatically assigns IP configuration to devices on a network, eliminating manual setup.

## What DHCP Assigns
 IP address
 Subnet mask
 Default gateway
 DNS server(s)
 Lease time

## Why DHCP Is Important
Without DHCP: manual setup, conflicts, hard management.
With DHCP: plug-and-play, centralized control, scalable.

## How DHCP Works (DORA Process)
1. Discover
2. Offer
3. Request
4. Acknowledge

## DHCP Ports
 UDP 67 (Server)
 UDP 68 (Client)

## DHCP Lease
 Temporary IP assignments
 Renewal before expiration
 Expired IP may be reassigned

## Types of DHCP Allocation
1. Dynamic Allocation
2. Automatic Allocation
3. Reservation

## DHCP vs Static IP

| Feature | DHCP | Static IP |
|---------|------|-----------|
| Configuration | Automatic | Manual |
| IP Conflicts | Rare | Common |
| Management | Easy | Hard |
| Use Case | Client devices | Servers, routers |

## DHCP in Networks
 Home: router is DHCP server, small IP pool
 Enterprise: dedicated DHCP servers, VLAN support, failover

## OSI Model
 Application Layer (Layer 7)

## Linux Commands
Check IP: `ip a`
Request new IP: `sudo dhclient` 
Release IP: `sudo dhclient -r`

## Common Issues
 APIPA (169.254.x.x)
 Rogue DHCP servers
 DHCP starvation attacks
