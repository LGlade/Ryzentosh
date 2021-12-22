# OpenCore (OC 0.7.5) EFI for AMD Ryzen 3 1300x or similar Ryzen Chips (macOS 10.13 - High Sierra Only | Nvidia GTX 1050ti
## Hardware
| **Component** | **Model** |
| ------------- | --------- |
| CPU | AMD Ryzen 3 1300x @ 3.5GHz |
| Motherboard | MSI B350M Gaming Pro | 
| RAM | 12GB (1 x 8gb, 1x 4gb) Corsair Vengeance DDR4 - 3200MHz|
| GPU | Nvidia GTX 1050ti |
| DISK | SK Hynix 500gb SSD |

**macOS v.** 10.13.6  
**OpenCore version**: 0.7.5

## Instructions
  1. Make your USB installer with (https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) either from macOS or Windows. The MacOS way is recommended with the use    of a real Mac or a virtualized mac via VirtualBox since network kexts don't always work.
  2. Copy the EFI and paste in at the root of the EFI of the formatted USB, if there is anything there delete it. You can mount the EFI either from Mac (mountefi) or Windows (Minitool Patition Wizard>Change letter>Apply).
  4. Download [**GenSMBIOS**](https://github.com/corpnewt/GenSMBIOS) to generate unique SMBIOS information and ensure you have the right type of mac for your hardware and input it into the software.
  5. Open config.plist with [**ProperTree**](https://github.com/corpnewt/ProperTree) and go to PlatformInfo > Generic. Set MLB (Board Serial), SystemSerialNumber (Serial) and SystemUUID (SmUUID) and input their respective values. Change ROM to your network card's MAC or physical address without the `:` characters. You can find out this information by running (ipconfig /all) on Windows.
  6. Boot from it and ensure you have the correct UEFI or BIOS configurations.

## All rights go to their respective owners:
**Software:**
 - [[Bootloader] OpenCore](https://github.com/acidanthera/OpenCorePkg)
 - [[Patch] AMD_Vanilla](https://github.com/AMD-OSX/AMD_Vanilla)
 - [[SSDT] EC-USBX-DESKTOP](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-EC-USBX-DESKTOP.aml)
 - [[Driver] OpenRuntime](https://github.com/acidanthera/OpenCorePkg)
 - [[Driver] HFSPlus](https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi)
 - [[Kext] Lilu](https://github.com/acidanthera/Lilu)
 - [[Kext] VirtualSMC](https://github.com/acidanthera/VirtualSMC)
 - [[Kext] WhateverGreen](https://github.com/acidanthera/WhateverGreen)
 - [[Kext] AMDRyzenCPUPowerManagement](https://github.com/trulyspinach/SMCAMDProcessor)
 - [[Kext] AppleMCEReporterDisabler](https://github.com/AMD-OSX/AMD_Vanilla/blob/experimental-opencore/Extra/AppleMCEReporterDisabler.kext.zip)

 **People:**
 - [Apple](https://apple.com) for macOS
 - [AMD-OSX Developers](https://github.com/AMD-OSX) for kernel patches for AMD CPUs
 - [Acidanthera](https://github.com/acidanthera) for OpenCore and most of used kexts
 - [Trulyspinach](https://github.com/trulyspinach) for Ryzen power management and monitoring kexts
 - [Dortania](https://github.com/dortania) for OpenCore configuration guides
<br>
