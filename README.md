# 🔐 Phased Secure Virtual Infrastructure Deployment Plan

**Project Owner:** Tyreke Heyward  
**Purpose:** Build a secure, scalable virtual infrastructure for cybersecurity training and systems engineering demonstration.  
**Platform:** VirtualBox + Windows Server 2022 + Windows 10 Workstation + Ubuntu Server + Windows 10 (Jump Box) 
**Lab Host:** Laptop w/ 2TB external drive, 8GB RAM

---

## 📅 Phase Overview

| Phase     | Description                                 | Status     |
|-----------|---------------------------------------------|------------|
| Day 0     | Prep and initial configuration              | ✅ Complete |
| Day 1     | Install Windows Server 2022 VM              | ✅ Complete |
| Day 2     | Base configuration (network, admin, updates)| ✅ Complete |
| Phase 1   | AD DS, DNS, DHCP, Domain Join               | ✅ Complete |
| Phase 2   | Group Policies, OU structure, logging       | 🔄 In Progress |
| Phase 3   | File server, VPN setup, hardening           | 🔲 Not Started |

---

## 🕐 Day 0 – Project Prep

- [x] Define lab goals
- [x] List required software and ISO files
- [x] Install VirtualBox on host machine
- [x] Create VM storage plan (external drive)
- [x] Download Windows Server 2022 and Windows 10 ISOs

---

## 🕐 Day 1 – Install Server OS

- [x] Create a new VirtualBox VM for Server 2022
- [x] Assign resources (2 CPU, 4GB RAM, 80GB disk)
- [x] Mount Server 2022 ISO
- [x] Run installer and set local admin credentials
- [x] Install VirtualBox Guest Additions

---

## 🕐 Day 2 – Base Server Setup

- [x] Set static IP: `192.168.1.10`
- [x] Rename computer: `DC1`
- [x] Set time zone, enable remote management
- [x] Run Windows Update
- [x] Enable Windows PowerShell

---

## 🛡️ Phase 1 – Core Services: AD DS, DNS, DHCP

### ✔️ Roles Installed

- [x] Active Directory Domain Services (AD DS)
- [x] DNS Server
- [x] DHCP Server

### ✔️ Actions Taken

- [x] Promoted `DC1` to domain controller for `heyward.local`
- [x] Created domain admin credentials
- [x] Configured DNS with forwarders (Google 8.8.8.8)
- [x] Authorized DHCP server in AD
- [x] Created DHCP scope: `192.168.1.100 – 192.168.1.200`

### ✔️ Workstation Setup

- [x] Created Windows 10 VM
- [x] Set static or DHCP IP
- [x] Joined `heyward.local` domain
- [x] Verified DNS and AD authentication

---

## 🛠️ Phase 2 – Group Policy & Structure

### 🎯 Goals

- Create Organizational Units: IT, HR, Workstations
- Apply password policy (min length, complexity)
- Add logon message via GPO
- Enable auditing for login events

### Tasks

- [ ] Install GPMC and `GroupPolicy` module
- [ ] Create GPO: `BaselineSecurityPolicy`
- [ ] Apply settings via `Set-GPRegistryValue`
- [ ] Link GPO to domain
- [ ] Test on Windows 10 VM

---

## 🔐 Phase 3 – Advanced Hardening (Planned)

- Set up a File Server role on DC or new VM
- Configure VPN access (e.g., OpenVPN or RRAS)
- Create regular backups of AD and DHCP
- Harden Windows Server with baseline security templates
- Enable Event Log forwarding to a central collector

---

## 📌 Notes

- VM Host: External SSD used to reduce I/O load
- DNS forwarders configured to Google DNS
- VMs tested in internal network only (no internet)

---

## 🚀 Summary

This phased approach reflects secure enterprise practices while constrained to a laptop environment. It demonstrates:
- Systems engineering design thinking
- Hands-on experience with AD, DNS, DHCP, GPOs
- Scripting, troubleshooting, and layered defense principles



<!---
JackTack-bit/JackTack-bit is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
