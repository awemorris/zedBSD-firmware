# rpi5-boot

```
Firmware: Raspberry Pi 5 boot files: the board's device trees (the BCM2712 C1
          and D0 steppings); the bootloader itself is in the board's EEPROM
Hardware: Raspberry Pi 5 (BCM2712)
Files:    the SD card's boot partition: /bcm2712-rpi-5-b.dtb,
          /bcm2712d0-rpi-5-b.dtb, /COPYING.linux
Source:   raspberrypi/firmware commit 3d301dd924bcd758a4c8cb19fe8531031f033f43 (boot/)

The device tree files are GPL-2.0, built from raspberrypi/linux commit
89586905b8603e545cce9089a81f5f35d65bc998 (arch/arm64/boot/dts/broadcom/
bcm2712-rpi-5-b.dts and bcm2712d0-rpi-5-b.dts with the files they include).
The license below is the one of the device trees.
```

## License

- [`COPYING.linux`](COPYING.linux)

bcm2712-rpi-5-b.dtb and bcm2712d0-rpi-5-b.dtb: GPL-2.0 (COPYING.linux); their complete source is in source/ (below).

The files are unmodified copies of the upstream files named above. Read the license before you
redistribute or use them.

## Files

| File | Size | SHA-256 |
| --- | ---: | --- |
| `bcm2712-rpi-5-b.dtb` | 78703 | `40a2fbe9c29e8b9a4912cf726a943068defb779fc052ec38e457a79c58abca00` |
| `bcm2712d0-rpi-5-b.dtb` | 78707 | `03d80fc8196bfd113f86534c60ee2cb35ba95ae182e34a42f66caf7fa15f48ba` |
| `COPYING.linux` | 18693 | `af8067302947c01fd9eee72befa54c7e3ef8a48fecde7fd71277f2290b2bf0f7` |

## Device tree source

`bcm2712-rpi-5-b.dtb` and `bcm2712d0-rpi-5-b.dtb` are GPL-2.0. Their
complete source is in `source/`, with the paths it has in
[raspberrypi/linux](https://github.com/raspberrypi/linux) at commit
`89586905b8603e545cce9089a81f5f35d65bc998` (the commit the firmware commit's
`extra/git_hash` names): the two `.dts` files, every `.dtsi` they include, and
the `include/dt-bindings/` headers those include.

- `source/arch/arm64/boot/dts/broadcom/bcm2712-rpi-5-b.dts`
- `source/arch/arm64/boot/dts/broadcom/bcm2712d0-rpi-5-b.dts`

With the C preprocessor and dtc 1.7.2, these commands make files identical,
byte for byte, to the ones in this directory:

```sh
cd source
for name in bcm2712-rpi-5-b bcm2712d0-rpi-5-b; do
    cpp -nostdinc -I include -I arch/arm64/boot/dts -I arch/arm64/boot/dts/broadcom \
        -undef -D__DTS__ -x assembler-with-cpp \
        arch/arm64/boot/dts/broadcom/$name.dts |
        dtc -@ -q -I dts -O dtb -o $name.dtb -
done
```

The files under `source/` are covered by `COPYING.linux` (GPL-2.0) and by the
license each file names in its SPDX line.
