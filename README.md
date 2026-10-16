# Virtual-Homelab-Active-Directory

## Recruiter TL;DR

Practical Windows help desk portfolio lab built with VirtualBox, Windows Server 2022, and Windows 11 Pro. Covers Active Directory setup, domain join, password resets, account enable/disable, group membership changes, shared-folder access, mapped drives, and Group Policy restrictions - documented with screenshots and help desk ticket write-ups.

This project is designed to demonstrate entry-level Windows support skills through hands-on lab work, troubleshooting, and technical documentation.

## Project Overview

A practical Windows help desk portfolio project documenting virtual machine setup, Windows Server preparation, Active Directory Domain Services configuration, and ticket-style troubleshooting workflows.

This project demonstrates the ability to follow a structured lab process, document work clearly, organize screenshots, troubleshoot setup issues, and explain Windows support tasks in a professional way.

## Why This Project Matters

Hiring managers evaluating entry-level support candidates need evidence that I can:

- Follow instructions and document their process.
- Set up a basic technical lab.
- Use Windows tools and command-line utilities.
- Prepare Windows Server and Windows client environments.
- Work with Active Directory users, groups, and access permissions.
- Capture clear troubleshooting evidence.
- Write ticket-style documentation.
- Explain what they did, what went wrong, how they fixed it, and why it matters.

## Lab Environment

| Component | Configuration |
|---|---|
| Host Machine | Windows PC |
| Virtualization | Oracle VirtualBox |
| Server OS | Windows Server 2022 Evaluation |
| Domain | `nicklab.local` |
| Client OS | Windows 11 Pro |
| Client VM | NICKLAB-WIN11-01 |
| Network | VirtualBox Internal Network |


## Tools Used

- Oracle VirtualBox
- Windows Server 2022 Evaluation ISO
- Windows 11 ISO
- Active Directory Domain Services
- DNS
- Active Directory Users and Computers
- Group Policy Management
- Windows networking tools
- PowerShell
- Git
- GitHub
- Markdown

## Current Status

The core lab setup and help desk scenarios are complete. The project includes the Windows Server environment, the `nicklab.local` domain, Active Directory users and groups, a Windows 11 domain client, shared-folder access, mapped drive configuration, and Group Policy testing.

Completed work includes:

- Created a project folder structure for screenshots and documentation.
- Installed and verified VirtualBox.
- Downloaded Windows Server and Windows 11 installation media.
- Created and configured the Windows Server virtual machine.
- Installed Windows Server 2022.
- Renamed and configured the server.
- Installed Active Directory Domain Services.
- Promoted the server to a domain controller.
- Created the `nicklab.local` domain.
- Created and organized Active Directory objects.
- Created test users and security groups.
- Assigned users to security groups.
- Created and installed the Windows 11 client virtual machine.
- Configured the client network and DNS settings.
- Joined Windows 11 to the domain.
- Practised password resets and account enable/disable workflows.
- Changed group membership to practise access management.
- Configured and tested shared-folder access and a mapped network drive.
- Configured and tested a Group Policy restriction.
- Documented the lab with screenshots and help desk scenarios.

## Screenshots

### 1. Project Folder Structure
Organized the project files into separate folders for screenshots, help desk tickets, notes, diagrams, and documentation to keep the lab evidence easy to navigate and maintain.

### 2. VirtualBox Installed
Installed and verified Oracle VirtualBox using PowerShell and winget. VirtualBox provides the virtualization environment for running the Windows Server and Windows client machines on one computer.

### 3. Windows Server ISO Downloaded
Downloaded the Windows Server 2022 Evaluation ISO to use as the installation media for the server virtual machine.

### 4. Windows 11 ISO Download Started
Started downloading the Windows 11 ISO using the PowerShell/Fido method to prepare the installation media for the client workstation.

### 5. Windows 11 ISO Downloaded
Verified that the Windows 11 ISO downloaded successfully and was ready to be attached to the client virtual machine.

### 6. Windows Server VM ISO Setup
Created the Windows Server virtual machine in VirtualBox and attached the installation ISO so the VM could boot into Windows Setup.

### 7. Windows Server VM Hardware Setup
Configured the virtual machine's memory, CPU, and virtual disk allocation to provide the resources required to run Windows Server.

### 8. Windows Server VM Created
Verified that the server VM was created with the expected hardware allocation and installation media before beginning the operating system installation.

### 9. Windows Server Setup Start
Booted the server VM from the attached ISO and started the Windows Server installation process.

### 10. Windows Server Edition Selection
Selected Windows Server 2022 Standard Evaluation with Desktop Experience to provide a graphical interface for server configuration and administration.

### 11. Windows Server Custom Install Type
Selected the custom installation option to perform a clean Windows Server installation on the VM's virtual disk.

### 12. Windows Server Drive Selection
Selected the 60 GB unallocated virtual disk as the installation destination for Windows Server.

### 13. Windows Server Login Screen
Confirmed that Windows Server completed installation and reached the login screen, indicating that the VM was ready for initial configuration.

### 14. Windows Server Manager Dashboard
Verified that Server Manager launched successfully after installation. Server Manager provides access to server configuration and role management, including the setup of Active Directory Domain Services.

### 15. Server Renamed
Renamed the server to establish a consistent hostname for the lab. A clearly identified server is easier to recognize when configuring services and troubleshooting connectivity.

### 16. Add Roles and Features Wizard
Opened the Add Roles and Features Wizard in Server Manager to begin installing the server role required for Active Directory administration.

### 17. Active Directory Domain Services Selected
Selected Active Directory Domain Services (AD DS), which provides centralized management of domain accounts, computers, and authentication.

### 18. Confirm AD DS Installation
Reviewed the selected AD DS role and installation options before confirming the installation.

### 19. AD DS Installed — Promotion Required
Completed the AD DS role installation. The server still required promotion to a domain controller before it could host the Active Directory domain.

### 20. Domain Controller Deployment Configuration
Started the domain controller promotion process and configured a new forest for the `nicklab.local` lab domain.

### 21. DNS Options Warning
Reviewed the DNS delegation warning displayed during setup. This warning is expected in a standalone lab without an existing parent DNS zone configured for delegation.

### 22. Review Domain Controller Options
Reviewed the domain controller deployment settings and confirmed the intended forest and domain configuration before proceeding.

### 23. Prerequisites Check Passed
Confirmed that the prerequisite checks passed, allowing the domain controller promotion process to continue.

### 24. Server Manager After Domain Reboot
Verified that the server restarted after promotion and returned to the desktop, allowing the new domain controller configuration to take effect.

### 25. Domain Confirmed on Local Server
Verified the server's domain configuration after promotion, confirming that the Active Directory environment was established for the lab.

### 26. Active Directory Users and Computers Open
Opened Active Directory Users and Computers (ADUC) to manage domain user accounts, security groups, and organizational units.

### 27. Active Directory OU Structure Created
Created an organizational unit (OU) structure to separate users, groups, disabled accounts, and workstations. This organization makes directory objects easier to manage and supports more targeted administration.

### 28. Active Directory Security Groups Created
Created security groups for the lab's access-control scenarios. Group-based permissions make it easier to manage access to shared resources according to users' roles or departments.

### 29. Active Directory Test Users Created
Created test user accounts representing different departments and support roles. These accounts provide a controlled way to practise account administration, authentication checks, and access troubleshooting.

### 30. Active Directory Group Membership Assigned
Assigned test users to the appropriate security groups to demonstrate role-based access management and prepare for shared-resource permission testing.

### 31. Windows 11 Client VM Created
Created a Windows 11 client VM to represent an employee workstation. The client is used to test domain connectivity, user authentication, and access to network resources.

### 32. Windows 11 Client VM Network Settings
Reviewed the client's network adapter configuration. Correct network connectivity and DNS settings are essential for locating the domain controller and successfully joining an Active Directory domain.

### 33. Windows 11 Client Installation Started
Started installing Windows 11 on the client VM to prepare the workstation for domain configuration and endpoint support testing.

### 34. Windows 11 Client Desktop Ready
Confirmed that Windows 11 completed installation and reached the desktop. The client was ready for network configuration, domain joining, and user authentication testing.

### 35. Domain Administrator Login Proof
Verified that the Windows client could authenticate using a domain administrator account after joining the lab domain. This helps confirm that domain authentication is functioning on the workstation.

### 36. Domain User Login Proof
Tested sign-in with a standard domain user account to verify that the client could authenticate regular users, not only an administrator.

### 37. Password Reset Success — Jane Smith
Reset Jane Smith's domain account password through Active Directory Users and Computers. This demonstrates a common help desk task for resolving account sign-in issues.

### 38. Account Disabled — Alex Turner
Disabled Alex Turner's domain account in Active Directory to demonstrate how user access can be suspended while the account record remains available for administration.

### 39. Account Enabled — Alex Turner
Re-enabled Alex Turner's account to demonstrate restoring account access after a previous disablement.

### 40. Group Membership Added — Alex Turner
Updated Alex Turner's security group membership in Active Directory to demonstrate how group assignments can be used to manage access to department resources.

### 41. Sales Shared Folder Access — Jane Smith
Verified Jane Smith's access to the Sales shared folder after configuring the required group membership and permissions. This demonstrates how to test whether a user can access a network resource.

### 42. Sales Mapped Drive Access — Jane Smith
Mapped the Sales network share to drive `Z:` on the Windows client and verified access to the shared resource. A mapped drive provides users with a convenient way to access a network folder through File Explorer.

### 43. Group Policy Control Panel Restriction — Jane Smith
Configured a Group Policy Object (GPO) to restrict access to Control Panel and PC Settings for standard domain users. Updated policy on the client and tested the result to verify that the restriction was applied.

## Project Documents

## Help Desk Ticket Writeups

## Completed Help Desk Scenarios

This project documents practical experience with:

- Windows 11 client setup and connectivity troubleshooting.
- Active Directory password reset workflow.
- Disabled-account and account re-enable workflow.
- Group membership and access changes.
- Shared-folder permissions and access testing.
- Mapped network drive setup.
- Group Policy restriction and verification.

## Future Optional Enhancements

Possible future additions include:

- A dedicated DNS troubleshooting scenario.
- Printer or shared-resource troubleshooting.
- Windows performance triage.
- A simple network diagram.
- Additional documented support tickets.
- Basic PowerShell automation for user administration.

## Portfolio Value

This project demonstrates practical Windows support skills, Active Directory administration, basic troubleshooting, and clear technical documentation for entry-level IT support roles.
