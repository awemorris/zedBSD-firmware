# amd-navi

```
Firmware: AMD Navi 10 (RDNA1) GPU firmware: the PSP secure OS and ASD, the SMU,
          the command processor (PFP, ME, CE, MEC, MEC2), the RLC and the SDMA engines
Hardware: AMD Radeon RX 5600 / 5600 XT / 5700 / 5700 XT (Navi 10, gfx1010)
Files:    /lib/firmware/amdgpu/navi10_*.bin
Source:   linux-firmware tag 20260410 (commit dc85ccedc9c973682fbcf4d628ca61174bcc3120), amdgpu/

Copyright (C) 2024  Advanced Micro Devices, Inc. All rights reserved.
```

## License

- [`LICENSE.amdgpu`](LICENSE.amdgpu)

Redistribution of the unmodified binaries is permitted, provided the copyright notice, the permission notice and
the disclaimers are reproduced; no reverse engineering, decompilation or disassembly; the files are subject to
United States export laws and regulations.

The files are unmodified copies of the upstream files named above. Read the license before you
redistribute or use them. `navi10_ta.bin` (HDCP and DTM applications) and `navi10_vcn.bin` (the video
decoder) are not included.

## Files

| File | Size | SHA-256 |
| --- | ---: | --- |
| `navi10_sos.bin` | 184512 | `3112ea8519545ac89c1623e2e08e841a6a9bc31c2aab2f9b787979e51277e395` |
| `navi10_asd.bin` | 205312 | `2d084493e763e60cd90ac25b054f73e4857a24864334cd3c5b092f3273cd12de` |
| `navi10_smc.bin` | 267970 | `49ed339d0ff71fe64347380ee12b00c3c69a546f454bcd4323c411c72fe6fb2e` |
| `navi10_pfp.bin` | 263424 | `310032fe0698871b80be6eb5877ae7ed3395cb712629698c5c631e0af7c4e04a` |
| `navi10_me.bin` | 263424 | `faf2f9ff33580b53f7b90f410447efa1d2b21366f344ff5a383d074bf1ea8c35` |
| `navi10_ce.bin` | 263296 | `074ec5270eb7cad73906a1a591c274a40895b170091bc8068180a4c4d7771165` |
| `navi10_mec.bin` | 268160 | `936de4938bcfd5e1691b1e544247000f7b4b7430eef317e28f8560bb9e88e758` |
| `navi10_mec2.bin` | 268160 | `936de4938bcfd5e1691b1e544247000f7b4b7430eef317e28f8560bb9e88e758` |
| `navi10_rlc.bin` | 43952 | `1f52478fb78dee904361b93ad67955fcff151bb7a7772bbfbd2c448c814be1f5` |
| `navi10_sdma.bin` | 33792 | `3fc635b9a17819eaf13913882676f0cd07a6c1a31c87b3ef0dcedebf594c8dd0` |
| `navi10_sdma1.bin` | 33792 | `317b398d0563c8c89b10c31712296843143385f5a1ddcee2031536fe67576c3b` |
| `LICENSE.amdgpu` | 2938 | `572872598565dc3513470de971a32bf9db301f47afeef3636345eadae33b2eee` |
| `WHENCE` | 425450 | `c282239a5a2d849677e9304e6f361e475e1b6e71e7c771c03f8986f71b309527` |
