# Claude Fuel: downloads

Claude Fuel is a small always-on-top pod with two gauges for your Claude usage limits: the **5-hour window** and the **week**. Click it for details like reset times, time to the limit at your current pace and context-window fill. If you use Cursor, it shows your Cursor plan usage too.

**[Download the latest version →](https://github.com/digital-marketer-vibe-coder/claude-fuel-releases/releases)**

This repository only holds the installers. The source code is private.

## Which file do I need?

Windows only for now. The Mac version is coming later.

| Your computer | Download |
|---|---|
| Windows 10 / 11 | `Claude-Fuel-Setup-<version>.exe` |

You also need [Claude Code](https://claude.com/claude-code) installed and signed in on the same computer. Claude Fuel reads Claude Code's logs and the usage numbers Claude Code reports.

## Install on Windows

1. Download `Claude-Fuel-Setup-<version>.exe` and open it.
2. Windows may show **"Windows protected your PC"**, because the app isn't code-signed. Click **More info**, then **Run anyway**.
3. It installs for your user account only, with no admin rights needed, and starts right away. The gauges appear in the top-right corner, and an icon appears in the system tray (it may be under the **^** arrow).

On first start Claude Fuel asks **"Show your exact Claude limits?"** Click **Connect** so the gauges show the same numbers as `/usage`, updated after every Claude Code reply. Your own status line, if you have one, keeps working.

**Coming from Usage Gauge?** Install Claude Fuel, then uninstall Usage Gauge. Your settings, position and status-line connection move across on first start.

To uninstall: open ⚙ Settings, untick *Exact numbers from Claude Code* and Save (that puts your Claude Code status line back), then **Settings → Apps → Installed apps → Claude Fuel → Uninstall**.

## Using it

- **Drag** the pod anywhere. **Click** it to open the details panel, and press **Esc** to close it.
- **⚙ Settings** has your limits, weekly reset, *Always show*, *Start at login*, *Exact numbers from Claude Code*, *Exact numbers from my Claude account* and *Show my Cursor plan usage*.
- The tray icon has show/hide, reset position and quit.

## Privacy, in short

- Claude Fuel reads Claude Code's logs on your computer. If you click **Connect**, it changes one thing: the `statusLine` entry in Claude Code's `settings.json`, which it puts back when you turn that off. The status-line script only saves the numbers Claude Code gives it, on your computer.
- By default it never reads your Claude sign-in token.
- **Cursor (on by default):** only if you're signed in to Cursor, at most every 5 minutes it asks `cursor.com` for your plan usage, using Cursor's own sign-in from your computer. Turn off *Show my Cursor plan usage* to stop it.
- **Exact numbers from my Claude account (off by default):** if you turn it on, every 3 minutes it asks Anthropic (`GET https://api.anthropic.com/api/oauth/usage`) for your % used and reset times, with Claude Code's sign-in token. Anthropic's terms are unclear about tools doing this, so it's your choice.
- Tokens are never stored, logged or sent anywhere other than the company they belong to. With both settings off, Claude Fuel makes no network requests at all.
- No analytics, no tracking, no accounts.

Claude Fuel is an independent community project. It isn't made or endorsed by Anthropic.
