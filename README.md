# lspci

lspci -v
```
00:00.0 Host bridge: Intel Corporation 2nd Generation Core Processor Family DRAM Controller (rev 09)
        Subsystem: Apple Inc. 2nd Generation Core Processor Family DRAM Controller
        Flags: bus master, fast devsel, latency 0
        Capabilities: [e0] Vendor Specific Information: Len=0c <?>

00:01.0 PCI bridge: Intel Corporation Xeon E3-1200/2nd Generation Core Processor Family PCI Express Root Port (rev 09) (prog-if 00 [Normal decode])
        Flags: bus master, fast devsel, latency 0, IRQ 16
        ...
        Kernel driver in use: pcieport
        Kernel modules: shpchp

00:01.1 PCI bridge: Intel Corporation Xeon E3-1200/2nd Generation Core Processor Family PCI Express Root Port (rev 09) (prog-if 00 [Normal decode])
        ...
        Kernel driver in use: pcieport
        Kernel modules: shpchp
```

lspci -s 00:01.0
```
 lspci -s 00:01.0 -v
00:01.0 PCI bridge: Intel Corporation Xeon E3-1200/2nd Generation Core Processor Family PCI Express Root Port (rev 09) (prog-if 00 [Normal decode])
	Flags: bus master, fast devsel, latency 0, IRQ 16
	Bus: primary=00, secondary=01, subordinate=01, sec-latency=0
	Memory behind bridge: a0800000-a08fffff
	Capabilities: [88] Subsystem: Apple Inc. Xeon E3-1200/2nd Generation Core Processor Family PCI Express Root Port
	Capabilities: [80] Power Management version 3
	Capabilities: [90] MSI: Enable- Count=1/1 Maskable- 64bit-
	Capabilities: [a0] Express Root Port (Slot+), MSI 00
	Capabilities: [100] Virtual Channel
	Capabilities: [140] Root Complex Link
	Kernel driver in use: pcieport
	Kernel modules: shpchp
```
