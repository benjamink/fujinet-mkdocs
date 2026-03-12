---
title: Getting Started
description: Choose your platform and connect your FujiNet in minutes
tags:
  - getting-started
---

# Getting Started

Select your vintage computer platform below to get a step-by-step connection guide.

## Choose your platform

<div class="grid cards" markdown>

-   :material-controller: **Atari 8-bit**

    The original FujiNet platform with the richest app and game library.
    Supports all Atari 8-bit computers: 400, 800, 600XL, 800XL, 130XE, and XEGS.

    [Get started →](atari-8bit.md){ .md-button }

-   :fontawesome-brands-apple: **Apple II**

    Connect via the SmartPort or Disk II bus. Supports Apple II, II+, IIe, IIc, IIgs, and Apple III.

    [Get started →](apple-ii.md){ .md-button }

-   :material-television-classic: **Coleco ADAM**

    Attach to the AdamNet peripheral bus alongside existing ADAM drives and peripherals.

    [Get started →](coleco-adam.md){ .md-button }

-   :material-controller: **Commodore 64**

    Plug into the IEC serial bus. Compatible with C64, C128, and VIC-20.

    [Get started →](commodore-64.md){ .md-button }

-   :material-television-play: **Tandy Color Computer**

    Connect via DriveWire or Bit-Banger serial port. Supports CoCo 1, 2, and 3.

    [Get started →](coco.md){ .md-button }
    [The Basics →](coco-basics.md){ .md-button }


</div>

---

## What you'll need (all platforms)

Before you start, make sure you have:

- [x] A FujiNet device for your platform (see [Where to buy](#where-to-buy))
- [x] A Wi-Fi network (2.4 GHz, WPA2) with the password handy
- [x] A microSD card formatted as **FAT32** (optional but recommended)
- [x] The correct cable or connector for your platform (usually ships with the device)

## Where to buy

FujiNet hardware is produced by community members and sold through various channels:

- **[Tindie](https://www.tindie.com/search/?q=fujinet)** — Community sellers, various platforms
- **[FujiNet.online](https://fujinet.online)** — Official project site with current availability

!!! note "FujiNet is open hardware"
    All hardware designs are open source. Experienced makers can build their own from the schematics on [GitHub](https://github.com/FujiNetWIFI/fujinet-hardware).

## What happens after setup?

Once connected, your FujiNet will:

1. Power on automatically when your vintage computer powers on
2. Connect to your Wi-Fi network
3. Load a boot disk from your SD card **or** from an online TNFS server
4. Make the `CONFIG` application available at any time

The CONFIG app is your dashboard for managing disk images, Wi-Fi, and device settings. Each platform has its own CONFIG navigation guide — linked from the **[Using CONFIG](../config/index.md)** section.
