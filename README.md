# Wanderlust

> **Spoof your iOS device location** — set a fixed GPS position by searching an address or dropping a pin on the map.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/) ![GitHub commit activity](https://img.shields.io/github/commit-activity/t/rixxvin/wanderlust?style=flat) ![](https://img.shields.io/badge/language-swift-orange)

Wanderlust is a native SwiftUI app that uses Apple’s developer location simulation service (via the [idevice](https://github.com/jkcoxson/idevice) framework) together with a LocalDevVPN to change the location reported by your iPhone or iPad.

No jailbreak required.

## Features
- Set a **fixed location** by:
- - Searching for an address / place name
- - Dropping a pin directly on the map
- Clean native SwiftUI interface


## Requirements
| Requirement | Details |
|----------------------:|:----------------------------------|
| iOS / iPadOS | **26.0 or later** |
| Developer Mode | Must be enabled |
| LocalDevVPN | Allows app talk to device |
| Device pairing | [iLoader](https://github.com/nab138/iloader), [idevice_pair](https://github.com/jkcoxson/idevice_pair), or equivalent |  

## Installation

### Option 1 – SideStore (recommended)  

1. Download the latest `.ipa` from the [Releases](https://github.com/rixxvin/Wanderlust/releases) page.
2. Make sure a LocalDevVPN is active.
3. Open SideStore and install the IPA.
  

### Option 2 – LiveContainer / other sideloading tools

You can also run Wanderlust inside LiveContainer or any other tool that supports running or installing unsigned apps.
  

## Usage

1. Enable **Developer Mode** on your device (Settings → Privacy & Security → Developer Mode).
2. Start LocalDevVPN tunnel.
3. Open Wanderlust.
4. Click **Change location**
5. Search for a place **or**move map.
6. Tap **Start spoofing** to begin location simulation.
7. Open Maps or any location-based app to verify the spoofed position.

To stop spoofing, simply stop the simulation inside the app.
  

## Screenshots


Welcome Screen | Main screen |  Choose location
:-:|:-:|:-:
![](https://github.com/rixxvin/Wanderlust/blob/main/docs/3.jpg?raw=true)  |  ![](https://github.com/rixxvin/Wanderlust/blob/main/docs/1.jpg?raw=true)  |  ![](https://github.com/rixxvin/Wanderlust/blob/main/docs/2.jpg?raw=true)

  
## How it works (high level)

  

Wanderlust talks to the iOS developer location-simulation service through the [idevice](https://github.com/jkcoxson/idevice) library.

A LocalDevVPN creates the necessary secure tunnel so the app can set the simulated coordinates system-wide.

  

## Credits

  

- [idevice](https://github.com/jkcoxson/idevice) — pure Rust library for interacting with iOS services (used as internal framework)

- [LocalDevVPN](https://github.com/jkcoxson/LocalDevVPN) implementations that make the required tunnel possible

  

## License

  

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.
