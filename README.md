# 🏗️ Secure Virtual Infrastructure Deployment Lab
**Created by: Tyreke A. Heyward**

**Goal:** Build a lightweight, secure virtual infrastructure to simulate a small enterprise network with AD, Linux server, centralized logging, and system hardening.

---

## 📅 Project Timeline Overview

| Phase | Description | Duration |
|-------|-------------|----------|
| Phase 0 | Prep | 2 Days |
| Phase 1 | Domain Controller Deployment | Week 1 |
| Phase 2 | Harden & Secure DC1 | Week 2 |
| Phase 3 | Linux Server + Logging Setup | Week 3 |
| Phase 4 | User Workstation Setup | Week 4 |
| Phase 5 | Centralized Logging | Week 5 |
| Phase 6 | Documentation & Wrap-Up | Week 6 |
| Bonus | Stretch Goals | Optional |

---

## 🔹 Phase 0: Prep (Day 0–2)

- [x] Install VirtualBox + Extension Pack
- [x] Format external drive (exFAT or NTFS)
- [x] Set VirtualBox VM folder to external drive
- [x] Download required ISOs:
  - [x] Windows Server 2022 (Core or GUI)
  - [x] Ubuntu Server 22.04 LTS
  - [x] Windows 10 ISO
- [x] Create folders for documentation and screenshots
- [x] (Optional) Create GitHub repo for tracking

---

## 🔹 Phase 1: Domain Controller (Week 1)

- [x] Create VM: `DC1` (2.5 GB RAM, 60 GB disk)
- [x] Install Windows Server
- [x] Promote to Domain Controller (AD DS + DNS)
- [x] (Optional) Install DHCP
- [x] Create:
  - [x] 1 User account
  - [x] 1 Security Group
  - [x] 1 Organizational Unit (OU)
- [x] Configure Group Policies:
  - [x] Enforce password complexity
  - [x] Create login banner
  - [x] Enable audit policy
- [x] Export configurations and take screenshots

---

## 🔹 Phase 2: Harden & Secure DC1 (Week 2)

- [ ] Rename default Administrator account
- [ ] Configure Windows Firewall
- [ ] Apply STIGs or CIS benchmarks
- [ ] Enable auditing:
  - [ ] Logon events
  - [ ] Privilege use
  - [ ] Object access
- [ ] Export and document GPO baseline (`.xml` or `.html`)

---

## 🔹 Phase 3: Ubuntu Server + Web + Logging (Week 3)

- [ ] Create VM: `WEB1` (1.5 GB RAM, 20 GB disk)
- [ ] Install and configure:
  - [ ] Nginx (internal web page)
  - [ ] `ufw` firewall
  - [ ] `fail2ban`
- [ ] Secure SSH:
  - [ ] Disable root login
  - [ ] Enable SSH key authentication
- [ ] Install logging tools:
  - [ ] `rsyslog` or Filebeat
  - [ ] `auditd`

---

## 🔹 Phase 4: User Workstation (Week 4)

- [ ] Create VM: `USER1` (2.5 GB RAM, 30 GB disk)
- [ ] Join domain `securelab.local`
- [ ] Log in as domain user
- [ ] Verify GPOs are applied:
  - [ ] Password policy
  - [ ] Login banner
  - [ ] Audit policy
- [ ] Test access to:
  - [ ] Internal website on `WEB1`
  - [ ] SSH access (if permitted)
- [ ] (Bonus) Map network drive to DC1 or shared folder

---

## 🔹 Phase 5: Centralized Logging (Week 5)

- [ ] Configure centralized logging on `WEB1`
- [ ] Forward logs from:
  - [ ] DC1 (via Winlogbeat)
  - [ ] USER1
- [ ] Test and verify:
  - [ ] Failed login attempts
  - [ ] GPO changes
  - [ ] File access attempts
- [ ] Save log samples and screenshots for documentation

---

## 🔹 Phase 6: Final Touches + Documentation (Week 6)

- [ ] Create visual architecture diagram (draw.io)
- [ ] Write README.md including:
  - [ ] Overview
  - [ ] Tools used
  - [ ] VM specs
  - [ ] Security highlights
- [ ] Create:
  - [ ] GPO and hardening checklist
  - [ ] Screenshots of configurations
- [ ] (Optional) Record a walkthrough video
- [ ] (Optional) Push to GitHub repo (private or public)

---

## 🧩 Bonus Stretch Goals (Optional)

- [ ] Install pfSense VM as firewall/router
- [ ] Simulate VPN tunnel into the lab
- [ ] Set up backups with Windows Backup or `rsync`
- [ ] Deploy full ELK stack for advanced logging

---



<!---
JackTack-bit/JackTack-bit is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
