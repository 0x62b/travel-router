# CM5 Router
A carrier board for Raspberry Pi CM5 with dual 1G ethernet and wifi that turns it into a portable travel router. Also supports LTE/5G dongle over USB ([example](https://www.telstra.com.au/internet/mobile-broadband/prepaid/4gx-mf833v-usb-2026)). Using OpenWRT for firmware.

Functions:
* Dual 1G ethernet
* Wifi through onboard antenna and USB
* Support for LTE/5G dongle over USB
* Portable size

## Repo Structure
`cad`: CAD files, 3D models, case design\
`pcb`: KiCad design files\
`production`: Production files (gerbers and case models)\
`bom.csv`: BOM
`lcsc.csv`: LCSC BOM list export

## Cost
LCSC: 32.49 USD parts + 21.28 USD shipping = 53.77 USD\
PCB: 7 USD + 1.50 USD shipping = 8.50 USD\
Total: 62.27 USD

## Assembly
Prerequisites: soldered PCB and printed case
There's many small SMD components on the PCB that you most likely want to get PCBA'd, like the module's connector, QFNs, etc.

1. Attach the CM5 module to the carrier board
2. Put in an RTC battery
3. (optional but recommended) Screw in a heatsink/fan assembly and plug its connector into the fan connector on the carrier.
4. Place into case and screw into place
5. Affix the wifi/BT antenna and plug into the CM5
6. Plug in an HDMI cable and flash and configure OpenWRT
7. (TODO CONFIG INSTRUCTIONS
8. Disconnect the HDMI cable and screw on the top case
9. Glue the power button into place
10. yay

## Images
### Schematic
<img width="1538" height="1040" alt="image" src="https://github.com/user-attachments/assets/ed2abf24-4986-47e3-9e00-073c60967ed6" />
<img width="1543" height="1063" alt="image" src="https://github.com/user-attachments/assets/96cd3e1b-4ae9-48a2-9e0a-eb0a5adad160" />
<img width="1546" height="1063" alt="image" src="https://github.com/user-attachments/assets/b31f70ff-911a-40f3-aa66-ae7c1e17534e" />
<img width="1546" height="1063" alt="image" src="https://github.com/user-attachments/assets/dc7cad6c-3484-423b-983c-8d2dae439fc3" />

### PCB render
<img width="1241" height="1125" alt="image" src="https://github.com/user-attachments/assets/f4e66f0b-72fc-420f-8c99-cff9f82f8d94" />

### Full render
<img width="1271" height="895" alt="image" src="https://github.com/user-attachments/assets/b9c107d1-065a-491a-add4-dd584dee0878" />

### Zine page
<img width="486" height="690" alt="image" src="https://github.com/user-attachments/assets/fc87d2a8-d078-4cf6-bfca-625877372399" />
