# [Hackintosh] OMEN_by_HP_Laptop_15-ce0xx
<p><center>EFI源自<a href="https://github.com/t-shao">t-shao</a></center></p>

## EFI改进
- 修复屏闪、裂屏
- 修复国产暗影精灵3的有线网卡驱动
- 注入序列号，使appleID正常登入

EFI bootloader (OpenCore) configuration for OMEN by HP Laptop 15-ce0xx


OpenCore 版本: 0.6.7

## 配置
| 产品名称暗影精灵3 | OMEN by HP Laptop 15-ce0xx                |
| ----------------- | ----------------------------------------- |
| BIOS              | F.20 / F.19                               |
| 处理器            | Intel(R) Core(TM) i5-7300HQ / i7-7700HQ   |
| 独立显卡          | NVIDIA GeForce GTX 1050ti                 |
| 显卡              | Intel(R) HD Graphics 630                  |
| 声卡              | Realtek ALC295                            |
| 硬盘              | HP SSD KIOXIA 512G、WD 500G               |
| 网卡              | Realtek RTL8111                           |

(*) 兼容以上配置

## Progress
### System Support
- Windows 10 and up to macOS Big Sur 11.2.3 (my current setup)
- Others are not tested, feedback is welcome.

### Hardware Functionality
#### Power Management
- Working
    - battery status, charge, and discharge
    - sleep and wake (including PowerNap, sleep when lid close on battery, and wake by peripherals on AC)
    - CPU PM (to be further tested)
- Not working
    - you tell me

#### Display
- Working
    - internal display and brightness adjustment (by System Preferences or hotkeys)
    - external display through USB-C port
    - HiDPI by scripts
- Nor working
    - discrete GPU
    - digital audio of external display

#### Audio
- Working
    - analog audio including speaker, headphones, and internal microphone array
    - digital audio through USB-C port
- Not working
    - external microphone (not tested)

#### Network
- Working
    - wired Ethernet
    - USB network tethering
    - Intel WiFi and BT (quite stable, currently support system wifi management interface and partial Continuity features including Handoff and Universal Clipboard)
- Not working
    - stock Realtek wireless network and bluetooth adapter

#### I/O
- Working
    - USB ports (including Type-C)
    - touchpad (support multi-finger gestures and ForceTouch simulation, need some changes in the kext config)
    - card reader? (not tested)
- Not working
    - miniDP, HDMI ports (via dGPU)

## Instructions
1. Disable the CFG Lock of the motherboard (see guide in directory 'Disable_CFG_Lock')
2. Copy (replace) 'BOOT' and 'OC' under 'EFI' directory of this repo into the 'EFI' directory of your ESP (EFI) partition.
3. Adjust the kexts and OpenCore config file depending on your hardware configuration.

## Notes
- Be free to use and tweak the configuration, but it's *at your own risk*. **Not recommended for production environment.**
- Recommended to update the BIOS and ME to the latest version.
- When encountering battery malfunction, try to press and hold the power button for 20 seconds when powered off with all peripherals and power cord disconnected.

## Acknowlegement
- [Acidanthera](https://github.com/acidanthera) for maintaining [OpenCore](https://github.com/acidanthera/OpenCorePkg) and many essential kexts.
- [daliansky](https://github.com/daliansky) for [macOS installation images, tutorials](https://blog.daliansky.net/), and the [ACPI hotpatches](https://github.com/daliansky/OC-little).
- [shimakazechan](https://github.com/shimakazechan) for the [OpenCore configuration](https://github.com/shimakazechan/OMEN-by-HP-3-Hackintosh) of the same model for reference.
- 794767404 from PCbeta for the [partial solution](http://bbs.pcbeta.com/viewthread-1702113-1-1.html) to the battery problem of HP OMEN series.
- [zxystd](https://github.com/zxystd) for Intel [wifi](https://github.com/zxystd/itlwm) and [bt](https://github.com/zxystd/IntelBluetoothFirmware) driver.
