# Ticket 01 — Windows 11 Client VM Boot Troubleshooting

## Ticket Details

- **Category:** Hardware / Virtual Machine
- **Priority:** Medium
- **Status:** Resolved
- **Environment:** Oracle VirtualBox, Windows 11 Pro client VM

## Issue Reported

The Windows 11 client virtual machine did not complete startup as expected during lab setup. The client needed to boot correctly before it could be configured for domain connectivity and user sign-in testing.

## Troubleshooting Steps

1. Reviewed the client VM configuration in VirtualBox, including the attached installation media and virtual hardware settings.
2. Checked the VM startup configuration and confirmed it was using the intended Windows 11 installation.
3. Restarted the VM and continued through Windows Setup to confirm the client could complete installation.
4. Verified that Windows 11 reached the desktop before proceeding with network configuration.

## Resolution

Corrected the client VM setup and continued the Windows 11 installation until the workstation reached the desktop successfully.

## Verification

Confirmed that the client VM started and loaded the Windows 11 desktop. The machine was then available for network configuration and joining the Active Directory domain.

## Support Notes

A virtual machine that does not start correctly should be checked systematically, beginning with its configuration and boot media before moving on to operating system troubleshooting. Confirming that the desktop loads provides a clear checkpoint before continuing with domain and network setup.
