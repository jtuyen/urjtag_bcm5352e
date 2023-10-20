This repo is a urjtag DMA configuration for Broadcom bcm5352e. Copy these files to `/usr/local/share/urjtag/broadcom`

Using Tigard, here is a list of brief instructions to interface with the processor:
1. `cable ft2232 vid=0x0403 pid=0x6010 interface=1`
2. `detect`
```
IR length: 8
Chain length: 1
Device Id: 00000101001101010010000101111111 (0x0535217F)
  Manufacturer: Broadcom (0x17F)
  Part(0):      BCM5352E (0x5352)
  Stepping:     V1
  Filename:     /usr/local/share/urjtag/broadcom/bcm5352e/bcm5352e
ImpCode=00000000100000000000100100000100
EJTAG version: <= 2.0
EJTAG Implementation flags: R4k DMA MIPS32
Clear memory protection bit in DCR
Clear Watchdog
Potential flash base address: [0x0], [0x0]
Processor successfully switched in debug mode.
```
3. `initbus ejtag_dma`
