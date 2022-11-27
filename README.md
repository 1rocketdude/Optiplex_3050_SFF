# Optiplex_3050_SFF
OpenCore for Optiplex 3050 SFF - a lower powered version Kaby Lake processor. This machine is so quiet, I can't hear the fan running. The PCIe M.2 SSD works flawlessly at x4. Plenty of performance for a server that stays on all the time. This is a computer that has no comparable Apple product, so no SIMBIOS is a perfect match. Fortunately, WhateverGreen and Lilu handle everything. Strangely, the 'About this Mac' reports a Core i7 processor. Probably something to fix within ACPI, but it's purely cosmetic.

CPU: I3-7100T with HD630 integrated graphics (Intel Iris Plus Graphics 655 - Mobile!),
ALC3234 audio,
Realtek RTL8111HSD-CG GigEth,
USB3.1, USB2 front panel,
USB3.1, USB2 rear panel,
HDMI,
DisplayPort,
PCIe M.2 SSD,
Bios 1.22.1 - latest as of 2022-10-17

OS: Big Sur 11.7.1

OpenCore: 0.8.6

SMBIOS: iMac 18,1

SMBIOS that does not work: Macmini8,1

Dortania Guide for everything in setup: see https://dortania.github.io/OpenCore-Install-Guide/config.plist/kaby-lake.html

<b>What's working</b>
<ul>
<li>ethernet
<li>audio
<li>dual monitors (1920x1080) - a bit of a subtlety here, consistent with other people have experienced with dual monitors on 3050 variants. I could not get dual <b>HDMI</b> monitors to function. It would always cause a hang half way through the Apple boot screen. However, plugging a DP or DVI monitor into the DP port on the 3050 and an HDMI monitor into the HDMI monitor would result in both monitors working. This is my daily setup that has been solid from the start. A single DVI monitor plugged into the HDMI port functions, but to get dual monitors. I did not have to do any framebuffer patching. After reading a dozen descriptions about how to configure framebuffer within config.plist, I succeeded with a hardware solution - connect the proper cable to the correct port on the 3050. That was a painful 3 hour lesson.
</ul>

<b>What's not working</b>
<ul>
<li>Wifi and bluetooth - my computer was barebones, not including a drive or wireless card. Since I operate with hardwire ethernet, no need to test wireless. I would expect the same challenges as with other non-Apple wifi cards.
<li>Sleep/wake - my computer is always on, so no need to test. I assume that HD630 iGPU will cause problems here as elsewhere.
<li>Airdrop - no bluetooth
<li>iMessage - never use it, but I suspect getting a working WiFi/Bluetooth card would allow this
<li>Sidecar - while Sidecar shows up in System Preferences, I couldn't get a modern iPad to communicate even when plugged in via a USB cable
<li>Microphone - others have mentioned this is a challenge. I don't need a microphone, so I disabled it in the BIOS
</ul>

