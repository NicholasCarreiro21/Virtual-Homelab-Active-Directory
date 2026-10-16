# Ticket 02 - Password Reset - Jane Smith

## Summary

Jane Smith reported that she was unable to sign in using her domain account. I used Active Directory Users and Computers to locate her account, perform a password reset, and confirm that the change was successful.

## Environment

- Host OS: Windows PC
- Virtualization platform: Oracle VirtualBox
- Domain: `nicklab.local`
- Server VM: `NICKLAB-DC01`
- User account: `NICKLAB\j.smith`
- Tool used: Active Directory Users and Computers

## Issue

Jane Smith could not sign in with her domain account and required a password reset.

## Troubleshooting Steps

1. Opened Active Directory Users and Computers on the domain controller.
2. Located Jane Smith in the Users OU.
3. Selected the account's Reset Password option and completed the password reset process.
4. Verified that Active Directory displayed a confirmation indicating the password had been changed successfully.

## Resolution

Jane Smith's domain password was reset successfully. Screenshot 37 provides evidence of the successful password reset confirmation.

## Screenshot Reference

- `screenshots/active-directory/37-password-reset-success-jane-smith.png`

## Skills Demonstrated

Password reset support, Active Directory account lookup, user lifecycle support, and clean support documentation.

## Help Desk Takeaway

When a user cannot sign in to their domain account, a technician should locate the correct account in Active Directory, follow the password reset procedure, and confirm that the change was completed successfully. Documenting the result provides a clear record of the support action.
