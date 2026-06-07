# CM5 Router
A carrier board for Raspberry Pi CM5 with dual 1G ethernet and wifi that turns it into a portable travel router. Also supports LTE/5G dongle over USB ([example](https://www.telstra.com.au/internet/mobile-broadband/prepaid/4gx-mf833v-usb-2026)). Using OpenWRT for firmware.

Functions:
* Dual 1G ethernet
* Wifi through onboard antenna and USB
* Support for LTE/5G dongle over USB
* 100x100mm board, portable case

## Motivation
I had a spare CM5 lying around, as any normal person would (/s). I also wanted to learn high-speed signal routing, so making a CM5 carrier board would be a perfect excuse. Also, I needed a travel router, so I figured that this would be a fun project to make.

As you can see by the cost breakdown later, this project is not economical at all if you want to build it from scratch and don't have a CM5 already. However, if you already have a CM5, this can be used just like any other carrier board.

## Repo Structure
`cad`: CAD files, 3D models, case design\
`pcb`: KiCad design files\
`production`: Production files (gerbers and case models)\
`bom.csv`: BOM\
`lcsc.csv`: LCSC BOM list export

## Cost breakdown
LCSC: 32.49 USD parts + 21.28 USD shipping = 53.77 USD\
Other (parts I own but are still in the BOM):
* Heatsink/fan assembly: 15 USD from amazon / 7 USD + shipping from Waveshare
* CM5 2GB/32GB w/ wireless: 97.50 USD from DigiKey

PCB: 7 USD + 1.50 USD shipping = 8.50 USD\
Total: 62.27 USD (parts I need) // 174.77 USD (total)

## Assembly
### Soldering
This can't really be made much more simple. It is a very hard board to handsolder, even with decent equipment. There are very fine-pitch QFNs and connectors, along with some 0201 passives (decoupling caps). If you are building this for some reason and really want to solder the board yourself, start with the smaller passives and work up to bigger parts, doing the big through hole components last.

### 3D printing
This should be a very easy print. No specific print settings or filament are required, except for supports for the ports on the bottom case. A BambuStudio 3mf file is included in the `cad/` subdirectory.

### Full assembly
1. Attach the CM5 module to the carrier board
2. Put in an RTC battery
3. (optional but recommended) Screw in a heatsink/fan assembly and plug its connector into the fan connector on the carrier.
4. Place into case and screw into place
5. Affix the wifi/BT antenna and plug into the CM5
6. Plug in an HDMI cable and flash and configure OpenWRT
7. Follow the instructions in `Configuring OpenWRT`
8. Disconnect the HDMI cable and screw on the top case
9. Glue the power button into place
10. yay

## Configuring OpenWRT
(this is a wip as i try to figure out how this software works)\
(no i do not know. once i finish building this thing, assuming it works, ill have to wing it)\
The basic gist of it is that you want one of the Ethernet ports configured as a WAN port, one as a LAN port, and wifi set up as a bridge, where you can get a "WAN" network over wifi and broadcast it as "LAN". If you have a USB cellular modem, you can also add that.

The wired interfaces configuration _should_ be relatively self-explanatory.
Follow this [guide](https://www.linuxscrew.com/openwrt-network-setup) for the Wifi bridge part.
Follow this [guide](https://ten64doc.traverse.com.au/applications/cellular/) for the cellular modem part.

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
