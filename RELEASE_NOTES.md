# Release Notes

## v1.3.2 (2025-12-07)

### 🚀 New Features

#### Auto-Start on Login
- **Windows Startup Integration** - New setting to automatically launch xZenith when you log in to Windows
- **Toggle Control** - Enable/disable auto-start from Settings > Settings Management
- **Persistent Configuration** - Auto-start preference saved and applied on each app launch

#### Enhanced Update System
- **Download Progress Tracking** - Real-time progress bar showing download percentage during updates
- **Reusable Update Dialog** - Centralized `UpdateDialog` component shared between loading screen and settings
- **Better UX Feedback** - Clear visual indicators for:
  - Download in progress with percentage
  - Installation phase after download completes
  - Disabled controls during update process
- **Improved Error Handling** - Better error messages and state cleanup on update failures

### 🐛 Bug Fixes

#### Auto-Start Configuration
- **Fixed Hardcoded Behavior** - Auto-start now properly respects user settings instead of always enabling
- **Settings Synchronization** - Auto-start state correctly loads from settings store on app launch
- **Clean Imports** - Removed unused `MacosLauncher` imports (Windows-only app)

#### Update System Improvements
- **Type Safety** - Fixed TypeScript errors with Tauri's `DownloadEvent` types
- **Accurate Progress** - Download progress now tracks cumulative bytes instead of individual chunks
- **Event Handling** - Proper handling of Started, Progress, and Finished download events

---

## v1.3.1 (2025-12-07)

### 🐛 Bug Fixes

#### xZenithCast Improvements
- **Removed Recording Feature** - Removed unstable recording-to-file functionality that was producing blank files
- **Simplified Audio Options** - Removed recording UI controls and validation logic
- **Removed Experimental Features** - Cleaned up unstable advanced options:
  - Removed H.265 and AV1 video codecs (kept stable H.264)
  - Removed camera video source option
  - Removed FLAC and Raw audio codecs
  - Removed entire Camera Options section
  - Removed OTG Mode option
  - Removed AOA modes from keyboard/mouse/gamepad controls
- **Improved Stability** - Focus on core mirroring functionality with proven stable features

#### First-Run Tour Fixes
- **Fixed Sidebar Highlighting** - Corrected sidebar navigation item IDs to use dashes instead of spaces
- **Added New Tour Steps** - Enhanced tour coverage:
  - Drivers Lookup page with search functionality
  - Process Manager page with process search
- **Improved Navigation Flow** - Tools page now shows xZenithCast and xZenithBoost highlights in context
- **Better Timing** - Added extra wait times to ensure elements are ready before highlighting

---

## v1.3.0 (2025-12-07)

### 🚀 New Features & Improvements

This update introduces auto-update functionality, enhanced user experience with toast notifications, centralized app configuration, and improved Discord Rich Presence integration.

---

### ✨ What's New

#### Auto-Update System

- **Automatic Update Checking** - App checks for updates automatically on startup (silent mode)
- **Manual Update Check** - Check for updates anytime from Settings > Application Status
- **Auto-Update Toggle** - Enable/disable automatic updates from Settings
- **Toast Notifications** - Clean toast notifications for update status:
  - Success toast when you're already on the latest version
  - Error toast if update check fails
  - Native dialog for available updates with release notes
- **Signed Updates** - Secure update distribution with cryptographic signing
- **Custom NSIS Installer** - Windows installer with xZenith branding:
  - System compatibility check (Windows 10 1809+)
  - Automatic dependency installation (VC++ Redistributable)
  - WebView2 availability detection
  - Graceful handling of running instances
  - Registry and user data cleanup on uninstall
  - Custom install/uninstall dialogs

#### Discord Rich Presence Enhancements

- **Enhanced Discord Rich Presence** - Now shows actual hardware in your Discord status:
  - System model (e.g., "ASUS ROG Strix")
  - CPU model (e.g., "Intel Core i9-14900K")
  - GPU model (e.g., "NVIDIA RTX 4090")
  - Smart truncation for long hardware names

#### Enhanced Hardware Monitoring

- **Always-On Monitoring** - Automatic monitoring starts when opening the page
- **Continuous CSV Logging** - New "Start/Stop Logging" toggle button for real-time data recording
- **Comprehensive Data Export** - CSV logs now include 75+ hardware metrics:
  - CPU: Temperature (main, package, avg, max), Power (package, avg, max, Intel breakdown), Voltage (core, SoC), Load, Frequency, Bus Speed
  - GPU: Temperature (core, hotspot, memory, junction), Power (current, max, PPT, SoC, core), Voltage (core, SoC, memory), Load, Clock, Memory usage, Fan metrics
  - Motherboard: Temperatures (system, VRM, CPU, PCH), Voltages (Vcore, +3.3V, +5V, +12V)
  - Network: Speed, Utilization, Total transferred data
  - Storage: Temperature (primary, sensor 2), Activity, Throughput (read/write rates), Health (remaining life, spare, percentage used, errors, shutdowns), Lifetime data (GB read/written, power-on hours), Capacity used
- **Streamlined Chart Exports** - Chart dropdowns now only show PNG export (CSV export moved to logging feature)
- **Enhanced CPU Data** - Intel power breakdown (cores, graphics, memory, platform), voltage tracking, bus speed
- **Enhanced GPU Data** - Memory temperature, memory junction temperature, AMD power breakdown (PPT, SoC, Core), expanded voltage and memory metrics
- **Storage Monitoring** - Comprehensive NVMe/SATA drive monitoring with:
  - Real-time temperature tracking with dual sensors
  - Activity monitoring and throughput metrics (read/write rates)
  - Health status monitoring (remaining life, spare blocks, percentage used)
  - Lifetime statistics (total data read/written, power-on hours)
  - Per-drive selection with device metadata (model, interface, media type)
  - Detailed storage information dialog
  - CSV logging integration
  - Automatic capacity formatting (GB/GiB for <1TB drives, TB/TiB for ≥1TB drives)
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
- Live hardware monitoring with performance charts for CPU, GPU, and Storage
- Temperature and power tracking for Intel, AMD, and NVIDIA hardware
- Storage device selection with health status indicators
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


### 🙏 Feedback

Your feedback is valuable! Please join our [Discord Server](https://discord.gg/HKG9GNTesb) to:

- Report bugs
- Suggest features
- Get support
- Connect with the community

---

**Full Changelog:** [v1.3.0](https://github.com/xFlawlessDev/xzenith/releases/tag/v1.3.0)

---

<div align="center">
  
  Made with ❤️ by xFlawlessDev
  
</div>
