# Hackintosh Catalina Installation Guide for ASUS ROG STRIX Z390-I GAMING Motherboard

Perfect Vanilla Hackintosh with OpenCore bootloader like real mac.

OpenCore supports boot hotkeys, hold Option or ESC at startup to choose a boot device, Command+R to enter Recovery or Command+Option+P+R to reset NVRAM.

I used this guides as starting point:

https://github.com/khronokernel/Opencore-Vanilla-Desktop-Guide
https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Configuration.pdf

iMacPro1,1 SMBIOS + AMD GPU - DRM Workaround works best on Coffee Lake - Disabled iGPU in BIOS

## Hardware

![IMG_20191204_135309](images/hardware/IMG_20191204_135309.jpg)

![IMG_20191204_135408](images/hardware/IMG_20191204_135408.jpg)

![IMG_20191204_135454](images/hardware/IMG_20191204_135454.jpg)

![IMG_20191204_135634](images/hardware/IMG_20191204_135634.jpg)

![IMG_20191204_135652](images/hardware/IMG_20191204_135652.jpg)


- Gigabyte ASUS ROG STRIX Z390-I GAMING
- Intel Core i5-8500T
- 2 x Kingston HyperX Predator 8GB DDR4 3000MHz
- 1 x SAPPHIRE PULSE Radeon RX 570 ITX 4GB
- 1 x Samsung SSD 850 EVO 250GB
- 1 x Broadcom BCM94350ZAE/DW1820A M.2 WiFi/ac and BT4LE (replaced on the motherboard)
  - BCM4350 cards proved unreliable in terms of usage. Only some models work properly
  - BCM94352Z/DW1560 is better

![About My Mac](images/about.png)
![About My Mac Display](images/about-display.png)
![System Preferences Display](images/syspref-display.png)
![System Info GPU](images/systeminfo-gpu.png)
![System Info Bluetooth](images/systeminfo-bluetooth.png)
![System Info Ethernet](images/systeminfo-ethernet.png)
![System Info PCI](images/systeminfo-pci.png)
![System Info Wi-Fi](images/systeminfo-wifi.png)
![System Info USB](images/systeminfo-usb.png)

## Everything Works

- Sleep / Wake
- Power Nap (sleep with background operations such as Time Machine)
- Audio (select internal speakers)
- Ethernet
- Bluetooth (lag when Wi-Fi is on)
- Wi-Fi
- 15 USB port

## USBMap

Selected 15 XHC port

| Ports | Type | Description |
| --- | --- | --- |
| HS02 | USB 2 Type C connector | Rear USB Type-C |
| HS03 | USB 3 Standard-A connector | Rear USB 3.1 Gen 2 (red) |
| HS04 | USB 3 Standard-A connector | Rear USB 3.1 Gen 2 (red) |
| HS05 | USB 2 Type A connector | Rear USB 2.0 (black) |
| HS06 | USB 2 Type A connector | Rear USB 2.0 (black) |
| HS07 | USB 3 Standard-A connector | Rear USB 3.1 Gen 1 (blue) |
| HS08 | USB 3 Standard-A connector | Rear USB 3.1 Gen 1 (blue) |
| HS09 | USB 3 Standard-A connector | Front USB 3.1 Gen 1 |
| HS10 | USB 3 Standard-A connector | Front USB 3.1 Gen 1 |
| HS13 | Internal connector | RGB LED Lighting - AURA MOTHERBOARD |
| HS14 | Internal connector | Bluetooth/Wifi - BCM2045A0 |
| SS03 | USB 3 Standard-A connector | Rear USB 3.1 Gen 2 (red) |
| SS04 | USB 3 Standard-A connector | Rear USB 3.1 Gen 2 (red) |
| SS09 | USB 3 Standard-A connector | Front USB 3.1 Gen 1 |
| SS10 | USB 3 Standard-A connector | Front USB 3.1 Gen 1 |

## Bios settings

![191204130256](images/bios/191204130256.jpg)

![191204130313](images/bios/191204130313.jpg)

![191204130321](images/bios/191204130321.jpg)

![191204130355](images/bios/191204130355.jpg)

![191204130418](images/bios/191204130418.jpg)

![191204130533](images/bios/191204130533.jpg)

![191204130545](images/bios/191204130545.jpg)

![191204130552](images/bios/191204130552.jpg)

![191204130556](images/bios/191204130556.jpg)

![191204130604](images/bios/191204130604.jpg)

![191204130608](images/bios/191204130608.jpg)

![191204130612](images/bios/191204130612.jpg)

![191204130617](images/bios/191204130617.jpg)

![191204130625](images/bios/191204130625.jpg)

![191204130628](images/bios/191204130628.jpg)

![191204130636](images/bios/191204130636.jpg)

![191204130649](images/bios/191204130649.jpg)

![191204130657](images/bios/191204130657.jpg)

![191204130700](images/bios/191204130700.jpg)

![191204130718](images/bios/191204130718.jpg)

![191204130720](images/bios/191204130720.jpg)

![191204130727](images/bios/191204130727.jpg)

![191204130741](images/bios/191204130741.jpg)

![191204130758](images/bios/191204130758.jpg)

![191204130829](images/bios/191204130829.jpg)

![191204130835](images/bios/191204130835.jpg)

![191204130844](images/bios/191204130844.jpg)

![191204130849](images/bios/191204130849.jpg)

![191204130853](images/bios/191204130853.jpg)

![191204130928](images/bios/191204130928.jpg)
