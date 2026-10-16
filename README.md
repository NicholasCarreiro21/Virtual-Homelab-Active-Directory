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
| Server VM | NICKLAB-WIN11-01 |
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
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/setup/Project%20Folder%20Structure.png
Organized the project files into separate folders for screenshots, help desk tickets, notes, diagrams, and documentation to keep the lab evidence easy to navigate and maintain.

### 2. VirtualBox Installed
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/setup/VirtualBox%20Installation.png
Installed and verified Oracle VirtualBox using PowerShell and winget. VirtualBox provides the virtualization environment for running the Windows Server and Windows client machines on one computer.

### 3. Windows Server ISO Downloaded
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/setup/Windows%20Server%20ISO%20Download.png
Downloaded the Windows Server 2022 Evaluation ISO to use as the installation media for the server virtual machine.

### 4. Windows 11 ISO Download Started
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/setup/Windows%2011%20ISO%20Install.png
Started downloading the Windows 11 ISO using the PowerShell/Fido method to prepare the installation media for the client workstation.

### 5. Windows 11 ISO Downloaded
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/setup/Windows%2011%20ISO%20Install%20Complete.png
Verified that the Windows 11 ISO downloaded successfully and was ready to be attached to the client virtual machine.

### 6. Windows Server VM ISO Setup
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%20Server%20VM%20ISO%20Setup.png
Created the Windows Server virtual machine in VirtualBox and attached the installation ISO so the VM could boot into Windows Setup.

### 7. Windows Server VM Hardware Setup
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%20Server%20VM%20Hardware%20Setup.png
Configured the virtual machine's memory, CPU, and virtual disk allocation to provide the resources required to run Windows Server.

### 8. Windows Server VM Created
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%20Server%20VM%20Created.png
Verified that the server VM was created with the expected hardware allocation and installation media before beginning the operating system installation.

### 9. Windows Server Setup Start
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%20Server%20Setup%20Start.png
Booted the server VM from the attached ISO and started the Windows Server installation process.

### 10. Windows Server Edition Selection
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%20Server%20Edition%20Selection.png
Selected Windows Server 2022 Standard Evaluation with Desktop Experience to provide a graphical interface for server configuration and administration.

### 11. Windows Server Custom Install Type
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%20Server%20Custom%20Install%20Type.png
Selected the custom installation option to perform a clean Windows Server installation on the VM's virtual disk.

### 12. Windows Server Drive Selection
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%20Server%20Drive%20Selection.png
Selected the 60 GB unallocated virtual disk as the installation destination for Windows Server.

### 13. Windows Server Login Screen
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%20Server%20Login%20Screen.png
Confirmed that Windows Server completed installation and reached the login screen, indicating that the VM was ready for initial configuration.

### 14. Windows Server Manager Dashboard
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/server-configuartion/Windows%20Server%20Manager%20Dashboard.png
Verified that Server Manager launched successfully after installation. Server Manager provides access to server configuration and role management, including the setup of Active Directory Domain Services.

### 15. Server Renamed
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/server-configuartion/Server%20renamed%20to%20NICHOLASLAB-DC01.png
Renamed the server to establish a consistent hostname for the lab. A clearly identified server is easier to recognize when configuring services and troubleshooting connectivity.

### 16. Add Roles and Features Wizard
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Add%20Roles%20to%20Features%20Wizard.png
Opened the Add Roles and Features Wizard in Server Manager to begin installing the server role required for Active Directory administration.

### 17. Active Directory Domain Services Selected
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Active%20Directory%20Domain%20Services%20Selected.png
Selected Active Directory Domain Services (AD DS), which provides centralized management of domain accounts, computers, and authentication.

### 18. Confirm AD DS Installation
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Confirm%20AD%20DS%20Installation.png
Reviewed the selected AD DS role and installation options before confirming the installation.

### 19. AD DS Installed — Promotion Required
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/AD%20DS%20Installed%20-%20Promotion%20required.png
Completed the AD DS role installation. The server still required promotion to a domain controller before it could host the Active Directory domain.

### 20. Domain Controller Deployment Configuration
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Domain%20Controller%20Deployment%20Configuration.png
Started the domain controller promotion process and configured a new forest for the `nicklab.local` lab domain.

### 21. DNS Options Warning
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/DNS%20Options%20Warning.png
Reviewed the DNS delegation warning displayed during setup. This warning is expected in a standalone lab without an existing parent DNS zone configured for delegation.

### 22. Review Domain Controller Options
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Review%20Domain%20Controller%20Options.png
Reviewed the domain controller deployment settings and confirmed the intended forest and domain configuration before proceeding.

### 23. Prerequisites Check Passed
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Prerequisites%20Check%20Passed.png
Confirmed that the prerequisite checks passed, allowing the domain controller promotion process to continue.

### 24. Server Manager After Domain Reboot
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Server%20Manager%20After%20Domain%20Reboot.png
Verified that the server restarted after promotion and returned to the desktop, allowing the new domain controller configuration to take effect.

### 25. Domain Confirmed on Local Server
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Domain%20Confirmed%20On%20Local%20Server.png
Verified the server's domain configuration after promotion, confirming that the Active Directory environment was established for the lab.

### 26. Active Directory Users and Computers Open
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Active%20Directory%20Users%20and%20Computers%20Open.png
Opened Active Directory Users and Computers (ADUC) to manage domain user accounts, security groups, and organizational units.

### 27. Active Directory OU Structure Created
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Active%20Directory%20OU%20Structure%20Created.png
Created an organizational unit (OU) structure to separate users, groups, disabled accounts, and workstations. This organization makes directory objects easier to manage and supports more targeted administration.

### 28. Active Directory Security Groups Created
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Active%20Directory%20Security%20Groups%20Created.png
Created security groups for the lab's access-control scenarios. Group-based permissions make it easier to manage access to shared resources according to users' roles or departments.

### 29. Active Directory Test Users Created
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Active%20Directory%20Test%20Users%20Created.png
Created test user accounts representing different departments and support roles. These accounts provide a controlled way to practise account administration, authentication checks, and access troubleshooting.

### 30. Active Directory Group Membership Assigned
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Active%20Directory%20Group%20Memebership%20Assigned.png
Assigned test users to the appropriate security groups to demonstrate role-based access management and prepare for shared-resource permission testing.

### 31. Windows 11 Client VM Created
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%2011%20Client%20VM%20Created.png
Created a Windows 11 client VM to represent an employee workstation. The client is used to test domain connectivity, user authentication, and access to network resources.

### 32. Windows 11 Client VM Network Settings
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%2011%20Clinet%20VM%20Network%20Settings.png
Reviewed the client's network adapter configuration. Correct network connectivity and DNS settings are essential for locating the domain controller and successfully joining an Active Directory domain.

### 33. Windows 11 Client Installation Started
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%2011%20Client%20Installation%20Started.png
Started installing Windows 11 on the client VM to prepare the workstation for domain configuration and endpoint support testing.

### 34. Windows 11 Client Desktop Ready
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/vm-setup/Windows%2011%20Client%20Desktop%20Ready.png
Confirmed that Windows 11 completed installation and reached the desktop. The client was ready for network configuration, domain joining, and user authentication testing.

### 35. Domain Administrator Login Proof
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Domain%20Administrator%20Login%20Proof.png
Verified that the Windows client could authenticate using a domain administrator account after joining the lab domain. This helps confirm that domain authentication is functioning on the workstation.

### 36. Domain User Login Proof
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Domain%20User%20Login%20Proof.png
Tested sign-in with a standard domain user account to verify that the client could authenticate regular users, not only an administrator.

### 37. Password Reset Success — Jane Smith
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Password%20Reset%20Success%20-%20Jane%20Smith.png
Reset Jane Smith's domain account password through Active Directory Users and Computers. This demonstrates a common help desk task for resolving account sign-in issues.

### 38. Account Disabled — Alex Turner
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Account%20Disabled%20-%20Alex%20Turner.png
Disabled Alex Turner's domain account in Active Directory to demonstrate how user access can be suspended while the account record remains available for administration.

### 39. Account Enabled — Alex Turner
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Account%20Enabled%20-%20Alex%20Turner.png
Re-enabled Alex Turner's account to demonstrate restoring account access after a previous disablement.

### 40. Group Membership Added — Alex Turner
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Group%20Membership%20Added%20-%20Alex%20Turner.png
Updated Alex Turner's security group membership in Active Directory to demonstrate how group assignments can be used to manage access to department resources.

### 41. Sales Shared Folder Access — Jane Smith
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Sales%20Shared%20Folder%20Access%20-%20Jane%20Smith.png
Verified Jane Smith's access to the Sales shared folder after configuring the required group membership and permissions. This demonstrates how to test whether a user can access a network resource.

### 42. Sales Mapped Drive Access — Jane Smith
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Sales%20Mapped%20Drive%20Access.png
Mapped the Sales network share to drive `Z:` on the Windows client and verified access to the shared resource. A mapped drive provides users with a convenient way to access a network folder through File Explorer.

### 43. Group Policy Control Panel Restriction — Jane Smith
!https://github.com/NicholasCarreiro21/Virtual-Homelab-Active-Directory/blob/main/screenshots/active-directory/Group%20Policy%20Control%20Panel%20Restriction%20-%20Jane%20Smith.png
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
