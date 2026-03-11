---
title: CONFIG — Coleco ADAM
description: How to navigate the FujiNet CONFIG application on the Coleco ADAM
tags:
  - config
  - coleco-adam
---

# Using CONFIG: Coleco ADAM

CONFIG on the Coleco ADAM is a native ADAM application using the ADAM keyboard and display system.

## Launching CONFIG

| Method | How |
|---|---|
| Automatic | FujiNet presents the CONFIG digital data pack on boot |
| Physical button | Press the CONFIG button on FujiNet to reload CONFIG |

## Keyboard reference

| Key | Action |
|---|---|
| Arrow keys | Navigate menus |
| `Return` | Select / confirm |
| `Escape` | Go back |
| `Backspace` | Delete character |

## Main menu

```
┌─────────────────────────────────────┐
│        FujiNet CONFIG               │
│                                     │
│  1  Hosts & Devices                 │
│  2  Network                         │
│  3  Printer                         │
│  4  Clock                           │
│  5  System Info                     │
│  6  Reboot                          │
│                                     │
│  FW: 1.5  IP: 192.168.1.42         │
└─────────────────────────────────────┘
```

## Screen 1: Hosts & Devices

**Supported image formats for ADAM:**

| Extension | Description |
|---|---|
| `.ddp` | Digital Data Pack (tape drive image) |
| `.dsk` | Disk image |

**Drive slots:**

| Slot | Description |
|---|---|
| T1 / T2 | Tape drive 1 / 2 |
| D1 / D2 | Disk drive 1 / 2 |

Mount images from SD card or TNFS server just as on other platforms.

## Screen 2: Network

Scan for and connect to Wi-Fi networks.

## Screen 3: Printer

Configure printer output (AdamNet printer emulation, output to PDF).

## Screen 4: Clock

FujiNet provides the current time to ADAM software via the SmartBASIC clock interface.

## Popular TNFS servers for ADAM

| Server | Contents |
|---|---|
| `tnfs.fujinet.online` | Official community server |
| `adam.irata.online` | Coleco ADAM software archive |
