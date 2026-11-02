# Air Sensor Board

A low-power air sensor board (temperature and humidity) based on the Nordic **nRF54L15** SoC, designed to run as a **Matter** device.

The hardware is designed in KiCad.

## Features

- **MCU:** Nordic nRF54L15 (2.4 GHz radio, Thread / Bluetooth LE)
- **Sensor:** Sensirion SHT3x digital temperature and humidity sensor (I²C)
- **Status LED:** indicates device state (pairing, network connection, errors)
- **Button:** user input (e.g. commissioning, factory reset)
- **External flash memory:** extra storage, e.g. for OTA firmware updates (DFU)
- **Antenna:** 2.4 GHz PCB antenna
- **Power:** CR2032 coin cell battery
- **Battery monitoring:** battery voltage measured with the built-in SAADC
- **Clocks:** two external crystal oscillators
  - high-frequency crystal (HFXO, 32 MHz) for the radio and high-speed clock
  - low-frequency crystal (LFXO, 32.768 kHz) for low-power timekeeping in sleep modes

## Matter

The board is built to work in a **Matter** network, using **Thread** as the transport and **Bluetooth LE** for commissioning. It is meant to report temperature, humidity, and battery level to a Matter controller (e.g. Apple Home, Google Home, Home Assistant).

## Repository layout

| File | Description |
|------|-------------|
| `air_sensor_board.kicad_pro` | KiCad project |
| `air_sensor_board.kicad_sch` | Schematic |
| `air_sensor_board.kicad_pcb` | PCB layout |

## Tools

- [KiCad](https://www.kicad.org/) (hardware design)
- [nRF Connect SDK](https://www.nordicsemi.com/Products/Development-software/nRF-Connect-SDK) (firmware, Matter support)
