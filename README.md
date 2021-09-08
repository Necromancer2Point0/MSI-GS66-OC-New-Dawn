# MSI-GS66-OC-New-Dawn

This is my EFI build and troubleshooting repository for my MSI GS66.

The directories are pretty self-explanatory:

- "Latest Stable Bootable" is the most functional bootable build I am currently running [EFI A]
- "Latest WiP Unbootable (0.7.2)" is a work in progress unbootable build I am tinkering with [EFI B]
- Debug contains a record of all debug logs for troubleshooting purposes ---> ** as regards [EFI A] **

Please note that SMBIOS data (ie serials, hardware uuids...) have been redacted. If you wish to use this EFI, 
please generate your own info and adjust the config.plist accordingly.

**CHANGELOG**

**V 0.3**

- Fixed speakers & headphone audio (VooDoo HDA)
- Fixed brightness keys (kext)
- Fixed dGPU turning on upon wake from sleep (sleep works perfectly so far)

**V 0.2**

- Experiments with CPUFriend

**V 0.1**

- The journey begins
