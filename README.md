this is my first try to build TWRP please forgive me :)

based on https://github.com/cooked71/device_realme_RMX3834_twrp/tree/main from gitFASTBOOT (is the nearest devtree found)
from scratch

we have shell,logs,external_sd, no data decrypt, gatekepeer up, android.health up, keymint up
still need to cleanup useless stuff

seems that an issue is present on twrp_manifest in recovery log trows Atomic commit failed ret=-22 that prevent ui to come up ,seems that is due to an updated vesion of graphics_drm.cpp to come up
replaced  graphics_drm.cpp in ../bootable/recovery/minuitwrp/  

built using twrp minimal manifest 12.1

bootloader was unlocked using https://github.com/TomKing062/CVE-2022-38694_unlock_bootloader/wiki/SupportList

firmware dump on local (unable to put on line 13GB) using dumpyara

nearest found https://dumps.tadiphone.dev/dumps/realme/re58c2

the device was flashed with the exactly the same firmware dumped in local

android 14
Chipset	Unisoc Tiger T612 (12 nm)
CPU	Octa-core (2x1.8 GHz Cortex-A75 & 6x1.8 GHz Cortex-A55)
GPU	Mali-G57
Memory	Card slot	microSDXC (dedicated slot)
Internal	128GB 6GB RAM

