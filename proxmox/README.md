# 💽 Proxmox Virtual Environment (PVE)

This directory documents the backbone of my home infrastructure. My environment is optimized for high-availability network services, media automation, and isolated security research laboratories.

## 🏗️ Hardware & Performance
The primary node utilizes a server-grade HEDT platform to maximize I/O throughput and multi-threaded performance.

- **CPU:** Intel Xeon E5-2680 v4 (14 Cores / 28 Threads)
- **RAM:** 64GB DDR4 ECC.
- **GPU:** GTX 1660Ti (when needed)
- **Storage Local:** 512GB NVMe.
- **Storage de Dados:** 2x 1TB HDD em Raid0 para media e backups.

## 📊 Instance Fleet (VMs & LXC Containers)

My fleet is strategically split between stable production machines and ephemeral testing environments:

| ID | Name | Role/Status | Type |
| :--- | :--- | :--- | :--- |
| **100** | AdGuard | Production - Network DNS & Ad-blocking | LXC |
| **101** | HomeAssistant | Production - Smart Home Automation | VM |
| **102** | Plex | Media Server - Hardware Transcoding | VM |
| **103** | Crafty | Dedicated Game Server Hosting | VM |
| **104** | Kali | Security & Pentesting Lab | VM |
| **105** | Jackett | Media Stack - Tracker Indexer | LXC |
| **106** | qBittorrent | Media Stack - Download Client | LXC |
| **107** | Radarr | Media Stack - Movie Management | LXC |
| **108** | Sonarr | Media Stack - TV Show Management | LXC |
| **109** | Proxy | Nginx Proxy Manager (External Access) | LXC |
| **110** | Arch | Minimalist Development Environment | VM |
And others...

## 💾 Storage Management
I utilize a tiered storage hierarchy to balance speed, reliability, and capacity:

- **local**: Reserved for LXC templates.
- **local-lvm**: High-performance storage for VM and Container Root FS.
- **2xHD**: Dedicated mechanical drive for media and backups.

## 🛡️ Backup & Retention Policy
Data protection is fully automated via the Proxmox Backup Manager with the following specs:

- **Schedule**: Daily at 03:00 AM.
- **Mode**: `Snapshot` (Ensures zero downtime during backup).
- **Compression**: `ZSTD` (Fastest compression with optimal CPU usage).
- **Retention**: "Keep Last: 3" (Maintains the 3 most recent backups per instance).
- **Note Template**: `{{guestname}} - {{vmid}}` for rapid identification during recovery.

---
> **Technical Note**: Network isolation is achieved via Linux bridges (`vmbr0`), allowing AdGuard Home to act as the primary DNS sinkhole for all internal traffic.
