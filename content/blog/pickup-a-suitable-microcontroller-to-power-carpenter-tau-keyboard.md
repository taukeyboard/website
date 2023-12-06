---
title: "Pickup a Suitable Microcontroller to power Carpenter Tau Keyboard"
date: 2023-12-06T21:08:49+08:00
---

In this blog post, we're going to research and figure out a suitable microcontroller to power Carpenter Tau Keyboard. 

Since we're building a tri-mode keyboard, it would be best to have a SoC that integrates bluetooth and raw 2.4GHz RF protocol. Otherwise, we can find a generic MCU and a dedicate RF chip for handling bluetooth and 2.4GHz.

Suprisingly there isn't many options on the market. Many famous bluetooth chips, such as ESP8266, doesn't have low level access to raw 2.4GHz transmission. The only feasible options I found: Nordic NRF52 series, TI CC2544 / CC2640, WCH CH582 and other WCH 5xx series. After a thorough study, I decide to proceed with WCH CH582. Here is the reason:

# Nordic NRF52

The main problem is the chip size. We need to build a USB dongle that is just as small as a Logitech's Unify receiver, that means the dongle's PCB should fit in a size of a USB Type A connector metal shell, plus 5mm plastic case. The smallest NRF52 series with USB feature is NRF52820, which is 5mmx5mm and would be quite challenge to fit in to this small dongle. In fact, the official dongle design and reference keyboard dongle (nrf Ready 2) are big ones.

Nordic do have a weaker, smaller NRF24lu1 chip that can fit into the small USB dongle, but it's discontinued.

# TI CC2544 / CC2640

TI CC2544 is a RF SoC powered by a 8051 microcontroller core, which is pretty weak, 32K flash and 2K ram. With this configuration you basically cannot run Zephyr OS and challenging to run FreeRTOS. And you have to build with official, raw APIs. 

TI CC2640 is much better, ARM Cortex-M3, up to 48MHz, 128K flash and 8k ram. but let's also check the last candidate

# WCH CH582 and WCH CH5xx series

WCH CH582 is powered by a RISC-V4A architectured, 32 bit MCU, with up to 80MHz clock speed, 512K flash and 32K ram. It's no doubt the most powerful option than TI CC2640. There are other CH5xx chips that varies on ports, flash and ram size, but otherwise quite similar. I'll pick CH582 since it's the mainstream on the product line, with great support and good official reference design.

# A Generic MCU with RF Chips
Alternatively, many keyboards are built with a generic MCU. They are mostly starting as a wired-only keyboard, and then look for bluetooth or tri-mode upgration. They would then add a bluetooth chip or a bluetooth & 2.4GHz chip such as ESP8266, NRF24LU1 or CH2544 discussed above. This would be useful if the keyboard MCU or the 2.4GHz chip alone is not power enough to handle dual-mode or tri-mode application logic, for example, 8 bit atmega32u4. But it's not a problem for a powerful 32 bit RISCV MCU powered SoC. It can also save the development cost, if you have already developed the wired keyboard firmware and you want to add the wireless part, it's simply adding the wireless transmission and could be developed separately, storing the program in the separate RF chip. But we can also port open source keyboard firmwares to CH582 and add tri mode support.

For who are interested in this approach, most common microcontrollers for building keyboard is atmega32u4 and STM32. I wouldn't recommend atmega32u4 because they're extremely over priced. Because many famous and open source keyboard firmware, such as QMK is starting on top of atmega32u4, this chip is in high demand. And it result in, this 8 bit, quite weak MCU can be more expensive than a powerful 32 bit Cortex-M3 stm32f10c8t6. Even the STM32 option, plus another RF chip is not cost effective and STM32 core can be less powerful than 2.4GHz & bluetooth SoCs such as NRF52840 and CH582, so I think built on a powerful 2.4GHz & bluetooth SOC is the best option.


# Summary

In this blog post, we looked and compared for feasible SoCs and MCUs on the market that suit for our requirement. As a result, we choose WCH CH582 for it's powerful SoC core, direct access to raw 2.4GHz RF protocol and small packaged size.
