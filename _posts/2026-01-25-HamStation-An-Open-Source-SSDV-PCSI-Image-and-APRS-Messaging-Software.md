---
title:  "HamStation: An Open Source SSDV/PCSI Image & APRS Messaging Software"
---

<img width="100%" alt="hamstation_main1" src="https://github.com/user-attachments/assets/e460a109-f127-46cb-8aca-432d718f04b5" />


## Introduction

**HamStation** is an amateur radio communication software designed for Windows. It facilitates image and short message transmission over VHF/UHF analog FM channels and is suitable for both terrestrial and satellite communication scenarios.

HamStation features built-in support for both English and Chinese.

## Main Features

The software supports two image encoding formats:
 - SSDV Format: A specialized implementation based on JPEG that allows for image recovery and display even when some data packets are lost.
 - PCSI Format: Utilizes Compressed Sensing technology where each data packet contains partial information of the complete image. The image clarity progressively improves as the number of received packets increases.

Image Transmission supports 1200 or 2400bps AFSK modulation with the following selectable data protocols:
 - AX.25 Protocol: Compatible with common soundmodem software and built-in radio modems (TNCs).
 - CCSDS Protocol: Uses Reed-Solomon Forward Error Correction (FEC) for better sensitivity.

Additionally, HamStation supports sending, receiving, and forwarding APRS short messages at a rate of 1200bps and provides basic QSO logging functionality.

**Demo:** To see the effects of the different image transmission modes, please visit: [https://www.bilibili.com/video/BV1WP4y1q7Ly/](https://www.bilibili.com/video/BV1WP4y1q7Ly/)

## Development Team

 - HIT LilacSat Student Micro/nano-satellite Team
 - HIT Amateur Radio Club (BY2HIT)
 - HIT Open Source Student Club
 - HIT Lilac CTF Team

**Key Developers:** Logiase, leylee, LittleQ, Sora, bg2bhc

## File Structure

 - **controller.exe:** The main application program.
 - **data (folder):** Stores operation logs and other data.
 - **panel.yaml:** Default interface parameters can be modified here.
 - **Modem Programs:** arcssd-ax25.exe, arcssd-ccsds-1200.exe, arcssd-ccsds-2400.exe

## Choosing the Right Modem Program

The arcssd folder contains three versions of the modem: invemphasis, noemphasis, and noemphasis_noshare.
 - **invemphasis:** Suitable for standard FM radios with audio pre-emphasis enabled (this is the default version used in the package).
 - **noemphasis:** Suitable for FM radios where pre-emphasis can be turned off, or for the "9600 mode" on certain radios. This version offers better modulation/demodulation performance.
 - **noemphasis_noshare:** Based on noemphasis, but enables Exclusive Mode for the sound card, offering better stability for long-term operation.

## Device Setup

 - **Audio:** The software transmits and receives data via the radio's audio interface (USB audio or analog audio/mic/spk jacks are both supported).
 - **PTT Control:** Supported via Serial Port RTS or DTR. Alternatively, select "None" to use manual PTT or the radio's VOX function.

## Known Issues

 - **Windows 11 Audio Device Names:** On some Windows 11 computers, the backend may fail to start due to character encoding issues with the built-in sound card's device name. Try renaming the audio device in Windows settings, or switch to a USB sound card or virtual audio cable.
 - **2400 Mode Audio Quality:** The 2400bps mode requires high audio flatness from the radio. If you experience high packet loss, try adjusting the radio's audio balance/EQ configuration.
 - **Antivirus Alerts:** The packaged .exe file may trigger false positive warnings from antivirus software. Run the Python source code directly, re-package the software locally on your own machine, or run the software in a sandbox environment.

## Software Download

For source code
 - Frontend: [https://github.com/by2hit/arcss_panel_pc](https://github.com/by2hit/arcss_panel_pc)
 - Modem: [https://github.com/by2hit/arcssd-go](https://github.com/by2hit/arcssd-go)
 - PCSI: [https://github.com/by2hit/pcsi](https://github.com/by2hit/pcsi)

For packaged binaries
 - [https://github.com/by2hit/arcss_panel_pc/releases/download/v1.0/HamStation_20230609.zip](https://github.com/by2hit/arcss_panel_pc/releases/download/v1.0/HamStation_20230609.zip)
