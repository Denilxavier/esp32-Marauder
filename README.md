# esp32-Marauder
ESP32-based wireless tool for both offensive testing and defensive detection deauth attacks, rogue AP spoofing, BLE attacks, plus real-time threat monitoring

**Red team meets blue team on ESP32** offensive attack modules (deauth, evil twin, BLE spoofing) paired with defensive threat detection and alerting, built and tested as a personal wireless security lab project.

## Overview

This project combines offensive wireless testing capabilities with real-time defensive monitoring on a single ESP32 platform. It's designed for hands-on security research simulate common Wi-Fi/BLE attacks to understand how they work, then switch to detection mode to see how the same attacks look from a defender's perspective.

## Features

### Offensive WiFi
- Deauthentication flood
- Probe request flood
- Beacon spam (list-based and randomized SSIDs)
- AP clone spam (evil twin)
- Karma attack
- Evil Portal (captive-portal phishing page)
- Rick Roll beacon
- Bad packet / malformed frame injection
- Association sleep attack
- SAE commit flood
- Channel switch / quiet time disruption

### Offensive Bluetooth
- Sour Apple (Apple BLE spam)
- Swiftpair spam (Windows)
- Samsung BLE spam
- Flipper BLE spam
- BT spam all (multi-vendor BLE spam)
- Airtag spoofing

### Offensive Other
- BadUSB / Ducky Script execution

### Defensive Detection & Monitoring
- Deauth attack sniffing
- Pwnagotchi detection
- EAPOL / PMKID sniffing
- Signal monitor
- Channel analyzer
- Packet monitor and packet count
- Card skimmer detection (Bluetooth-based)
- Airtag sniff and monitor
- Meta Ray-Ban / Meta device detection
- FindMy sound (locate spoofed/lost trackers)
- Flock camera sniff and wardrive detection

### Reconnaissance & Scanning
- Beacon and probe request sniffing
- Scan APs / scan stations / scan all
- Raw packet sniffing
- MAC address tracking
- WiFi and Bluetooth wardriving (with GPS tagging)
- ARP scan, port scan, SSH scan, Telnet scan
- Ping scan
- Fox hunt (RF signal direction finding)

### Device Management
- OTA firmware updates (Web flasher or SD card)
- Settings management and device info
- SPIFFS backup and restore
- SD card file browser
- GPS data logging and tracking
- CLI / headless mode for scripted operation

## Hardware

- ESP32 (board model: e.g. ESP32-WROOM-32 / ESP32-S3)
- (any additional modules used — antenna, display, etc.)

## Setup

1. Flash the firmware using a browser based flasher no Arduino IDE or PlatformIO required:
   - [JCMK Marauder Installer](https://justcallmekoko.github.io/MarauderInstaller/) — official installer for standard ESP32 Marauder builds
   - [ESP Terminator](https://espterminator.com/) — alternative multi-firmware web flasher (also supports Bruce, GhostESP, etc.)
2. Connect your ESP32 to your computer via USB
3. Open the flasher site in **Chrome or Edge** (required for Web Serial support)
4. Select your exact board model and click Flash
5. Once flashed, configure Wi-Fi/BLE scan targets via the on-device menu
6. Power on and monitor alerts via (serial console / display / app)

## Usage

(Briefly describe how to switch between offensive and defensive modes, and what the alerts look like e.g. LED indicator, display output, serial log.)

## Disclaimer

This tool was built and tested strictly in a personal, authorized lab environment. It is intended for educational and defensive security research purposes only. Do not use against networks or devices you do not own or have explicit permission to test.
