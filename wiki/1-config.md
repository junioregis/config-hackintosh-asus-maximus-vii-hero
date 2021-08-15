# 1. Config

## 1.1. Generate SMBIOS

Use `GenSMBIOS` tool for this.

## 1.2. Config

For all settings not listed, keep default.

### 1.2.1. ACPI

- SSDT-EC-DESKTOP
- SSDT-PLUG-DRTNIA

### 1.2.2. DeviceProperties

**PciRoot(0x0)/Pci(0x1b,0x0)**:

| Key                        | Value  |
| -------------------------- | ------ |
| PciRoot(0x0)/Pci(0x1b,0x0) | 0x0C0C |

**PciRoot(0x0)/Pci(0x2,0x0)**:

| Key                     | Value    |
| ----------------------- | -------- |
| AAPL,ig-platform-id     | 0300220D |
| device-id               | 12040000 |
| ramebuffer-patch-enable | 01000000 |
| framebuffer-stolenmem   | 00003001 |
| framebuffer-fbmem       | 00009000 |

| AAPL,ig-platform-id | Description                                                                                     |
| ------------------- | ----------------------------------------------------------------------------------------------- |
| 0300220D            | Used when the Desktop Haswell iGPU is used to drive a display                                   |
| 04001204            | Used when the Desktop Haswell iGPU is only used for computing tasks and doesn't drive a display |

### 1.2.3. Kernel

#### 1.2.3.1. Add

> _Yes, kext order matters :)_

| Position | Kext             |
| -------- | ---------------- |
| 1        | Lilu             |
| 2        | VirtualSMC       |
| 3        | AppleALC         |
| 4        | IntelMausi       |
| 5        | NVMeFix          |
| 6        | SMCLightSensor   |
| 7        | SMCProcessor     |
| 8        | SMCSuperIO       |
| 9        | WhateverGreen    |
| 10       | HibernationFixup |
| 11       | CPUFriend        |

#### 1.2.3.2. Quirks

| Key                     | Value |
| ----------------------- | ----- |
| AppleCpuPmCfgLock       | False |
| AppleXcpmCfgLock        | True  |
| CustomSMBIOSGuid        | False |
| DisableIoMapper         | True  |
| LapicKernelPanic        | False |
| PanicNoKextDump         | True  |
| PowerTimeoutKernelPanic | True  |
| XhciPortLimit           | True  |

### 1.2.4. Misc

| Node     | Key             | Value    |
| -------- | --------------- | -------- |
| Debug    | AppleDebug      | True     |
| Debug    | ApplePanic      | True     |
| Debug    | DisableWatchDog | True     |
| Debug    | Target          | 67       |
| Security | AllowNvramReset | True     |
| Security | AllowSetDefault | True     |
| Security | ScanPolicy      | 0        |
| Security | SecureBootModel | Default  |
| Security | Vault           | Optional |

### 1.2.5. NVRAM

| Key               | Value                             |
| ----------------- | --------------------------------- |
| boot-args         | -v keepsyms=1 debug=0x100 alcid=1 |
| csr-active-config | 00000000                          |

**System Integrity Protection (SIP)**:

| Value    | Description                                                                                                     |
| -------- | --------------------------------------------------------------------------------------------------------------- |
| 00000000 | SIP completely enabled (0x0)                                                                                    |
| 03000000 | Disable kext signing (0x1) and filesystem protections (0x2)                                                     |
| FF0F0000 | Disable all flags in macOS Big Sur (0xfff) which has another new flag for authenticated root (opens new window) |

### 1.2.6. PlatformInfo

| GenSMBIOS    | config.plist       |
| ------------ | ------------------ |
| Type         | SystemProductName  |
| Serial       | SystemSerialNumber |
| Board Serial | MLB                |
| SmUUID       | SystemUUID         |
| Apple ROM    | MAC Address        |

| ROM      | Description                             |
| -------- | --------------------------------------- |
| iMac14,4 | Haswell with only iGPU (integrated GPU) |
| iMac15,1 | Haswell with dGPU (dedicated GPU)       |

| Type     | Serial | Board Serial | SmUUID | Apple ROM |
| -------- | ------ | ------------ | ------ | --------- |
| iMac14,4 | -      | -            | -      | -         |
| iMac15,1 | -      | -            | -      | -         |

### 1.2.7. UEFI

#### 1.2.7.1. Drivers

- AudioDxe.efi
- HfsPlus.efi
- OpenCanopy.efi
- OpenRuntime.efi

#### 1.2.7.2. Quirks

| Key                    | Value |
| ---------------------- | ----- |
| IgnoreInvalidFlexRatio | True  |
