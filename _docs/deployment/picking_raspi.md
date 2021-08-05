---
layout: default
title: Picking Raspberries
parent: Display deployment
grand_parent: Deployment
nav_order: 3
has_children: false
last_modified_date: 2021-07-03 16:38
---

# Selecting a model of Raspberry Pi
{: .no_toc }

<details close markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

The Raspberry Pi is a single-board computer which has undergone several iterations in design since its initial release in early 2012. It is built around an ARM-based system-on-chip, the same kind of chip that you might find in your phone or tablet. Due to its small form factor design, respectable performance and being relatively inexpensive, it is perfect for use as a display driver. Depending on the model of Raspberry Pi you plan to use, each unit should cost (excluding the display) around £50.

## What you'll need

To create a Raspberry Pi-based display, you'll need a Raspberry Pi (as expected), along with a few peripherals. These will depend on the Raspberry Pi that you use. You may use any current variety of Raspberry Pi, but for your convenience, the following list is provided ranking models of Pi from most to least convenient, along with justification and price. We have also provided a list of Raspberry Pi models which are not suitable.

### Suitable Raspberry Pi models
- Raspberry Pi 3B/3B+ (~£34)
  - A full complement of USB ports, a full-sized RJ45 jack, a full-sized HDMI connector, a WiFi chip, along with a Micro-USB connector for power make this the ideal model for finding suitable and inexpensive accessories.
- Raspberry Pi 4B (~£34-74)
  - These are some of the most powerful variants of the Pi family, with a faster clock speed on the SoC and increased RAM. The 2GB (cheapest) model will suffice for this deployment. Be aware that this model has 2 Micro-HDMI connectors (instead of 1 full-sized HDMI connector), which could be useful if you plan to set up two displays in the same location. This variant also uses a USB-C connector for power. Apart from these differences, the Pi 4 is virtually the same as the 3B/3B+.
- Raspberry Pi 3A+ (~£24)
  - Mostly as previous for the 'B/B+' variant of the Raspberry Pi 3. This version is cost-reduced and sports a different form factor, 1 USB port and no RJ45 jack. Avoid this one if you plan to set the Pis up with wired internet.
- Raspberry Pi Zero W (~£9)
  - This is the most inexpensive version of the Pi models that are recommended. The Zero W has support for WiFI unlike its cheaper counterpart. In terms of peripherals, the Zero W makes use of Mini-HDMI for display out, and a Micro-USB port for USB peripherals (which must be connected through a USB OtG adapter). There is no provision for in-built wired networking on this model. Performance may be somewhat sluggish on this Pi, but there is no reason why it should not be tested (especially considering the low unit price). When factoring in the price of peripherals, the price difference is negligible between this model and a more capable one.


### Unsuitable Raspberry Pi models
- Raspberry Pi Pico (~£3)
  - This is a programmable microcontroller. It lacks the networking, display connectors or the possibility to run a full operating system. This won't work.
- Raspberry Pi Zero (~£5)
  - Although it is possible to use this Pi as a computer, with a full operating system, the lack of accessible networking make it too inconvenient to use without using WiFi dongles/Networking HATs (that plug into the GPIO pins on top).
- Raspberry Pi 400 (~£67)
  - Internally this is a Raspberry Pi 4 that has been enclosed in an all-in-one housing, with a keyboard on top. This body design is (as part of the Pi's stated aims to be an educational computer) made this way in reference to the popular microcomputers of the 1980s, in this case emulating the design aims of the Sinclair ZX Spectrum. Although this is a stylish reimagining of the Pi 4B, it offers no advantages over the standard 4B for this deployment, and is much larger.
- Raspberry Pi Compute family
  - This modular family is designed for hardware development for the Pi family, it is relatively much more expensive than other options, and much larger.
- Anything older than the Raspberry Pi 3 family
  - Although perfectly serviceable, these Pis are no longer supported by the Pi Foundation.

### Accessories

Depending on the model of Pi you have selected, you'll need a few different accessories and peripherals to set them up.

#### For all models

- A Micro SD card, at least 8GB in capacity, preferably 16/32GB. Make sure you buy one from a reputable brand, as no-name brands of SD card can fail earlier than expected. This means brands like SanDisk, Samsung, Toshiba or Kingston. SD cards with fast read-write speeds are useful (i.e. SanDisk's Ultra, Extreme or Extreme PRO series). (~£5-10)
- A USB keyboard/mouse. You won't necessarily need to buy one set for each Pi you purchase, as they only need to be connected when you set up or perform maintenance on the units. (~£5)
- A heatsink. Regardless of the model of Pi you choose, some degree of cooling will be needed to ensure 24/7 usage. Only passive cooling is needed for this, hence a heatsink will be suitable. (~£2)
- A case. There are many cases available for each model of Pi listed here. When selecting one, you should think about the environment you are to place the Pi into (is dust/water ingress a concern?), 

#### If you plan to use a display with DVI input only

- An HDMI to DVI adapter. You can get these in cable or dongle format. (~£5)

#### If you plan to use a display with VGA input only

- An HDMI to VGA adapter. Make sure they convert in this direction (HDMI → VGA), as adapters that work in the opposite direction might not work. (~£10)

#### For Raspberry Pi 3A

- A Micro-USB power supply. The official model should suffice for this task. (~£8)
- A USB hub. This will allow you to connect more than 1 USB device at a time to the Pi. You won't necessarily need to buy one set for each Pi you purchase, as it only needs to be connected when you set up or perform maintenance on the units. (<£5)

#### For Raspberry Pi 3B/3B+

- A Micro-USB power supply. The official model should suffice for this task. (~£8)

#### For Raspberry Pi 4B

- A USB-C power supply. The official model should suffice for this task. (~£8)
- A Micro-HDMI to full-sized HDMI adapter. You can get these in cable or dongle format. (~£5)

#### For Raspberry Pi Zero W

- A Micro-USB power supply. The official model should suffice for this task. (~£8)
- A Mini-HDMI to full-sized HDMI adapter. You can get these in cable or dongle format. (~£5)
- A USB On-the-Go (OTG) adapter. This will allow you to connect a USB mouse and keyboard to the Pi. (~£2)
- A USB hub. This will allow you to connect more than 1 USB device at a time to the Pi. You won't necessarily need to buy one set for each Pi you purchase, as it only needs to be connected when you set up or perform maintenance on the units. (<£5)