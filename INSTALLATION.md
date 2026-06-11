# 📦 Installation Guide - Telegram Auto Gift Buyer

Complete installation instructions for Windows 10/11

---

## 🎯 Quick Installation (5 Minutes)

### For Most Users

1. **Download** → [Get Latest Release](https://github.com/yourusername/telegram-auto-gift-buyer/releases/latest)
2. **Extract** → Right-click ZIP → "Extract All"
3. **Run** → Double-click `TelegramAutoGiftBuyer.exe`
4. **Setup** → Follow the setup wizard
5. **Done!** → Start sending gifts

---

## 📋 Detailed Installation Steps

### Step 1: System Preparation

#### Check System Requirements

Before installing, ensure your system meets the requirements:

- ✅ Windows 10 (64-bit) Build 19041 or later
- ✅ Windows 11 (any version)
- ✅ At least 4 GB RAM
- ✅ 100 MB free disk space
- ✅ Active internet connection
- ✅ Administrator privileges (for installation)

#### Verify Your Windows Version

```
1. Press Windows Key + R
2. Type: winver
3. Press Enter
4. Check version number
```

Required: Windows 10 version 2004 (19041) or higher

---

### Step 2: Download the Software

#### Official Download Sources

**Primary:** [GitHub Releases](https://github.com/yourusername/telegram-auto-gift-buyer/releases)

Always download from official sources only!

#### Verify Download

After downloading, verify the file:

- **Filename:** `TelegramAutoGiftBuyer-v2.0.0-Windows.zip`
- **Size:** Approximately 15.2 MB
- **Format:** ZIP archive

#### Optional: Verify Checksum

For security-conscious users:

```powershell
# PowerShell command
Get-FileHash TelegramAutoGiftBuyer-v2.0.0-Windows.zip -Algorithm SHA256
```

Compare with official checksum on releases page.

---

### Step 3: Extract the Archive

#### Using Windows Explorer

1. Locate the downloaded ZIP file
2. Right-click on the file
3. Select "Extract All..."
4. Choose destination folder (recommended: `C:\Program Files\TelegramAutoGiftBuyer`)
5. Click "Extract"

#### Using Command Line (Advanced)

```powershell
# PowerShell
Expand-Archive -Path "TelegramAutoGiftBuyer-v2.0.0-Windows.zip" -DestinationPath "C:\Program Files\TelegramAutoGiftBuyer"
```

---

### Step 4: Handle Security Warnings

#### Windows SmartScreen

When running for the first time, Windows may show SmartScreen warning:

1. Click "More info"
2. Click "Run anyway"

This is normal for new software. We're working on code signing certificates.

#### Antivirus Software

Some antivirus programs may flag the software:

- **Windows Defender** - Usually no issues
- **Third-party AV** - May require manual allow-listing

**To whitelist in Windows Defender:**

```
1. Open Windows Security
2. Go to Virus & threat protection
3. Click Manage settings
4. Scroll to Exclusions
5. Click Add or remove exclusions
6. Add the installation folder
```

---

### Step 5: First Launch

#### Run the Application

1. Navigate to installation folder
2. Double-click `TelegramAutoGiftBuyer.exe`
3. Wait for application to load (5-10 seconds)

#### Initial Setup Wizard

The setup wizard will guide you through:

**Screen 1: Welcome**
- Introduction to the software
- Click "Next" to continue

**Screen 2: License Agreement**
- Read the MIT license
- Check "I accept" to continue

**Screen 3: System Check**
- Automatic system compatibility check
- Displays any warnings or issues

**Screen 4: Data Location**
- Choose where to store data:
  - `%APPDATA%\TelegramAutoGiftBuyer` (Recommended)
  - Custom location
- Click "Next"

**Screen 5: Security Settings**
- Set master password (optional but recommended)
- Enable/disable auto-lock
- Configure security preferences

**Screen 6: Completion**
- Review settings
- Click "Finish" to complete setup

---

### Step 6: Configure Telegram Account

#### Add Your First Account

1. Click "Add Account" button on main screen
2. Enter your phone number (with country code, e.g., +1234567890)
3. Click "Send Code"
4. Check your Telegram app for verification code
5. Enter the 5-digit code
6. If you have 2FA enabled, enter your password
7. Click "Authorize"

#### Account Verification

The app will verify your account:
- ✅ Account connected successfully
- 📊 Syncing contact list...
- 🎁 Fetching available gifts...

This may take 30-60 seconds on first connection.

---

### Step 7: Configure Basic Settings

#### Recommended Initial Settings

Navigate to **Settings** (gear icon) and configure:

**General Settings:**
- ✅ Enable auto-start with Windows
- ✅ Enable desktop notifications
- ✅ Check for updates automatically
- Theme: Choose Dark/Light/Auto

**Gift Settings:**
- Default gift type: Premium Star
- Maximum daily budget: $100 (adjust as needed)
- Confirmation before sending: Yes (recommended for beginners)

**Advanced Settings:**
- Enable logging: Yes
- Log level: Normal
- Auto-backup: Daily

Click "Save Settings" when done.

---

## 🔧 Advanced Installation

### Silent Installation (IT Administrators)

For deploying to multiple machines:

```powershell
# Extract silently
Expand-Archive -Path "TelegramAutoGiftBuyer-v2.0.0-Windows.zip" -DestinationPath "C:\Program Files\TelegramAutoGiftBuyer" -Force

# Create desktop shortcut
$WshShell = New-Object -comObject WScript.Shell
$Shortcut = $WshShell.CreateShortcut("$env:Public\Desktop\Telegram Auto Gift Buyer.lnk")
$Shortcut.TargetPath = "C:\Program Files\TelegramAutoGiftBuyer\TelegramAutoGiftBuyer.exe"
$Shortcut.Save()
```

### Portable Installation

To run from USB drive or without installation:

1. Extract to USB drive
2. Run `TelegramAutoGiftBuyer.exe` directly
3. Data will be stored in `.\data` folder

---

## 🔍 Verification & Testing

### Verify Installation

After installation, verify everything works:

#### Test 1: Application Launch
- ✅ Application starts without errors
- ✅ Main window displays correctly
- ✅ No crash or freeze

#### Test 2: Account Connection
- ✅ Can add Telegram account
- ✅ Receives verification code
- ✅ Successfully authenticates

#### Test 3: Basic Functionality
- ✅ Can view available gifts
- ✅ Can add recipients
- ✅ Interface responds smoothly

#### Test 4: Network Connection
- ✅ Status shows "Connected"
- ✅ Can fetch contact list
- ✅ Can view gift catalog

---

## 🆘 Troubleshooting Installation Issues

### Common Installation Problems

#### Issue: "Windows cannot open this file"

**Solution:**
- File extension is hidden or renamed
- Re-download the file
- Ensure file is `TelegramAutoGiftBuyer.exe`, not `.zip.exe`

#### Issue: "Application won't start"

**Possible Solutions:**
1. Run as Administrator (right-click → Run as administrator)
2. Install Visual C++ Redistributables:
   - Download from [Microsoft](https://aka.ms/vs/17/release/vc_redist.x64.exe)
   - Install and restart computer
3. Install .NET Framework 4.8:
   - Download from [Microsoft](https://dotnet.microsoft.com/download/dotnet-framework/net48)
4. Update Windows to latest version
5. Disable antivirus temporarily during first launch

#### Issue: "SmartScreen prevented an unrecognized app"

**Solution:**
- Click "More info"
- Click "Run anyway"
- This is expected for newly released software

#### Issue: "Access Denied" error

**Solution:**
- Extract to a folder where you have write permissions
- Don't extract to `C:\Program Files` unless running as admin
- Try `C:\Users\YourName\Documents\TelegramAutoGiftBuyer`

#### Issue: "Missing DLL" error

**Solution:**
1. Install Visual C++ Redistributable (x64)
2. Install all Windows updates
3. Re-extract the archive (may have corrupted during extraction)

#### Issue: Can't connect to Telegram

**Solution:**
1. Check internet connection
2. Verify Telegram is not blocked by firewall
3. Try disabling VPN temporarily
4. Check if Telegram servers are operational
5. Configure proxy settings if needed

---

## 🔄 Updating

### Update from Previous Version

#### Automatic Update (Recommended)

1. Application will notify when update available
2. Click "Update Now"
3. Download completes automatically
4. Restart application
5. Update installed!

#### Manual Update

1. Download latest version
2. Close running application
3. Backup `data` folder (important!)
4. Extract new version over old installation
5. Launch application
6. Verify settings preserved

### Preserve Settings When Updating

Your settings are stored in:
- `%APPDATA%\TelegramAutoGiftBuyer\config.json`
- `%APPDATA%\TelegramAutoGiftBuyer\accounts\`

These are NOT overwritten during updates.

---

## 🗑️ Uninstallation

### Complete Removal

If you need to uninstall:

#### Step 1: Close Application
- Right-click system tray icon
- Select "Exit"

#### Step 2: Remove Program Files
- Delete installation folder
- Default: `C:\Program Files\TelegramAutoGiftBuyer`

#### Step 3: Remove User Data (Optional)
- Delete `%APPDATA%\TelegramAutoGiftBuyer`
- This removes all settings and session data

#### Step 4: Remove Registry Entries (Optional)
```powershell
# PowerShell (Run as Administrator)
Remove-Item -Path "HKCU:\Software\TelegramAutoGiftBuyer" -Recurse -ErrorAction SilentlyContinue
```

#### Step 5: Remove Shortcuts
- Delete desktop shortcut
- Remove from Start Menu

---

## 📞 Installation Support

### Need Help?

If you encounter issues during installation:

- 📧 **Email:** support@example.com
- 💬 **Telegram:** [@TelegramGiftBuyerSupport](https://t.me/example)
- 🐛 **GitHub Issues:** [Report Issue](https://github.com/yourusername/telegram-auto-gift-buyer/issues)
- 📖 **Documentation:** [Full Docs](https://github.com/yourusername/telegram-auto-gift-buyer/wiki)

### Before Contacting Support

Please gather this information:

1. Windows version (`winver` command)
2. Application version (shown in About screen)
3. Error messages (screenshot if possible)
4. Installation folder location
5. Antivirus software name
6. Steps that led to the issue

---

## ✅ Post-Installation Checklist

After successful installation:

- [ ] Application launches without errors
- [ ] Telegram account connected successfully
- [ ] Settings configured to your preferences
- [ ] Desktop shortcut created (if desired)
- [ ] Notifications working correctly
- [ ] Can view available gifts
- [ ] Can add recipients
- [ ] Understand basic operations
- [ ] Read Quick Start Guide
- [ ] Bookmark documentation

---

## 🎓 Next Steps

Now that installation is complete:

1. **Read Quick Start Guide** - Learn basic operations
2. **Watch Video Tutorials** - Visual learning resources
3. **Join Community** - Connect with other users
4. **Explore Features** - Discover advanced functionality
5. **Send First Gift** - Test the system

---

## 📝 Notes

- Installation typically takes 5-10 minutes
- First launch may take longer (30-60 seconds)
- Initial Telegram sync can take 1-2 minutes
- Updates are smaller (usually 2-5 MB)
- Settings persist across updates
- Portable mode available for advanced users

---

**Installation Guide Version:** 2.0.0  
**Last Updated:** June 11, 2026  
**Platform:** Windows 10/11 (64-bit)

[← Back to README](./README.md) | [View FAQ →](./FAQ.md)
