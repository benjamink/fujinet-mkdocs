---
title: Features
description: Overview of all FujiNet features and peripheral emulations
tags:
  - features
---

# FujiNet Features

FujiNet provides two categories of functionality: **peripheral emulation** (replacing vintage hardware you might not have) and **network features** (connecting your vintage computer to the internet).

## Peripheral emulation

```mermaid
graph LR
    FN[FujiNet]
    FN --> DD[Virtual Disk Drives\nUp to 8 drives · SD card & network]
    FN --> TP[Tape / Cassette\nLoad CAS tape images]
    FN --> MD[Modem\nBBS via Telnet]
    FN --> PR[Printer\nOutput to PDF]
    FN --> CK[Clock\nReal-time via NTP]
    FN --> SP[SAM Speech\nText-to-speech · Atari only]
```

| Feature | What it does | Guide |
|---|---|---|
| Virtual Disk Drives | Mount disk images from SD card or network as real drives | [Disk Drives](disk-drives.md) |
| Network Device (N:) | TCP/IP networking for vintage apps | [Network Device](network-device.md) |
| Modem & BBS | Dial in to BBSes using Telnet | [Modem & BBS](modem.md) |
| Printer Emulation | Capture printer output as PDF | [Printer](printer.md) |
| Network Clock | Provide real-time date/time via NTP | [Clock](clock.md) |
| TNFS File Servers | Browse community software libraries | [TNFS](tnfs.md) |

## Network features

The **Network Device** (`N:`) is what makes FujiNet unique among peripheral emulators. It gives your vintage computer access to:

- HTTP and HTTPS websites
- FTP servers
- SSH sessions
- Telnet / BBS connections
- TNFS file servers
- TCP and UDP sockets
- JSON parsing

See **[Network Device (N:)](network-device.md)** for the full breakdown.
