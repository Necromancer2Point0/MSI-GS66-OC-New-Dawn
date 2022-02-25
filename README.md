# MSI-GS66-OC-New-Dawn

Welcome to my MSI GS66 hackintosh EFI build log and troubleshooting repository.

The directories and files are pretty self-explanatory:

- "Latest Stable Bootable" is the most functional bootable build I am currently running ---> OC 0.7.8
- archive contains a record of all previous stable build versions ---> OC 0.6.0 unless otherwise specified
- debug contains a record of all debug logs for troubleshooting purposes
- misc contains miscellaneous materials (BIOS settings, bug fixes, and an in-depth undervolting guide)
- README.md contains this message

Please note that SMBIOS data values (ie serials, hardware uuids...) have been redacted. If you wish to use this EFI, 
please generate your own info and adjust the config.plist accordingly.

If you do not have an MSI GS66, you may still find the undervolting and sleep dGPU fixes helpful as they are almost universally applicable.

#

# Current Functionality

| Function | Performance |
|:-: |:-: |
| USB Patching | Excellent |
| Sleep* | Excellent |
| Disable dGPU | Excellent |
| Enable iGPU | Excellent |
| 300hz Support | Excellent |
| Audio | Excellent |
| WiFi** | Very Good |
| Ethernet | Not Tested |
| Bluetooth | Excellent |
| Thunderbolt | Not Tested |
| CPU Optimisation | Excellent |
| Battery*** | Very Good |
| Undervolting | Excellent |
| Trackpad | Excellent |
| Brightness & Sound Keys | Excellent |
| General stability | Excellent |

#

*Sleep functions properly even over longer periods and the time it takes for the laptop to wake is relatively proportional to how long the machine has been asleep. Undervolted values are consistently applied in every instance ~~except~~ INCLUDING wake from auto-sleep (ie screen dims then sleeps after X amount of time idling)

**itlwm may fail to run (see misc folder for solution) and is sometimes slow to start up on boot or requires manually connecting to saved networks. Once connected, generally very stable with rare dips in signal strength that are negligible in terms of impacting the overall experience.

***Battery life seems reasonably solid. Around 6 hours on high brightness (2 ticks below max) with RGB keys turned on while web browsing, watching videos, using google maps streetview... CPUFriend is enabled (800mhz + default settings). Room for further tweaks in future. Users may wish to reduce refresh rate (see misc).

#

# MSI GS66 Stealth 10SGS-036

| Component | Details |
|:-: |:-: |
| Processor | Intel i7-10750H Hexa Core |
| RAM | 32GB DDR4 |
| SSD | NVMe |
| iGPU | Intel UHD 630 Graphics |
| ~~dGPU~~ | ~~NVIDIA GeForce RTX 2080 SUPER Max-Q 8GB~~ |
| Monitor | 15.6" FHD 300Hz |
| Audio | Dynaudio Speakers 2W |
| WiFi & Bluetooth | Intel Wi-Fi 6 AX201(2*2 ax) w/ Bluetooth 5.0 |
| OS Version | Catalina 10.15.7 (w/o Security Update 2021-004) |

#

# CHANGELOG


**V 0.8**

- Updated to latest OC version (0.7.8)
- Added 300hz support, streamlined EFI, and removed unnecessary Voodoo input kexts
- Uploaded instructions into misc folder about how to resolve "itlwm not running" bug + other tweaks

> Massive thank you to user Phu54321 for taking the time to share his vast knowledge and alternative EFI, which both served as invaluable references in the development of this update!

**V 0.7**

- Completely overhauled undervolting and fixed all issues; values are now applied on every wake from sleep
- Tested bluetooth functionality and found it works perfectly with a bluetooth speaker
- Revised my own, in-depth guide about the lengthy process of undervolting a hackintosh (see "misc" folder)

**V 0.6**

- Undervolted the machine to achieve better overall temperatures and efficiency (added VoltageShift.kext)
- Reverse engineered and updated SleepWatcher .plists so that the commands work for version 2.2.1
- Devised my own, in-depth guide about the lengthy process of undervolting a hackintosh (see "misc" folder)

**V 0.5**

- Fixed longstanding graphics bug that crashed many apps (injected graphics information into device properties)
- Verified CPU clock speeds are indeed dynamic (used IPG to monitor CPU under load, on idle, and on battery)

**V 0.4**

- Fixed battery management (disabled cfg and xcpm quirks in kernel)

**V 0.3**

- Fixed speakers & headphone audio (VooDoo HDA)
- Fixed brightness keys (kext)
- Fixed dGPU turning on upon wake from sleep (sleep works perfectly so far)

**V 0.2**

- Experiments with CPUFriend

**V 0.1**

- The journey begins
