# 2. Installer

### 2.1. Linux

#### 2.1.1. Download Big Sur Recovery

Enter dir `tmp/OpenCore/Utilities/macrecovery` and execute:

```sh
python ./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download
```

#### 2.1.2. Format Bootable Disk

Get Block:

```sh
sudo lsblk
```

Create Partition:

```sh
sudo gdisk /dev/Block

`o` # create a new empty GUID partition table (GPT)

`n` # add a new partition
    # partition number: keep blank for default
    # first sector:     keep blank for default
    # last sector:      keep blank for default
    # Hex code or GUID: 0700 for Microsoft basic data partition type

`w` # write table to disk and exit
```

```sh
sudo umount /dev/BlockX
sudo mkfs.vfat -F 32 -n "OPENCORE" /dev/BlockX
```

#### 2.1.2. Download Big Sur Recovery

Ender dir `OpenCore/Utilities/macrecovery` and execute:

```sh
python ./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download
```

#### 2.1.3. Copy `BaseSystem.dmg` and `BaseSystem.chunklist` to `boot/com.apple.recovery.boot` folder

#### 2.1.3. Copy all files from `boot` folder to EFI partition of `Bootable Disk`

### 2.2. MacOS

#### 2.2.1. Download Installer

```sh
mkdir -p ~/macOS-installer && cd ~/macOS-installer && curl https://raw.githubusercontent.com/munki/macadmin-scripts/main/installinstallmacos.py > installinstallmacos.py && sudo python installinstallmacos.py
```

#### 2.2.2. Format Bootable Disk

| Name     | Format                      |
| -------- | --------------------------- |
| OPENCORE | Mac OS Extended (Journaled) |

#### 2.2.3. Mount Installer

#### 2.2.4. Execute

```sh
sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/OPENCORE
```

#### 2.2.5. Mount EFI partition

#### 2.2.6. Copy `boot/EFI` folder to `/Volumes/OPENCORE`
