# Active Directory & Windows Server Home Lab

## Overview

A hands-on Windows Server and Active Directory home lab built using VMware Workstation to practice real-world IT Support, Windows Administration, Active Directory, and network infrastructure tasks.

The lab covers Domain Controller deployment, Active Directory administration, Organizational Units, user management, Group Policy, Active Directory Sites, Additional Domain Controllers, DHCP, NTFS permissions, and shared folder permissions.

---

## Lab Environment

* VMware Workstation
* Windows Server
* Windows 10 Client
* Active Directory Domain Services (AD DS)
* DNS
* DHCP
* Group Policy
* Active Directory Sites and Services
* NTFS Permissions
* Shared Folder Permissions

---


### Active Directory Structure

The Active Directory environment was organized into two main Organizational Units:

```text
Active Directory Domain
│
├── EG
│   ├── Department
│   │   └── Users
│   │
│   └── Department
│       └── Users
│
└── UK
    ├── Department
    │ └──HR
      └──IT ---- Users
    │
    └──  ├── Department
    │ └──HR
      └──IT ---- Users
```

The exact OU and department structure was created to simulate organizational separation and user management in a real business environment.

---

# Tasks Performed

## 1. Windows Server Installation

* Installed Windows Server inside VMware Workstation.
* Configured the initial server environment.
* Installed the Active Directory Domain Services role.
* Promoted the server to a Domain Controller.
* Configured the Active Directory domain environment.

---

## 2. Windows 10 Domain Client

* Installed Windows 10 on a separate VMware virtual machine.
* Activated and configured the operating system.
* Joined the Windows 10 client to the Active Directory domain.
* Tested domain authentication and user access.
* Removed the client from the domain and rejoined it during troubleshooting practice.

---

## 3. Domain Credential Troubleshooting

During the lab, I encountered an issue where Windows credentials became stuck during the login process after removing and reconnecting the client to the domain.

### Troubleshooting

The issue required resetting the affected environment and reconnecting the client to the domain to restore normal authentication behavior.

This provided practical experience troubleshooting domain authentication and client-side credential issues.

---

## 4. Organizational Units & User Management

Created and organized Active Directory Organizational Units to simulate different geographical locations and departments.

### Structure

* EG OU
* UK OU
* Department-level OUs
* User accounts within the appropriate departments

Created and managed users according to the organizational structure.

---

## 5. Password Reset & Account Management

Practiced common Help Desk tasks including:

* Resetting user passwords.
* Managing user accounts.
* Testing user authentication.
* Troubleshooting login-related issues.
* Verifying access after password changes.

These tasks simulate common Active Directory support requests handled by IT Help Desk teams.

---

## 6. Group Policy

Created and configured Group Policy Objects (GPOs) to manage user and computer settings within the Active Directory domain.

The lab included:

* Created and linked Group Policy Objects to specific Organizational Units (OUs).
* Configured a policy to allow designated domain users to access the Windows Server through **Remote Desktop (RDP)**.
* Tested Remote Desktop access using domain user accounts.
* Verified that the configured policy was applied successfully to the targeted users.
* Used Group Policy to centrally manage user access and permissions.


---

## 7. Active Directory Sites

Created multiple Active Directory Sites to simulate a geographically distributed organization.

The environment included:

```text
UK Site
└── Primary Domain Controller (PDC)

EG Site
└── Additional Domain Controller (ADC)
```

Configured the Active Directory environment so that the PDC and ADC were associated with different sites.

This provided practical experience with:

* Active Directory Sites and Services
* Domain Controller placement
* Multi-site Active Directory environments
* Replication concepts

---

## 8. Additional Domain Controller (ADC)

Configured an Additional Domain Controller to provide redundancy within the Active Directory environment.

The ADC was placed in the EG site while the primary Domain Controller was associated with the UK site.

This allowed me to practice the concepts involved in:

* Domain Controller redundancy
* Multi-site environments
* Active Directory replication
* Site-based Domain Controller organization

---

## 9. VMware Template / Sysprep

While creating the Additional Domain Controller environment, I used a Windows Server virtual machine as a base/template.

The virtual machine was prepared using **Sysprep** before being used as the basis for another server environment.

This was necessary to avoid cloning an existing Windows installation with the same machine identity.

---

## 10. DHCP Configuration

Configured DHCP within the Windows Server lab environment and tested IP address assignment for virtual machines.

The lab included:

* DHCP server configuration.
* DHCP scope configuration.
* IP address assignment.
* Network configuration for virtual clients.
* Testing DHCP communication.

### Troubleshooting Case

A DHCP-related issue was encountered during the lab while working with the VMware virtual network environment.

The issue was investigated and the underlying cause was identified.

The lab was intentionally left at that stage after understanding the cause and troubleshooting approach.

This provided practical experience with troubleshooting DHCP and virtual networking environments.

---

## 11. NTFS & Shared Folder Permissions

Configured and tested Windows file and folder permissions.

Practiced:

* NTFS permissions.
* Shared folder permissions.
* User access control.
* Permission inheritance.
* Testing access using different domain users.

The goal was to understand how Windows handles file-system permissions and network share access in a domain environment.

---

# Troubleshooting Experience

Throughout the lab, several issues were encountered and investigated instead of simply following a tutorial.

### Domain Credential / Login Issue

Encountered a credential-related issue after removing and reconnecting a Windows client to the domain.

**Approach:**

* Investigated the client authentication behavior.
* Identified the issue.
* Reset the affected environment.
* Reconnected the client to the domain.
* Verified authentication.

### DHCP / VMware Networking Issue

Encountered a DHCP-related issue while working with the VMware virtual network environment.

**Approach:**

* Checked the DHCP configuration.
* Investigated the virtual network configuration.
* Identified the underlying cause.
* Documented the troubleshooting process.

---

# Skills Demonstrated

* Windows Server Administration
* Active Directory Domain Services
* Domain Controller Configuration
* Additional Domain Controllers
* Active Directory Sites and Services
* User & Group Management
* Organizational Units
* Password Reset
* Group Policy
* DNS
* DHCP
* Windows Domain Joining
* NTFS Permissions
* Shared Folder Permissions
* VMware Workstation
* Sysprep
* Windows Troubleshooting
* IT Help Desk Administration

---

# Screenshots

Screenshots from the lab environment are included below to demonstrate the practical implementation.

### Windows Server / Domain Controller

![Domain Controller](screenshots/domain-controller.png)

### Active Directory Users & Computers

![Active Directory](screenshots/active-directory.png)

### Organizational Units

![Organizational Units](screenshots/organizational-units.png)

### Group Policy

![Group Policy](screenshots/group-policy.png)

### Active Directory Sites

![AD Sites](screenshots/ad-sites.png)

### Additional Domain Controller

![Additional Domain Controller](screenshots/additional-dc.png)

### DHCP

![DHCP](screenshots/dhcp.png)

### NTFS & Sharing Permissions

![Permissions](screenshots/permissions.png)

---

# Project Purpose

This project was created as a practical home lab to develop hands-on Windows Administration, Active Directory, networking, troubleshooting, and IT Support skills.

The lab was built and tested in a virtualized VMware environment to simulate common enterprise IT infrastructure scenarios.
