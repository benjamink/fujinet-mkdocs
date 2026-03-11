---
title: CONFIG — Color Computer
description: How to navigate the FujiNet CONFIG application on the Tandy Color Computer
tags:
  - config
  - coco
---

# Using CONFIG: Tandy Color Computer (CoCo)

CONFIG on the CoCo runs as a native 6809 machine-language or BASIC application.

!!! note "Early-stage platform"
    CONFIG for CoCo is actively being developed. Screenshots and specific key mappings may change with firmware updates. Check the [FujiNet Discord](https://discord.gg/7MfFTvD) for the latest.

## Launching CONFIG

From Color BASIC:
```basic
LOADM"CONFIG":EXEC
```

Or if the FujiNet auto-boot disk is configured:
- Power on — CONFIG loads automatically from the FujiNet drive.

## Keyboard reference

| Key | Action |
|---|---|
| Arrow keys | Navigate menus |
| `Enter` | Select / confirm |
| `Break` | Go back / cancel |
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

**Supported image formats:**

| Extension | Description |
|---|---|
| `.DSK` | CoCo disk image |
| `.VHD` | Virtual hard disk |

## Screen 2: Network

Configure Wi-Fi connections.

## Popular TNFS servers for CoCo

| Server | Contents |
|---|---|
| `tnfs.fujinet.online` | Official community server |
| `coco.irata.online` | CoCo software archive (growing) |
