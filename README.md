# Vₘₐₓ ROM
### Tailor-made for the V30, based on LineageOS 22.2 (Android 15)
[How to install](#installation) | [Releases & changelogs](https://github.com/cLick1338/vmax/releases) | [Other info](#other-info)

<img width="160" alt="Lock screen, charging" src="https://github.com/user-attachments/assets/ca61662f-b832-40a1-8129-2be01487c4b0" /> <img width="160" alt="Quick settings, notification" src="https://github.com/user-attachments/assets/8f14efb9-a748-481d-8eb8-ec855534e858" /> <img width="160" alt="Quad DAC Panel" src="https://github.com/user-attachments/assets/d9121b8f-c73e-4a96-93f3-166565c53d57" /> <img width="160" alt="Gamma correction" src="https://github.com/user-attachments/assets/5424a308-ba5c-4016-8b6f-461cabd534c8" /> <img width="160" alt="Display settings" src="https://github.com/user-attachments/assets/3353b1a9-91b7-41a2-9c04-875fabe8a25e" />




**Quad DAC: Bit-perfect audio up to 352.8kHz/32-bit, 384kHz/24-bit & DSD128 (DoP)***
- Quad DAC QS tile and menu show the current status
- More reliable impedance detection & override modes
- Up to 50 volume steps with DVC support and AVC configuration
- Reduced noises and pops when mode switching + other bug fixes

**Display improvements:**
- Display panel gamma calibration: OLED "black crush" issue resolved
- Resolution switching (panel-level)
- Automatic color mangement with wide gamut and HDR support with SDR coexistence**
- Improved brightness ramp, lower minimum and HBM (high brightness mode)

**Improved smoothness & responsiveness with equal or better battery life; Slightly improved memory.**

And more:
- OTA updates with boot image updating optional
- Quick settings & brightness slider customization (System -> Status bar)
- 3 button navigation customization (size & color)
- Spoofing against custom ROM detection (System -> Spoofing)
- Better lockscreen charging info
- CRT screen off animation
- & Others

<sub> \* Requires compatible, properly configured players (most work). DSD/DoP requires special support (Contacted Poweramp dev and got DoP support in latest Poweramp beta; UAPP will not get support for now)</sub>

<sub> \** Wide gamut & HDR requires compatible apps. Chrome browsers may need certain flags. Recommend Youtube in browser for HDR, the app can lag more and have wrong tonemapping.</sub>

---
### Installation
TL;DR flash the recovery then the ROM

At the moment there's only been extensive testing on H930. Other variants work but do it at your own risk. Any feedback is always welcome

1. You need a V30 "joan" model with an unlocked bootloader and a computer with adb+fastboot
2. [Download the latest release](https://github.com/cLick1338/vmax/releases) on the computer
3. Back up everything important from your phone; To avoid FRP issues you should disable the screen lock and remove Google accounts
4. Reboot to fastboot/bootloader and fastboot flash recovery the recovery.img (can use LOS recovery but unattended OTA updates do not work with it)
5. Reboot to recovery, full wipe (only if you're coming from another ROM) then Apply update -> Apply from ADB -> adb sideload the ROM zip
6. Flash GApps if you need them. Recommend [Lite GApps](https://litegapps.github.io/) 15.0 - [Lite](https://sourceforge.net/projects/litegapps/files/litegapps/arm64/35/lite/2026-10-01/LiteGapps-arm64-15.0-20261001-official.zip/download) or [Core](https://sourceforge.net/projects/litegapps/files/litegapps/arm64/35/core/2026-10-01/LiteGapps-core-arm64-15.0-20261001-official.zip/download) package
7. Reboot and enjoy!
---
### Other info
- If you need root (besides the available adb root) only use methods that patch boot.img; Vmax has a custom kernel, using any other kernel will break features.
- Youtube uses VP9 Profile 2 for HDR which is SW-decode-only on SD835; Performance has been improved (in browsers) up to 720p60/1080p30 but there are still issues and SW decode has inherently high power usage. Use HEVC files for HW decoded HDR.
