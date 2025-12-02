# Installation Guide

## 📋 Prerequisites

Before installing xZenith, ensure your system meets the following requirements:

### System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **Operating System** | Windows 10 (version 1809+) | Windows 11 |
| **Architecture** | x64 (64-bit) | x64 (64-bit) |
| **RAM** | 4 GB | 8 GB |
| **Disk Space** | 200 MB | 500 MB |
| **Display** | 1280x720 | 1920x1080 |

### Required Dependencies

#### 1. Microsoft Edge WebView2 Runtime
xZenith uses WebView2 for its user interface. Most Windows 10/11 systems have this pre-installed.

**Check if installed:**
- Open Settings > Apps > Installed apps
- Search for "WebView2"

**If not installed:**
- Download from [Microsoft WebView2](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)
- Or the xZenith installer will automatically install it

#### 2. Visual C++ Redistributable (2015-2022)
Required for native components.

**Download:**
- [VC++ Redistributable x64](https://aka.ms/vs/17/release/vc_redist.x64.exe)

#### 3. .NET Framework 4.7.2+
Usually pre-installed on Windows 10/11.

**Check if installed:**
```
Open PowerShell and run:
(Get-ItemProperty "HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full").Release -ge 461808
```

**If not installed:**
- Download from [Microsoft .NET](https://dotnet.microsoft.com/download/dotnet-framework)

---

## 📥 Download

1. Go to [Releases](https://github.com/xFlawlessDev/xZenith-Releases/releases/latest)
2. Download one of the following:
   - `xZenith_x.x.x_x64-setup.exe` - NSIS Installer (Recommended)
   - `xZenith_x.x.x_x64_en-US.msi` - MSI Installer

---

## 🔧 Installation Methods

### Method 1: NSIS Installer (Recommended)

1. Download `xZenith_x.x.x_x64-setup.exe`
2. Right-click the installer > **Run as administrator**
3. If Windows SmartScreen appears:
   - Click "More info"
   - Click "Run anyway"
4. Follow the installation wizard:
   - Accept the license agreement
   - Choose installation directory (default: `C:\Program Files\xZenith`)
   - Select Start Menu folder
   - Choose additional options (Desktop shortcut, etc.)
5. Click **Install**
6. Click **Finish** when complete

### Method 2: MSI Installer

1. Download `xZenith_x.x.x_x64_en-US.msi`
2. Right-click the installer > **Run as administrator**
3. Follow the installation wizard
4. Click **Finish** when complete

---

## 🚀 First Launch

### Running with Administrator Privileges

For full functionality, xZenith requires administrator privileges:

**Option 1: One-time run**
1. Right-click xZenith shortcut
2. Select **Run as administrator**

**Option 2: Always run as admin (Recommended)**
1. Right-click xZenith shortcut
2. Select **Properties**
3. Go to **Compatibility** tab
4. Check **Run this program as an administrator**
5. Click **Apply** > **OK**

### First Run Experience
On first launch, xZenith will:
1. Show a welcome tour introducing features
2. Initialize hardware detection
3. Set up default settings

---

## 🔄 Updating

### Manual Update
1. Download the latest version from [Releases](https://github.com/xFlawlessDev/xZenith-Releases/releases/latest)
2. Close xZenith if running
3. Run the new installer (it will update the existing installation)

### Update Notifications
- Join our [Discord](https://discord.gg/HKG9GNTesb) for release announcements
- Watch this repository for release notifications

---

## 🗑️ Uninstallation

### Method 1: Windows Settings
1. Open **Settings** > **Apps** > **Installed apps**
2. Search for "xZenith"
3. Click the three dots (⋯) > **Uninstall**
4. Confirm uninstallation

### Method 2: Control Panel
1. Open **Control Panel** > **Programs** > **Uninstall a program**
2. Find "xZenith"
3. Click **Uninstall**

### Method 3: Start Menu
1. Open **Start Menu**
2. Find "xZenith" folder
3. Click **Uninstall xZenith**

### Clean Uninstall (Optional)
To remove all settings and data:
1. Uninstall xZenith using methods above
2. Delete the following folders:
   - `%APPDATA%\xZenith` - User settings
   - `%LOCALAPPDATA%\xZenith` - Cache and logs

---

## 🐛 Troubleshooting Installation

### Windows SmartScreen Warning
This appears because the app is new and not widely distributed yet.
1. Click **More info**
2. Click **Run anyway**

### "Windows protected your PC" message
Same as above - this is a reputation-based warning, not a security threat.

### Installation fails with error
1. Ensure you're running as administrator
2. Temporarily disable antivirus
3. Check if you have enough disk space
4. Try the MSI installer if NSIS fails (or vice versa)

### App won't start
1. Ensure WebView2 is installed
2. Install VC++ Redistributable
3. Try running as administrator
4. Check Windows Event Viewer for errors

### Missing hardware data
1. Run xZenith as administrator
2. Some laptop sensors are restricted by manufacturers
3. Restart the application

---

## 📞 Support

If you encounter issues:
1. Check the [FAQ](./README.md#-faq)
2. Join our [Discord Server](https://discord.gg/HKG9GNTesb)
3. Create an issue on GitHub

---

<div align="center">
  
  Made with ❤️ by xFlawlessDev
  
</div>
