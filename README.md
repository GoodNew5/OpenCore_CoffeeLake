<!-- @format -->

# Hackintosh documentation

SUPPORT: https://discord.com/invite/2QYd7ZT

**MOTHERBOARD:**
BRAND: Gigabyte Technology Co. Ltd.
MODEL: Z390 AORUS MASTER-CF
BUS SPECS: PCI-Express 3.0 (8.0 GT/s)

**CPU:**
NAME: Intel Core i7 9700K
ARCH: Coffee Lake
SOCKET: 1151 LGA
INTERNAL GRAPHICS CARD: UHD 630

**NETWORK:**
MAC address: B4:2E:99:FB:0B:B1
NIC: Intel(R) Ethernet Connection (7) 1219-V

**iService:**
Type: iMac19,1
Serial: C02C10FKJV3Q
Board Serial: C02953310QXLNV9JC
SmUUID: BAB10EE3-7D31-436F-B636-641F22E0E132
Apple ROM: C42C0358819B

### BIOS SETTINGS

[RECOMMENDED SETTINGS](https://dortania.github.io/OpenCore-Install-Guide/config.plist/coffee-lake.html#intel-bios-settings)

DEFAULT OVERRIDES....

**#Disable**
Fast Boot
Secure Boot
Serial/COM Port
Parallel Port
Compatibility Support Module (CSM)
Thunderbolt (For initial install, as Thunderbolt can cause issues if not setup correctly)
Intel SGX
Intel Platform Trust
CFG Lock

**#Enable**
VT-d
Above 4G Decoding
Hyper-Threading
Execute Disable Bit
EHCI/XHCI Hand-off
OS type: Windows 8.1/10 UEFI Mode (some motherboards may require "Other OS" instead)
DVMT Pre-Allocated (iGPU Memory): 64MB or higher (для того чтобы в BIOS появилась настройка нужно откатить к оптимальным настройкам load optimized defaults после это перезагрузится и сделать internal graphic = enabled, перегрузиться и воуля)
SATA Mode: AHCI

### TOOLS

Для работы с конфигом
https://github.com/corpnewt/ProperTree

Для генерации SMBIOS
https://github.com/corpnewt/GenSMBIOS

Для сопоставления USB на Mac
https://github.com/corpnewt/USBMap

Для сопоставления на Windows (Лучший вариант)
https://github.com/USBToolBox/tool

Hackintool
https://github.com/benbaker76/Hackintool

IORegistryExplorer
https://github.com/khronokernel/IORegistryClone/blob/master/ioreg-302.zip

### KEXTS

SOUND
https://github.com/acidanthera/AppleALC

- AppleALC.kext

BLUETOOTH
https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases

- IntelBluetoothFirmware.kext
- IntelBTPatcher.kext

WIFI
https://github.com/OpenIntelWireless/itlwm/releases/tag/v2.2.0

- itlwm.kext

SENSORS
https://github.com/Acidanthera/VirtualSMC/releases/tag/1.3.2

- ReadeonSensor.kext
- SMCRadeonGPU.kext
- SMCProcessor.kext
- SMCSuperIO.kext

### APPLICATIONS

TEMPERATURE dGPU
https://github.com/ChefKissInc/RadeonSensor

INTRFACE WIFI
https://github.com/OpenIntelWireless/HeliPort/releases
