# 💾 Backup & Data Protection Strategy

Security is a priority in this HomeLab. I implement a robust backup policy using Proxmox VE's native tools to ensure that any service can be restored quickly in case of failure.

## ⚙️ Backup Configuration (Proxmox Job)
- **Storage Target:** `backups-hd` (Dedicated physical drive)
- **Mode:** `Snapshot` (Ensures zero downtime during backup)
- **Compression:** `ZSTD (fast and good)` - Optimal balance between speed and disk space.
- **Schedule:** Daily at `03:00` AM.

## 📋 Retention Policy
I follow a controlled retention rotation to optimize storage:
- **Keep Last:** `3` backups per VM/LXC.
- **Note Template:** `{{guestname}} - {{vmid}}` (Automated tagging for easy identification).

## 🗄️ Protected Services
The following critical services are included in the daily backup job:

| ID | Name | Type |
| :--- | :--- | :--- |
| 100 | AdGuard | LXC Container |
| 101 | Home Assistant | Virtual Machine |
| 102 | Plex | Virtual Machine |
| 103 | Crafty | Virtual Machine |
| 105-108 | Arr Stack | LXC Containers (Jackett, qBit, Radarr, Sonarr) |
| 109 | Proxy | LXC Container |
| 115 | Vault Warden | LXC Container |
| 116 | VPN | LXC Container |
| 118 | Kuma | LXC Container |
| 121 | Frigate | LXC Container |
| 122 | Grafana | LXC Container |
| 123 | Omada | LXC Container |
| 125 | Portainer | LXC Container |

---
> **Tip:** Non-essential test environments like Kali (104) and Arch (110) are excluded from the automated job to save disk space, as they can be easily redeployed from scripts.
