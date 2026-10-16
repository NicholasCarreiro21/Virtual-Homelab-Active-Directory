# Ticket 01 — Windows 11 Client VM Network Troubleshooting

## Summary

While configuring the Windows 11 client for the help desk lab, the workstation received an automatic private IP address (`169.254.126.117`) instead of the intended static address. This prevented the client from communicating with the domain controller as required for Active Directory and domain services. I reviewed the VirtualBox network configuration and configured static IP addressing and DNS settings for the lab network.

## Environment

- Host OS: Windows PC
- Virtualization platform: Oracle VirtualBox
- Server VM: NickLab domain controller
- Server OS: Windows Server 2022 Evaluation
- Client VM: Windows 11 Pro
- Domain: `nicklab.local`
- VirtualBox network: Internal Network (`nicklab`)
- Server IP address: `192.168.100.10`
- Client IP address: `192.168.100.20`
- Client DNS server: `192.168.100.10`

## Issue

The Windows 11 client initially displayed an APIPA address in the `169.254.x.x` range rather than an address configured for the lab network. The client also needed to use the domain controller for DNS resolution to support communication with the `nicklab.local` domain.

## Troubleshooting Steps

1. Reviewed the Windows 11 client's IP configuration and identified the APIPA address `169.254.126.117`.
2. Checked the VirtualBox network adapter configuration for the client and server virtual machines.
3. Configured both virtual machines to use the same VirtualBox Internal Network named `nicklab`.
4. Assigned the domain controller the static IP address `192.168.100.10` with subnet mask `255.255.255.0`.
5. Configured the domain controller's DNS setting to use `127.0.0.1`.
6. Assigned the Windows 11 client the static IP address `192.168.100.20` with subnet mask `255.255.255.0`.
7. Configured the client's preferred DNS server as `192.168.100.10`, directing domain-related DNS queries to the domain controller.
8. Reviewed the client network configuration to confirm the intended IP address and DNS server were set.
9. Tested connectivity and domain-related functionality after correcting the network settings.

## Resolution

Configured the Windows Server 2022 domain controller and Windows 11 client with static IP addresses on the same VirtualBox Internal Network. The client was configured to use the domain controller at `192.168.100.10` for DNS, providing the network configuration required for the `nicklab.local` Active Directory environment.

## Skills Demonstrated

- Basic Windows IP configuration
- APIPA address identification
- Static IP addressing
- DNS configuration for an Active Directory environment
- VirtualBox network adapter configuration
- Basic client-to-server connectivity troubleshooting
- Documenting troubleshooting steps and configuration changes

## Help Desk Takeaway

When a workstation cannot communicate with domain services, review its IP address, subnet, DNS settings, and virtual or physical network connection. An APIPA address can indicate that the system did not obtain a usable address automatically. In a small lab using an Internal Network without DHCP, static addressing provides a predictable configuration for the client and domain controller.
