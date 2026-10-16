# Ticket 03 - Account Disable and Re-enable - Alex Turner

## Summary

Alex Turner required his domain account to be disabled and later re-enabled as part of an account lifecycle support task. I used Active Directory Users and Computers to perform both account changes and verified the confirmation messages.

## Environment

- Host OS: Windows PC
- Virtualization platform: Oracle VirtualBox
- Domain: `nicklab.local`
- Server VM: `NICKLAB-DC01`
- User account: Alex Turner
- Tool used: Active Directory Users and Computers

## Issue

Alex Turner's account access needed to be disabled and subsequently restored as part of the account lifecycle workflow.

## Troubleshooting Steps

1. Opened Active Directory Users and Computers on the domain controller.
2. Located Alex Turner in the Users OU.
3. Disabled the user account and verified that the success confirmation appeared.
4. Re-enabled the user account and verified the corresponding success confirmation.

## Resolution

The account disable and re-enable process was completed successfully. Screenshots 38 and 39 document the two account lifecycle changes.

## Screenshot References

- `screenshots/active-directory/38-account-disabled-alex-turner.png`
- `screenshots/active-directory/39-account-enabled-alex-turner.png`

## Skills Demonstrated

Account lifecycle support, access control, offboarding-style account handling, restoring access, and audit-friendly documentation.

## Help Desk Takeaway

Account lifecycle tasks require technicians to manage account access carefully and verify each change. Confirming both the disabled and enabled states helps ensure that the requested account action was completed and documented.
