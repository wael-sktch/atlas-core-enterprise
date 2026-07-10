# pfSense Firewall Policy

## USERS VLAN (10.10.10.0/24)

Allowed:
- DNS to DC01
- Active Directory Services
- File Server Access (FS01)
- Internet Access

Blocked:
- DMZ Network
- MGMT Network

## DMZ VLAN (10.10.30.0/24)

Allowed:
- DNS to DC01
- Internet Access

Blocked:
- USERS Network
- SERVERS Network
- MGMT Network

## MGMT VLAN (10.10.40.0/24)

Allowed:
- RDP (3389)
- SSH (22)
- HTTPS (443)
- Internet Access
