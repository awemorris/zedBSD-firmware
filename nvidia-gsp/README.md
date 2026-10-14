# nvidia-gsp

```
Firmware: NVIDIA GSP-RM firmware 570.144 for Turing (TU102, TU104, TU106)
Hardware: NVIDIA GeForce RTX 20xx (Turing TU10x) graphics cards, used by the
          nvrtx driver (CONFIG_DRIVER_PCI_NVRTX)
Files:    /lib/firmware/nvidia/tu102/gsp/gsp-570.144.bin (GSP-RM image)
          /lib/firmware/nvidia/tu102/gsp/bootloader-570.144.bin
          /lib/firmware/nvidia/tu102/gsp/booter_load-570.144.bin
          /lib/firmware/nvidia/tu102/gsp/booter_unload-570.144.bin
          /lib/firmware/nvidia/tu102/acr/bl.bin
Source:   linux-firmware tag 20260410 (commit dc85ccedc9c973682fbcf4d628ca61174bcc3120)

Copyright NVIDIA Corporation or its suppliers.  Redistributed unmodified,
for use with an operating system distributed under an OSI-approved open
source license, together with this license (LICENCE.nvidia section 2.1.2).
```

## License

- [`LICENCE.nvidia`](LICENCE.nvidia) (WHENCE: the `nvidia/tu102` entries)

**Redistribution is permitted only unmodified, for use with an operating system distributed under an OSI-approved open source license, and together with a copy of the license (LICENCE.nvidia section 2.1.2).** Reverse engineering, decompiling, disassembling and translation are prohibited. Read the whole license before you use or redistribute these files.

## Source

linux-firmware tag 20260410, commit dc85ccedc9c973682fbcf4d628ca61174bcc3120: `nvidia/tu102/gsp/{gsp,bootloader,booter_load,booter_unload}-570.144.bin`, `nvidia/tu102/acr/bl.bin` (here `bl.bin`), `LICENCE.nvidia`, `WHENCE`. Byte-identical copies.

| File | Size | SHA-256 |
| --- | --- | --- |
| `gsp-570.144.bin` | 28542040 | `3052aee2872182a14d8d7c069e3a14fe4642405894b24692c4aca4101dfb1809` |
| `bootloader-570.144.bin` | 4196 | `12e987b636c2f00fa40f42fd95097515c0817b158119c584049a37faf38f8f96` |
| `booter_load-570.144.bin` | 59272 | `7bb181f544a942299bbf4642da6d9bb58bfed8459725094e2ace56647cd3ec8c` |
| `booter_unload-570.144.bin` | 39304 | `5c7f1aa37d045cc20bb81584a830e8dfa4483f1cd63943de83a58c4be19a1782` |
| `bl.bin` | 1280 | `01326cc997716bebb0eab9fe1f463fffa0ee586079e4ca0e5bb096ab6fcfedab` |
| `LICENCE.nvidia` | 6212 | `bc5225a57f49c5249dcf238e4ae6437811677a2a8a7f579c3d839e058653ee44` |
| `WHENCE` | 425450 | `c282239a5a2d849677e9304e6f361e475e1b6e71e7c771c03f8986f71b309527` |
