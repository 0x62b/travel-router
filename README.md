# CM5 Router
A carrier board for Raspberry Pi CM5 with dual 1G ethernet and wifi that turns it into a portable travel router. Also supports LTE/5G dongle over USB ([example](https://www.telstra.com.au/internet/mobile-broadband/prepaid/4gx-mf833v-usb-2026)). Using OpenWRT for firmware.

Functions:
* Dual 1G ethernet
* Wifi through onboard antenna and USB
* Support for LTE/5G dongle over USB
* 80x80mm board, portable case

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
LCSC: 34.59 USD parts + 8.1 USD shipping = 42.69 USD\
Other (parts I own but are still in the BOM):
* Heatsink/fan assembly: 15 USD from amazon / 7 USD + shipping from Waveshare
* CM5 2GB/32GB w/ wireless: 97.50 USD from DigiKey

PCB: 7 USD + 1.50 USD shipping = 8.50 USD\
Total: 51.19 USD (parts I need) // 163.69 USD (total)

## Assembly
### Soldering
This can't really be made much more simple. It is a very hard board to handsolder, even with decent equipment. There are very fine-pitch QFNs and connectors, along with some 0201 passives (decoupling caps). If you are building this for some reason and really want to solder the board yourself, start with the smaller passives and work up to bigger parts, doing the big through hole components last. If you want to recreate this project, PCBA may be a good choice, at least for part of the board.

### 3D printing
This should be a very easy print. No specific print settings or filament are required, except for supports for the ports on the bottom case. A BambuStudio 3mf file is included in the `cad/` subdirectory.

### Full assembly
[to update]

## Configuring OpenWRT
(this is a wip as i try to figure out how this software works)\
(no i do not know. once i finish building this thing, assuming it works, ill have to wing it)\
The basic gist of it is that you want one of the Ethernet ports configured as a WAN port, one as a LAN port, and wifi set up as a bridge, where you can get a "WAN" network over wifi and broadcast it as "LAN". If you have a USB cellular modem, you can also add that.

The wired interfaces configuration _should_ be relatively self-explanatory.
Follow this [guide](https://www.linuxscrew.com/openwrt-network-setup) for the Wifi bridge part.
Follow this [guide](https://ten64doc.traverse.com.au/applications/cellular/) for the cellular modem part.

## Images
### Schematic
<img width="1557" height="1069" alt="image" src="https://github.com/user-attachments/assets/eaa025f9-a796-48bc-b48e-eb06d95c2980" />
<img width="1557" height="1069" alt="image" src="https://github.com/user-attachments/assets/1d73d44c-23b6-4bde-9b6c-a603a32e9d7d" />
<img width="1557" height="1069" alt="image" src="https://github.com/user-attachments/assets/e26ea8ff-ee85-4236-9142-29a85059598b" />
<img width="1557" height="1069" alt="image" src="https://github.com/user-attachments/assets/89dddebb-a0d1-40b8-87a2-ee03db9734ec" />

### PCB render
<img width="1238" height="1123" alt="image" src="https://github.com/user-attachments/assets/3fb5c116-3a4a-4d5a-95f5-2b7d286f4261" />

### Full render
<img width="948" height="678" alt="image" src="https://github.com/user-attachments/assets/41a96ce0-df74-4c52-9b15-2e5245bd45cf" />

### Zine page
<img width="1410" height="2000" alt="CM5 Router" src="https://github.com/user-attachments/assets/075bf0ed-646b-42b6-bf56-f32f1d56188a" />
