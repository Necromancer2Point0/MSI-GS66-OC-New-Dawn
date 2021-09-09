# MSI-GS66-OC-New-Dawn

This is my EFI and troubleshooting repository for my MSI GS66 hackintosh build.

The directories and files are pretty self-explanatory:

- "Latest Stable Bootable" is the most functional bootable build I am currently running [EFI A]
- "Latest WiP Unbootable" is a work in progress unbootable build I am tinkering with [EFI B] ---> OC 0.7.2
- archive contains a record of all previous stable build versions
- debug contains a record of all debug logs for troubleshooting purposes ---> ** as regards [EFI A] **
- README.md contains this message

Please note that SMBIOS data (ie serials, hardware uuids...) have been redacted. If you wish to use this EFI, 
please generate your own info and adjust the config.plist accordingly.

# CHANGELOG

**V 0.3**

- Fixed speakers & headphone audio (VooDoo HDA)
- Fixed brightness keys (kext)
- Fixed dGPU turning on upon wake from sleep (sleep works perfectly so far)

**V 0.2**

- Experiments with CPUFriend

**V 0.1**

- The journey begins

# MSI GS66 Stealth 10SGS-036

| Component | Details |
|:-: |:-: |
| Processor | i7-10750H Hexa Core  |
| RAM | 32GB DDR4 |
| SSD | NVMe |
| iGPU | Intel UHD 630 Graphics |
| dGPU | Nvidia GeForce RTX 2080 Super Max-Q 8GB (hard disabled) |
| Monitor | 15.6" FHD 300Hz |
| Audio | Dynaudio Speakers 2W |
| WiFi & Bluetooth | Intel® Wi-Fi 6 AX201(2*2 ax) w/ Bluetooth 5.0 |
