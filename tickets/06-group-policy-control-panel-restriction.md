# Ticket 06 - Control Panel Restricted by Group Policy

## Summary

Jane Smith attempted to open Control Panel on the Windows 11 client and was blocked by an administrator restriction message. I configured a Group Policy Object to restrict access to Control Panel and PC Settings, refreshed policy on the client, and tested the restriction while signed in as the standard domain user.

## User Impact

The user could not access Control Panel or PC Settings because a domain policy restricted access for standard users.

## Environment

- Host OS: Windows PC
- Virtualization platform: Oracle VirtualBox
- Domain: `nicklab.local`
- Server VM: `NICKLAB-DC01`
- Client workstation: `NICKLAB-WIN11-01`
- User: `NICKLAB\j.smith`
- GPO: Control Panel restriction GPO
- Linked OU: Users OU

## Issue

Jane Smith was blocked from opening Control Panel on the Windows 11 client because of an administrator restriction applied through Group Policy.

## Troubleshooting Steps

1. Opened Group Policy Management on `NICKLAB-DC01`.
2. Created a new Group Policy Object for the Control Panel restriction.
3. Linked the GPO to the Users OU.
4. Edited the GPO under User Configuration > Policies > Administrative Templates > Control Panel.
5. Enabled the **Prohibit access to Control Panel and PC settings** policy.
6. Ran `gpupdate /force` on the Windows 11 client to refresh Group Policy.
7. Tested Control Panel access while signed in as `NICKLAB\j.smith`.
8. Confirmed that Windows blocked access and displayed an administrator restriction message.

## Resolution

A Group Policy Object was configured and applied to prevent standard domain users in the targeted OU from opening Control Panel and PC Settings. The restriction was verified on the Windows 11 client.

## Portfolio Evidence

- `screenshots/active-directory/Group%20Policy%20Control%20Panel%20Restriction%20-%20Jane%20Smith.png`

## Skills Demonstrated

- Group Policy Management
- GPO creation and OU linking
- User Configuration policy enforcement
- gpupdate testing
- Windows client policy verification
- Help desk documentation

## Help Desk Takeaway

Group Policy can be used to enforce user restrictions across a domain. A technician should configure the correct user policy, link the GPO to the intended OU, refresh policy on the client, and test the setting under the affected user account to verify that it works as expected.
