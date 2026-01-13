# 🎥 High-Performance Media Center

This stack handles my automated media pipeline, leveraging Proxmox's LXC containers for efficiency and a dedicated VM for Plex streaming.

## 🏗️ Architecture
- **Download Client**: qBittorrent (LXC 106) - High-speed, lightweight torrenting.
- **Automation**: Radarr (LXC 107) and Sonarr (LXC 108) for movie and TV show management.
- **Indexer Proxy**: Jackett (LXC 105) to centralize trackers.
- **Media Server**: Plex (VM 102) - Dedicated environment for transcoding and library hosting.

## 🗄️ Storage Layout
The library is hosted on a **Raid0 array (2x 1TB HDDs)**.
Paths are mounted via NFS/Bind Mounts to ensure all containers see the same file structure, preventing "file not found" errors during the import process.
