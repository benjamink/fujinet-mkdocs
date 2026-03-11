---
title: CONFIG — Commodore 64
description: How to navigate the FujiNet CONFIG application on the Commodore 64
tags:
  - config
  - commodore
---

# Using CONFIG: Commodore 64

CONFIG on the Commodore 64 is a native C64 application displayed using PETSCII character set and standard C64 color palette.

## Launching CONFIG

```basic
LOAD"CONFIG",8,1
RUN
```

Or if FujiNet is configured to auto-boot:
- Power on the C64 — FujiNet presents the CONFIG disk as device 8 and it loads automatically.

## Keyboard reference

| Key | Action |
|---|---|
| Cursor keys | Navigate menus |
| `Return` | Select / confirm |
| `Run/Stop` | Go back / cancel |
| `Del` | Delete character |
| `F1` / `F3` | Page up/down in file lists |

## Main menu

```
.------------------------------------.
|        FUJINET CONFIG              |
|                                    |
|  1  HOSTS & DEVICES                |
|  2  NETWORK                        |
|  3  PRINTER                        |
|  4  CLOCK                          |
|  5  SYSTEM INFO                    |
|  6  REBOOT                         |
|                                    |
|  FW: 1.5  IP: 192.168.1.42        |
'------------------------------------'
```

## Screen 1: Hosts & Devices

**Supported image formats:**

| Extension | Description |
|---|---|
| `.D64` | 1541 single-sided double-density |
| `.D71` | 1571 double-sided double-density |
| `.D81` | 1581 double-sided high-density |
| `.T64` | Tape image |

**Device slots:**

| Device | Description |
|---|---|
| 8 | Primary disk device (default) |
| 9 | Secondary disk device |
| 10 | Tertiary disk device |

!!! tip "Avoid conflict with real drives"
    If you have a real 1541 drive on device 8, change FujiNet's device number in Network settings to 9 or 10.

## Screen 2: Network

Configure Wi-Fi and view FujiNet's IP address.

## Screen 3: Printer

| Setting | Options |
|---|---|
| Emulation | MPS-803, 1525, Epson MX-80, generic |
| Output | PDF on SD, PDF server |

## Popular TNFS servers for Commodore

| Server | Contents |
|---|---|
| `tnfs.fujinet.online` | Official community server |
| `c64.irata.online` | Commodore 64 software archive |
