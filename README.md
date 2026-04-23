# SCREEK BP2-POE

ESPHome configuration for the SCREEK `BP2-POE` Bluetooth Proxy device.

Official product page: [screek.io/bp2-poe](https://screek.io/bp2-poe)

## Overview

This repository contains the ESPHome YAML used for the SCREEK BP2-POE device:

- [`SCREEK-BP2-POE.yaml`](./SCREEK-BP2-POE.yaml): main ESPHome configuration

The configuration is intended for a Bluetooth Proxy over Ethernet/PoE and includes:

- ESP32-S3 with ESP-IDF
- W5500 Ethernet support
- Bluetooth Proxy support
- BLE scan mode and scan timing controls
- Diagnostic sensors, buttons, and LED entity

## Requirements

Before building or flashing, make sure you have:

- ESPHome installed locally, or the ESPHome add-on in Home Assistant
- A SCREEK BP2-POE device
- Required secrets configured for your environment, especially OTA credentials

## Quick Start

1. Review and adjust the configuration in [`SCREEK-BP2-POE.yaml`](./SCREEK-BP2-POE.yaml) if needed.
2. Make sure the referenced secrets are available in your ESPHome setup.
3. Compile and upload with ESPHome:

```bash
esphome run SCREEK-BP2-POE.yaml
```

You can flash over USB for first-time setup, then use OTA for later updates.

## Home Assistant

Once the device is online, add it through the ESPHome integration in Home Assistant. After that, it can be used as a Bluetooth Proxy for nearby BLE devices.

The configuration also exposes diagnostic and control entities such as:

- IP and MAC address
- Uptime and reboot reason
- Heap, CPU frequency, and CPU temperature
- Reboot, safe mode, and factory reset buttons
- BLE active scan switch
- BLE scan interval and window controls
