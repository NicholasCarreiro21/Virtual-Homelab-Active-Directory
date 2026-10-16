# Ticket 01 — Windows 11 Client VM Boot Troubleshooting

## Summary

During setup of the Windows 11 client virtual machine for the help desk lab, the VM did not boot into Windows Setup as expected. The screen remained black or the VM failed to start from the installation media. I approached the issue methodically by checking the symptoms, reviewing the VM configuration, testing possible fixes individually, and documenting the successful resolution.

## Environment

- Host OS: Windows PC
- Virtualization platform: Oracle VirtualBox
- Server VM: `NICKLAB-DC01`
- Client VM: `NICKLAB-WIN11-01`
- Intended client OS: Windows 11
- Installation media: Windows 11 ISO (`Windows.iso`)

## Issue

The Windows 11 client virtual machine would not launch the Windows installer normally. Instead, it displayed a black screen or failed to boot from the attached installation media.

## Troubleshooting Steps

1. Checked that the boot issue affected the Windows 11 client VM rather than the existing domain controller VM.
2. Shut down the affected client VM before changing its configuration.
3. Confirmed that the Windows 11 ISO had been downloaded and attached as virtual DVD installation media.
4. Reviewed the VM boot order and configured the optical drive to boot before the virtual hard disk.
5. Checked the EFI and Secure Boot settings in VirtualBox for possible boot compatibility issues.
6. Reviewed the virtual machine display configuration to address the black-screen behavior.
7. Ensured that the Windows 11 ISO was mounted when prompted for installation media.
8. Restarted the VM and pressed a key when the "Press any key to boot from CD or DVD" prompt appeared.

## Resolution

The Windows 11 client VM successfully reached Windows Setup after the ISO was mounted as virtual DVD media and the boot order was configured to prioritize the optical drive.

## Skills Demonstrated

- Virtual machine troubleshooting
- Boot media troubleshooting
- ISO/DVD attachment verification
- Boot order validation
- Basic VirtualBox configuration
- Calm problem solving under a setup failure
- Documenting a real troubleshooting path instead of hiding the mistake

## Help Desk Takeaway

When a device fails to start as expected, a technician should isolate the affected system, confirm the symptoms, and check the most likely causes before making changes. Verifying the installation media and boot configuration, testing your fixes and documenting the process and resolution clearly provides a structured starting point for resolving virtual machine boot problems.
