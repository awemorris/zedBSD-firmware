# amlogic-s7d

**An unmodified copy of Hardkernel's official ODROID-C5 image, redistributed
only for use on the Hardkernel ODROID-C5** (see "License" below).

```
Firmware: Hardkernel's official ODROID-C5 Ubuntu image,
          ubuntu-22.04-gnome-desktop-odroidc5-20260610-bsp-boot.img.xz,
          kept for its bootloader: Amlogic's boot stages (BL2 and the stages
          it loads, BL30, BL31 and BL32, signed and encrypted for the
          S905X5M) and Hardkernel's U-Boot (BL33), in the image's sectors 1
          to 6538, between the MBR and the first partition (sector 16384)
Hardware: Hardkernel ODROID-C5 (Amlogic S905X5M, SoC family S7D; the BL30 in
          the image names itself "S7D-s905x5m-26052812")
Use:      zedBSD's ODROID-C5 image build (package amlogic-s7d-bootloader)
          decompresses the image, takes its sectors 1 to 6538 and writes them
          to the SD card from sector 1, where Hardkernel's image has them;
          the MBR's boot code stays zero. Nothing else of the image is used.
Source:   Hardkernel's download site for the ODROID-C5 (dn.odroid.com; the
          site's exact path was not recorded), file
          ubuntu-22.04-gnome-desktop-odroidc5-20260610-bsp-boot.img.xz,
          37760380 bytes, SHA-256
          04b9817d4e5e27ac4cc46dc4ad48fbc164e9a6c6f42eb1b0ba8d7a927accc5f2,
          kept here byte for byte under its own name.

Copyright (C) 2018 Amlogic, Inc. (the boot stages BL2 to BL32)
Copyright the U-Boot authors and Hardkernel Co., Ltd. (U-Boot)
Copyright the respective authors (the rest of the image; zedBSD uses none
of it)
```

The image uncompresses to 545259520 bytes (520 MiB). Its MBR has zero boot
code, the signature 55aa and one partition (type 0x83) from sector 16384.
Sectors 1 to 6538 (bytes 512 to 3347967, 3347456 bytes) have the SHA-256
`6c5316ed320c78c9c2a67665cdee1089339be25bee625cf1eaffb0a6277c6562`; sectors
6539 to 16383 are all zero, and sectors 1 to 16383 have the SHA-256
`b6a4b424f0a6dac33be4287d2bad6f2651466d983ca9e4146a29357b8e3c8cba`. The same
bytes come from

```
xz -dc ubuntu-22.04-gnome-desktop-odroidc5-20260610-bsp-boot.img.xz |
    head -c 3347968 | tail -c 3347456 > bootloader.bin
```

## License

[`LICENSE.amlogic`](LICENSE.amlogic) is Amlogic's license for its boot
stages. It forbids redistribution and use without Amlogic's prior written
permission.

Amlogic has given that prior written permission to Hardkernel, which
distributes these boot stages in its images made for the ODROID-C5, and such
an image, which can be used only on this board, may be redistributed. On
that basis the owner of this repository judged that the permission covers
the use of the boot stages on the ODROID-C5, and that Hardkernel's image may
be redistributed, unmodified, for use on that board. Accordingly:

- The image here is an unmodified copy of Hardkernel's official image, under
  its original name. It is redistributed only for use on the Hardkernel
  ODROID-C5.
- Use it, and the boot stages in it, only on a Hardkernel ODROID-C5. Do not
  use them on any other board or for any other purpose.
- Redistribute it only unmodified, with `LICENSE.amlogic` and this README,
  and only for use on the ODROID-C5.
- The boot ROM accepts only stages signed for the S905X5M, so they are used
  as they are; nothing here is modified, re-signed or rebuilt.

U-Boot (BL33) is under the GNU General Public License version 2. Its
corresponding source is Hardkernel's: the submodule `bl33/v2023` of the
branch `odroidc5-v2023.01` of https://github.com/hardkernel/u-boot (commit
c99f3409d5cad031b365fd871e543f97af893f88), which points to
https://git.odroid.com/yocto/uboot, branch `odroidc5-v2023.01`. That source
is not in this directory. The rest of the image (Ubuntu and Hardkernel's
Linux kernel) is under the licenses of its own components, as Hardkernel
distributes it; zedBSD uses none of it.

## Files

| File | Size | SHA-256 |
| --- | ---: | --- |
| `ubuntu-22.04-gnome-desktop-odroidc5-20260610-bsp-boot.img.xz` | 37760380 | `04b9817d4e5e27ac4cc46dc4ad48fbc164e9a6c6f42eb1b0ba8d7a927accc5f2` |
| `LICENSE.amlogic` | 1273 | `5e8f7ad650a0af4a14ad5641817323f654d0e1b8dc2019aa6f0944ba9108ff65` |
