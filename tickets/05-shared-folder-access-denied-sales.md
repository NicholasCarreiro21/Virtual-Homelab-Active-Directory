# Ticket 05 - Shared Folder Access Denied - Sales Share

## Summary

Jane Smith attempted to open the Sales shared folder from the Windows 11 client but received a network access denied message. I investigated the share and the user's group membership, updated the relevant access membership, refreshed the user's session, and tested the shared folder and mapped drive again.

## User Impact

The user could not access the department's shared folder needed for Sales files.

## Environment

- Host OS: Windows PC
- Virtualization platform: Oracle VirtualBox
- Domain: `nicklab.local`
- Server VM: `NICKLAB-DC01`
- Client workstation: `NICKLAB-WIN11-01`
- User: `NICKLAB\j.smith`
- Shared folder path: `\\NICKLAB-DC01\Sales`
- Security group: `Sales-Shared`

## Issue

Jane Smith received an access denied message when trying to open the Sales shared folder from the Windows 11 client.

## Troubleshooting Steps

1. Verified that the Sales SMB share existed on `NICKLAB-DC01`.
2. Checked that the shared folder path could be reached from the Windows 11 client.
3. Confirmed that the user received an access denied message, indicating that the network path was reachable but access was being denied.
4. Reviewed Active Directory group membership for the `Sales-Shared` security group.
5. Added Jane Smith to the `Sales-Shared` security group.
6. Signed the user out and back in so the updated group membership could take effect in the user session.
7. Tested access to `\\NICKLAB-DC01\Sales` again from the Windows 11 client.
8. Verified that the user could open the shared folder and view `Sales-Info.txt`.
9. Mapped the Sales share to drive letter `Z:` and confirmed that the mapped drive worked.

## Resolution

Jane Smith (`NICKLAB\j.smith`) was added to the `Sales-Shared` Active Directory security group. After refreshing the user session, I verified access to the Sales shared folder and confirmed that the share worked as mapped drive `Z:`.

## Portfolio Evidence

- `screenshots/active-directory/Sales%20Shared%20Folder%20Access%20-%20Jane%20Smith.png`
- `screenshots/active-directory/Sales%20Mapped%20Drive%20Access.png`

## Skills Demonstrated

- Active Directory group membership troubleshooting
- Shared folder permission validation
- SMB share access testing
- Mapped network drive setup
- User-session refresh after permission changes
- Clear help desk ticket documentation

## Help Desk Takeaway

When a user receives an access denied message for a network share, a technician should verify the share and its reachability, check the user's group membership, apply the appropriate access change, and refresh the user session if necessary. Retesting both the shared folder and mapped drive confirms whether access has been restored.
