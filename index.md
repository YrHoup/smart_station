---
id: daria.gladkykh
title: Smart Station
sidebar_label: Smart Station
---

# Smart Station
Author: Daria Gladkykh  
GitLab Repo: [Smart Station on GitLab](https://gitlab.cs.pub.ro/daria.gladkykh/pmrust.pages.upb.ro)

---

## Project Description

Smart Station is an ambient-aware music controller built on the Raspberry Pi Pico W. It integrates various input/output components to create a reactive music environment. The system uses a light sensor to detect room brightness and automatically start/stop music. An RGB LED provides a visual status indicator, and an OLED touchscreen allows full music control (play/pause, next, previous) along with clock and alarm functionality using an RTC module.

---

## Team Members
- Daria Gladkykh

---

## Objectives
- React to ambient light levels by controlling music playback
- Provide user interface via OLED touchscreen
- Show equalizer-style feedback using RGB LED
- Display clock and set alarms to control playback
- Build full system using embedded Rust

---

## Implementation

- The light sensor feeds brightness data into the Pico W, which starts/stops playback depending on the light condition.
- An RGB LED lights up red (system off), yellow (paused), or pulses with music (playing).
- The OLED touchscreen allows full interaction with the music player and also displays the current time and any active alarms.
- Optionally, a real-time clock (RTC) module enables scheduled alarms for auto playback control.
- The logic is written in Rust using embedded HAL and associated crates.

---

## Architecture

![System Architecture](/mnt/data/A_block_diagram_showcases_the_architecture_of_a_sm.png)

---

## Hardware

| Device                        | Quantity | Price (RON) |
|------------------------------|----------|-------------|
| Raspberry Pi Pico W          | 3        | 120         |
| TFT SPI Display ST7789V      | 1        | 70          |
| Light sensor (LDR)           | 1        | 10          |
| Kit with LEDs, buttons, etc. | 1        | 60          |
| RGB LED                      | 1        | 5           |
| Jumper wires (various sets)  | -        | 40          |
| Breadboards                  | 3        | 35          |
| Total                    |          | 340 RON |

---

## Software

| Library / Crate     | Description                                  | Usage                                      |
|---------------------|----------------------------------------------|--------------------------------------------|
| embedded-hal      | Hardware abstraction layer                   | Interface for GPIO, ADC, I2C, SPI, etc.     |
| rppal             | Raspberry Pi Peripheral Access Library       | GPIO and sensor communication               |
| ssd1306           | OLED display driver                          | OLED screen rendering                       |
| fugit             | Time-keeping utility                         | RTC and alarm scheduling                    |
| embedded-graphics | 2D graphics library                          | Drawing UI on OLED                          |
| st7789            | ST7789V display driver                       | Controls the TFT SPI display (if used)      |

---

## Results

- Responsive music control based on environment light
- Interactive OLED screen with full music player interface
- Simple visual music feedback via RGB LED
- Clock and alarm playback automation

---

## Resources
- [Rust Embedded HAL Documentation](https://docs.rs/embedded-hal/)
- [Raspberry Pi Pico W Datasheet](https://www.raspberrypi.com/documentation/microcontrollers/)
- [GitLab Project Repo](https://gitlab.cs.pub.ro/daria.gladkykh/pmrust.pages.upb.ro)
