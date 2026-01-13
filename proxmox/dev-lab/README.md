# 🧪 Dev-Lab & Security Testing

This section of the lab is dedicated to security research, software development, and experimental hosting. These environments are often isolated or ephemeral, used for learning and testing new tools.

## 🛡️ Security & Pentesting
I maintain dedicated virtual environments for security analysis and learning:
- **Kali Linux (VM 104)**: The primary suite for penetration testing and network auditing.
- **Parrot Security**: (Optional/Testing) used for lightweight security tasks.

## 🕹️ Game Server Management
- **Crafty Controller (VM 103)**: A dedicated VM running Crafty for hosting and managing Minecraft servers with a web-based GUI. This allows for easy resource allocation and server monitoring.

## 💻 OS Library (Testing & Legacy)
I keep a library of Operating Systems to test compatibility and software behavior across different versions:
- **Modern**: Ubuntu, Mint, Zorin OS.
- **Legacy**: Windows 7, Windows 8, and Windows 10 (v1507) for specialized testing.

## ⚙️ Resource Management
Since these are laboratory machines, they are excluded from the main daily backup job to save storage space. However, they benefit from:
- **Quick Snapshots**: Before running experimental scripts or updates.
- **Isolated VLANs**: Ensuring that testing activities do not interfere with the core network (Network-Security).
