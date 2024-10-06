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

OS: Sonoma 14.7 (likely the upgrade to Sequoia would be successful, but since this is my daily use machine, I'm waiting until early 2025 to give it a go)

OpenCore: 1.0.1

SMBIOS: iMac 19,1

SMBIOS that does not work: Macmini8,1

Dortania Guide for everything in setup: see https://dortania.github.io/OpenCore-Install-Guide/config.plist/kaby-lake.html

<b>What's working - everything necessary to make this a stable mac-mini like computer</b>
<ul>
<li>ethernet
<li>audio
<li>Sleep/wake - Magically, this started working in a recent OpenCore update.
<li>dual monitors (1920x1080) both HDMI; one attaches to the 3050's HDMI port and the other HDMI cable through an adapter to DisplayPort.
<li>Messages - just works as expected
<li>USB - full USB3 speeds off all the ports
</ul>

<b>What hasn't been tested?</b>
<ul>
<li>Wifi and bluetooth - my computer was barebones, not including a drive or wireless card. Since I operate with hardwire ethernet, no need to test wireless. I would expect the same challenges as with other non-Apple wifi cards.
<li>Airdrop - no bluetooth or wifi
<li>Microphone - others have mentioned this is a challenge. I don't need a microphone, so I disabled it in the BIOS. I use a USB webcam with mic, which just works.
</ul>

