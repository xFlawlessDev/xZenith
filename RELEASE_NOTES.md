# Release Notes

## v1.1.0 (2025-12-06)

### 🚀 New Features & Improvements

This update brings significant enhancements to the monitoring system with always-on monitoring, continuous CSV logging, and comprehensive hardware data coverage.

---

### ✨ What's New

#### Enhanced Hardware Monitoring

- **Always-On Monitoring** - Automatic monitoring starts when opening the page
- **Continuous CSV Logging** - New "Start/Stop Logging" toggle button for real-time data recording
- **Comprehensive Data Export** - CSV logs now include 56+ hardware metrics:
  - CPU: Temperature (main, package, avg, max), Power (package, avg, max, Intel breakdown), Voltage (core, SoC), Load, Frequency, Bus Speed
  - GPU: Temperature (core, hotspot, memory, junction), Power (current, max, PPT, SoC, core), Voltage (core, SoC, memory), Load, Clock, Memory usage, Fan metrics
  - Motherboard: Temperatures (system, VRM, CPU, PCH), Voltages (Vcore, +3.3V, +5V, +12V)
  - Network: Speed, Utilization, Total transferred data
- **Streamlined Chart Exports** - Chart dropdowns now only show PNG export (CSV export moved to logging feature)
- **Enhanced CPU Data** - Intel power breakdown (cores, graphics, memory, platform), voltage tracking, bus speed
- **Enhanced GPU Data** - Memory temperature, memory junction temperature, AMD power breakdown (PPT, SoC, Core), expanded voltage and memory metrics
- **Drivers Lookup** - New page to view all installed device drivers with:
  - Hardware IDs and driver version information
  - Filter by device category (Network, Display, Audio, USB, etc.)
  - Show/hide Microsoft drivers toggle
  - Problem device detection with error codes and descriptions
  - Search by device name, manufacturer, or hardware ID
  - Copy device information to clipboard
  - Search online for driver updates
  - Responsive design with desktop table and mobile card views

#### Dashboard & Monitoring

- Real-time system dashboard with CPU, GPU, RAM, Battery, and Storage overview
- Live hardware monitoring with performance charts
- Temperature and power tracking for Intel, AMD, and NVIDIA hardware
- Customizable update intervals (0.5s - 5s)
- Min/Max/Current value tracking with history

#### System Tools

- **File System Cleaner** - Remove temporary files and free disk space
- **Driver Backup & Restore** - Backup and restore system drivers
- **DNS Changer** - Quick DNS configuration with preset providers
- **App Installer** - Install apps via Windows Package Manager (winget)
- **System Utilities** - SFC, DISM, network reset, flush DNS
- **System Diagnostics** - Sleep study, battery reports, memory diagnostics
- **xZenith Cast** - Mirror Android devices to PC
- **xZenith Boost** - Performance optimization profiles for gaming and productivity
- **Process Manager** - Monitor and control running processes with app grouping

#### System Tweaks

- Performance optimizations (HAGS, Ultimate Performance Plan)
- Privacy enhancements (Telemetry, Core Isolation settings)
- Network optimizations
- Windows debloat options
- Apply/Unapply with history tracking

#### Additional Features

- Global Search Command (Ctrl+K) for quick navigation
- Discord Rich Presence integration
- On-Screen Display (OSD) for system events
- 8 color themes: xZenith, Midnight, Ocean, Forest, Sunset, Aurora, Rose, Cyber
- Dynamic backgrounds: Gradients, Shooting Stars, DarkVeil
- System Restore Points management
- First-run guided tour

---

### 💻 System Requirements

- **OS:** Windows 10 (1809+) or Windows 11
- **RAM:** 4 GB minimum, 8 GB recommended
- **Disk:** 200 MB free space
- **Prerequisites:** Edge WebView2, VC++ Redistributable, .NET Framework 4.7.2+

---

### ⚠️ Known Limitations

- Some laptop sensors may show limited data due to manufacturer restrictions
- OSD may not display on certain multi-monitor setups
- First launch may take longer while initializing hardware detection

---

### 📝 Notes

- Run as **Administrator** for full functionality
- Some features require system restart to take effect
- Please report any bugs on our Discord

---

### 🔧 Bug Fixes

- Fixed GPU temperature readings for NVIDIA and AMD graphics cards
- Fixed WiX MSI installer build errors
- Resolved TypeScript type errors in monitoring component
- Fixed Clippy warnings in hardware modules
- Corrected sensor data extraction for comprehensive monitoring

---

### 🔜 Coming Soon

- Auto-update functionality
- More system tweaks and optimizations
- Localization support
- Additional theme customization

---

### 🙏 Feedback

Your feedback is valuable! Please join our [Discord Server](https://discord.gg/HKG9GNTesb) to:

- Report bugs
- Suggest features
- Get support
- Connect with the community

---

**Full Changelog:** [v1.1.0](https://github.com/xFlawlessDev/xZenith/releases/tag/v1.1.0)

---

<div align="center">
  
  Made with ❤️ by xFlawlessDev
  
</div>
