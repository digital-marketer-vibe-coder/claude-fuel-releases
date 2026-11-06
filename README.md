# Claude Fuel: downloads

Claude Fuel is a small always-on-top pod with two gauges for your Claude usage limits: the **5-hour window** and the **week**. Click it for details like reset times, time to the limit at your current pace and context-window fill.

**[Download the latest version →](https://github.com/digital-marketer-vibe-coder/claude-fuel-releases/releases)**

This repository only holds the installers. The source code is private.

## Which file do I need?

| Your computer | Download |
|---|---|
| Windows 10 / 11 | `Claude-Fuel-Setup-<version>.exe` |
| Mac (Apple Silicon or Intel) | `Claude-Fuel-<version>-universal.dmg` |

You also need [Claude Code](https://claude.com/claude-code) installed and signed in on the same computer. Claude Fuel reads Claude Code's sign-in and logs.

## Install on Windows

1. Download `Claude-Fuel-Setup-<version>.exe` and open it.
2. Windows may show **"Windows protected your PC"**, because the app isn't code-signed. Click **More info**, then **Run anyway**.
3. It installs for your user account only, with no admin rights needed, and starts right away. The gauges appear in the top-right corner, and an icon appears in the system tray (it may be under the **^** arrow).

To uninstall: **Settings → Apps → Installed apps → Claude Fuel → Uninstall**.

## Install on a Mac

1. Download the `.dmg`, open it, and drag **Claude Fuel** into **Applications**.
2. Open Claude Fuel from Applications. The first time, macOS will say it can't check the app for malicious software, because the app isn't notarized by Apple. To open it anyway:
   - Open **System Settings → Privacy & Security**, scroll down to the message about Claude Fuel, click **Open Anyway** and confirm with your password; **or**
   - In Finder, Control-click (or right-click) Claude Fuel in Applications, choose **Open**, then **Open** again.
3. If macOS says the app **"is damaged and can't be opened"**, that's the download quarantine flag, not real damage. Run this once in Terminal, then open the app again:

   ```bash
   xattr -dr com.apple.quarantine "/Applications/Claude Fuel.app"
   ```

The gauges appear in the top-right corner, and an icon appears in the menu bar.

## Using it

- **Drag** the pod anywhere. **Click** it to open the details panel, and press **Esc** to close it.
- **⚙ Settings** has your limits, weekly reset, *Always show*, *Start at login*, and *Use exact numbers from my Claude account*.
- The tray or menu-bar icon has show/hide, reset position and quit.

## Privacy, in short

- Claude Fuel reads Claude Code's logs and sign-in on your computer, and never changes them.
- With *Use exact numbers from my Claude account* on (the default), every 3 minutes it sends one request to Anthropic (`GET https://api.anthropic.com/api/oauth/usage`) with your Claude Code sign-in token. That's the only network request it makes, and it gets back only your % used and reset times. The token is never stored, logged or sent anywhere else.
- Turn that setting off and Claude Fuel makes no network requests at all; it shows estimates from Claude Code's logs instead.
- No analytics, no tracking, no accounts.

Claude Fuel is an independent community project. It isn't made or endorsed by Anthropic.
