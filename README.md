# 🏠 g | HomeLab & Infrastructure

Welcome to my HomeLab documentation. This repository tracks my journey managing virtualization, networking, and home automation across multiple hardware platforms.

## 📊 System Status (Proxmox 9.1.4)
Currently operating a high-performance mixed cluster, managing LXC containers for core network services and VMs for testing/dev environments.

### 🖥️ Hardware Fleet
| Machine | Specs | OS / Role |
| :--- | :--- | :--- |
| **Main Station** | Ryzen 7 9800x3D - RTX 3060 TI | Windows 11 / Gaming & Work |
| **Server (PVE)** | Xeon 2680V4 - 64GB ECC | Proxmox VE / Core Infrastructure |
| **Lab/Hackintosh** | i7 7820x (X299) - RX 580 8GB | macOS Sequoia / Windows 11 |
| **Media/Console** | Ryzen 7 5700x - RX 5700 XT | Win11 / Emulation & Gamming on TV |

---

## 📂 Repository Structure

I've organized my lab into logical categories for better maintainability and documentation:

- **[🛡️ Network & Security](./proxmox/network-security)**: AdGuard Home (DNS), WireGuard (VPN), and TP-Link Omada Controller.
- **[🎬 Media Center](./proxmox/media-center)**: Plex Media Server and the full *Arr stack (Radarr, Sonarr, Jackett, qBit).
- **[🧪 Dev-Lab & Testing](./proxmox/dev-lab)**: Kali Linux, Arch Linux, and Crafty Controller for game servers.
- **[💾 Backup Strategy](./proxmox/backups)**: My automated data protection and retention policies.
- **[🍎 Hackintosh Build](./hackintosh)**: Detailed setup for running macOS Sequoia natively on X299.
- **[🏠 Automation](./proxmox/automation-monitoring)**: (In Progress) Home Assistant dashboards and monitoring.

---

## 🛠️ Infrastructure Overview

### Networking
My network is powered by the **TP-Link Omada** ecosystem (ER605 Gateway) and a 1GB link. I focus on network-wide ad blocking via AdGuard and secure remote access through WireGuard.

### Monitoring & Energy
I use **Home Assistant** to monitor system health and energy consumption. 
- **Current Load**: ~12 Containers and 3 VMs active. (24/7)
- **Energy Tracking**: Real-time wattage monitoring for the Server and Main Setup via smart sockets.

---
