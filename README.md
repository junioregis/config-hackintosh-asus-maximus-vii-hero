# Hardware Info

| Component          | Model                                     |
| ------------------ | ----------------------------------------- |
| Motherboard        | ASUS Maximus VII Hero                     |
| BIOS Version       | 3503-BETA                                 |
| CPU                | Intel Core i7-4790k 4.40ghz 8mb           |
| CPU Socket         | LGA1150                                   |
| CPU Arch           | Haswell                                   |
| CPU Device Id      | 0x412                                     |
| CPU Thermal Grease | Cooler Master MasterGel Maker             |
| RAM                | Kingston HyperX Savage 2x8GB DDR3 2400MHz |
| Video              | HD Intel 4600                             |
| Audio Codec        | Realtek ALC1150                           |
| Network            | Intel Gigabit Ethernet I218-V             |
| OS Disk            | SSD Adata XPG GAMMIX S11 Pro 256GB        |
| Bootable Disk      | Kingston DataTraveler 100G3 32Gb          |
| PSU                | Corsair ATX RM850                         |

# BIOS Settings

Set `Load Optmized Defaults` and change config bellow:

| Key                                     | Value        |
| --------------------------------------- | ------------ |
| CFG Lock                                | Disabled     |
| CPU Graphics Memory                     | 512MB        |
| EHCI Hand-off                           | Enabled      |
| Execute Disable Bit                     | Enabled      |
| Fast Boot                               | Enabled      |
| Hyper-Threading                         | Enabled      |
| Intel Rapid Smart Technology            | Enabled      |
| Intel Virtualization Technology         | Enabled      |
| Intel xHCI Mode                         | Enabled      |
| Launch CSM                              | Enabled      |
| Legacy USB Support                      | Enabled      |
| Network Stack                           | Disabled     |
| OS Type                                 | Other OS     |
| PCI Express X4_3 Slot (Black) Bandwidth | M.2 Mode     |
| Primary Display                         | CPU Graphics |
| SATA Mode Selection                     | AHCI         |
| VT-d                                    | Disabled     |

# Tools

| Name                                                               | Version  |
| ------------------------------------------------------------------ | -------- |
| [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)                 | Master   |
| [GFXUtil](https://github.com/acidanthera/gfxutil/releases)         | 1.81b    |
| [Hackintool](https://github.com/headkaze/Hackintool/releases)      | 3.6.2    |
| OpenCoreConfigurator                                               | 2.48.0.0 |
| [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg/releases) | 0.7.2    |
| [ProperTree](https://github.com/corpnewt/ProperTree)               | Master   |

# ACPI

| Name                                                                                                                                     | Description                                       |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| [SSDT-EC-DESKTOP](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-EC-DESKTOP.aml?raw=true)   | Allows for native CPU power management on Haswell |
| [SSDT-PLUG-DRTNIA](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PLUG-DRTNIA.aml?raw=true) | Fixes the embedded controller                     |

# Kexts

| Name                                                                         | Version |
| ---------------------------------------------------------------------------- | ------- |
| [AppleALC](https://github.com/acidanthera/AppleALC/releases)                 | 1.6.3   |
| [CPUFriend](https://github.com/acidanthera/CPUFriend/releases)               | 1.2.4   |
| [HibernationFixup](https://github.com/acidanthera/HibernationFixup/releases) | 1.4.2   |
| [IntelMausi](https://github.com/acidanthera/IntelMausi/releases)             | 1.0.7   |
| [Lilu](https://github.com/acidanthera/Lilu/releases)                         | 1.5.5   |
| [NVMeFix](https://github.com/acidanthera/NVMeFix/releases)                   | 1.0.9   |
| [SMCLightSensor](https://github.com/acidanthera/virtualsmc/releases)         | 1.2.6   |
| [SMCProcessor](https://github.com/acidanthera/virtualsmc/releases)           | 1.2.6   |
| [SMCSuperIO](https://github.com/acidanthera/virtualsmc/releases)             | 1.2.6   |
| [VirtualSMC](https://github.com/acidanthera/virtualsmc/releases)             | 1.2.6   |
| [WhateverGreen](https://github.com/acidanthera/whatevergreen/releases)       | 1.5.2   |

# Drivers

| Name                                                                                            | Description                                                                                      | Version |
| ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ------- |
| [AudioDxe](https://github.com/acidanthera/AppleSupportPkg/releases)                             | HDA audio support driver in UEFI firmware for most Intel and some other analog audio controllers | 2.1.7   |
| [HfsPlus](https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi?raw=true) | Filesystem driver for HFS+                                                                       | 0.7.2   |
| [OpenCanopy](https://github.com/acidanthera/OpenCorePkg/releases)                               | OpenCore plugin implementing graphical interface                                                 | 0.7.2   |
| [OpenRuntime](https://github.com/acidanthera/OpenCorePkg/releases)                              | OpenCore plugin implementing OC_FIRMWARE_RUNTIME protocol                                        | 0.7.2   |

# Apps

| Name                                               | Description                                                             | Version |
| -------------------------------------------------- | ----------------------------------------------------------------------- | ------- |
| [Rectangle](https://rectangleapp.com)              | Move and resize windows in macOS using keyboard shortcuts or snap areas | 0.48    |
| [Stats](https://github.com/exelban/stats/releases) | MacOS system monitor in your menu bar                                   | 2.6.3   |

# Credits

[OpenCore-Install-Guide](https://dortania.github.io/OpenCore-Install-Guide/config.plist/haswell.html)

[OpenCore-Post-Install](https://github.com/dortania/OpenCore-Post-Install)

[Dicas do Mateus](https://youtu.be/5kUQ4_juA5w)

[Gabriel Luchina](https://www.youtube.com/watch?v=vaUy_2hFbso)

[Chris Titus Tech](https://www.youtube.com/watch?v=eUnVzJsINCI)

# Manuals

[OpenCore Reference Manual](https://dortania.github.io/docs/latest/Configuration.html)

[ASUS Maximus VII Hero](./manual/MAXIMUS_VII_HERO_V2.pdf)

# Wiki

1. [Config](./wiki/1-config.md)
2. [Installer](./wiki/2-installer.md)
3. [Post Install](./wiki/3-post-install.md)
4. [Screenshots](./wiki/4-screenshots.md)
