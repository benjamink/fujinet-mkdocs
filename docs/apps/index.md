---
title: Apps
description: FujiNet-enabled applications for vintage computers
tags:
  - apps
---

# FujiNet Apps

FujiNet unlocks a new category of software for vintage computers: **network-aware applications** that use the N: device to pull live data from the internet or communicate with other users.

## What makes an app "FujiNet-enabled"?

A FujiNet-enabled app uses one or more of:

- **N: device** — to fetch live data (weather, news, Wikipedia) or communicate in real time
- **High score server** — to submit and retrieve scores over the network
- **TNFS** — to stream disk images or data files from community servers
- **Printer/clock emulation** — for productivity software that needs real hardware

## Cross-platform apps

These apps run on multiple FujiNet-supported platforms:

| App | Platforms | Description |
|---|---|---|
| **Five Card Stud Poker** | Atari · Apple II · C64 · CoCo · ADAM | Online multiplayer poker |
| **Fujitzee** | Atari · Apple II · C64 · CoCo · ADAM | Online multiplayer Yahtzee |
| **BBS Terminal** | All | Telnet to classic bulletin board systems |

## Atari 8-bit apps

| App | Description |
|---|---|
| **FujiNet Weather** | Real-time weather for your location (uses IP geolocation) |
| **Wikipedia Reader** | Search and read Wikipedia articles |
| **FujiNet Chat** | Simple multi-user chat rooms |
| **Synchromesh** | TNFS-based file manager |
| **FujiNet BASIC Programs** | Collection of BASIC demos using N: device |

### Where to find Atari apps

- `tnfs.fujinet.online` — `/atari8/apps/`
- `irata.online` — curated Atari software library

## Apple II apps

| App | Description |
|---|---|
| **ProDOS Network Utilities** | Network tools for ProDOS |
| **Apple II Weather** | Real-time weather (in development) |

### Where to find Apple II apps

- `tnfs.fujinet.online` — `/apple2/`
- `apple2.irata.online`

## Commodore 64 apps

| App | Description |
|---|---|
| **C64 Network Demo** | Demonstration of N: device capabilities |
| **CCGMS** | Terminal program with Telnet/BBS support |

### Where to find C64 apps

- `tnfs.fujinet.online` — `/c64/`

## CoCo apps

| App | Description |
|---|---|
| **CoCo Network Demo** | Demonstrates FujiNet network device |

!!! note "Library is growing"
    The app library grows continuously. Check the [FujiNet Discord](https://discord.gg/7MfFTvD) and [fujinet.online](https://fujinet.online) for announcements about new software.

## Writing your own FujiNet app

Interested in creating a FujiNet-enabled program? The N: device works like a standard file/serial interface in each platform's native language:

- **Atari** — CIO calls with `N:` device, or use `OPEN #n,mode,0,"N:..."` in BASIC
- **Apple II** — ProDOS file calls against the FujiNet volume
- **C64** — Standard IEC device reads

See the [FujiNet firmware wiki](https://github.com/FujiNetWIFI/fujinet-firmware/wiki) for protocol documentation, and ask on Discord for help getting started.
