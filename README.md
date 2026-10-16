# Virtual-Homelab-Active-Directory
# Help Desk Homelab

## Recruiter TL;DR

Practical Windows help desk portfolio lab built with VirtualBox, Windows Server 2022, and Windows 11 Pro. Covers Active Directory setup, domain join, password resets, account enable/disable, group membership changes, shared-folder access, mapped drives, and Group Policy restrictions — documented with screenshots and help desk ticket write-ups.

This project is designed to demonstrate entry-level Windows support skills through hands-on lab work, troubleshooting, and technical documentation.

## Project Overview

A practical Windows help desk portfolio project documenting virtual machine setup, Windows Server preparation, Active Directory Domain Services configuration, and ticket-style troubleshooting workflows.

This project is designed for help desk, IT support, and technical support roles. It demonstrates the ability to follow a structured lab process, document work clearly, organize screenshots, troubleshoot setup issues, and explain Windows support tasks in a professional way.

## Why This Project Matters

Hiring managers evaluating entry-level support candidates need evidence that they can:

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
| Directory Services | Active Directory Domain Services |
| Name Resolution | DNS |
| Network | VirtualBox Internal Network |

Update the server and client names below if you want to document their exact hostnames.

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
- Git and GitHub
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

The screenshots below document the lab setup and the support tasks performed. Each description explains what the step demonstrates and how it relates to a practical Windows administration or help desk workflow.

### 1. Project Folder Structure

**Screenshot label:** Project folder structure

Created a clean local project structure for screenshots, tickets, notes, diagrams, and portfolio documentation. Keeping project files organized makes technical work easier to review, maintain, and share with recruiters or other IT professionals.

### 2. VirtualBox Installed

**Screenshot label:** VirtualBox installed

Installed and verified Oracle VirtualBox, the virtualization platform used to run the Windows Server and Windows 11 virtual machines. Virtualization allows the lab to simulate a small business environment without requiring separate physical computers.

### 3. Windows Server ISO Downloaded

**Screenshot label:** Windows Server ISO downloaded

Downloaded and verified the Windows Server 2022 Evaluation installation media. This ISO provides the operating system needed to build the server that will host Active Directory Domain Services and DNS for the lab.

### 4. Windows 11 ISO Download Started

**Screenshot label:** Windows 11 ISO download started

Started downloading the Windows 11 installation media for the client workstation. The client represents an employee computer that can later be configured, joined to the domain, and used to test user sign-in, permissions, and support scenarios.

### 5. Windows 11 ISO Downloaded

**Screenshot label:** Windows 11 ISO downloaded

Verified that the Windows 11 installation media had downloaded successfully and was ready to use. Having the installation media prepared makes it possible to build the client virtual machine and continue with the endpoint support portion of the lab.

### 6. Windows Server VM ISO Setup

**Screenshot label:** Server VM ISO setup

Created the Windows Server virtual machine profile in VirtualBox and attached the Windows Server 2022 ISO. This prepares the virtual machine to boot from the installation media and begin the server operating system installation.

### 7. Windows Server VM Hardware Setup

**Screenshot label:** Server VM hardware setup

Assigned memory, CPU resources, and virtual disk capacity to the Windows Server virtual machine. Choosing suitable virtual hardware is an important preparation step because the server needs enough resources to run Windows Server and the directory services required for the lab.

### 8. Windows Server VM Created

**Screenshot label:** Server VM created

Confirmed that the Windows Server virtual machine was created in VirtualBox with the intended hardware and installation media settings. This established the virtual server that would later become the domain controller for `nicklab.local`.

### 9. Windows Server Setup Start

**Screenshot label:** Windows Server setup start

Started the Windows Server installation inside the VirtualBox virtual machine. This begins the process of building the server environment that will provide centralized user and computer management for the lab.

### 10. Windows Server Edition Selection

**Screenshot label:** Windows Server edition selection

Selected the Windows Server 2022 Standard Evaluation edition with Desktop Experience. The graphical interface makes it easier to practise Windows administration tasks using Server Manager, Active Directory Users and Computers, and other management consoles.

### 11. Windows Server Custom Install Type

**Screenshot label:** Windows Server custom install type

Selected a custom Windows Server installation to perform a clean installation on the virtual machine. This provides a fresh operating system environment for configuring the server roles and domain services required by the lab.

### 12. Windows Server Drive Selection

**Screenshot label:** Windows Server drive selection

Selected the virtual disk as the Windows Server installation target. This step establishes where the operating system will be installed inside the VM and completes an important part of the server build process.

### 13. Windows Server Login Screen

**Screenshot label:** Windows Server login screen

Confirmed that Windows Server installed successfully and reached the login screen. This shows that the initial operating system installation completed and the server was ready for its initial configuration.

### 14. Windows Server Manager Dashboard

**Screenshot label:** Windows Server Manager dashboard

Opened Server Manager after logging into Windows Server. Server Manager is a central administrative console used to review server status, manage roles and features, and begin configuring services such as Active Directory Domain Services.

### 15. Server Renamed

**Screenshot label:** Server renamed confirmed

Renamed the Windows Server virtual machine to give it a consistent identity within the lab. A clear computer name makes it easier to identify the server when managing domain services, configuring network settings, and troubleshooting connections from the Windows client.

### 16. Add Roles and Features Wizard

**Screenshot label:** Add Roles and Features Wizard

Opened the Add Roles and Features Wizard to begin installing the server roles needed for the domain environment. This wizard provides a guided way to add Windows Server functionality without installing a separate operating system.

### 17. Active Directory Domain Services Selected

**Screenshot label:** Active Directory Domain Services selected

Selected Active Directory Domain Services as the server role for the lab. AD DS provides centralized management of domain user accounts, computers, security groups, and authentication, which are foundational concepts in many Windows business environments.

### 18. Confirm AD DS Installation

**Screenshot label:** Confirm AD DS installation

Reviewed and confirmed the Active Directory Domain Services installation selections. Reviewing the selected roles and features before proceeding helps ensure the correct server functionality is installed for the planned domain controller configuration.

### 19. AD DS Installed — Promotion Required

**Screenshot label:** AD DS installation complete

Completed the AD DS role installation and confirmed that the server still needed to be promoted to a domain controller. Installing the role makes the functionality available, while promotion configures the server to host the Active Directory domain.

### 20. Domain Controller Deployment Configuration

**Screenshot label:** Domain controller deployment configuration

Started the domain controller promotion process and configured a new forest for the lab. Creating a new forest establishes the foundation for the `nicklab.local` domain and provides the directory environment used to manage lab users and computers.

### 21. DNS Options Warning

**Screenshot label:** DNS options warning

Reviewed the DNS delegation warning shown during domain controller configuration. In a small standalone lab, this warning can appear when there is no existing parent DNS zone to delegate to. Understanding the message helps distinguish an expected lab warning from a genuine configuration failure.

### 22. Review Domain Controller Options

**Screenshot label:** Review domain controller options

Reviewed the domain controller configuration options before proceeding with promotion. This step confirms the settings for the new domain environment and helps ensure the server is being configured for the intended Active Directory deployment.

### 23. Prerequisites Check Passed

**Screenshot label:** Prerequisites check passed

Confirmed that the domain controller prerequisite checks passed before continuing. These checks help identify configuration problems that could prevent the server from being promoted successfully.

### 24. Server Manager After Domain Reboot

**Screenshot label:** Server Manager after domain reboot

Confirmed that the server restarted successfully after domain controller promotion. A successful restart is an important checkpoint because the server must complete the promotion process before the new domain can be used for administration and client authentication.

### 25. Domain Confirmed on Local Server

**Screenshot label:** Domain confirmed on local server

Confirmed that the server was configured for the `nicklab.local` domain. This demonstrates that the Active Directory domain was created and provides the basis for centralized user, group, and workstation administration.

### 26. Active Directory Users and Computers Open

**Screenshot label:** Active Directory Users and Computers open

Opened Active Directory Users and Computers on the domain controller and confirmed that the `nicklab.local` domain was available for administration. This management console is used to create and manage user accounts, security groups, organizational units, and other directory objects.

### 27. Active Directory OU Structure Created

**Screenshot label:** Active Directory OU structure created

Created an organizational unit structure to keep directory objects organized. Separating users, groups, disabled accounts, and workstations into appropriate containers makes administration easier and can help apply policies to the correct users or computers in a business environment.

### 28. Active Directory Security Groups Created

**Screenshot label:** Active Directory security groups created

Created security groups for the lab's access-management scenarios, including the groups used for department or shared-resource access. Security groups help administrators manage permissions through group membership rather than assigning every permission to each user individually.

### 29. Active Directory Test Users Created

**Screenshot label:** Active Directory test users created

Created test domain user accounts to represent users who would need access to the lab environment. These accounts provide a way to practise common help desk tasks such as password resets, account status changes, access changes, and domain sign-in testing without using real employee accounts.

### 30. Active Directory Group Membership Assigned

**Screenshot label:** Active Directory group membership assigned

Assigned users to the appropriate security groups for the lab's role-based access examples. This demonstrates basic identity and access management: users can be placed into groups that represent their department or support role, and group membership can be used to control access to shared resources.

### 31. Windows 11 Client VM Created

**Screenshot label:** Windows 11 client VM created

Created the Windows 11 Pro client virtual machine. This client represents a normal employee workstation that can be configured and joined to `nicklab.local` to demonstrate domain sign-in, shared-resource access, policy application, and endpoint troubleshooting.

### 32. Windows 11 Client VM Network Settings

**Screenshot label:** Windows 11 client VM network settings

Reviewed and configured the Windows 11 virtual machine's network settings before completing the client setup. Correct network configuration is essential for domain join and Active Directory authentication, especially because the client must be able to locate the domain controller through DNS.

### 33. Windows 11 Client Installation Started

**Screenshot label:** Windows 11 client installation started

Started the Windows 11 installation process for the client workstation. This is the foundation of the endpoint support portion of the lab, where the workstation can later be configured for network access, joined to the domain, and used to test standard user workflows.

### 34. Windows 11 Client Desktop Ready

**Screenshot label:** Windows 11 client desktop ready

Confirmed that the Windows 11 client successfully reached the desktop after installation. This shows that the endpoint operating system is ready for the next steps, including network and DNS configuration, domain joining, domain user sign-in, and help desk task testing.

### 35. Domain Administrator Login Proof

**Screenshot label:** Domain administrator login proof

Confirmed that the Windows 11 client was joined to the `nicklab.local` domain and used a domain account to sign in. Where included, the `whoami` output helps distinguish a domain identity from a local Windows account. This demonstrates the domain authentication path used for administrative testing in the lab.

### 36. Domain User Login Proof

**Screenshot label:** Domain user login proof

Confirmed that the Windows 11 client could sign in with a standard domain test account. This demonstrates that the environment supports normal Active Directory user authentication, not only administrative access, and provides a basis for testing permissions and policies under a standard user's context.

### 37. Password Reset Success — Jane

**Screenshot label:** Password reset success for Jane

Reset the password for the standard domain user account Jane using Active Directory Users and Computers. This demonstrates a common help desk workflow: assisting a user who cannot sign in by resetting an Active Directory password and confirming that the administrative action was completed.

### 38. Account Disabled — Alex

**Screenshot label:** Account disabled for Alex

Disabled the standard domain user account Alex in Active Directory Users and Computers. This demonstrates a common account lifecycle and access-control workflow, such as disabling an account when access should no longer be available while retaining the account record for administrative purposes.

### 39. Account Enabled — Alex

**Screenshot label:** Account enabled for Alex

Re-enabled Alex's domain user account after the account-disable test. This demonstrates the account lifecycle workflow in reverse: restoring an account's enabled status when access should be reinstated and confirming the change in Active Directory.

### 40. Group Membership Added — Alex

**Screenshot label:** Group membership updated for Alex

Updated Alex's security group membership in Active Directory Users and Computers. This demonstrates a common help desk access-management workflow: changing a user's group membership so the account can receive the appropriate department or shared-resource access through group-based permissions.

### 41. Sales Shared Folder Access — Jane

**Screenshot label:** Sales shared folder access

Configured the Sales shared folder and tested Jane's access from the Windows 11 client. This demonstrates a common help desk permissions workflow: reviewing share and NTFS permissions, using group membership to manage access, and verifying that a standard domain user can reach a shared resource.

### 42. Sales Mapped Drive Access — Jane

**Screenshot label:** Sales mapped drive access

Mapped the Sales shared folder as a network drive on the Windows 11 client while signed in as Jane. This demonstrates a common help desk task: connecting a user to a department network drive, checking the mapped path, and confirming that the user can access the shared content through the mapped drive.

### 43. Group Policy Control Panel Restriction — Jane

**Screenshot label:** Group Policy Control Panel restriction

Created and applied a Group Policy Object that prevents standard domain users from opening Control Panel and PC Settings. This demonstrates a basic Windows administration workflow: creating a GPO, linking it to the appropriate user scope, refreshing Group Policy on the Windows 11 client, and verifying that the restriction applies to a standard domain user.

## Project Documents

- **Case Study:** `case-study.md` — objectives, lab setup, configuration, challenges, and lessons learned.
- **Help Desk Ticket Write-Ups:** `tickets/` — individual support scenarios documenting the issue, investigation, actions taken, and outcome.
- **Lessons Learned:** `lessons-learned.md` — technical lessons and troubleshooting experience gained while building the lab.
- **Security Notes:** `security-notes.md` — notes about account management, group membership, permissions, and access control.

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

This project is intentionally entry-level and focused on practical learning. It does not claim senior-level administration experience. Instead, it demonstrates foundational Windows support skills, structured lab setup, Active Directory basics, user and group management, shared-resource troubleshooting, mapped drive configuration, Group Policy testing, screenshot documentation, and ticket-style communication.

The project provides evidence of hands-on practice relevant to entry-level help desk, IT support, and technical support roles.
