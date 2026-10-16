# Ticket 01: Windows Client VM Boot Troubleshooting

## Ticket Information
- **Ticket ID:** HD-001
- **Category:** Hardware / Virtual Machine
- **Priority:** Medium
- **Status:** Resolved
- **Affected System:** Windows 11 Pro Client VM
- **Environment:** Oracle VirtualBox

## Issue
The Windows 11 client virtual machine was not communicating correctly with the domain controller. Initial troubleshooting showed that the client had an APIPA address (`169.254.126.117`), indicating that it had not obtained a usable network configuration.

## Troubleshooting Steps
1. Opened Oracle VirtualBox and reviewed the Windows 11 client VM settings.
2. Verified that the client and Windows Server 2022 domain controller were connected to the same Internal Network.
3. Configured the Internal Network name as `nicklab` on both virtual machines.
4. Configured the client with a static IPv4 address of `192.168.100.20`.
5. Set the subnet mask to `255.255.255.0`.
6. Configured the preferred DNS server as `192.168.100.10`, the domain controller's IP address.
7. Verified that the domain controller used the static IP address `192.168.100.10`.
8. Tested network connectivity between the client and domain controller.

## Resolution
The client was configured to use the correct internal virtual network and static network settings. The client could communicate with the domain controller and locate the domain for joining.

## Skills Demonstrated
- Virtual machine troubleshooting
- IPv4 configuration
- DNS configuration
- Basic network troubleshooting
- Windows client administration
