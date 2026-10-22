# nvidia-gsp

```
Firmware: NVIDIA GSP-RM firmware 570.144 for Turing (TU102, TU104, TU106,
          TU116, TU117), Ampere (GA102 to GA107) and Ada (AD102 to AD107)
Hardware: NVIDIA GeForce RTX 20xx, GTX 16xx, RTX 30xx and RTX 40xx graphics
          cards, used by the nvrtx driver (CONFIG_DRIVER_PCI_NVRTX)
Files:    /lib/firmware/nvidia/tu102/gsp/gsp-570.144.bin (GSP-RM image, Turing)
          /lib/firmware/nvidia/tu102/gsp/bootloader-570.144.bin
          /lib/firmware/nvidia/tu102/gsp/booter_load-570.144.bin
          /lib/firmware/nvidia/tu102/gsp/booter_unload-570.144.bin
          /lib/firmware/nvidia/tu102/acr/bl.bin
          /lib/firmware/nvidia/tu116/gsp/booter_load-570.144.bin
          /lib/firmware/nvidia/tu116/gsp/booter_unload-570.144.bin
          /lib/firmware/nvidia/ga102/gsp/gsp-570.144.bin (GSP-RM image, Ampere and Ada)
          /lib/firmware/nvidia/ga102/gsp/bootloader-570.144.bin
          /lib/firmware/nvidia/ga102/gsp/booter_load-570.144.bin
          /lib/firmware/nvidia/ga102/gsp/booter_unload-570.144.bin
          /lib/firmware/nvidia/ad102/gsp/bootloader-570.144.bin
          /lib/firmware/nvidia/ad102/gsp/booter_load-570.144.bin
          /lib/firmware/nvidia/ad102/gsp/booter_unload-570.144.bin
Source:   linux-firmware tag 20260410 (commit dc85ccedc9c973682fbcf4d628ca61174bcc3120)

Copyright NVIDIA Corporation or its suppliers.  Redistributed unmodified,
for use with an operating system distributed under an OSI-approved open
source license, together with this license (LICENCE.nvidia section 2.1.2).
```

## License

- [`LICENCE.nvidia`](LICENCE.nvidia) (WHENCE: the `nvidia/tu102`, `nvidia/tu116`, `nvidia/ga102` and `nvidia/ad102` entries)

**Redistribution is permitted only unmodified, for use with an operating system distributed under an OSI-approved open source license, and together with a copy of the license (LICENCE.nvidia section 2.1.2).** Reverse engineering, decompiling, disassembling and translation are prohibited. Read the whole license before you use or redistribute these files.

## Source

linux-firmware tag 20260410, commit dc85ccedc9c973682fbcf4d628ca61174bcc3120: `nvidia/tu102/gsp/{gsp,bootloader,booter_load,booter_unload}-570.144.bin`, `nvidia/tu102/acr/bl.bin` (here `bl.bin`), `nvidia/tu116/gsp/{booter_load,booter_unload}-570.144.bin` (here `tu116-*`), `nvidia/ga102/gsp/{gsp,bootloader,booter_load,booter_unload}-570.144.bin` (here `ga102-*`), `nvidia/ad102/gsp/{bootloader,booter_load,booter_unload}-570.144.bin` (here `ad102-*`), `LICENCE.nvidia`, `WHENCE`. Byte-identical copies.

| File | Size | SHA-256 |
| --- | --- | --- |
| `gsp-570.144.bin` | 28542040 | `3052aee2872182a14d8d7c069e3a14fe4642405894b24692c4aca4101dfb1809` |
| `bootloader-570.144.bin` | 4196 | `12e987b636c2f00fa40f42fd95097515c0817b158119c584049a37faf38f8f96` |
| `booter_load-570.144.bin` | 59272 | `7bb181f544a942299bbf4642da6d9bb58bfed8459725094e2ace56647cd3ec8c` |
| `booter_unload-570.144.bin` | 39304 | `5c7f1aa37d045cc20bb81584a830e8dfa4483f1cd63943de83a58c4be19a1782` |
| `bl.bin` | 1280 | `01326cc997716bebb0eab9fe1f463fffa0ee586079e4ca0e5bb096ab6fcfedab` |
| `tu116-booter_load-570.144.bin` | 59016 | `9bd01804b4b91d92904e7735b025e07a3c935bc6fb92e3833e85c297546025b9` |
| `tu116-booter_unload-570.144.bin` | 39048 | `bf4a2b778722dde57850839bb9f7651ae29592ce85d6df4160d2d228ff430156` |
| `ga102-gsp-570.144.bin` | 63571696 | `a8c3ebeed280323aedb51c061f321e73379cce7a9ae643a33dd03915df027f7f` |
| `ga102-bootloader-570.144.bin` | 24684 | `82428f532240727e95bb3083fbaaba9b2cc7b937314323f2d546ce7245f27fad` |
| `ga102-booter_load-570.144.bin` | 61304 | `4497e3eff7e95c774b8a569d17b27c08c9650158d10b229d2be81cdcad9a085b` |
| `ga102-booter_unload-570.144.bin` | 41080 | `8e63db5b78d7d3e349f20a2d11099c3d7109081393cb09ffc0a28133324ae009` |
| `ad102-bootloader-570.144.bin` | 36972 | `65ab2e6b6e0fca95365c4deac79a34582abcfeb15b6ae234138f22e7183118a8` |
| `ad102-booter_load-570.144.bin` | 57720 | `8b293e19b637c5e22c87a2428d1c71bb13e0904e8a88ac6b3c6c1f2679c6e37a` |
| `ad102-booter_unload-570.144.bin` | 41592 | `975b85a14ded8e430d30f000c3c1afdd55c15dee04f35ff9dfd876acd7e67186` |
| `LICENCE.nvidia` | 6212 | `bc5225a57f49c5249dcf238e4ae6437811677a2a8a7f579c3d839e058653ee44` |
| `WHENCE` | 425450 | `c282239a5a2d849677e9304e6f361e475e1b6e71e7c771c03f8986f71b309527` |
