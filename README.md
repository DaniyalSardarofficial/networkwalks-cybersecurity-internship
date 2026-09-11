# WK1-PM1 — Cybersecurity Testing Lab Setup

**Intern:** Daniyal Ahmed
**Course:** Cybersecurity & Ethical Hacking
**Task ID:** WK1-PM1
**Intern ID:** NW-83-4UP
**Organization:** Networkwalks Technologies

## Overview

This task involved building a cybersecurity testing lab on a personal machine using a hypervisor to host an attacking machine (Kali Linux) on an isolated, NAT-based internal network. The reference lab guide used Oracle VirtualBox; this submission uses **VMware Workstation Pro 17** instead, mapping each VirtualBox concept to its VMware equivalent.

## Environment

| Component | Detail |
|---|---|
| Hypervisor | VMware Workstation Pro 17 |
| Attacking machine | Kali Linux 2026.2 (official pre-built VMware image) |
| Network mode | NAT (VMware's built-in NAT, equivalent to VirtualBox NATNetwork) |
| Target subnet | 10.0.0.0/24 |
| Kali static IP | 10.0.0.2/24 |
| Gateway | 10.0.0.1 |
| DNS | 8.8.8.8 |

## Setup Steps

1. **Install VMware Workstation Pro** — downloaded and installed as the base hypervisor platform.
2. **Launch VMware Workstation Pro** — verified the home screen with options to create/open VMs.
3. **Download the Kali Linux pre-built VM** — obtained the official VMware-ready image from kali.org/get-kali (default credentials `kali/kali`).
4. **Import/Open the Kali Linux VM** — opened the `.vmx` file directly in VMware Workstation, registering it in the library.
5. **Configure the network adapter to NAT** — set the adapter to NAT with "Connect at power on" enabled, placing the VM on VMware's isolated internal NAT network (VMnet8).
6. **Configure display/graphics settings** — enabled 3D acceleration, host monitor settings, and 256 MB of graphics memory for smooth desktop performance.
7. **Assign the static IP to Kali Linux** — added a static address (10.0.0.2/24, gateway 10.0.0.1, DNS 8.8.8.8) alongside the default DHCP method via Network Manager.

## Task Requirements Checklist

- [x] VMware Workstation Pro installed and used as the hypervisor
- [x] Kali Linux imported as the attacking/hacker machine
- [x] Network configured in subnet 10.0.0.0/24 using NAT
- [x] Kali Linux assigned static IP 10.0.0.2/24
- [x] Kali Linux configured with full internet access via NAT gateway (10.0.0.1)
- [ ] Clipboard, drag-and-drop, and shared folders — to be enabled via VM Settings > Options > Shared Folders / Guest Isolation (requires VMware Tools)

## Notes

All configuration steps mirror the reference lab guide (WK1-PM1), substituting VMware Workstation Pro 17 for Oracle VirtualBox. Functionally equivalent settings were used throughout — VMware's NAT network in place of VirtualBox's NATNetwork, and VMware's per-VM Network Adapter / Display / Shared Folders panels in place of VirtualBox's corresponding tabs.

A snapshot of the completed VM should be taken (`VM > Snapshot > Take Snapshot`) to preserve this working state before proceeding to Phase 2 of the lab.
