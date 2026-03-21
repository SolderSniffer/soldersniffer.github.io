---
layout: post
---

Here's my Aliexpress haul from the previous post:

#### 1. Seeed XIAO nRF54L15

Tiny but powerful little board. Seriously, the amount of stuff they managed to cram into this board.. onboard CMSIS-DAP debugger (ATSAMD11), which appears as a composite USB device with a USB-UART (they wired one of the nRF54 UARTs to the SAMD11) so you can choose between RTT or UART logging. Onboard lipo charger is a nice touch. Battery voltage measurement is gated by a load switch, so the voltage divider is only powered when you want to sample. Uses a buck converter for 3.3V instead of a LDO like the XIAO nRF52840. 

This is all in addition the nRF54L15 itself, I won't bore you with the specs but the highlight for me is the 0.6uA System OFF current with the new GRTC peripheral still running. 

This got me thinking about what I could build with it, which leads me to the next item in the haul...

#### 2. 1.54" SSD1681 ePaper Display

What good is a ultra low power watch MCU if the display is a power hungry OLED? This will be the first EPD added to my collection, and I am excited to see how it works in practice. I've only ever seen them on things like Kindles and price tags, so it will be interesting to see how to best use them for a watchface.

#### 3. 280mAh LiPo Battery

Admittedly this is a bit overkill and bulky for a watch, but I wanted to have a good chance at building a watch that can last months on a single charge. I am considering either a smaller lipo or CR2032 coin cell for the final design, but this will be good for testing and prototyping.

#### 4. Miscellaneous Parts

While the previous three items should be sufficient to build a minimal functional watch, I also ordered a bunch of other parts that may come in handy along the way. Some of these include:
- LIS3DH accelerometer breakout board - For motion wakeup (gpio interrupt) and maybe even step counting? Gestures might be a stretch but we will see.
- A bunch of different buttons and switches for testing user input options.
- Cheap Apple Watch silicone case for a potential enclosure. Kinda bulky tho.
- NATO-style watch strap - I like the look of these and they are easy to swap out.
- PCF8563 RTC breakout board - The nRF54 has a built in GRTC that can be used for timekeeping, but I want to have a backup in case the GRTC doesn't work out as expected. Plus it will be interesting to compare the power consumption of the two approaches.
- A reel of 100 PFETs - incase I want to power gate the display or other peripherals to save power.

Tune in next time for Zephyr baby steps and hardware bringup!