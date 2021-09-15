# MSI-GS66-OC-New-Dawn

Welcome to my MSI GS66 hackintosh EFI build log and troubleshooting repository.

The directories and files are pretty self-explanatory:

- "Latest Stable Bootable" is the most functional bootable build I am currently running [EFI A] ---> OC 0.6.0
- "Latest WiP Unbootable" is a work in progress unbootable build I am tinkering with [EFI B] ---> OC 0.7.3
- archive contains a record of all previous stable build versions
- debug contains a record of all debug logs for troubleshooting purposes ---> ** as regards [EFI A] **
- misc contains miscellaneous materials, such as some screenshots of my BIOS settings
- README.md contains this message

Please note that SMBIOS data values (ie serials, hardware uuids...) have been redacted. If you wish to use this EFI, 
please generate your own info and adjust the config.plist accordingly.

#

# Current Functionality

| Function | Performance |
|:-: |:-: |
| USB Patching | Excellent |
| Sleep* | Excellent |
| Disable dGPU | Excellent |
| Enable iGPU | Excellent |
| Audio | Excellent |
| WiFi** | Very Good |
| Ethernet | Not Tested |
| Bluetooth | Not Tested |
| CPU Optimisation | Excellent |
| Battery*** | Very Good |
| Brightness & Sound Keys | Excellent |
| General stability | Excellent |

#

*Sleep functions properly even over longer periods and the time it takes for the laptop to wake is relatively proportional to how long the machine has been asleep.

**Heliport rarely fails to load and is sometimes slow to start up on boot or requires manually connecting to saved networks. Once connected, generally very stable with rare dips in signal strength that are neglible in terms of impacting the overall experience.

***Battery life seems reasonably solid. Around 6 hours on high brightness (2 ticks below max) with RGB keys turned on while web browsing, watching videos, using google maps streetview... CPUFriend is enabled (800mhz + default settings). Room for further tweaks in future.

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

**V 0.5**

- Fixed longstanding graphics bug that crashed many apps (injected graphics information into device properties)
- Verified CPU clock speeds are indeed dynamic (used IPG to monior CPU under load, on idle, and on battery)

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
