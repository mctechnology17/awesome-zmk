<h3 align="center"><img src="images/logo2.png" alt="logo2"></h3>

# Awesome ZMK

A curated list of awesome ZMK firmware resources, links, zmk-config's, zmk-drivers, tools, hardware, and community projects.

## Contents

<a name="top"></a>

- [What is ZMK](#what-is-zmk)
  - [What is a board](#what-is-a-board)
  - [What is a shield](#what-is-a-shield)
  - [What are Modules](#what-are-modules)
- [Official Resources](#official-resources)
  - [Additional Resources](#additional-resources)
- [Quick start](#quick-start)
- [Community zmk-config user configurations](#community-zmk-config-user-configurations)
  - [Split Wired](#split-wired)
- [Community Documentation](#community-documentation)
  - [Useful Awesome List](#useful-awesome-list)
  - [Vendor Documentation](#vendor-documentation)
- [Community firmware Modules and Behaviors](#community-firmware-modules-and-behaviors)
  - [Custom Behaviors](#custom-behaviors)
  - [Drivers](#drivers)
    - [Drivers Trackpad](#drivers-trackpad)
    - [Drivers Trackball](#drivers-trackball)
    - [Drivers Trackpoint](#drivers-trackpoint)
    - [Drivers Analog Joystick](#drivers-analog-joystick)
    - [Drivers Haptic](#drivers-haptic)
    - [Drivers Display](#drivers-display)
    - [Drivers LEDS Backlight Underglow](#drivers-leds-backlight-underglow)
    - [Drivers Others](#drivers-others)
  - [Display Modules](#display-modules)
    - [Dongles Modules](#dongles-modules)
       - [Dongles Design](#dongles-design)
       - [Dongle Prospector Vendor](#dongle-prospector-vendor)
    - [Display Modules Hardware](#display-modules-hardware)
- [Tools and Software](#tools-and-software)
  - [Keymap Editors GUI](#keymap-editors-gui)
  - [Power Estimation](#power-estimation)
  - [Display Utilities](#display-utilities)
  - [RAW HID Host](#raw-hid-host)
  - [CLI and Utilities](#cli-and-utilities)
- [Community Pointing Projects as Computer Mouse](#community-pointing-projects-as-computer-mouse)
- [Guides and Tutorials](#guides-and-tutorials)
  - [Solder and Desolder Tools](#solder-and-desolder-tools)
  - [How to Solder](#how-to-solder)
  - [How to Desolder](#how-to-desolder)
  - [Solder and Desolder Videos](#solder-and-desolder-videos)
  - [Supported Hardware](#supported-hardware)
  - [Hardware Tutorials](#hardware-tutorials)
  - [Software Tutorials](#software-tutorials)
  - [Learn Touch Typing](#learn-touch-typing)
- [Keyboard Shops](#keyboard-shops)
- [Keyboard News](#keyboard-news)
  - [Keyboard News ErgoMechKeyboards](#keyboard-news-ergomechkeyboards)
- [Projects using ZMK closed-source or not upstreamed](#projects-using-zmk-closed-source-or-not-upstreamed)
- [Related projects](#related-projects)
- [License](#license)

---

## What is ZMK
> Pete Johanson [^6] is the creator and lead maintainer of the ZMK Firmware project

Zephyr™ Mechanical Keyboard (ZMK) Firmware

[![Discord](https://img.shields.io/discord/719497620560543766)](https://zmk.dev/community/discord/invite)
[![Build](https://github.com/zmkfirmware/zmk/workflows/Build/badge.svg)](https://github.com/zmkfirmware/zmk/actions)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)
![GitHub last commit](https://img.shields.io/github/last-commit/zmkfirmware/zmk) ![GitHub Repo stars](https://img.shields.io/github/stars/zmkfirmware/zmk)

[ZMK Firmware](https://zmk.dev/) [^1][^2] is an open source (MIT) keyboard firmware built on the [Zephyr™ Project](https://www.zephyrproject.org/) Real Time Operating System (RTOS) [^3][^4]. ZMK's goal is to provide a modern, wireless, and powerful firmware free of licensing issues.

### What is a board
In ZMK, a board defines the PCB that includes the microcontroller unit (MCU). For keyboards, this is one of two options:

Complete keyboard PCBs that include the MCU (e.g. the Planck or Preonic).
Small MCU boards (e.g. the nice!nano or Seeed Studio Xiao RP2040) that expose pins and are designed to be combined with larger keyboard PCBs, or hand-wired to switches to create the final keyboard [^12].

### What is a shield
In ZMK, a shield is a PCB or hardwired set of components that when combined with an MCU-only board, like the SparkFun Pro Micro RP2040 or nice!nano, results in a complete usable keyboard. Examples would be keyboard PCBs like the Kyria or Lily58. The shield is usually the big PCB containing all the keys [^12].

### What are Modules
ZMK makes use of Zephyr modules to include additional source code or configuration files into its build. You can think of them as similar to plugins or themes. The most common uses of this feature are:

* Building firmware for a keyboard external to ZMK's tree [^13]
* Adding functionality to ZMK, such as a driver or a behavior [^13]

## Official Resources

* [ZMK Documentation](https://zmk.dev/docs) - The primary source for all information regarding ZMK.
* [ZMK GitHub Repository](https://github.com/zmkfirmware/zmk) - The source code and development hub.
* [ZMK Discord Server](https://discord.com/invite/sycytVQ) - The main hub for community discussion, support, and development.

### Additional Resources
Zephyr Project:
* [Zephyr Project Documentation](https://docs.zephyrproject.org/latest/develop/getting_started/index.html) - The underlying RTOS for ZMK. Useful for deep-dives and driver development.
* [Zephyr Project Code Repository on GitHub](https://github.com/zephyrproject-rtos/zephyr) - Primary Git Repository for the Zephyr Project. Zephyr is a new generation, scalable, optimized, secure RTOS for multiple hardware architectures.

Nordic Semiconductor:
* [nRF Connect SDK (sdk-nrf)](https://github.com/nrfconnect/sdk-nrf) - Main nRF Connect SDK repository (west manifest, subsystems, samples).
* [Nordic DevZone (Q&A & Forums)](https://devzone.nordicsemi.com) - official community forum and tech Q&A (searchable issues, examples, vendor replies).
* [nRF Connect SDK docs / install guide](https://docs.nordicsemi.com/bundle/ncs-latest/page/nrf/installation/install_ncs.html) - official installation & platform-specific setup for NCS.
* [Nordic Developer Academy / Tutorials](https://github.com/NordicDeveloperAcademy/ncs-fund) - self-paced courses and examples (useful to onboard newcomers).

ZSWatch - Zephyr Smartwatch:
* [jakkra/ZSWatch](https://github.com/jakkra/ZSWatch) - ZSWatch the Open Source Zephyr™ based Smartwatch, including both HW and FW.
  * [ZSWatch](https://zswatch.dev/) - Smartwatch built from scratch, both hardware and software. Built on the Zephyr™ Project RTOS, hence the name ZSWatch - Zephyr Smartwatch.

## Quick Start
* [Getting Started Guide](https://zmk.dev/docs/user-setup) - The official guide to setting up your `zmk-config` repository.
* [Unified ZMK Config Template](https://github.com/zmkfirmware/unified-zmk-config-template) - A template for managing multiple boards and shields in a single configuration repository.
* [ZMK Module Template](https://github.com/zmkfirmware/zmk-module-template) - A template for creating your own external ZMK modules (behaviors, drivers, etc.).

## Community zmk-config user configurations

* [mctechnology17/zmk-config](https://github.com/mctechnology17/zmk-config) - Quickly and easily configure your Wireless corne - sofle - lily58 keyboard with ZMK
* [urob/zmk-config](https://github.com/urob/zmk-config) - Personal ZMK firmware configuration for various boards (34-keys, Corneish Zen, Planck)
* [caksoylar/zmk-config](https://github.com/caksoylar/zmk-config) - ZMK user config containing keymap for 26-36 key keyboards
* [badjeff/zmk-config](https://github.com/badjeff/zmk-config) - Personal ZMK firmware configuration for various boards
* [manna-harbour/miryoku_zmk](https://github.com/manna-harbour/miryoku_zmk) - Miryoku is an ergonomic, minimal, orthogonal, and universal keyboard layout. Miryoku ZMK is the Miryoku implementation for ZMK.
* [sadekbaroudi/zmk-fingerpunch-keyboards](https://github.com/sadekbaroudi/zmk-fingerpunch-keyboards) - The purpose of this repository is to house all the ZMK boards and shields associated with fingerpunch keyboards.
* [englmaxi/zmk-config](https://github.com/englmaxi/zmk-config) - Personal zmk-config for my ergo keyboards
* [sunaku/glove80-keymaps](https://github.com/sunaku/glove80-keymaps) - Glorious Engrammer keymap for Glove80 keyboard
* [SethMilliken/zmk-config aka araxia](https://github.com/SethMilliken/zmk-config) - ZMK Firmware Configuration
* [tokyo2006/zmk-config-corne](https://github.com/tokyo2006/zmk-config-corne) - ZMK Firmware Configuration
* [a741725193/zmk-new_corne](https://github.com/a741725193/zmk-new_corne) - ZMK Firmware Configuration
* [eigatech/zmk-config](https://github.com/eigatech/zmk-config) - ZMK Firmware Configuration
* [MickiusMousius/RolioFirmware](https://github.com/MickiusMousius/RolioFirmware) - Firmware for the Rolio split wireless keyboard.

### Split Wired

* [ZMK Documentation Wired Splits](https://zmk.dev/docs/config/split#wired-splits) - **WARNING** Hardware UARTs have a few different modes/approaches to sending and receiving data, with different levels of complexity and performance...
* [ZMK Documentation Wired Splits (Board Pin Control - rp2040)](https://zmk.dev/docs/development/hardware-integration/pinctrl) - **WARNING** The details of pin control can vary from vendor to vendor.
* [petejohanson/splitkb-halcyon-zmk-config](https://github.com/petejohanson/splitkb-halcyon-zmk-config) - Unofficial [splitkb.com Halcyon](https://splitkb.com/products/halcyon-kyria?srsltid=AfmBOoo-Cv2EjX1G1NHV5swo4dR6QqYDoxO30uTHhAOrlnbu1AvAVtPW) ZMK Config
* [petejohanson/splitkb-halcyon-zmk-module](https://github.com/petejohanson/splitkb-halcyon-zmk-module) - SplitKB Halcyon ZMK Module
* [paulshir/zmk-board-iris-ce](https://github.com/paulshir/zmk-board-iris-ce.git) - ZMK board definition for Iris CE by Keebio
* [SSheldon/zmk-keyboard-chiri-ce](https://github.com/SSheldon/zmk-keyboard-chiri-ce) - [The Chiri CE (Compact Edition)](https://keeb.io/products/chiri-ce-keyboard-kit?srsltid=AfmBOopwnxFWr1kaGPoG6r7je1GEXMA29YCX01t8OEYUgrCqfq4o1ZUD) is just like the Iris CE, but with one less row to make it even more compact, like a Corne!

## Community Documentation
* [maksimdrachov/zephyr-rtos-tutorial](https://github.com/maksimdrachov/zephyr-rtos-tutorial) - Zephyr: Tutorial for beginners
* [golioth/awesome-zephyr-rtos](https://github.com/golioth/awesome-zephyr-rtos) - Awesome Zephyr (curated resources), community-curated lists of tools, guides & projects.
* [joric/nrfmicro/wiki](https://github.com/joric/nrfmicro/wiki) - Joric's nRFMicro Wiki, an extensive wiki covering the nRFMicro board, batteries, displays, and ZMK.
* [araxia.net/keyboards](https://araxia.net/keyboards/) - Personal blog with detailed build logs and ZMK insights.
* [Codethetical/reddit.com](https://www.reddit.com/r/ErgoMechKeyboards/comments/15t3o6k/custom_art_on_niceview_displays/) - Custom Art on Nice!View Displays
* [whoop-t/nice-shield-base](https://github.com/whoop-t/nice-shield-base) -  create your own!

### Useful Awesome List
* [sdras/awesome-actions](https://github.com/sdras/awesome-actions) - A curated list of awesome things related to GitHub Actions.
* [moul/awesome-ssh](https://github.com/moul/awesome-ssh) - A curated list of SSH apps, libraries and resources.
* [dictcp/awesome-git](https://github.com/dictcp/awesome-git) - A curated list of amazingly awesome Git tools, resources and shiny things.
* [veggiemonk/awesome-docker](https://github.com/veggiemonk/awesome-docker) - A curated list of Docker resources and related projects about the Docker ecosystem.
* [dreftymac/awesome-yaml](https://github.com/dreftymac/awesome-yaml) - A curated collection of YAML tools, templating libraries and related resources.
* [fffaraz/awesome-cpp](https://github.com/fffaraz/awesome-cpp) - A curated list of awesome C++ (or C) frameworks, libraries, resources, and shiny things.

### Vendor Documentation

* [42keebs](https://42keebs.eu/build-guides/)
* [Bastard Keyboards](https://docs.bastardkb.com/)
* [beekeeb](https://docs.beekeeb.com/)
* [Keebio](https://docs.keeb.io/main)
* [MoErgo (Glove80)](https://docs.moergo.com/layout-editor-guide/)
* [SplitKB](https://docs.splitkb.com/)
* [Typeractive](https://docs.typeractive.xyz/)
* [MBUK - mechboards](https://guides-mechboards.gitbook.io/guides)

## Community firmware Modules and Behaviors

### Custom Behaviors

* [ZMK Behaviors Documentation](https://zmk.dev/docs/keymaps/behaviors) - Official documentation on how behaviors work.
* [urob/zmk-helpers](https://github.com/urob/zmk-helpers) - Convenience macros simplifying ZMK's keymap configuration
* [urob/zmk-auto-layer](https://github.com/urob/zmk-auto-layer) - Auto-layer (including num-word) implementation.
* [urob/zmk-adaptive-key](https://github.com/urob/zmk-adaptive-key) - A ZMK module adding a adaptive-key behavior.
* [urob/zmk-leader-key](https://github.com/urob/zmk-leader-key) - A ZMK module adding a leader-key behavior.
* [urob/zmk-unicode](https://github.com/urob/zmk-unicode) - ZMK module for Unicode input
* [dhruvinsh/zmk-tri-state](https://github.com/dhruvinsh/zmk-tri-state) - Tri-state (swapper) implementation.
* [dhruvinsh/zmk-num-word](https://github.com/dhruvinsh/zmk-num-word) - Num-word implementation.
* [badjeff/zmk-split-peripheral-bonding-tweak](https://github.com/badjeff/zmk-split-peripheral-bonding-tweak) - This an experimental of an experimental module that grant ability to a split central and peripherals to bond on top of a forgettable bluetooth pairing. Two add-on feature are designed to serve this purpose on ZMK.
* [badjeff/zmk-hid-io](https://github.com/badjeff/zmk-hid-io) - This module add new HID Usage Page for ZMK.
* [badjeff/zmk-split-peripheral-input-relay](https://github.com/badjeff/zmk-split-peripheral-input-relay) - This would allow, for example, sending trackpoint events from the peripheral to the center split.
* [badjeff/zmk-split-peripheral-output-relay](https://github.com/badjeff/zmk-split-peripheral-output-relay) - This is a [ZMK](https://zmk.dev) *Split Transport* module adding support for [Enhanced ShockBurst (ESB)](https://docs.nordicsemi.com/bundle/ncs-latest/page/nrf/protocols/esb/index.html) protocol on Nordic nRF5 Series device.
* [badjeff/zmk-split-peripheral-bonding-tweak](https://github.com/badjeff/zmk-split-peripheral-bonding-tweak) - This an experimental of an experimental module that grant ability to a split central and peripherals to bond on top of a forgettable bluetooth pairing.
* [badjeff/zmk-behavior-insomnia](https://github.com/badjeff/zmk-behavior-insomnia/) - Insomnia Behavior for ZMK. This module prevents the board from entering sleep mode if BLE is connected, useful for multi-peripheral setups to avoid continuous BLE advertisement scanning.
* [badjeff/zmk-output-behavior-listener](https://github.com/badjeff/zmk-output-behavior-listener) - It allows to config a feedback of state change event by binding behaviors to feedback devices, such as, eccentric rotating mass (ERM) motors, Linear Resonant Actuator (LRA) vibration motors, LED indicators, serve motors, motorized fader, etc.
* [badjeff/zmk-input-processor-mixer](https://github.com/badjeff/zmk-input-processor-mixer) - This module interrupt, combine, sync incoming input events from Zephyr input subsystem for ZMK.
* [badjeff/zmk-feature-split-esb](https://github.com/badjeff/zmk-feature-split-esb)
* [badjeff/zmk-behavior-key-press-lip](https://github.com/badjeff/zmk-behavior-key-press-lip) - Implementation of [Last Input Priority](https://www.hitboxarcade.com/blogs/support/what-is-socd) key press favor for ZMK.
* [badjeff/zmk-input-processor-xyz](https://github.com/badjeff/zmk-input-processor-xyz) - This module is used to quantize X and Y value set to fit inside single payload of pointing device on split peripheral, to reduce the bluetooth connection loading between the peripherals and the central.
* [ssbb/zmk-antecedent-morph](https://github.com/ssbb/zmk-antecedent-morph) - ZMK Antecedent Morph Behavior aka Adaptive Keys.
* [ssbb/zmk-deadkey-slayer](https://github.com/ssbb/zmk-deadkey-slayer) - A ZMK module to drop illegal keycodes.
* [ssbb/zmk-listeners](https://github.com/ssbb/zmk-listeners)- ZMK module to invoke behaviors on certain events.
* [zzeneg/zmk-raw-hid](https://github.com/zzeneg/zmk-raw-hid) - ZMK module for Raw HID communication
* [englmaxi/zmk-hid-trackball-interface](https://github.com/englmaxi/zmk-hid-trackball-interface) - ZMK trackball interface using HID indicators
* [elpekenin/zmk-userspace](https://github.com/elpekenin/zmk-userspace) - "tiny" and "useful" bits to reuse across ZMK boards

### Drivers

#### Drivers Trackpad
* [petejohanson/cirque-input-module](https://github.com/petejohanson/cirque-input-module) - Zephyr module for the Cirque Pinnacle input driver.
* [AYM1607/zmk-driver-azoteq-iqs5xx](https://github.com/AYM1607/zmk-driver-azoteq-iqs5xx) - ZMK driver for Azoteq IQS5XX trackpads
* [sekigon-gonnoc/iqs7211e-trackpad-module](https://github.com/sekigon-gonnoc/iqs7211e-trackpad-module) - iQS7211E sensor driver with 30 mm diameter trackpad, low consumption (~ 1.5 mA) and admits multitactile (two points).

#### Drivers Trackball
* [badjeff/zmk-pmw3610-driver](https://github.com/badjeff/zmk-pmw3610-driver) - PMW3610 sensor driver.
* [badjeff/zmk-paw3395-driver](https://github.com/badjeff/zmk-paw3395-driver) - This is an ZMK pointer input module, that grant ability to call a non-disclosed PAW3395 driver library.
  * [badjeff/paw3395-pcb](https://github.com/badjeff/paw3395-pcb) - PixArt PAW3395DM-T6QU low power laser mouse sensor breakout board.
* [inorichi/zmk-pmw3610-driver](https://github.com/inorichi/zmk-pmw3610-driver) - PMW3610 sensor driver.
* [twinoner/t0bybr_pim447](https://github.com/twinoner/t0bybr_pim447) - Pimoroni PIM447 trackball driver
* [t0bybr/pim447](https://github.com/t0bybr/pim447) - Pimoroni PIM447 trackball driver
* [sekigon-gonnoc/zmk-driver-paw3222](https://github.com/sekigon-gonnoc/zmk-driver-paw3222) - This driver enables the use of the PIXART PAW3222 optical sensor with the ZMK framework.

#### Drivers Trackpoint
* [badjeff/kb_zmk_ps2_mouse_trackpoint_driver](https://github.com/badjeff/kb_zmk_ps2_mouse_trackpoint_driver) - PS/2 trackpoint driver fork updated for mainline ZMK.
* [infused-kim/zmk-ps2-mouse-trackpoint-driver](https://github.com/infused-kim/kb_zmk_ps2_mouse_trackpoint_driver) - PS/2 trackpoint driver.

#### Drivers Analog Joystick
* [badjeff/zmk-analog-input-driver](https://github.com/badjeff/zmk-analog-input-driver) - This driver groups ADC io channels into single input event for input subsystem.

#### Drivers Haptic
* [badjeff/zmk-drv2605-driver](https://github.com/badjeff/zmk-drv2605-driver/) - DRV2605 haptic feedback driver.

#### Drivers Display
* [mctechnology17/zmk-oled-adapter](https://github.com/mctechnology17/zmk-oled-adapter) - use different OLED screen sizes without modifying code (for 128x32, 128x64 and 128x128 OLED screens)
* [MickiusMousius/zmk-ls0xxvcom-driver](https://github.com/MickiusMousius/zmk-ls0xxvcom-driver) - Zephyr driver for LS0XX displays with the VCOM fix applied

#### Drivers LEDS Backlight Underglow
> [!NOTE]
> [elpekenin/zmk-userspace](https://github.com/elpekenin/zmk-userspace) These drivers can be easily located here and not only in behaviors

* [caksoylar/zmk-rgbled-widget](https://github.com/caksoylar/zmk-rgbled-widget) - A ZMK module to add battery & BT indicators using an RGB LED (like in Xiao BLEs).
* [sekigon-gonnoc/zmk-feature-status-led](https://github.com/sekigon-gonnoc/zmk-feature-status-led) - This module provides LED status indicators for ZMK keyboards using gpio-leds.
* [joelspadin/zmk-keyboards](https://github.com/joelspadin/zmk-keyboards) - marten_numpad and indicator LEDs driver
* [dhruvinsh/zmk-config](https://github.com/dhruvinsh/zmk-config/tree/legacy) - **legacy branch** This repository tracks my keyboard configuration.
* [englmaxi/zmk-config](https://github.com/englmaxi/zmk-config/tree/main/boards/shields/led_indicator) - single LED indicator widget based on [caksoylar/zmk-rgbled-widget](https://github.com/caksoylar/zmk-rgbled-widget)

#### Drivers Others
* [badjeff/zmk-adns9800-driver](https://github.com/badjeff/zmk-adns9800-driver) - ADNS9800 sensor driver.
* [badjeff/zmk-tb6612fng-driver](https://github.com/badjeff/zmk-tb6612fng-driver) - This module exposes TB6612FNG inputs via Zephyr's sensor_driver_api and key press behavior.
* [badjeff/zmk-drv883x-driver](https://github.com/badjeff/zmk-drv883x-driver) - This module exposes DRV883x inputs via Zephyr's sensor_driver_api and key press behavior.
* [petejohanson/ec-support-zmk-module](https://github.com/petejohanson/ec-support-zmk-module) - Electrostatic Capacitive (Topre) matrix scan implementation.
* [sekigon-gonnoc/zmk-feature-non-lipo-battery-management](https://github.com/sekigon-gonnoc/zmk-feature-non-lipo-battery-management) - This module provides battery management functionality for non-LiPo batteries (such as alkaline or NiMH) in ZMK keyboards. It includes voltage monitoring, battery percentage calculation, and power management features.

### Display Modules

* [mctechnology17/zmk-nice-oled](https://github.com/mctechnology17/zmk-nice-oled) - vertical widgets for oled and niceview screens using zmk (for split and non-split keyboards)
* [mctechnology17/zmk-dongle-display-view](https://github.com/mctechnology17/zmk-dongle-display-view) - horizontal widgets for keyboards with dongles, splits and non-splits using the nice!view (bongocat, wpm, caps, batt, etc.)
* [MickiusMousius/RolioFirmware (for Vista508)](https://github.com/MickiusMousius/RolioFirmware) - The Vista508 is a low-power, high refresh rate display meant to replace I2C OLEDs traditionally used.
* [M165437/nice-view-gem](https://github.com/M165437/nice-view-gem) - A sleek customization for the nice!view shield
* [zzeneg/zmk-nice-view-hid](https://github.com/zzeneg/zmk-nice-view-hid) - ZMK module for nice!view widget with Raw HID functionality
* [infely/nice-view-battery](https://github.com/infely/nice-view-battery) - A clean customization for the nice!view displays
* [GPeye/hammerbeam-slideshow](https://github.com/GPeye/hammerbeam-slideshow) - A zmk module to implement a slideshow of 30 of Hammerbeam's 1 bit art on the peripheral (right) nice!view display.
* [GPeye/urchin-peripheral-animation](https://github.com/GPeye/urchin-peripheral-animation) - Urchin Peripheral Animation
* [GPeye/mario-peripheral-animation](https://github.com/GPeye/mario-peripheral-animation) - Urchin Peripheral Animation
* [dsifry/nice-view-mod](https://github.com/dsifry/nice-view-mod) - A copy of the nice!view shield from the official ZMK repo as a ZMK module for the purposes of easily customizing
* [Ziembski/nice-view-press-start](https://github.com/Ziembski/nice-view-press-start) - Custom shield for nice!view with retro feeling
* [whoop-t/nice-one-punch-ok](https://github.com/whoop-t/nice-one-punch-ok) - one punch
* [whoop-t/nice-adventure-time](https://github.com/whoop-t/nice-adventure-time) - adventure time
* [whoop-t/nice-futurama-sus](https://github.com/whoop-t/nice-futurama-sus) - futurama
* [whoop-t/nice-fry-button-miss](https://github.com/whoop-t/nice-fry-button-miss) - futurama fry
* [whoop-t/nice-luffy-wanted](https://github.com/whoop-t/nice-luffy-wanted) - luffy
* [whoop-t/nice-luffy-gear-five](https://github.com/whoop-t/nice-luffy-gear-five) - luffy gear five
* [Jestar342/nice-view-spacemarine](https://github.com/Jestar342/nice-view-spacemarine) - This is a base repo to help anyone get started creating their own images/animations for their nice!view.
* [kevinpastor/nice-view-elemental](https://github.com/kevinpastor/nice-view-elemental) - A bold while minimalistic interface for your keyboard's display

#### Dongles Modules
> NOTE
> ZMK Supports Dongle scheme for 3 controllers (host + 2 halves). It's a little bit more battery friendly (up to a month on a 100 mAh) than a battery-powered BT host (up to 7 days) [^7].

* [mctechnology17/zmk-dongle-display-view](https://github.com/mctechnology17/zmk-dongle-display-view) - horizontal widgets for keyboards with dongles, splits and non-splits using the nice!view (bongocat, wpm, caps, batt, etc.)
* [englmaxi/zmk-dongle-display](https://github.com/englmaxi/zmk-dongle-display) - Custom status screen for zmk dongles
* [carrefinho/prospector-zmk-module](https://github.com/carrefinho/prospector-zmk-module) - ZMK module for the Prospector dongle
* [janpfischer/zmk-dongle-screen](https://github.com/janpfischer/zmk-dongle-screen.git) - YADS - Yet another Dongle Screen for ZMK
* [victorlucachi/charybdis-zmk-module](https://github.com/victorlucachi/charybdis-zmk-module) - zmk module for bkb charybdis mini/nano with pmw3610 and xiao/nicenano dongle
* [joaopedropio/snake-module](https://github.com/joaopedropio/snake-module.git) - Snake Dongle Shell 🐍
* [dhruvinsh/zmk-prospector](https://github.com/dhruvinsh/zmk-prospector) - Prospector but for ST7735S display

##### Dongles Design
* [carrefinho/prospector](https://github.com/carrefinho/prospector) - Desktop ZMK Dongle with color 1.69-inch IPS LCD screen with curved cover glass screen
* [tokyo2006/prospector-zmk-module/support_nicenano](https://github.com/tokyo2006/prospector-zmk-module/blob/support_nicenano/stl/Back.stl) - Desktop ZMK Dongle with color 1.69-inch IPS LCD screen with curved cover glass screen
* [rain2813/zmk-cygnus-oled](https://github.com/rain2813/zmk-cygnus-oled) - This is keymap configuration for redox zmk firmware, 1.3-inch I2C OLED display
* [englmaxi/zmk-dongle-display 1](https://github.com/englmaxi/zmk-dongle-display/tree/main/cases) - case1
* [englmaxi/zmk-dongle-display 2](https://github.com/englmaxi/zmk-dongle-display/tree/main/cases) - case2
* [rafaelromao/keyboards](https://github.com/rafaelromao/keyboards/tree/main/stls/Dongle) - Cyberdeck
* [spe2/zmk_dongle_hardware](https://github.com/spe2/zmk_dongle_hardware) - Dongle PCB
* [rain2813/makerworld.com](https://makerworld.com/en/models/403660) - Macintosh
* [rurounikexin/makerworld.com](https://makerworld.com/en/models/242951) - Redox
* [leafflat/sai44](https://github.com/leafflat/sai44/tree/main/STL/Dongle) - sai44 Dongle
* [yingeling/makerworld.com](https://makerworld.com/en/models/496738) - ZMK Display Dongle
* [James_909973/printables.com](https://www.printables.com/model/1207682-zmk-nice-nano-128x64-oled-dongle) - ZMK Nice Nano 128x64 OLED Dongle
* [rafaelromao/keyboards](https://github.com/rafaelromao/keyboards/tree/main/src/keyboards/bastardkb/dilemma/boards/shields/dilemma) - Dilemma DIY with 128x32 OLED
* [dohn-joh/dongle-zmk](https://github.com/dohn-joh/dongle-zmk) - Dongle ZMK
* [joaopedropio/snake-dongle](https://github.com/joaopedropio/snake-dongle.git) - Snake Dongle is a compact, highly customizable ZMK-powered dongle that features a Snake‑game-style animation and optional sound effects.
  * [joaopedropio/snake-dongle-shell](https://github.com/joaopedropio/snake-dongle-shell.git) - Snake Dongle Shell 🐍

##### Dongle Prospector Vendor
* [keycapsss.com/Prospector Kit - ZMK dongle with full color LCD screen (standard)](https://keycapsss.com/Prospector-Kit-ZMK-dongle-with-full-color-LCD-screen/KC10254-STD) - The Prospector is a customisable status screen designed for wireless ZMK-based keyboards. It features a full-colour LCD screen and an ambient light sensor (not Eco variant).
* [keycapsss.com/Prospector Kit - ZMK dongle with full color LCD screen (ECO)](https://keycapsss.com/Prospector-Kit-ZMK-dongle-with-full-color-LCD-screen/KC10254-ECO) - NO Adafruit APDS9960 (Proximity, Light, RGB, and Gesture Sensor)
* [beekeeb.com/Pre-soldered Prospector - ZMK Dongle](https://shop.beekeeb.com/products/pre-soldered-prospector-zmk-dongle?variant=52494461600051) - NO Adafruit APDS9960 (Proximity, Light, RGB, and Gesture Sensor)
* [beekeeb.com/ZMK Dongle - Prospector DIY Kit](https://shop.beekeeb.com/products/zmk-wireless-dongle-prospector-diy-kit) - NO Adafruit APDS9960 (Proximity, Light, RGB, and Gesture Sensor)
* [ergohaven.xyz/Ergohaven's Qube](https://ergohaven.xyz/shop/tproduct/767895441-375223366762-ergohavens-qube) - This universal device is designed to be an essential companion for wireless keyboards. It works as a dongle and displays useful information and reduces your keyboard's energy consumption

#### Display Modules Hardware
* [OLED Display 128x32](https://keycapsss.com/0.91-OLED-LCD-Display-128x32-SSD1306-I2C/KC10048-BL) - 0.91 OLED LCD Display 128x32 SSD1306 I2C
* [OLED Display 128x64](https://keycapsss.com/0.96-OLED-LCD-Display-128x64-SSD1306-I2C/KC10129-BL) - 0.96 OLED LCD Display 128x64 SSD1306 I2C
* [nice!view](https://nicekeyboards.com/docs/nice-view/) - A sharp, low-power E-Ink display designed to be easily added to a nice!nano. SHARP MiP DISPLAYS, cutting edge Memory-in-Pixel technology - 30Hz at minmal power draw.
* [VISTA508 Low Power Display](https://keydio.shop/products/vista508-low-power-display) - The Vista508 is a MIPS display with excellent power consumption characteristics that is pin compatible with the very popular nice!view display.
* [Vista272 Low Power Display](https://keydio.shop/products/vista272) - The Vista272 is a drop in replacement for the nice!view display, it uses the exact same MIPS display module.
* [Halcyon TFT LCD Display](https://splitkb.com/products/halcyon-tft-lcd-display-module?_pos=2&_sid=89f88ba1c&_ss=r) - The Halcyon TFT LCD Display Module provides your Halcyon keyboard with a responsive and vibrant colour display

## Tools and Software

### Keymap Editors GUI

* [ZMK Studio - Official GUI Support (Online via USB)](https://zmk.studio/) - ZMK Studio provides runtime update functionality to ZMK powered devices, allowing users to change their keymap layers without flashing new firmware to their keyboards.
* [ZMK Studio (Offline via BLE)](https://github.com/zmkfirmware/zmk-studio/releases) - A desktop application that allows you to modify your keymap offline via Bluetooth.
* [nickcoutsos/keymap-editor](https://nickcoutsos.github.io/keymap-editor/) - A web based graphical editor of ZMK keymaps.
  * [nickcoutsos/keymap-editor](https://github.com/nickcoutsos/keymap-editor) -  source code on GitHub
  * [nickcoutsos/keymap-editor/wiki](https://github.com/nickcoutsos/keymap-editor/wiki) - keymap-editor wiki!
* [caksoylar/keymap-drawer](https://keymap-drawer.streamlit.app/) - Visualize keymaps that use advanced features like hold-taps and combos, with automatic parsing.
  * [caksoylar/keymap-drawer](https://github.com/caksoylar/keymap-drawer) - source code on GitHub
* [ZMK Firmware official hardware-integration/physical-layouts](https://zmk.dev/docs/development/hardware-integration/physical-layouts) - Physical Layouts
  * [zmk-physical-layout-converter by caksoylar](https://zmk-physical-layout-converter.streamlit.app/) - Web app for converting between physical layout formats for ZMK Studio [^11].
    * [caksoylar/zmk-physical-layout-converter](https://github.com/caksoylar/zmk-physical-layout-converter) - source code on GitHub
  * [keymap-layout-tools by nickcoutsos](https://nickcoutsos.github.io/keymap-layout-tools/) - Helper code for dealing with rendering keyboard layouts. [^11].
    * [nickcoutsos/keymap-layout-tools](https://github.com/nickcoutsos/keymap-layout-tools) - source code on GitHub
* [joelspadin/zmk-locale-generator](https://github.com/joelspadin/zmk-locale-generator) - Python module to generate localized keyboard layout headers for ZMK Firmware.
* [An experimental tool to create ZMK shields by Genteure](https://shield-wizard.genteure.workers.dev) - A web-based tool to create ZMK configurations for custom keyboards.
* [MrMarble/zmk-viewer](https://github.com/MrMarble/zmk-viewer) - cli tool to generate preview images from a zmk .keymap file

### Power Estimation

* [ZMK Power Profiler](https://zmk.dev/power-profiler) - An online tool to estimate your keyboard's power usage and battery life based on its components
* [Online Power Profiler for BLE](https://devzone.nordicsemi.com/power/w/opp/2/online-power-profiler-for-bluetooth-le) - The tool is based on a model of measured values, and is not showing the actual measurement [^5].
* [codyd51/Mighty-Mitts](https://github.com/codyd51/Mighty-Mitts) - macOS menu bar applet for battery levels of ZMK split keyboards
* [kot149/zmk-battery-center](https://github.com/kot149/zmk-battery-center) - A system tray app to monitor the battery level of ZMK-based keyboards for MacOS/Windows
* [Maksim-Isakau/zmk-split-battery](https://github.com/Maksim-Isakau/zmk-split-battery) ZMK Split Battery Status in system tray for Windows
* [mh4x0f/zmkBATx](https://github.com/mh4x0f/zmkBATx) - Opensource tool for peripheral battery monitoring zmk split keyboard over BLE for linux


### Display Utilities
* [LVGL Image Converter](https://lvgl.io/tools/imageconverter) - Convert BMP, JPG, PNG or SVG files to C arrays (or various binary formats) for use with LVGL.
* [javl/image2cpp](https://javl.github.io/image2cpp/) - image2cpp is a simple tool to change images into byte arrays (or arrays back into images) for use with (monochrome) displays such as OLEDs on your Arduino or Raspberry Pi.
* [joric/qle (QMK Logo Editor)](https://joric.github.io/qle/) - QMK Logo Editor is a lightweight web editor for creating and exporting small monochrome logos / glyphs for keyboard OLEDs.
* [notisrac/FileToCArray](https://notisrac.github.io/FileToCArray/) - Coverts any file to a C style array. (It can also do image color format and size coversion)


### RAW HID Host
* [zzeneg/qmk-hid-host](https://github.com/zzeneg/qmk-hid-host) - ZMK and QMK HID Host. Host component for communicating with ZMK and QMK keyboards using Raw HID feature.
* [badjeff/zmk-companion-macos](https://github.com/badjeff/zmk-companion-macos) - ZMK Companion. A main menu macOS application communicate to ZMK powered HID device.

### CLI and Utilities
* [zmkfirmware/zmk-cli](https://github.com/zmkfirmware/zmk-cli) - Command line tool for ZMK Firmware
* [zmkfirmware/zmk-docker](https://github.com/zmkfirmware/zmk-docker) - Lightweight Docker images for ZMK
* [urob/zmk-actions](https://github.com/urob/zmk-actions) - Github workflows for maintaining ZMK modules

## Community Pointing Projects as Computer Mouse
* [badjeff/leylabella-zmk-config](https://github.com/badjeff/leylabella-zmk-config) - This is the ZMK firmware config repository for [leylabella](https://github.com/badjeff/leylabella), a computer mouse 🐭.
* [badjeff/moudabella-zmk-config](https://github.com/badjeff/moudabella-zmk-config) - This is the ZMK firmware config repository for [moudabella](https://github.com/badjeff/moudabella), an open source bluetooth mouse 🐭 for CAD 🐱.

## Guides and Tutorials

### Solder and Desolder Tools
> NOTE
> These tools have been tested first -hand (Except for Parllel Clamping, I have a model very similar to that) and could say that they are essential (personal perspective) helped me and still help me repeatedly and they have validated every penny!
* [PINECIL – Smart Mini Portable Soldering Iron (Version 2)](https://pine64.com/product/pinecil-smart-mini-portable-soldering-iron/) - The Pinecil is a smart mini portable soldering iron with a 32-bit RISC-V SoC featuring a sleek design, auto standby and it heats up to an operating temperature in just 6 seconds!
* [Stannol Kristall 611 Fairtin Solder](https://keycapsss.com/accessories/229/stannol-kristall-611-fairtin-solder-lead-free-lead-free-sn99-3cu0-7-rem1-100g-0.5-mm) - Stannol Kristall 611 Fairtin Solder, lead-free Lead-free Sn99,3Cu0,7 REM1 100g 0.5 mm
* [flux paste](https://www.amazon.de/Flussmittel-Paste-flussmittel-l%C3%B6tflussmittel-Mechaniker-Bauelemente/dp/B0BQCHSQLB/ref=sr_1_3?brr=1&dib=eyJ2IjoiMSJ9.i5OJNeqPZsOWvTWOPhJfemcq5Vshx8bOfpCJvo6uHYeaUnEt59THLE2HTngdkTB0kjbNvZELXJhgKUJy4JlBEo9yrfwOefmYt4wOzco4nsFQ_Ix-K5YO4a-nP6tIzJ1dKX5az_weIXCalzWCMHaGoT0MreIIoBJWN7o8F7KgG9SAJwwzp-kgdFTWAuIR8dcTRO_G7AajTdJjWuZiPDkgBcbX9nSu2ME2bCNHZBr4344.SV-83bxaSj-1NyW18QdA39UbNKZxFD8JSyUCKXEizek&dib_tag=se&qid=1759839725&rd=1&s=diy&sr=1-3) - 1 piece of 10g of flux paste, soldering fat flux, soldering paste, soldering fluid, soldier paste, solder paste, for mechanics, metal, tin, telephone, PC cards, components
* [Liquiq flux no-clean](https://www.amazon.de/Flasche-Pinsel-L%C3%B6twasser-Weichl%C3%B6ten-Flussmittel/dp/B0C1C4S5BT/ref=sr_1_73?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dib=eyJ2IjoiMSJ9.wg0NoP9fb_OM2clfuWyenF-EWg_MTOOICkLDWaJI7xCmIIZl0t0y8HvM_FIxR9icffXTV0Byerp2-jmj373ERgL4S7pMtyUy1pEMV8JPNTvgIzcsNV5c5A-7oQNqVHAkTuYRlJ7dRXM3BRnQClWDgh7dp7XVGXfRSaGOHqTIywC-bAqKXPS9J-hAC5l16lmG.v_EGninoAXlVV0GqPDScXjWAgo4HKGNV9A9ErBMppRE&dib_tag=se&keywords=flux+no+clean+for+soldering&qid=1759839868&s=diy&sr=1-73&xpid=1eHgHndJ67fZa) - 50 ml bottle with brush soldering water soldering soft soldering river SMD BGA zinc
* [Desolder / solder SEQURE HT140 2-IN-1 Hot Tweezers](https://sequremall.com/products/sequre-ht140-2in1-hot-tweezers-soldering-iron-desoldering-repair-tool-for-smd?variant=44204748308668) - SEQURE HT140 2-IN-1 Hot Tweezers And Soldering Iron Compatible with C210 Soldering Tips And C120 Hot Tweezers Cartridge Tips Desoldering Tips Support PD QC DC Power Supply Desoldering Repair Tool for SMD
* [Desolder pump](https://de.aliexpress.com/item/1005005632540345.html?spm=a2g0o.order_list.order_list_main.329.49775c5fDIIQvQ&gatewayAdapt=glo2deu) - Tin-suction vacuum with 3-suction nozzle, EU/US plug, soldering, removal of the pump, electrical soldering device ADT03, new removal machine
* [Desolder / solder air pump](https://de.aliexpress.com/item/1005006284776301.html?spm=a2g0o.order_list.order_list_main.324.49775c5fDIIQvQ&gatewayAdapt=glo2deu) - Yihua micro hot air pistol C/F temp set 8858IV 700 W solder rework welding station LCD digital hot air pistol BGA IC soldering tools
* [Parallel Clamping](https://omnifixo.com/en-eu) - Firm grip that keeps components in place, large jaw opening (9/16", 14mm), no bitemarks or scratching, narrow and flat jaws, easy to find somewhere to hold
* [Precision Tweezers Set](https://www.ifixit.com/products/precision-tweezers-set) - Grab everything from screws to eyebrows with iFixit's Precision Tweezers Set.
* [Soldering Tip Cleaning Ball Hakko 599B](https://www.ifixit.com/products/soldering-tip-cleaning-ball-hakko-599b) - The HAKKO 599B cleans your soldering iron tips without water! The 599B is made from coils of brass, which is softer than the tip plating yet harder than the oxidation that forms on the tip.
* [Diagonal Cutters](https://www.adafruit.com/product/152) - Diagonal cutters, large super-comfortable grip to use and have strong nippers for perfect trimming of wires and leads

### How to Solder
* [Making a good solder joint](https://learn.adafruit.com/adafruit-guide-excellent-soldering/making-a-good-solder-joint) - by Bill Earl published September 06, 2012, last edited May 01, 2024 posted in Tools/ Hand Tools Tools/ Soldering
* [Surface Mount Components](https://learn.adafruit.com/adafruit-guide-excellent-soldering/surface-mount) - by Bill Earl published September 06, 2012, last edited May 01, 2024 posted in Tools/ Hand Tools Tools/ Soldering
* [Common Soldering Problems](https://learn.adafruit.com/adafruit-guide-excellent-soldering/common-problems) - by Bill Earl published September 06, 2012, last edited May 01, 2024 posted in Tools/ Hand Tools Tools/ Soldering
* [Tools](https://learn.adafruit.com/adafruit-guide-excellent-soldering/) - Personally I prefer the tools above "[Solder and Desolder Tools](#solder-and-desolder-tools)", but of course those are much cheaper!
* [How to Solder: Through-Hole Soldering](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering) - Soldering is one of the most fundamental skills needed to dabble in the world of electronics.
* [How to Test Diodes with a Digital Multimete](https://www.fluke.com/en-au/learn/blog/digital-multimeters/how-to-test-diodes) - Digital multimeters can test diodes using one of two methods

### How to Desolder
* [How To Solder and Desolder Connections](https://www.ifixit.com/Guide/How+To+Solder+and+Desolder+Connections/750) - While many repairs can be accomplished without soldering, there are times when it's necessary to replace soldered-down components, e.g., joysticks, headphone batteries, and rumble motors.
* [The Ultimate Guide to Desoldering](https://www.instructables.com/The-Ultimate-Guide-to-Desoldering/) - From using desoldering irons to sketchily knocking breadboard components off on the side of a table, there are tons of ways to remove components from a circuit board.

### Solder and Desolder Videos
* [mrsolderfix3996/youtube.com](https://www.youtube.com/@mrsolderfix3996) - My video's will be covering many aspects of soldering ,  ranging from the very basic stuff to the very extreme difficult projects, with the odd fun project to make popped in along the way
* [paceworldwide/youtube.com](https://www.youtube.com/@paceworldwide) - For over forty years, PACE, Inc. has provided state-of-the-art, hands-on solder training to the electronics industry around the world. Courses and support materials are available for Surface Mount Technology, Through-Hole Technology and Multilayer PCB Repairs.
* [How to solder and desolder SMD using hot air](https://www.youtube.com/watch?v=pIX3sGDs3CQ) - A quick and complete tutorial about surface mount components (SMD/SMT) soldering and desoldering using hot air station.

### Supported Hardware
> NOTE
> These are the most popular boards, [but there are more](https://zmk.dev/docs/hardware)

Wireless - Pro Micro Interconnect (nRF52840 and others)

* [nice!nano v2](https://nicekeyboards.com/nice-nano/) - Board: `nice_nano_v2`
* [nice!nano v1](https://nicekeyboards.com/nice-nano/) - Board: `nice_nano`
* [Puchi-BLE V1](https://keycapsss.com/keyboard-parts/mcu-controller/202/puchi-ble-wireless-microcontroller-pro-micro-replacement) - Board: `puchi_ble_v1`
* [SuperMini NRF54840](https://de.aliexpress.com/item/1005006035267231.html?gatewayAdapt=glo2deu) - Board: `nice_nano_v2`
* [Mikoto](https://github.com/zhiayang/mikoto) - Board: `mikoto`
* [Vikoto](https://fingerpunch.xyz/product/vikoto/) - Board: `vikoto`
* [nRFMicro 1.1/1.2](https://github.com/joric/nrfmicro) - Board: `nrfmicro_11`
* [nRFMicro 1.3/1.4](https://github.com/joric/nrfmicro) - Board: `nrfmicro_13`

Wired - Pro Micro Interconnect (RP2040 and others)
* [SparkFun Pro Micro RP2040](https://www.sparkfun.com/sparkfun-pro-micro-rp2040.html) - Board: `sparkfun_pro_micro_rp2040`
* [BoardSource blok RP2040](https://peg.software/docs/blok) - Board: `boardsource_blok`
* [Adafruit KB2040](https://www.adafruit.com/product/5302) - Board: `adafruit_kb2040`
* [QMK Proton-C](https://www.google.com/search?q=https://qmk.fm/proton-c/) - Board: `proton_c`
* [Svlinky](https://fingerpunch.xyz/product/svlinky/) - Board: `svlinky@0.2.0` and `svlinky@0.1.0`


Wireless - Seeed XIAO Interconnect (nRF52840 and others)
* [Seeed Studio XIAO nRF52840](https://www.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html) - Board: `seeeduino_xiao_ble`

Wired - Seeed XIAO Interconnect (RP2040 and others)
* [Adafruit QT Py RP2040](https://www.adafruit.com/product/4900) - Board: `adafruit_qt_py_rp2040`
* [Seeed Studio XIAO RP2040](https://www.seeedstudio.com/XIAO-RP2040-v1-0-p-5026.html) - Board: `seeeduino_xiao_rp2040`
* [Seeed Studio XIAO SAMD21](https://wiki.seeedstudio.com/Seeeduino-XIAO/) - Board: `seeeduino_xiao`
* [Xivik](https://fingerpunch.xyz/product/xivik/) - Board: `xivik@0.1.0`,`xivik@0.2.0` and `xivik@0.3.0`

### Hardware Tutorials
* [diimdeep/awesome-split-keyboards](https://github.com/diimdeep/awesome-split-keyboards) - A collection of ergonomic split keyboards
* [ebastler/zmk-designguide](https://github.com/ebastler/zmk-designguide) - A short hardware-designguide for ZMK keyboards.
* [Thumb cluster comfort from SplitKB made by jhelvy](https://compare.splitkb.com/) - Thumb cluster comfort is pretty individual based on hand size. You can use  scaled on a screen or printout to get an idea of how your hand fits different thumb clusters.
* [ebastler/zmk-designguide](https://github.com/ebastler/zmk-designguide) - A community-written guide for designing PCBs intended to be used with ZMK.
* [Compare Keycaps Profiles](https://www.keycaps.info/) - Support Choc and Cherry MX

### Software Tutorials
* [Maintaining a personal ZMK fork](https://gist.github.com/urob/68a1e206b2356a01b876ed02d3f542c7) - A cookbook approach to maintaining a personal ZMK fork.
* [mod-tap/mod-tap/homerow mods bible](https://precondition.github.io/home-row-mods) - behaviors bible
* [KeymapDB](https://keymapdb.com/) - KeymapDB (“Keymap Database”) is a public and open-source online database for keymaps of programmable keyboards, with a focus on ZMK / QMK ergonomic keyboards.

### Learn Touch Typing
* [Typeracer](https://play.typeracer.com/) - The award-winning online typing competition, TypeRacer, allows people to race each-other by typing quotes from books, movies, and songs. It is the first multiplayer typing game on the web.
* [Monkeytype](https://monkeytype.com/) - Monkeytype is a minimalistic and customizable typing test.
* [keybr](https://www.keybr.com/) - This web application will help you to learn touch typing which means typing through muscle memory without using your eyesight to find the keys. With multiplayer typing game on the web

## Keyboard News
* [kbd.news](https://kbd.news/) - KBD.news is a blog and newsletter on DIY mechanical keyboards. A hand-picked selection of posts from a keyboard enthusiast's perspective
* [ErgoMechKeyboards/reddit.com](https://www.reddit.com/r/ErgoMechKeyboards/) - A community focused around Ergonomic Mechanical Keyboards and strange input devices. Embrace the jank. Created Sep 2, 2019
* [crkbd/reddit.com](https://www.reddit.com/r/crkbd/) - crkbd, a.k.a. Corne Keyboard https://github.com/foostan/crkbd https://discord.com/invite/aWCZWnS Created Dec 16, 2019

<!-- ### Keyboard News ErgoMechKeyboards -->
<!-- REDDIT:START -->
<!-- REDDIT:END -->

## Keyboard Shops

* [mechanical keyboard vendors list](https://kbd.news/vendors) - Where to buy mechanical keyboards, switches or keycaps? This keyboard shop database lists 600+ stores offering keyboards, kits, various parts and accessories.

## Projects using ZMK closed-source or not upstreamed
* [Naya Keyboard](https://naya.tech/) - Fully modular hardware and endlessly customizable software engineered for effortless ergonomics and peak performance.
* [Keychron B1 Pro Ultra-Slim Wireless Keyboard](https://www.keychron.com/products/keychron-b1-pro-ultra-slim-wireless-keyboard) - Keychron B1 Pro is an ultra-slim wireless keyboard. It supports 2.4 GHz, Bluetooth, and a wired connection.
  * [Keychron source code on GitHub](https://github.com/Keychron/zmk/tree/keychron_bpro/app/boards/shields/keychron)
* [Advantage360 Professional](https://kinesis-ergo.com/shop/adv360pro/) - Our flagship fully-split contoured keyboard designed to provide maximum comfort and adjustability.
  * [Adv360-Pro-ZMK source code on GitHub](https://github.com/KinesisCorporation/Adv360-Pro-ZMK) - Production repository for the all-new Advantage360 Professional using ZMK engine
* [Disconnect MK1](https://www.hidergo.fi/) - The culmination of function, productivity and appearance. Disconnect MK1 is the ultimate keyboard for work and play.
  * [osmakari/zmk source code on GitHub](https://github.com/osmakari/zmk) - For the curious, we keep the firmware open source! You are free to hack away on the firmware and make it truly your own!
* [taichan1113/AdeptBLE](https://github.com/taichan1113/AdeptBLE) - This is alpha version of Ploopy Adept BLE modification.
  * [Post on reddit](https://www.reddit.com/r/Trackballs/comments/rtmeeq/a_portable_trackball_i_wanted_zmk_powered_some/)
  * [Video and photos](https://imgur.com/gallery/zmk-trackball-prototype-RhXke0e)

## Related projects

* [ssbb/awesome-zmk](https://github.com/ssbb/awesome-zmk) - curated list of ZMK drivers, behaviors, tools and guides.
* [iDoka/awesome-nRF5](https://github.com/iDoka/awesome-nRF5) - curated resources for nRF5 (libraries, examples, build helpers).
* [dotintent/awesome-ble](https://github.com/dotintent/awesome-ble) - general BLE resources (useful Nordic links included).
* [whoop-t/nice-shield-collection](https://github.com/whoop-t/nice-shield-collection) - A collection of links to nice!view shield designs

## License

This list is licensed under the [Creative Commons Zero v1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).

<p align="right">
  <a href="#top">⬆️  back to Table of Contents</a>
</p>

[^1]: ZMK Firmware official website: https://zmk.dev
[^2]: ZMK Firmware official code repository: https://github.com/zmkfirmware/zmk
[^3]: Zephyr Project official website: https://www.zephyrproject.org
[^4]: Zephyr Project Code Repository: https://github.com/zephyrproject-rtos/zephyr
[^5]: Online Power Profiler for Bluetooth LE: https://devzone.nordicsemi.com/power/w/opp
[^6]: Pete Johanson: https://petejohanson.dev/
[^7]: joric dongles wiki: https://github.com/joric/nrfmicro/wiki/Alternatives#dongles
[^11]: ZMK Firmware official physical layouts integration: We recommend the use of this tool for writing a physical layout or converting one from a QMK JSON definition. If your keyboard already has a physical layout defined for the use with KLE, we recommend using this other tool first to convert your existing layout into QMK JSON. The second tool can also import the position data from KiCAD, if said program was used to design the keyboard - https://zmk.dev/docs/development/hardware-integration/physical-layouts
[^12]: Hardware Integration: https://zmk.dev/docs/development/hardware-integration#what-is-a-shield
[^13]: Modules: https://zmk.dev/docs/features/modules
