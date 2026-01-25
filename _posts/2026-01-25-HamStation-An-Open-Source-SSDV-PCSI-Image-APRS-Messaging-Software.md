---
title:  "HamStation: An Open Source SSDV/PCSI Image & APRS Messaging Software"
---

HamStation is an amateur radio communication software designed for Windows. It facilitates image and short message transmission over VHF/UHF analog FM channels and is suitable for both terrestrial and satellite communication scenarios.

<img width="2098" height="1192" alt="hamstation_main1" src="https://github.com/user-attachments/assets/e460a109-f127-46cb-8aca-432d718f04b5" />

## Main Features

The software supports two image encoding formats:
 - SSDV Format: A specialized implementation based on JPEG that allows for image recovery and display even when some data packets are lost.
 - PCSI Format: Utilizes Compressed Sensing technology where each data packet contains partial information of the complete image. The image clarity progressively improves as the number of received packets increases.

Image Transmission supports 1200 or 2400bps AFSK modulation with the following selectable data protocols:
 - AX.25 Protocol: Compatible with common soundmodem software and built-in radio modems (TNCs).
 - CCSDS Protocol: Uses Reed-Solomon Forward Error Correction (FEC) for higher transmission sensitivity.

Additionally, HamStation supports sending, receiving, and forwarding APRS short messages at a rate of 1200bps and provides basic QSO (contact) logging functionality.

Demo: To see the effects of the different image transmission modes, please visit: https://www.bilibili.com/video/BV1WP4y1q7Ly/

## UHF Downlink

|                       | Data   | Unit |
| --------------------- | ------ | ---- |
| Frequency             | 437    | MHz  |
| Distance              | 1399.3 | km   |
| Modulation Type       | FM     | -    |
| TX Power              | 0      | dBW  |
| TX Gain               | -6     | dBi  |
| Ant Polarization Loss | 3      | dB   |
| Free Space Loss       | 148.2  | dB   |
| Other Path Loss       | 1      | dB   |
| RX Gain               | 10     | dBi  |
| RX Input Level        | -118.2 | dBm  |
| Sensitivity           | -121   | dBm  |
| Margin                | 2.8    | dB   |

