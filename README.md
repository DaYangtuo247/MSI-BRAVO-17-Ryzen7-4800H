# macOS on Msi-bravo-17 - Ryzen 4800H

## Specifications

| Item                 | Info                              |
| -------------------- | --------------------------------- |
| Model                | MSI BRAVO 17                      |
| CPU                  | AMD Ryzen™ 7 4800H Processor IGPU |
| DGPU                 | AMD Radeon RX 5500M Disabled      |
| RAM                  | 2x 8GB  DDR4 3200 MHz             |
| NVMe                 | WD_BLACK SN750 1TB                |
| WIFI                 | Intel® Wi-Fi 6E AX200             |
| Bluetooth            | With Intel wifi combo card        |
| Ethernet             | Realtek RTL8111                   |
| Audio                | Realtek ALC235                    |
| LCD Panel            | 17.2 FHD IPS 144Hz                |
| Opencore Version     | 0.9.8                             |
| SMBIOS used          | MacBookPro16,3                    |
| Target MacOS Version | MacOS Sonoma 14.3                 |

## What's Working

| Item            | Status | Notes                                                        |
| --------------- | ------ | ------------------------------------------------------------ |
| CPU             | ✅      | AMD Vanilla Kernel Patches ([Modify according to yours Core Count](https://github.com/AMD-OSX/AMD_Vanilla)) |
| HDMI A/V out    | ✅      |                                                              |
| USB             | ✅      | All ports working with USBToolBox.kext                       |
| Keyboard        | ✅      | Voodoops2controller Kext + Karabiner-Elements app for mapping |
| Audio           | ✅      | AppleALC kext working with layout-id 3                       |
| Trackpad        | ✅      | VoodooI2C                                                    |
| Ethernet        | ✅      | RealtekRTL8111 Kext                                          |
| Intel WIFI      | ✅      | AirportItlwm Kext                                            |
| Bluetooth       | ✅      | Internal Intel combo card with IntelBluetoothFirmware.kext + BlueToolFixup Kext |
| Battery         | ✅      | SMCBatteryManager.kext + SMCDellSensors.kext + ECEnabler.kext |
| AppleTV+ DRM    | ✅      | Work with CFG_LINK_FIXED_MAP=1                               |
| iServices       | ✅      | Message/Facetime tested and working                          |
| Shutdown/Reboot | ✅      |                                                              |

## What's not Working

* unknow

## BIOS option
* Secure Boot **Disabled**

* [Optional] 

  * `ADVANCED` -> `AMD CBS` -> `NBIO Common Options` -> `GFX Configuration` -> `iGPU Configuration` -> `UMA_SPECIFIED`

    > [!NOTE]
    >
    > do not select igpu disable, Otherwise, the computer will not be able to boot and you will need to disassemble it and remove the bios battery.

  * `ADVANCED `-> `AMD CBS` -> `NBIO Common Options` -> `GFX Configuration` -> `UMA Frame buffer Size` -> `set > 512MB`

