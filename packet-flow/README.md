
# Network Packet Flow

This section explains how packets move from a client to the internet.



## Typical Packet Flow
1. **DHCP**
   - Client requests IP configuration
2. **DNS**
   - Domain name resolved to IP
3. **Routing**
   - Packet sent to default gateway
4. **NAT**
   - Private IP translated to public IP
5. **Internet**
   - Packet reaches destination
6. **Response**
   - Translated back and delivered


## Example: Visiting google.com
1. Device gets IP via DHCP
2. DNS resolves google.com
3. Router forwards traffic
4. NAT translates address
5. Response returns to client


## Why This Matters
 Troubleshooting
 Security analysis
 Network design
