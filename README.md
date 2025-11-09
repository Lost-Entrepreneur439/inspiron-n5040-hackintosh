macOS High Sierra EFI for the Dell Inspiron N5040 using OpenCore. I will try to keep this EFI up to date with the latest OpenCore and kexts


# WARNING! SMBIOS DETAILS ARE NOT INCLUDED IN THE CONFIG.PLIST.
You will have to use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate a **MacBookPro7,1** SMBIOS for your system, and add them to the config.plist.
Make sure you're on BIOS [A05](https://www.dell.com/support/home/en-ca/drivers/driversdetails?driverid=8pc4x&oscode=biosa&productcode=inspiron-15-intel-n5040) before continuing. Older versions may cause issues

## Other macOS versions?
No. High Sierra is the latest supported by MacBookPro7,1, so it's all I'll ever support. If you want a different version, feel free to fork this repo to modify it for whatever version you want. Do note newer versions will likely require OCLP.

## System specs
Do note if your hardware differs, while unlikely, you may have issues.
- CPU: Intel Core i3-M380
- GPU: Intel HD Graphics (Arrandale)
- Chipset: Intel HM57
- Touchpad: ALPS PS/2
- Audio: IDT 92HD87B1/3
- Wi-Fi: Dell Wireless 1502
- Ethernet: Realtek RTL8139/810x
- Disk: Toshiba 160GB 7200RPM 2.5"

## Issues:
- Screen brightness cannot be changed. This is a known bug with Arrandale and can't be fixed.
- NVRAM does not work and likely never will. This also means sleep will not work.

If you notice any other problems, please open an issue (or pull request if you have a fix)

### BIOS settings
If you do not set these BIOS settings, macOS will **not** boot.
- Advanced -> Virtualization -> Enabled
- Advanced -> SATA Mode -> AHCI
