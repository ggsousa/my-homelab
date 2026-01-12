📊 System Status (Proxmox 9.1.4)

Currently operating a high-performance mixed cluster, managing LXC containers for core network services and VMs for testing/dev environments.

🖥️ Hardware Fleet

Machine	Specs	OS / Role
Main Station	Ryzen 7 9800x3D - RTX 3060 TI	Windows 11 / Gaming & Work
Server (PVE)	Xeon 2680V4 - 64GB ECC	Proxmox VE / Core Infrastructure
Lab/Hackintosh	i7 7820x (X299) - RX 580 8GB	macOS Sequoia / Windows 11
Media/Console	Ryzen 7 5700x - RX 5700 XT	Win11 / Emulation & Gamming on TV
🛠️ Active Services (Self-Hosted)

🌐 Core Network & Security

AdGuard Home: DNS filtering and network-wide ad blocking.
Nginx Proxy Manager: Reverse proxy and SSL management.
Vaultwarden: Self-hosted password management.
WireGuard VPN: Secure remote access.
TP-Link Omada Controller: Centralized network management (ER605 + EAPs).
🎬 Media Center (The *Arr Stack)

Plex Media Server: High-quality media streaming.
Radarr / Sonarr / Jackett: Automated movie and TV show library management.
qBittorrent: Integrated download client.
🏠 Automation & Monitoring

Home Assistant: Smart home brain (Lights, Soil Sensors, Garden monitoring).
Frigate: AI-powered NVR for security cameras.
Grafana + Prometheus: System telemetry and dashboards.
Uptime Kuma: Service uptime and health monitoring.
🧪 Pentest & Dev Lab (Proxmox)

OS Testing: Kali Linux, Parrot Security, Arch Linux, Mint, Ubuntu, Zorin.
Legacy Lab: Windows 7, Windows 8, Windows 10 (v1507).
Game Server: Crafty Control (Minecraft Server management).
📂 Repository Structure

/docker-compose: YAML configuration files for containers.
/proxmox: Optimization scripts and PVE notes.
/automation: Home Assistant blueprints and configs.
