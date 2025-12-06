<div align="center">
  <img src="./assets/xZenith-effect.png" alt="xZenith Logo" width="140"/>
  
  # xZenith
  
  **Unleash Peak Performance to the Zenith**
  
  A modern hardware monitoring and system optimization application for Windows.

[![Release](https://img.shields.io/github/v/release/xFlawlessDev/xZenith?style=for-the-badge&logo=github&color=blue)](https://github.com/xFlawlessDev/xZenith/releases)
[![Downloads](https://img.shields.io/github/downloads/xFlawlessDev/xZenith/total?style=for-the-badge&color=green)](https://github.com/xFlawlessDev/xZenith/releases)
[![Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/HKG9GNTesb)

  <br/>

[Features](#-features) •
[Screenshots](#-screenshots) •
[Download](#-download) •
[Installation](#-installation) •
[FAQ](#-faq)

</div>

---

## ✨ Highlights

<table>
<tr>
<td width="50%">

🚀 **Lightning Fast**

> Native performance with minimal resource usage

🎨 **Beautiful UI**

> Modern design with smooth animations and 8 color themes

📊 **Real-time Monitoring**

> Live hardware stats with continuous CSV logging and 56+ metrics

</td>
<td width="50%">

🛠️ **Powerful Tools**

> Process manager, system cleanup, driver backup, DNS changer, performance boost

⚡ **One-Click Tweaks**

> Apply optimizations safely with rollback support

🎮 **Discord Integration**

> Show your monitoring setup with Rich Presence

</td>
</tr>
</table>

---

## 🖼️ Screenshots

<div align="center">
  <img src="./screenshots/xZenith-photo-collage.jpg" alt="Collage" width="90%"/>
  <p><em>Dashboard - Real-time system overview</em></p>
  
  <img src="./screenshots/Monitoring-Top.png" alt="Monitoring" width="90%"/>
  <p><em>Hardware Monitoring - Detailed temperature and usage graphs</em></p>
  
  <img src="./screenshots/Tools.png" alt="Tools" width="90%"/>
  <p><em>System Tools - Utilities and optimization tools</em></p>
</div>

---

## 🌟 Features

### 📊 Dashboard & Monitoring

- **Real-time Dashboard** - System overview with CPU, GPU, RAM, Battery, and Storage stats
- **Always-On Monitoring** - Automatic monitoring starts when opening the page
- **Continuous CSV Logging** - Start/Stop logging toggle for real-time data recording
- **Comprehensive Data Export** - CSV logs include 56+ hardware metrics:
  - CPU: Temperature (main, package, avg, max), Power (package, avg, max, Intel breakdown), Voltage (core, SoC), Load, Frequency, Bus Speed
  - GPU: Temperature (core, hotspot, memory, junction), Power (current, max, PPT, SoC, core), Voltage (core, SoC, memory), Load, Clock, Memory usage, Fan metrics
  - Motherboard: Temperatures (system, VRM, CPU, PCH), Voltages (Vcore, +3.3V, +5V, +12V)
  - Network: Speed, Utilization, Total transferred data
- **Enhanced CPU Data** - Intel power breakdown (cores, graphics, memory, platform), voltage tracking, bus speed
- **Enhanced GPU Data** - Memory temperature, junction temperature, AMD power breakdown (PPT, SoC, Core)
- **Multi-sensor support** - Intel, AMD, and NVIDIA hardware detection
- **Customizable intervals** - Update rates from 0.5s to 5s
- **Min/Max/Current tracking** - Historical value tracking with complete history

### 🛠️ System Tools

| Tool                      | Description                                                                                                                |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **File System Cleaner**   | Remove temp files, clear cache, free disk space                                                                            |
| **Driver Backup/Restore** | Backup and restore system drivers                                                                                          |
| **Drivers Lookup**        | View all installed device drivers with hardware IDs, filter by category, detect problem devices, search online for updates |
| **DNS Changer**           | Quick DNS configuration (Google, Cloudflare, etc.)                                                                         |
| **App Installer**         | Install applications via Windows Package Manager                                                                           |
| **System Utilities**      | SFC, DISM, network reset, flush DNS, and more                                                                              |
| **System Diagnostics**    | Sleep study, battery reports, memory diagnostics                                                                           |
| **xZenith Cast**          | Mirror and control Android devices on PC                                                                                   |
| **xZenith Boost**         | Performance optimization profiles for gaming and productivity                                                              |
| **Process Manager**       | Monitor and control running processes with app grouping                                                                    |

### ⚡ System Tweaks

- Performance optimizations (HAGS, Ultimate Performance Plan)
- Privacy enhancements (Disable Telemetry, Core Isolation)
- Network optimizations and DNS configuration
- One-click apply/unapply with history tracking

### 🎮 Additional Features

- **Global Search Command (Ctrl+K)** - Quick navigation to any feature without using mouse
- **Discord Rich Presence** - Show monitoring status on Discord
- **On-Screen Display (OSD)** - Notifications for system events
- **8 Color Themes** - xZenith, Midnight, Ocean, Forest, Sunset, Aurora, Rose, Cyber
- **Dynamic Backgrounds** - Gradients, Shooting Stars, DarkVeil
- **System Restore Points** - Create and manage system checkpoints

---

## 📥 Download

### Latest Release

[![Download](https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge&logo=windows)](https://github.com/xFlawlessDev/xZenith/releases/latest)

| File                          | Description                  |
| ----------------------------- | ---------------------------- |
| `xZenith_x.x.x_x64-setup.exe` | NSIS Installer (Recommended) |
| `xZenith_x.x.x_x64_en-US.msi` | MSI Installer                |

---

## 💻 System Requirements

| Requirement    | Minimum            | Recommended |
| -------------- | ------------------ | ----------- |
| **OS**         | Windows 10 (1809+) | Windows 11  |
| **RAM**        | 4 GB               | 8 GB        |
| **Disk Space** | 200 MB             | 500 MB      |
| **Display**    | 1280x720           | 1920x1080   |

### Prerequisites

- Microsoft Edge WebView2 Runtime (auto-installed if missing)
- Visual C++ Redistributable 2015-2022
- .NET Framework 4.7.2+

> ⚠️ **Important:** Run as Administrator for full functionality

---

## 📦 Installation

### Quick Install

1. Download the latest installer from [Releases](https://github.com/xFlawlessDev/xZenith/releases/latest)
2. Run `xZenith_x.x.x_x64-setup.exe`
3. Follow the installation wizard
4. Launch xZenith from Start Menu
5. **Right-click > Run as Administrator** for full features

### Detailed Guide

See [INSTALLATION.md](./INSTALLATION.md) for detailed installation instructions.

---

## ❓ FAQ

<details>
<summary><b>Why does it need Administrator privileges?</b></summary>

xZenith requires admin access to:

- Read hardware sensors (CPU/GPU temperatures)
- Apply system tweaks and optimizations
- Manage system restore points
- Execute system utilities (SFC, DISM)
</details>

<details>
<summary><b>Hardware data not showing?</b></summary>

- Ensure you're running as Administrator
- Check if your hardware is supported
- Some laptop sensors may be limited by manufacturer restrictions
- First launch may take longer while initializing hardware detection
</details>

<details>
<summary><b>Discord RPC not working?</b></summary>

- Ensure Discord is running
- Enable Rich Presence in Settings
- Restart both applications
</details>

<details>
<summary><b>Is my data collected?</b></summary>

No. xZenith runs entirely offline and does not collect or transmit any user data.

</details>

<details>
<summary><b>xZenith Cast not working?</b></summary>

- Ensure USB debugging is enabled on your Android device
- Check that your device is properly connected
</details>

<details>
<summary><b>How to uninstall?</b></summary>

- Windows Settings > Apps > xZenith > Uninstall
- Or run the uninstaller from Start Menu
</details>

---

## 🐛 Bug Reports

Found a bug? Please report it on our [Discord Server](https://discord.gg/HKG9GNTesb) or create an issue.

When reporting bugs, please include:

- Windows version
- xZenith version
- Steps to reproduce
- Screenshots (if applicable)

---

## 🙏 Acknowledgments

- [Tauri](https://tauri.app/) - Cross-platform framework
- [Vue.js](https://vuejs.org/) - Reactive UI framework
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS
- [shadcn-vue](https://www.shadcn-vue.com/) - UI components
- [xZenithHardwareMonitor](https://github.com/xFlawlessDev/xZenithHardwareMonitor) - Hardware monitoring library
- [LibreHardwareMonitor](https://github.com/LibreHardwareMonitor/LibreHardwareMonitor) - Core hardware monitoring
- [scrcpy](https://github.com/Genymobile/scrcpy) - Android screen mirroring (xZenith Cast)
- [Lucide](https://lucide.dev/) & [Iconify](https://iconify.design/) - Icons

---

## 📝 License

xZenith is proprietary software. All rights reserved.

Copyright © 2025 xFlawlessDev

---

<div align="center">
  
  **Made with ❤️ by [xFlawlessDev](https://github.com/xFlawlessDev)**
  
  [![Discord](https://img.shields.io/badge/Discord-Join%20Us-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/HKG9GNTesb)
  [![Ko-fi](https://img.shields.io/badge/Support-Ko--fi-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/xflawlessdev)
  
  ⭐ **Star this repository to show your support!** ⭐

</div>
