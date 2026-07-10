# NAT Configuration

## Purpose

Allow internal networks to access external networks while hiding private IP ranges behind the WAN address.

## Internal Networks

- USERS (10.10.10.0/24)
- SERVERS (10.10.20.0/24)
- DMZ (10.10.30.0/24)
- MGMT (10.10.40.0/24)

## WAN

Internet-facing interface used for outbound traffic.

## NAT Mode

Automatic Outbound NAT

## Function

Outbound NAT translates private internal addresses to the WAN address before traffic is sent to the Internet.

## Result

All internal VLANs can access Internet resources while remaining hidden behind a single public-facing address.
