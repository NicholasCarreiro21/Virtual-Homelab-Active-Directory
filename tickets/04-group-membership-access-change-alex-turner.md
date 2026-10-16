# Ticket 04 - Group Membership Access Change - Alex Turner

## Summary

Alex Turner needed access associated with the `Sales-Shared` security group. I used Active Directory Users and Computers to locate his account, add him to the group, and verify that the membership update was successful.

## Environment

- Host OS: Windows PC
- Virtualization platform: Oracle VirtualBox
- Domain: `nicklab.local`
- Server VM: `NICKLAB-DC01`
- User account: Alex Turner
- Security group: `Sales-Shared`
- Tool used: Active Directory Users and Computers

## Issue

Alex Turner needed to be added to the `Sales-Shared` security group to receive the access associated with that group.

## Troubleshooting Steps

1. Opened Active Directory Users and Computers on the domain controller.
2. Located Alex Turner in the Users OU.
3. Used the Add to a group option to add Alex Turner to the `Sales-Shared` security group.
4. Confirmed that Active Directory reported the group membership update had completed successfully.

## Resolution

Alex Turner was successfully added to the `Sales-Shared` security group. Screenshot 40 documents the completed group membership change.

## Screenshot Reference

- `screenshots/active-directory/Group%20Membership%20Added%20-%20Alex%20Turner.png`

## Skills Demonstrated

Group membership updates, access management, role-based access basics, and support-style documentation.

## Help Desk Takeaway

Security group membership is one way to manage access in an Active Directory environment. A technician should locate the correct user, update the intended group membership, and verify that the change was successful.
