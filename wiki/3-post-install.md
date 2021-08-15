# 3. Post-Install

Config Changes:

| Key              | Value | Description                                                                                  |
| ---------------- | ----- | -------------------------------------------------------------------------------------------- |
| HideAuxiliary    | True  | Set to true to hide auxiliary entries from the picker menu                                   |
| PollAppleHotKeys | True  | Enable modifier hotkey handling in the OpenCore picker                                       |
| ShowPicker       | False | Hide a simple picker to allow boot entry selection                                           |
| AppleDebug       | False | Enable writing the boot.efi debug log to the OpenCore log                                    |
| Target           | 3     | A bitmask (sum) of enabled logging targets                                                   |
| AuthRestart      | True  | Enable VirtualSMC-compatible authenticated restart                                           |
| AudioSupport     | True  | Activate audio support by connecting to a backend driver                                     |
| VolumeAmplifier  | 143   | Multiplication coefficient for system volume to raw volume linear translation from 0 to 1000 |

## 3.1. Mount `EFI Partition` of `OS` with `OpenCoreConfigurator` tool

## 3.2. Replace `OS EFI Partition/EFI/OC/config.plist` to `post-install/config.plist`

## 3.3. Enable FileVault

System Preferences > Security & Privacy > FileVault

## 3.4. Install Apps from `post-install/apps` (Optional)
