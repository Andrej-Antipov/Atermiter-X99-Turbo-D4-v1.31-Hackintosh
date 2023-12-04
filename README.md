# Atermiter-X99-Turbo-D4-v1.31-Hackintosh
OpenCore EFI for install MacOS Ventura

## PC configuration
| Component | Name |
| - | - |
| Motherboard | Atermiter X99 Turbo D4 |
| CPU | Intel Xeon E5-2630v3 |
| RAM | Desktop DDR4 2666 MHz |
| GPU | Sapphire RX580 8Gb Pulse | 
| Storage (NVMe) | Netac NV7000 |
| Storage (SATA) | 2 x 1Tb Fanxiang s101 |
| Wi-Fi + BT | Broadcom BCM923602CS |

## Bugs
* Very light sleep depth (Motherboard problem)

## Working
* CPU
* GPU
* iServices
* Wi-Fi
* Bluetooth
* NVMe
* SATA disks
* All USB ports
* Sleep (only S1)
* FileVault2
  

## Installation
* BIOS: XHCI mode -> Smart Auto
* BIOS: CSM disabled
* **Set your own SMBIOS serial numbers in config.plist**

If you want VoodooHDA.kext instead of AppleAlc, the kext from addons have to be copied to /Library/Extensions folder with command:
sudo cp -R /Path to/VoodooHDA.kext /Library/Extensions/ ; sudo chown -R root:wheel /Library/Extensions/VoodooHDA.kext ; sudo chmod -R 755  /Library/Extensions/VoodooHDA.kext
Confirm in the system settings load the extensions.
Disable AppleAlc kext and enable AppleHDADisabler.kext in OpenCore config.plist


To improve CPU performance use PMDrvr.kext driver from addons, set it up with WakeUpSCr applet.
Confirm in the system settings
