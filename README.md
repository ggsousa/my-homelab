# 🏠 HomeLab & Infrastructure | *G*

🚀 Self-hosted infrastructure focused on performance, networking, and automation.

This repository documents a real-world homelab environment running virtualization, VLAN segmentation, media services, and smart home integrations.

---

## 📊 System Status

- 🖥️ **Proxmox VE 9.1.4**
- 📦 ~15 LXC containers running 24/7
- 🧠 10+ Virtual Machines (Dev / Testing / Services)
- 🌐 VLAN-segmented network (Main / IoT / Servers)
- 🔒 Secure remote access via WireGuard VPN

---

## 🖥️ Hardware Fleet

| Machine | Specs | Role |
| :--- | :--- | :--- |
| **Main Station** | Ryzen 7 9800X3D • RTX 3060 Ti | Workstation / Gaming |
| **Server (PVE)** | Xeon E5-2680 v4 • 64GB ECC | Proxmox / Core Infrastructure |
| **Hackintosh Lab** | i7-7820X (X299) • RX 5700XT • 80GB RAM | macOS Sequoia / Dev |
| **Media / Console** | Ryzen 7 5700X • RX 580 | Emulation / TV Gaming |
| **Gaming Ecosystem** | PS5 Slim • PS Portal | Remote Play / Console |

---

## 📂 Repository Structure

The lab is organized into modular components for maintainability and scalability:

- **🛡️ Network & Security**  
  AdGuard Home (DNS), WireGuard (VPN), TP-Link Omada Controller, VLAN architecture

- **🎬 Media Center**  
  Plex Media Server + *Arr stack (Radarr, Sonarr, Prowlarr, qBittorrent)

- **🧪 Dev Lab & Testing**  
  Kali Linux, Arch Linux, Crafty Controller (game servers)

- **💾 Backup Strategy**  
  Automated backup routines and retention policies

- **🍎 Hackintosh Build**  
  macOS Sequoia on X299 (OpenCore setup and tweaks)

- **🏠 Automation & Monitoring** *(WIP)*  
  Home Assistant dashboards, system monitoring and energy tracking

---

## 🛠️ Infrastructure Overview

My network is built around the **TP-Link Omada ecosystem**:

- ER605 Gateway with managed switching and access points
- VLAN segmentation:
  - Main Network
  - IoT Devices
  - Servers / Infrastructure
- Centralized DNS filtering with AdGuard Home
- Secure remote access via WireGuard VPN

---

## ⚡ Monitoring & Energy

Using **Home Assistant** for real-time monitoring and automation:

- 📊 System health and service monitoring
- ⚡ Real-time power consumption tracking
- 🌡️ Environmental sensors (temperature / humidity)
- 🔌 Smart plugs for analytics and automation

---
