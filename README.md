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
3. optional: `initbus ejtag_dma`
4. detectflash 0x1fc00000
```
Query identification string:
	Primary Algorithm Command Set and Control Interface ID Code: 0x0002 (AMD/Fujitsu Standard Command Set)
	Alternate Algorithm Command Set and Control Interface ID Code: 0x0000 (null)
Query system interface information:
	Vcc Logic Supply Minimum Write/Erase or Write voltage: 2700 mV
	Vcc Logic Supply Maximum Write/Erase or Write voltage: 3600 mV
	Vpp [Programming] Supply Minimum Write/Erase voltage: 0 mV
	Vpp [Programming] Supply Maximum Write/Erase voltage: 0 mV
	Typical timeout per single byte/word program: 16 us
	Typical timeout for maximum-size multi-byte program: 0 us
	Typical timeout per individual block erase: 1024 ms
	Typical timeout for full chip erase: 0 ms
	Maximum timeout for byte/word program: 512 us
	Maximum timeout for multi-byte program: 0 us
	Maximum timeout per individual block erase: 16384 ms
	Maximum timeout for chip erase: 0 ms
Device geometry definition:
	Device Size: 4194304 B (4096 KiB, 4 MiB)
	Flash Device Interface Code description: 0x0002 (x8/x16)
	Maximum number of bytes in multi-byte program: 1
	Number of Erase Block Regions within device: 2
	Erase Block Region Information:
		Region 0:
			Erase Block Size: 8192 B (8 KiB)
			Number of Erase Blocks: 8
		Region 1:
			Erase Block Size: 65536 B (64 KiB)
			Number of Erase Blocks: 63
Primary Vendor-Specific Extended Query:
	Major version number: 3
	Minor version number: 3
	Address Sensitive Unlock: Required
	Process Technology: 170-nm Floating Gate technology
	Erase Suspend: Read/write
	Sector Protect: 1 sectors per group
	Sector Temporary Unprotect: Not supported
	Sector Protect/Unprotect Scheme: 29BDS640 mode (Software Command Locking)
	Simultaneous Operation: 48 sectors
	Burst Mode Type: Supported
	Page Mode Type: Not supported
	ACC (Acceleration) Supply Minimum: 8500 mV
	ACC (Acceleration) Supply Maximum: 12500 mV
	Top/Bottom Sector Flag: Bottom boot device
	Program Suspend: Supported
	Unlock Bypass: Supported
	SecSi Sector (Customer OTP Area) Size: 0 bytes
	Embedded Hardware Reset Timeout Maximum: 0 ns
	Non-Embedded Hardware Reset Timeout Maximum: 0 ns
	Erase Suspend Timeout Maximum: 0 us
	Program Suspend Timeout Maximum: 0 us
```
