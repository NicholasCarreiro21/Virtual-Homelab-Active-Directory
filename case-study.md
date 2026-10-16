# Help Desk Homelab Case Study

## Overview

This project is a Windows help desk homelab built to practise and document entry-level IT support tasks. It uses VirtualBox, Windows Server 2022, Windows 11 Pro, Active Directory, DNS, shared folders, Group Policy, screenshots, and ticket-style writeups.

The focus is on demonstrating practical support fundamentals: configuring a small lab, troubleshooting connectivity and access, making account changes, checking results, and documenting the work clearly.

## Problem

Entry-level IT support skills can be difficult to demonstrate through a resume alone. This project provides a documented example of common Windows support workflows, with screenshots and ticket writeups showing the steps taken in a controlled lab environment.

## Lab Setup

The lab runs in Oracle VirtualBox on a Windows host and includes:

- A Windows Server 2022 Evaluation virtual machine configured as the domain controller
- An Active Directory domain named `nicklab.local`
- A Windows 11 Pro client virtual machine
- An internal VirtualBox network named `nicklab`
- Static IPv4 configuration for the server and client
- Active Directory users, organizational units, and security groups
- A Sales shared folder and mapped network drive
- A Group Policy restriction for Control Panel and PC Settings

The server uses `192.168.100.10/24` with DNS set to `127.0.0.1`. The client uses `192.168.100.20/24` and points DNS to the server at `192.168.100.10`. This allows the client to locate the domain controller on the lab network.

## What I Built

### 1. Virtual Machine Setup

Created the Windows Server and Windows 11 Pro virtual machines, installed their operating systems, and configured the client/server network for the lab.

### 2. Active Directory Configuration

Installed Active Directory Domain Services, promoted the server to a domain controller, and created the `nicklab.local` domain. Organized directory objects and created test accounts and security groups for user and access-management exercises.

### 3. Domain Connectivity and Sign-In

Configured the client's network settings and DNS, joined the Windows 11 Pro machine to the domain, and tested domain-user sign-in.

### 4. Account Support Workflows

Practised resetting a test user's password, disabling and re-enabling an account, and changing group membership in Active Directory Users and Computers.

### 5. Shared Folder and Mapped Drive

Configured a Sales shared folder and its permissions, tested access from the client, and mapped the share to a drive letter. The workflow demonstrates how group membership, share permissions, and NTFS permissions can affect access to a network resource.

### 6. Group Policy

Configured a Group Policy Object to restrict standard domain users from opening Control Panel and PC Settings. Updated policy on the client and checked the result using a standard domain account.

## Support Tickets

The accompanying tickets document six practice scenarios:

1. Windows 11 client virtual machine boot troubleshooting
2. Active Directory password reset
3. Account disable and re-enable
4. Security group membership change
5. Shared folder access denied
6. Control Panel and PC Settings restricted by Group Policy

Each ticket records the reported issue, the troubleshooting or administrative steps, the resolution, and how the result was checked. These are lab exercises, not production support incidents.

## Skills Demonstrated

- Windows Server setup basics
- Active Directory Users and Computers
- OU, user, and group organization
- Password reset workflow
- Account disable and re-enable workflow
- Security group membership changes
- Shared folder permission troubleshooting
- SMB share access testing
- Mapped network drive setup
- Group Policy Management
- gpupdate testing
- Windows 11 domain client validation
- PowerShell-assisted workflow
- Screenshot-based documentation
- Help desk ticket writing
- GitHub portfolio documentation

## What This Project Demonstrates

This homelab shows that I can follow a technical process, configure a basic Windows domain environment, practise common account and access tasks, investigate issues, verify changes, and explain the results in support-ticket format. It is a self-directed learning project intended to demonstrate foundational skills relevant to entry-level help desk and IT support roles.

## Current Status

The core lab scenarios have been completed and documented. The repository includes the README, case study, screenshots, and six help desk ticket writeups.
