# rpi4-boot

```
Firmware: Raspberry Pi 4 boot firmware: the GPU firmware (start4.elf, fixup4.dat),
          the board's device tree and the disable-bt overlay
Hardware: Raspberry Pi 4 Model B (BCM2711)
Files:    the SD card's boot partition: /start4.elf, /fixup4.dat,
          /bcm2711-rpi-4-b.dtb, /overlays/disable-bt.dtbo, /LICENCE.broadcom
Source:   raspberrypi/firmware commit 3d301dd924bcd758a4c8cb19fe8531031f033f43 (boot/)

Copyright (c) 2006, Broadcom Corporation.
Copyright (c) 2015, Raspberry Pi (Trading) Ltd
The device tree files are GPL-2.0, built from raspberrypi/linux commit
89586905b8603e545cce9089a81f5f35d65bc998 (arch/arm/boot/dts/broadcom/bcm2711-rpi-4-b.dts,
arch/arm/boot/dts/overlays/disable-bt-overlay.dts). The license below is the
one of start4.elf and fixup4.dat.
```

## License

- [`LICENCE.broadcom`](LICENCE.broadcom)
- [`COPYING.linux`](COPYING.linux)

start4.elf and fixup4.dat (LICENCE.broadcom): redistribution and use in binary form without modification, with the copyright notice and the disclaimer, and only for developing for, running or using a Raspberry Pi device. bcm2711-rpi-4-b.dtb and overlays/disable-bt.dtbo: GPL-2.0 (COPYING.linux); their complete source is in source/ (below).

The files are unmodified copies of the upstream files named above. Read the license before you
redistribute or use them.

## Files

| File | Size | SHA-256 |
| --- | ---: | --- |
| `start4.elf` | 2298048 | `6d540ddf77623976ba60de630e9300a5a099f7710e11ee85a7bf076f5931f4bc` |
| `fixup4.dat` | 5512 | `5818b069814c7f051d4c9246307dced983bcbdcc6a90d9e5491fc5c68159d077` |
| `bcm2711-rpi-4-b.dtb` | 56407 | `75761b73c284e26623e4d1624bff13e67bce2ae620880efd81d6571a3739fcfb` |
| `overlays/disable-bt.dtbo` | 1073 | `ea69d22dedc607fee75eec57d8a4cc0f0eab93cd75393e61a64c49fbac912d02` |
| `LICENCE.broadcom` | 1594 | `c7283ff51f863d93a275c66e3b4cb08021a5dd4d8c1e7acc47d872fbe52d3d6b` |
| `COPYING.linux` | 18693 | `af8067302947c01fd9eee72befa54c7e3ef8a48fecde7fd71277f2290b2bf0f7` |

## Device tree source

`bcm2711-rpi-4-b.dtb` and `overlays/disable-bt.dtbo` are GPL-2.0. Their
complete source is in `source/`, with the paths it has in
[raspberrypi/linux](https://github.com/raspberrypi/linux) at commit
`89586905b8603e545cce9089a81f5f35d65bc998` (the commit the firmware commit's
`extra/git_hash` names): the two `.dts` files, every `.dtsi` they include, and
the `include/dt-bindings/` headers those include.

- `source/arch/arm/boot/dts/broadcom/bcm2711-rpi-4-b.dts` (the 64-bit
  `source/arch/arm64/boot/dts/broadcom/bcm2711-rpi-4-b.dts` includes it)
- `source/arch/arm/boot/dts/overlays/disable-bt-overlay.dts`

With the C preprocessor and dtc 1.7.2, these commands make files identical,
byte for byte, to the ones in this directory:

```sh
cd source
cpp -nostdinc -I include -I arch/arm/boot/dts -I arch/arm/boot/dts/broadcom \
    -undef -D__DTS__ -x assembler-with-cpp \
    arch/arm/boot/dts/broadcom/bcm2711-rpi-4-b.dts |
    dtc -@ -q -I dts -O dtb -o bcm2711-rpi-4-b.dtb -
cpp -nostdinc -I include -I arch/arm/boot/dts -undef -D__DTS__ \
    -x assembler-with-cpp arch/arm/boot/dts/overlays/disable-bt-overlay.dts |
    dtc -@ -q -I dts -O dtb -o disable-bt.dtbo -
```

The files under `source/` are covered by `COPYING.linux` (GPL-2.0) and by the
license each file names in its SPDX line.
