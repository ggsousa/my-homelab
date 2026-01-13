# 🎬 Plex Media Server (VM 102)

My primary media server is running on a dedicated virtual machine for maximum stability and performance.

## ⚙️ VM Specifications
- **Cores:** 6 Cores [host] (Xeon 2680V4)
- **RAM:** 4GB
- **OS:** Ubuntu Server
- **Hardware Acceleration:** No, I will not pay for that.

## 📂 Storage & Library Mapping
The media library is stored on a **2x 1TB HDD Raid0** array and mounted via:
- **Mount Point:** `/mnt/media`
- **Structure:**
  - `/movies` (Managed by Radarr)
  - `/tv-shows` (Managed by Sonarr)

## 🔄 Integration
The server is integrated with the rest of the Arr stack (Radarr, Sonarr, qBittorrent) located in LXC containers. All communication happens over the internal Proxmox bridge for low latency.
