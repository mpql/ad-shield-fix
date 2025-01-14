# 🛡️ Slashdot Ad-Shield Fix for Chrome

A TamperMonkey script that prevents intrusive ad-enforcement popups and overlay messages on Slashdot while maintaining site functionality.

**NOTE:** This is specifically tested and working with Chrome on Windows, and with TamperMonkey. It has also been tested with uBlock Origin running with no issues. It *may* work in Firefox, and it *should* work on macOS, but this is untested. If you are having issues, please see [Troubleshooting](#-troubleshooting).

## 📋 Table of Contents
- [Overview](#-overview)
- [Installation](#-installation)
- [Features](#-features)
- [Technical Details](#-technical-details)
- [Troubleshooting](#-troubleshooting)
- [Credits](#-credits)
- [Contributing](#-contributing)
- [License](#-license)
- [Version History](#-version-history)

## 🎯 Overview
This script is designed to work around Slashdot's Ad-Shield system that can make the site unusable for users with ad blockers or if their network is subject to DNS filtering, resulting in the dreaded html-load.com error, amongst others. 

## 💾 Installation
### Automatic Installation
1. Install the [TamperMonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo) extension for Chrome
2. Click [here](https://github.com/platima/slashdot-ad-fix/raw/main/slashdot-ad-fix.user.js) to install the script (TamperMonkey will automatically detect and prompt you to install it)
3. Click "Install" in the TamperMonkey prompt

### Manual Installation
1. Open TamperMonkey in Chrome
2. Click the "Create a new script" button
3. Copy the entire content of `slashdot-ad-fix.user.js`
4. Paste it into the editor
5. Click File > Save or press Ctrl+S

## ✨ Features
The script provides comprehensive protection against intrusive advertising elements:

- Blocks Ad-Shield's intrusive popup messages
- Prevents page reloads and redirects
- Stops style sheet removal attempts
- Removes empty ad containers
- Cleans up overlay iframes
- Works on both www.slashdot.org and slashdot.org
- Persists across page navigation

## 🔧 Technical Details
The script implements several protective measures:

- Intercepting and neutralising alert() calls
- Preventing overlay iframe creation
- Blocking style sheet removal attempts
- Removing empty ad containers
- Running at document-start to ensure maximum effectiveness

## 🔍 Troubleshooting
***Last Tested Working:** 2025-01-15*

1. Ensure that the script is loading when you visit Slashdot by observing the red '1' on the TamperMonkey icon, and click it to confirm the script is active [as shown here](Example.png).
2. Make sure you're using Chrome with the TamperMonkey extension. Firefox is an unknown, as is GreaseMonkey.
3. Clear your browser's cache and cookies. Alternatively, enable TamperMonkey to run in Incognito Mode and open Slashdot in that mode.
4. Ensure no conflicting add-ons are running. Other addons or multiple scripts may interfere with the functionality.
5. Check your Chrome version is up to date (Settings > Help > About Google Chrome).
6. Verify that JavaScript is enabled in your browser settings.
7. Try disabling other extensions temporarily to identify any conflicts.
8. Check if the issue persists in a new Chrome profile (Chrome Menu > Add Profile).
9. Ensure your system's date and time are set correctly, as this might affect script execution.
10. Remove and re-install the extension and the script. This is just in case TamperMonkey is not functioning correctly or the script needs to be updated.
11. If using a work or school computer, check with your IT department about potential network restrictions.
12. Lodge an issue [using this template](https://github.com/platima/slashdot-ad-fix/issues/new?labels=bug&template=bug_report.md&title=%5BBUG%5D).

## 👥 Credits
- Original concept by Daniel Perelman (perelman@aweirdimagination.net / https://openuserjs.org/scripts/dperelman)
- Chrome/TamperMonkey adaptation by Platima
- Licensed under MIT License

## 🤝 Contributing
Pull requests are welcome! Please feel free to submit issues or improvements.

## 📄 License
MIT License - see `LICENSE` file for details.

## 📅 Version History
*Note: This may not always be up to date, but the commit history is ☺*

### 2025
- **2025-01-15**
  - Added issue template and troubleshooting guide
  - Refactored README.md
- **2025-01-13**
  - DPerelman added a fix for the alert blocking
- **2025-01-11**
  - Initial Chrome/TamperMonkey release
  - Enhanced iframe and popup blocking
  - Enhanced documentation
  - Added better metadata to script
  - Added licence
  - Added attribution URL
- **2025-01-08**
  - Initial Chrome/TamperMonkey release
  - Adapted from original Firefox/Greasemonkey script
  - Added support for Chrome
  - Enhanced iframe and popup blocking
  - Improved ad container cleanup

---
*🔄 Last updated: 15 January 2025*
