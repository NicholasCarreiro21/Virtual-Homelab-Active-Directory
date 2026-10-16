# Ticket 01 — Windows 11 Client VM Boot Troubleshooting

## Ticket Details

- **Ticket ID:** HD-001
- **Category:** Hardware / Virtual Machine Troubleshooting
- **Priority:** Medium
- **Status:** Resolved
- **Environment:** Oracle VirtualBox, Windows 11 Pro client VM

## Issue Reported

During the initial setup of the help desk homelab, the Windows 11 client virtual machine did not boot as expected. The client workstation needed to start correctly before Windows configuration, network connectivity testing, and Active Directory domain joining could be completed.

The issue needed to be investigated within VirtualBox to confirm that the virtual machine was configured correctly and that the Windows 11 installation could proceed.

## Troubleshooting Steps

1. Opened Oracle VirtualBox and selected the Windows 11 client virtual machine to review its configuration before continuing the installation.
2. Reviewed the virtual machine's hardware settings, including allocated memory, processor resources, virtual hard disk, and attached Windows 11 installation ISO.
3. Checked the virtual machine's storage configuration to confirm that the installation media was attached and available during startup.
4. Reviewed the boot configuration and confirmed that the virtual machine was attempting to start using the intended Windows 11 installation media.
5. Started the virtual machine and monitored the startup process to determine whether it could load the Windows installation environment.
6. Continued through the Windows 11 installation process, selecting the appropriate installation options and proceeding with the operating system setup.
7. Allowed Windows Setup to complete and confirmed that the client virtual machine could reach the Windows 11 desktop.
8. Verified that the workstation was ready for the remaining lab configuration, including network adapter setup, IP addressing, DNS configuration, and domain joining.

## Resolution

Corrected the client virtual machine setup and completed the Windows 11 installation. The workstation successfully reached the desktop and was ready for the next stages of the Active Directory lab.

## Verification

Confirmed that the Windows 11 client virtual machine started successfully in VirtualBox and loaded the desktop without requiring the installation process to be repeated. The client could then be configured for communication with the Windows Server 2022 domain controller.

## Root Cause / Findings

The issue was addressed by reviewing the virtual machine configuration and installation setup before proceeding with the operating system installation. This helped establish a working client environment for the remaining domain and help desk exercises.

## Support Notes

Virtual machine startup issues can originate from incorrect virtual hardware settings, missing installation media, or an incorrect boot configuration. A structured approach helps narrow down the problem before making unnecessary changes. Confirming that the operating system reaches the desktop is an important checkpoint before troubleshooting network connectivity or domain authentication.

This scenario demonstrates basic virtual machine troubleshooting, Windows installation, configuration review, and verification of a working client endpoint.
