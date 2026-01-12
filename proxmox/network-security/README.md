# 🛡️ Network & Security Stack

This folder contains the configuration and logic for my core network infrastructure. My goal is to maintain a high-performance, secure, and ad-free environment using a mix of dedicated hardware and Proxmox-hosted services.

## 🌐 Network Logic & Flow
The network architecture is designed around the **TP-Link Omada** ecosystem:

1. **Gateway**: A **TP-Link ER605** handles the main routing and DHCP.
2. **DNS Delegation**: The DHCP server is configured to point all clients to **AdGuard Home** (LXC 100) as the primary DNS provider.
3. **Filtering**: AdGuard Home filters network-wide ads and trackers using high-performance blocklists (OISD, Hagezi).
4. **External Access**: 
   - **WireGuard (LXC 116)**: Provides secure remote access to the local network.
   - **Nginx Proxy Manager (LXC 109)**: Manages internal service domains (e.g., `proxmox.home`, `plex.home`) and SSL certificates.

## 📦 Services in this Section

| Service | ID (LXC) | Description |
| :--- | :--- | :--- |
| **AdGuard Home** | 100 | Primary DNS with DoH (DNS over HTTPS) and network-wide blocking. |
| **WireGuard** | 116 | High-speed VPN for secure remote management. |
| **Omada Controller** | 123 | Central management for the ER605 and upcoming EAP653 Access Points. |
| **Proxy Manager** | 109 | Internal routing for local services with user-friendly hostnames. |
| **Vaultwarden** | 115 | Self-hosted password management for all lab services. |

## 🛠️ Upcoming Upgrades
- **Wi-Fi Migration**: Currently using Deco X50s in AP mode, migrating to **2x TP-Link EAP653** for better integration with the Omada Controller and VLAN management.
