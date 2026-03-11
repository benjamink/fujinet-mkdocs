---
title: Network Device (N:)
description: How FujiNet's network device gives vintage computers internet access
tags:
  - features
  - network
---

# Network Device (N:)

The **Network Device** — called `N:` on Atari, with equivalents on other platforms — is FujiNet's most powerful and unique feature. It gives your vintage CPU access to the modern internet without the computer itself needing to handle TCP/IP.

## The problem it solves

```mermaid
flowchart TD
    subgraph Without FujiNet
        CPU1[1 MHz 6502\nCannot handle TCP/IP] -. No connection .-> I1[Internet]
    end
    subgraph With FujiNet
        CPU2[1 MHz 6502\nReads/writes data] -->|Peripheral bus| ESP[FujiNet ESP32\nHandles all TCP/IP]
        ESP -->|Wi-Fi| I2[Internet]
    end
```

Your vintage computer treats the network device just like a serial port or file — it simply reads and writes bytes. FujiNet's ESP32 chip handles all the complex TCP/IP processing behind the scenes.

## Supported protocols

| Protocol | Use case |
|---|---|
| **HTTP** | Web pages, APIs, weather data |
| **HTTPS** | Secure web pages and APIs |
| **FTP** | File downloads from FTP servers |
| **SSH** | Secure shell sessions |
| **Telnet** | BBS connections, legacy systems |
| **TNFS** | FujiNet's retro-optimized file server protocol |
| **WebDAV** | Remote file access |
| **TCP** | Raw socket connections |
| **UDP** | Datagrams (used by some games) |
| **JSON** | Parsed HTTP+JSON responses |

## How applications use N:

### Atari example

On Atari, the `N:` device is accessed through CIO (Central I/O) just like any other device:

```asm
; Open N: device for HTTP GET
lda #$03        ; OPEN
sta ICCOM,x
lda #<ndevurl
sta ICBAL,x
lda #>ndevurl
sta ICBAH,x
lda #$04        ; read mode
sta ICAX1,x
jsr CIOV

ndevurl .byte "N:HTTP://api.example.com/data",0
```

BASIC programs can also use `OPEN #1,4,0,"N:HTTP://..."` to read from URLs.

### What this enables

Because apps just read/write strings, developers can create programs that were impossible on vintage hardware:

```mermaid
graph LR
    APP[Atari App] -->|N: device| FN[FujiNet]
    FN --> WX[Weather API\nCurrent conditions]
    FN --> WK[Wikipedia\nArticle text]
    FN --> HS[High Score\nServer]
    FN --> MP[Multiplayer\nGame Server]
    FN --> BBS[BBS / Telnet\nServer]
```

## Apps built on the network device

| App | Platform | What it does |
|---|---|---|
| FujiNet Weather | Atari | Real-time weather via IP geolocation |
| Wikipedia Reader | Atari | Search and browse Wikipedia |
| Five Card Stud | Multi-platform | Online poker over TCP |
| Fujitzee | Multi-platform | Online Yahtzee over TCP |
| High Score clients | Atari | Submit/retrieve game scores |
| BBS Terminal | All | Telnet into classic BBSes |

## JSON parsing

FujiNet includes an onboard JSON parser that simplifies API access. Instead of your vintage CPU parsing complex JSON text, FujiNet parses it and returns only the fields your program needs:

```mermaid
sequenceDiagram
    participant App as Vintage App
    participant FN as FujiNet
    participant API as Web API

    App->>FN: GET https://api.weather.com/v1/current
    FN->>API: HTTP GET request
    API-->>FN: {"temperature":72,"humidity":45,"city":"Springfield"}
    App->>FN: Parse JSON: ["temperature"]
    FN-->>App: "72"
```

The JSON query syntax uses a simple path notation (e.g., `["city"]["temperature"]`), letting even BASIC programs extract specific values from complex web API responses.
