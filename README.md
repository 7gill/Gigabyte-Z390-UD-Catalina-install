# Gigabyte-Z390-UD-Catalina-install

## Hardware
* **Gigabyte Z390 UD Motherboard (Bios F8)**
* **Intel Core i7-9700K Processor**
* **Noctua NH-D15S CPU Cooler**
* **Corsair Vengeance LPX 32GB (2x16GB) DDR4-2666 CL16 - White**
* l**MSI RADEON RX 580 ARMOR 8G OC Graphics Card**
* **Intel 660P Series 2TB M.2 NVMe SSD**
* **Deepcool MACUBE 550 TG Mid Tower Case - Black**
* **Silverstone Strider ST65F-GS 650W Full Modular 80Plus Gold Power Supply**
* **Noctua NF-P12 Redux-1300 PWM 120mm Fan x2**
* **Loctek DLB111 10”-30” Single Monitor Ergonomic Swivel Arm**
* **A bunch of old hard drives**

I wanted to go with OpenCore but my brain broke trying to configure it, I’ll give it a go at a later date. Also, I am no expert in this kind of stuff, I'm just a guy who followed some instructions on the internet. 

I used this guide as my starting point 
[Minimal Clover Config and Drivers for Gigabyte Z390 I WIFI : hackintosh](https://www.reddit.com/r/hackintosh/comments/az7ld1/minimal_clover_config_and_drivers_for_gigabyte/%0A)

## Issues

* Ethernet
	* fixed with RealtekRTL8111.kext 
* Bluetooth/Wifi
	* fixed with one of  [these](https://www.ebay.com/itm/HACKINTOSH-WIFI-AC-BLUETOOTH-4-0-ADAPTER-BCM94360CS2-PCI-x1-NATIVE-SUPPORT/173886173938?hash=item287c6c72f2:g:PqwAAOSwO7dcEF3c) 
* Audio
	* Fixed with AppleALC, used audio instructions from  [https://www.tonymacx86.com/threads/an-idiots-guide-to-lilu-and-its-plug-ins.260063/#AppleALC](https://www.tonymacx86.com/threads/an-idiots-guide-to-lilu-and-its-plug-ins.260063/#AppleALC) 
* Sleep/Shutdown
	~~Seems to work~~ Nope, fixed it with the instructions on [this](https://www.reddit.com/r/hackintosh/comments/bdbn8w/new_hackintosh_mostly_working_except_for/) page. As it states in the comments, they are not too sure if it is the  FakeSMC, EmuVariableUefi-64, HFSPlus-64, and slide=0 boot argument that fixed the issues but seems to work now. Long and short of it is that I had to replace VirtualSMC with FakeSMC. 
* NVRAM
	* Not fixed as of yet


## Comments
If anyone with similar hardware finds this useful, sweet. 

While the miminalist guide where I started was pretty sparse with the kexts and .efi file mine seems a bit more messy. To be honest I am not to sure the drivers>bios folder is needed at all but what do I know. It all seems to work so I am happy.  
