# CM5 Router
A carrier board for Raspberry Pi CM5 with dual 1G ethernet and wifi that turns it into a portable travel router. Also supports LTE/5G dongle over USB.

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
LCSC: 32.49 USD parts + 21.28 USD shipping = 53.77 USD
PCB: 7 USD + 1.50 USD shipping = 8.50 USD
Total: 62.27 USD

## Assembly
Prerequisites: soldered PCB and printed case
There's many small SMD components on the PCB that you most likely want to get PCBA'd, like the module's connector, QFNs, etc.

1. Attach the CM5 module to the carrier board
2. Place into case and screw into place
[todo]

## Images
[todo]