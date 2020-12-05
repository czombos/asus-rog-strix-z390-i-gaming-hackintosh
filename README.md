# Hackintosh Catalina Installation Guide for ASUS ROG STRIX Z390-I GAMING Motherboard

Perfect Vanilla Hackintosh with OpenCore bootloader like real mac.

I used this guides as starting point:

https://dortania.github.io/OpenCore-Install-Guide  
https://dortania.github.io/OpenCore-Post-Install

https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Configuration.pdf

Current OpenCore version 0.6.3

## OpenCore Startup Manager
![OpenCore GUI](images/opencore-gui.png)

## Hardware

- Fractal Design Era ITX
- ASUS ROG STRIX Z390-I GAMING
- Intel Core i5-8500T
- 2 x Kingston HyperX Predator 8GB DDR4 3000MHz
- 1 x SAPPHIRE PULSE RX 5600 XT BE 6GB
- 1 x Samsung 970 EVO Plus NVMe M.2 SSD 250 GB
- 1 x Broadcom BCM94360NG M.2 WiFi/ac and BT4LE (replaced on the motherboard)
  - macOS Plug and Play Native Support NO other kext or any patching needed

<details>
<summary>BCM94360NG</summary>

![BCM94360NG](images/hardware/BCM94360NG.png)

</details>

## What works

- Sleep / Wake
- Power Nap (sleep with background operations such as Time Machine)
- Audio (select internal speakers)
- Ethernet
- Bluetooth
- Wi-Fi
- 15 USB port
- AMD DRM for Music, Safari, TV, Plex, Prime, IQSV

<details>
<summary>4K HDR in Plex and INAA app</summary>

![Plex 4K HDR](images/plex.png)

![IINA 4K HDR](images/iina.png)

</details>

## My Workstation

<details>

![](images/hardware/IMG_20200719_134454.jpg)

![](images/hardware/IMG_20200719_134529.jpg)

![](images/hardware/IMG_20200719_134612.jpg)

![](images/hardware/IMG_20200719_134624.jpg)

</details>

## macOS System Information

<details>

![About My Mac](images/about.png)

![About My Mac Display](images/about-display.png)

![About My Mac Memory](images/about-memory.png)

![Intel Power Gadget](images/intel-power-gadget.png)

![System Preferences Display](images/syspref-display.png)

![System Preferences Display alt](images/syspref-display-alt.png)

![System Info Hardware](images/systeminfo-hw.png)

![System Info Audio](images/systeminfo-audio.png)

![System Info Bluetooth](images/systeminfo-bluetooth.png)

![System Info Ethernet](images/systeminfo-ethernet.png)

![System Info GPU](images/systeminfo-gpu.png)

![System Info Memory](images/systeminfo-ram.png)

![System Info NVMExpress](images/systeminfo-nvme.png)

![System Info PCI](images/systeminfo-pci.png)

![System Info SATA](images/systeminfo-sata.png)

![System Info USB](images/systeminfo-usb.png)

![System Info Wi-Fi](images/systeminfo-wifi.png)

</details>

## Benchmark

<details>

![NVMe Speed Test](images/nvme-speed-test.png)

![Geekbench 5 CPU](images/geekbench-cpu.png)

![Geekbench 5 Metal](images/geekbench-metal.png)

![Geekbench 5 OpenCL](images/geekbench-opencl.png)

![LuxMark](images/luxmark.png)

![Ethernet Speed Test](images/speedtest.png)

</details>

## USBMap

Selected XHC ports (max 15)

| Ports | Type | Description |
| --- | --- | --- |
| HS01 | USB 2 and USB 3 Type C connector with Switch | Front USB Type-C |
| HS05 | USB 2 Type A connector | Rear USB 2.0 (black) |
| HS06 | USB 2 Type A connector | Rear USB 2.0 (black) |
| HS07 | USB 3 Standard-A connector | Rear USB 3.1 Gen 1 (blue) |
| HS08 | USB 3 Standard-A connector | Rear USB 3.1 Gen 1 (blue) |
| HS09 | USB 3 Standard-A connector | Front USB 3.1 Gen 1 |
| HS10 | USB 3 Standard-A connector | Front USB 3.1 Gen 1 |
| HS14 | Internal connector | Bluetooth/Wifi - BRCM20702 Hub |
| SS01 | USB 2 and USB 3 Type C connector with Switch | Front USB Type-C |
| SS03 | USB 3 Standard-A connector | Rear USB 3.1 Gen 2 (red) |
| SS04 | USB 3 Standard-A connector | Rear USB 3.1 Gen 2 (red) |
| SS07 | USB 3 Standard-A connector | Rear USB 3.1 Gen 1 (blue) |
| SS08 | USB 3 Standard-A connector | Rear USB 3.1 Gen 1 (blue) |
| SS09 | USB 3 Standard-A connector | Front USB 3.1 Gen 1 |
| SS10 | USB 3 Standard-A connector | Front USB 3.1 Gen 1 |

## BIOS settings

<details>

```
Ai Overclock Tuner [XMP II]
XMP [XMP DDR4-2667 15-17-17-36-1.35V]
BCLK Frequency [100.0000]
ASUS MultiCore Enhancement [Disabled – Enforce All limits]
SVID Behavior [Auto]
CPU Core Ratio [Auto]
DRAM Odd Ratio Mode [Enabled]
DRAM Frequency [DDR4-2666MHz]
Power-saving & Performance Mode [Auto]
CPU SVID Support [Auto]
DRAM CAS# Latency [15]
DRAM RAS# to CAS# Delay [17]
DRAM RAS# ACT Time [36]
DRAM Command Rate [Auto]
DRAM RAS# to RAS# Delay L [7]
DRAM RAS# to RAS# Delay S [7]
DRAM REF Cycle Time [467]
DRAM REF Cycle Time 2 [347]
DRAM REF Cycle Time 4 [214]
DRAM Refresh Interval [Auto]
DRAM WRITE Recovery Time [Auto]
DRAM READ to PRE Time [Auto]
DRAM FOUR ACT WIN Time [30]
DRAM WRITE to READ Delay [Auto]
DRAM WRITE to READ Delay L [Auto]
DRAM WRITE to READ Delay S [Auto]
DRAM CKE Minimum Pulse Width [Auto]
DRAM Write Latency [Auto]
ODT RTT WR (CHA) [Auto]
ODT RTT PARK (CHA) [Auto]
ODT RTT NOM (CHA) [Auto]
ODT RTT WR (CHB) [Auto]
ODT RTT PARK (CHB) [Auto]
ODT RTT NOM (CHB) [Auto]
ODT_READ_DURATION [Auto]
ODT_READ_DELAY [Auto]
ODT_WRITE_DURATION [Auto]
ODT_WRITE_DELAY [Auto]
Data Rising Slope [Auto]
Data Rising Slope Offset [Auto]
Cmd Rising Slope [Auto]
Cmd Rising Slope Offset [Auto]
Ctl Rising Slope [Auto]
Ctl Rising Slope Offset [Auto]
Clk Rising Slope [Auto]
Clk Rising Slope Offset [Auto]
Data Falling Slope [Auto]
Data Falling Slope Offset [Auto]
Cmd Falling Slope [Auto]
Cmd Falling Slope Offset [Auto]
Ctl Falling Slope [Auto]
Ctl Falling Slope Offset [Auto]
Clk Falling Slope [Auto]
Clk Falling Slope Offset [Auto]
DRAM RTL INIT value [Auto]
DRAM RTL (CHA DIMM0 Rank0) [Auto]
DRAM RTL (CHA DIMM0 Rank1) [Auto]
DRAM RTL (CHA DIMM1 Rank0) [Auto]
DRAM RTL (CHA DIMM1 Rank1) [Auto]
DRAM RTL (CHB DIMM0 Rank0) [Auto]
DRAM RTL (CHB DIMM0 Rank1) [Auto]
DRAM RTL (CHB DIMM1 Rank0) [Auto]
DRAM RTL (CHB DIMM1 Rank1) [Auto]
DRAM IOL (CHA DIMM0 Rank0) [Auto]
DRAM IOL (CHA DIMM0 Rank1) [Auto]
DRAM IOL (CHA DIMM1 Rank0) [Auto]
DRAM IOL (CHA DIMM1 Rank1) [Auto]
DRAM IOL (CHB DIMM0 Rank0) [Auto]
DRAM IOL (CHB DIMM0 Rank1) [Auto]
DRAM IOL (CHB DIMM1 Rank0) [Auto]
DRAM IOL (CHB DIMM1 Rank1) [Auto]
CHA IO_Latency_offset [Auto]
CHB IO_Latency_offset [Auto]
CHA RFR delay [Auto]
CHB RFR delay [Auto]
Early Command Training [Enabled]
SenseAmp Offset Training [Enabled]
Early ReadMPR Timing Centering 2D [Enabled]
Read MPR Training [Enabled]
Receive Enable Training [Enabled]
Jedec Write Leveling [Enabled]
Early Write Time Centering 2D [Enabled]
Early Read Time Centering 2D [Auto]
Write Timing Centering 1D [Enabled]
Write Voltage Centering 1D [Enabled]
Read Timing Centering 1D [Enabled]
Dimm ODT Training* [Auto]
Max RTT_WR [ODT Off]
DIMM RON Training* [Auto]
Write Drive Strength/Equalization 2D* [Disabled]
Write Slew Rate Training* [Enabled]
Read ODT Training* [Enabled]
Read Equalization Training* [Enabled]
Read Amplifier Training* [Enabled]
Write Timing Centering 2D [Enabled]
Read Timing Centering 2D [Enabled]
Command Voltage Centering [Enabled]
Write Voltage Centering 2D [Enabled]
Read Voltage Centering 2D [Auto]
Late Command Training [Auto]
Round Trip Latency [Auto]
Turn Around Timing Training [Disabled]
Rank Margin Tool [Disabled]
Memory Test [Disabled]
DIMM SPD Alias Test [Enabled]
Receive Enable Centering 1D [Enabled]
Retrain Margin Check [Disabled]
Write Drive Strength Up/Dn independently [Disabled]
tRDRD_sg [Auto]
tRDRD_dg [Auto]
tRDWR_sg [Auto]
tRDWR_dg [Auto]
tWRWR_sg [Auto]
tWRWR_dg [Auto]
tWRRD_sg [Auto]
tWRRD_dg [Auto]
tRDRD_dr [Auto]
tRDRD_dd [Auto]
tRDWR_dr [Auto]
tRDWR_dd [Auto]
tWRWR_dr [Auto]
tWRWR_dd [Auto]
tWRRD_dr [Auto]
tWRRD_dd [Auto]
TWRPRE [Auto]
TRDPRE [Auto]
tREFIX9 [Auto]
OREF_RI [Auto]
MRC Fast Boot [Auto]
Delay after Train [Disabled]
DRAM CLK Period [Auto]
Memory Scrambler [Enabled]
Channel A DIMM Control [Enable both DIMMs]
Channel B DIMM Control [Enable both DIMMs]
MCH Full Check [Auto]
Training Profile [Auto]
DLLBwEn [Auto]
SPD Write Disable [TRUE]
CPU Load-line Calibration [Auto]
Synch ACDC Loadline with VRM Loadline [Disabled]
CPU Current Capability [Auto]
CPU VRM Switching Frequency [Auto]
VRM Spread Spectrum [Auto]
CPU Power Duty Control [T.Probe]
CPU Power Phase Control [Auto]
CPU VRM Thermal Control [Auto]
CPU Graphics Load-line Calibration [Auto]
CPU Graphics Current Capability [Auto]
CPU Graphics VRM Switching Frequency [Auto]
CPU Graphics Power Phase Control [Auto]
Intel(R) SpeedStep(tm) [Enabled]
Turbo Mode [Enabled]
Long Duration Package Power Limit [Auto]
Package Power Time Window [Auto]
Short Duration Package Power Limit [Auto]
IA AC Load Line [Auto]
IA DC Load Line [Auto]
TVB Voltage Optimizations [Auto]
Realtime Memory Timing [Disabled]
FCLK Frequency for Early Power On [Auto]
BCLK Amplitude [Auto]
BCLK Spread Spectrum [Auto]
BCLK Frequency Slew Rate [Auto]
DRAM VTT Voltage [Auto]
VPPDDR Voltage [Auto]
DMI Voltage [Auto]
Internal PLL Voltage [Auto]
GT PLL Voltage [Auto]
Ring PLL Voltage [Auto]
System Agent PLL Voltage [Auto]
Memory Controller PLL Voltage [Auto]
CPU Core/Cache Current Limit Max. [Auto]
CPU Graphics Current Limit [Auto]
Min. CPU Cache Ratio [32]
Max CPU Cache Ratio [32]
Max. CPU Graphics Ratio [Auto]
CPU Core/Cache Voltage [Auto]
DRAM Voltage [1.35000]
CPU VCCIO Voltage [Auto]
CPU System Agent Voltage [Auto]
CPU Graphics Voltage Mode [Auto]
PCH Core Voltage [Auto]
CPU Standby Voltage [Auto]
DRAM CTRL REF Voltage [Auto]
DRAM DATA REF Voltage on CHB [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank0 BL0 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank0 BL1 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank0 BL2 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank0 BL3 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank0 BL4 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank0 BL5 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank0 BL6 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank0 BL7 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank1 BL0 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank1 BL1 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank1 BL2 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank1 BL3 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank1 BL4 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank1 BL5 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank1 BL6 [Auto]
DRAM DATA REF Voltage on CHA DIMM0 Rank1 BL7 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank0 BL0 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank0 BL1 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank0 BL2 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank0 BL3 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank0 BL4 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank0 BL5 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank0 BL6 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank0 BL7 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank1 BL0 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank1 BL1 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank1 BL2 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank1 BL3 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank1 BL4 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank1 BL5 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank1 BL6 [Auto]
DRAM DATA REF Voltage on CHA DIMM1 Rank1 BL7 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank0 BL0 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank0 BL1 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank0 BL2 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank0 BL3 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank0 BL4 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank0 BL5 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank0 BL6 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank0 BL7 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank1 BL0 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank1 BL1 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank1 BL2 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank1 BL3 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank1 BL4 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank1 BL5 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank1 BL6 [Auto]
DRAM DATA REF Voltage on CHB DIMM0 Rank1 BL7 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank0 BL0 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank0 BL1 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank0 BL2 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank0 BL3 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank0 BL4 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank0 BL5 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank0 BL6 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank0 BL7 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank1 BL0 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank1 BL1 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank1 BL2 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank1 BL3 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank1 BL4 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank1 BL5 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank1 BL6 [Auto]
DRAM DATA REF Voltage on CHB DIMM1 Rank1 BL7 [Auto]
PCI Express Native Power Management [Disabled]
PCH DMI ASPM [Disabled]
ASPM [Disabled]
L1 Substates [Disabled]
PCI Express Clock Gating [Enabled]
DMI Link ASPM Control [Disabled]
PEG - ASPM [Disabled]
Software Guard Extensions (SGX) [Disabled]
Tcc Offset Time Window [Auto]
Hardware Prefetcher [Enabled]
Adjacent Cache Line Prefetch [Enabled]
Intel (VMX) Virtualization Technology [Enabled]
Active Processor Cores [All]
Thermal Monitor [Enabled]
Intel(R) SpeedStep(tm) [Enabled]
Intel(R) Speed Shift Technology [Enabled]
Turbo Mode [Enabled]
CPU C-states [Auto]
CFG Lock [Disabled]
VT-d [Enabled]
Above 4G Decoding [Enabled]
Memory Remap [Enabled]
Primary Display [PEG]
iGPU Multi-Monitor [Enabled]
DVMT Pre-Allocated [32M]
RC6(Render Standby) [Auto]
PCIEX16 Link Speed [Gen3]
PCIe Speed [Gen3]
IOAPIC 24-119 Entries [Enabled]
SATA Controller(s) [Enabled]
SATA Mode Selection [AHCI]
Aggressive LPM Support [Disabled]
SMART Self Test [Enabled]
SATA6G_1(Black) [Enabled]
SATA6G_1 Hot Plug [Enabled]
SATA6G_2(Black) [Enabled]
SATA6G_2 Hot Plug [Enabled]
SATA6G_3(Black) [Enabled]
SATA6G_3 Hot Plug [Enabled]
SATA6G_4(Black) [Enabled]
SATA6G_4 Hot Plug [Enabled]
M.2_2 [Enabled]
Intel Platform Trust Technology [Disabled]
Hyper M.2X16 [Disabled]
HD Audio [Enabled]
Intel LAN Controller [Enabled]
Intel PXE Option ROM [Disabled]
When system is in working state [On]
When system is in sleep, hibernate or soft off states [Off]
USB power delivery in Soft Off state (S5) [Enabled]
Wi-Fi Controller [Enabled]
Bluetooth Controller [Enabled]
ErP Ready [Disabled]
CEC Ready [Disabled]
Restore AC Power Loss [Power Off]
Power On By PCI-E [Disabled]
Power On By RTC [Disabled]
SR-IOV Support [Disabled]
Legacy USB Support [Disabled]
XHCI Hand-off [Enabled]
U31G2_3 [Enabled]
U31G2_4 [Enabled]
USB_5 [Enabled]
USB_6 [Enabled]
U31G1_7 [Enabled]
U31G1_8 [Enabled]
U31G1_9 [Enabled]
U31G1_10 [Enabled]
USB_11 [Enabled]
USB_12 [Enabled]
U31G2_C1\U31G1_C5 [Enabled]
Network Stack [Enabled]
Ipv4 PXE Support [Disabled]
Ipv6 PXE Support [Disabled]
Device [Samsung SSD 850 EVO 250GB]
CPU Temperature [Monitor]
MotherBoard Temperature [Monitor]
PCH Temperature [Monitor]
T_Sensor Temperature [Monitor]
CPU Fan Speed [Monitor]
Chassis Fan Speed [Monitor]
AIO PUMP Speed [Monitor]
CPU Core Voltage [Monitor]
CPU Graphics Voltage [Monitor]
3.3V Voltage [Monitor]
5V Voltage [Monitor]
12V Voltage [Monitor]
PCH Core Voltage [Monitor]
CPU System Agent Voltage [Monitor]
CPU VCCIO Voltage [Monitor]
DRAM Voltage [Monitor]
CPU Standby Voltage [Monitor]
CPU Q-Fan Control [PWM Mode]
CPU Fan Step Up [0 sec]
CPU Fan Step Down [0 sec]
CPU Fan Speed Lower Limit [200 RPM]
CPU Fan Profile [Silent]
Chassis Fan Q-Fan Control [DC Mode]
Chassis Fan Q-Fan Source [Multiple Sources]
Temperature Source 1 [CPU]
Temperature Source 2 [MotherBoard]
Temperature Source 3 [PCH]
Chassis Fan Step Up [0 sec]
Chassis Fan Step Down [0 sec]
Chassis Fan Speed Low Limit [200 RPM]
Chassis Fan Profile [Silent]
AIO PUMP Control [Disabled]
CPU Temperature LED Switch [Enabled]
Fast Boot [Disabled]
Boot Logo Display [Auto]
POST Delay Time [1 sec]
Bootup NumLock State [On]
Wait For 'F1' If Error [Enabled]
Option ROM Messages [Force BIOS]
Interrupt 19 Capture [Disabled]
AMI Native NVMe Driver Support [Enabled]
Setup Mode [Advanced Mode]
Launch CSM [Disabled]
OS Type [Windows UEFI mode]
Load from Profile [1]
Profile Name [macOS]
Save to Profile [1]
DIMM Slot Number [DIMM_A1]
Bus Interface [PCIEX16]
Download & Install ARMOURY CRATE app [Disabled]
```

</details>

<space><space>

<details>
<summary>Screenshots</summary>

![](images/bios/JPEG/201011224212.jpeg)

![](images/bios/JPEG/201011222950.jpeg)

![](images/bios/JPEG/201011223006.jpeg)

![](images/bios/JPEG/201011223037.jpeg)

![](images/bios/JPEG/201011223046.jpeg)

![](images/bios/JPEG/201011223134.jpeg)

![](images/bios/JPEG/201011223201.jpeg)

![](images/bios/JPEG/201011223257.jpeg)

![](images/bios/JPEG/201011223303.jpeg)

![](images/bios/JPEG/201011223307.jpeg)

![](images/bios/JPEG/201011223323.jpeg)

![](images/bios/JPEG/201011223328.jpeg)

![](images/bios/JPEG/201011223331.jpeg)

![](images/bios/JPEG/201011223342.jpeg)

![](images/bios/JPEG/201011223353.jpeg)

![](images/bios/JPEG/201011223402.jpeg)

![](images/bios/JPEG/201011223426.jpeg)

![](images/bios/JPEG/201011223449.jpeg)

![](images/bios/JPEG/201011223504.jpeg)

![](images/bios/JPEG/201011223513.jpeg)

![](images/bios/JPEG/201011223518.jpeg)

![](images/bios/JPEG/201011223522.jpeg)

![](images/bios/JPEG/201011223526.jpeg)

![](images/bios/JPEG/201011223533.jpeg)

![](images/bios/JPEG/201011223557.jpeg)

![](images/bios/JPEG/201011223641.jpeg)

![](images/bios/JPEG/201011223646.jpeg)

![](images/bios/JPEG/201011223712.jpeg)

![](images/bios/JPEG/201011224030.jpeg)

![](images/bios/JPEG/201011224047.jpeg)

![](images/bios/JPEG/201011224101.jpeg)

![](images/bios/JPEG/201011224157.jpeg)

</details>
