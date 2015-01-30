# wiiesc-oneshot125
This is a fork from google code with additional code that detects oneshot125 signal and converts the PWM input to normal PWM range.


#Original Documentation from Google Code

About
This firmware designed as a replacement for many commercially available ESC designs based on the AVR MCU. It implements scalar sensor less method to drive Brushless Motor by detecting BEMF zero-crossing instants. The goal of this project is to create firmware most suitable to use in multi-rotors, using cheap and commercially available hardware.

Features:
Fastest possible power response.
Up to 4000 steps of resolution.
Low noise with comparatively high efficiency (Sigma-delta modulator, instead of fixed frequency PWM)
Linear power response. (completely no "bump" at 100%)
Jitter-free input PWM measurement without harware assisted input capture.
Accepts any PWM update rate
Sync recovery.
Safe stall detection.
Complimentary PWM support (AKA: active freewheeling, active rectification)
Fixed throttle end-points. No need to calibrate. (since version 2.0.9 it is also possible to calibrate end-points using stick programming procedure)
Automatic oscillator calibration.
Enhanced PPM filter, preventing accidental motor startup (when FC is rebooted, for example)
Configurable. The configuration parameters are stored in EEPROM. The Wii-ESC flash tool has visual parameters editor. No more stick programming.
Modularity. The high-level implementation is separated from actual hardware with HAL layer.
Portability. The firmware is written in C++, which means it can be easilly ported to different platform.
Supported Hardware:
For complete mapping betwen targets and real hardware, it is possible to use RapidESC Database. Currently tested targets:

bs.hex
bs_nfet.hex
bs40a.hex
kda.hex
qynx.hex
rb50a.hex
rct30nfs.hex
rct45nfs.hex
tgy.hex
tp.hex
tp_nfet.hex
Latest releases:
Firmware: 2.1.1 
Flash Tool: 0.7 
ESC reflashing procedure:
Project Wiki
RCGroups Thread
{goblin} blog (Russian)
For simplified firmware update, it is possible to use the following tools:

KKmulticopter Flash Tool - it supports both Wii-ESC and RapidESC. This tool downloads latest revision of firmware directly from SVN
Wii-ESC Flash Tool. Simple small and portable flash tool for Win32. It also downloads latest revision from SVN and features visual EEPROM parameters editor.
