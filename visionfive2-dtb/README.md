# visionfive2-dtb

```
Firmware: StarFive VisionFive 2 device trees (board revisions v1.2a and v1.3b),
          compiled by zedBSD from the mainline Linux sources
Hardware: StarFive VisionFive 2 (JH7110)
Files:    the EFI system partition: /dtb/jh7110-starfive-visionfive-2-v1.2a.dtb,
          /dtb/jh7110-starfive-visionfive-2-v1.3b.dtb (and the same files below
          /dtb/starfive/), /dtb/LICENSE
Source:   Linux v6.12, torvalds/linux commit adc218676eef25575469234709c2d87185ca223a
          (arch/riscv/boot/dts/starfive/, include/dt-bindings/)

Copyright (C) 2022 Emil Renner Berthing <kernel@esmil.dk>
Copyright (C) 2022-2023 StarFive Technology Co., Ltd.
Copyright (C) 2013 Texas Instruments
```

## License

- [`LICENSE`](LICENSE)
- [`source/COPYING`](source/COPYING), [`source/LICENSES/preferred/`](source/LICENSES/preferred/)

The device tree sources are GPL-2.0 OR MIT (the GPIO and power-domain headers
GPL-2.0 OR BSD-2-Clause); zedBSD distributes the compiled device trees under
the MIT license (`LICENSE`), with the copyright notice and the permission notice.
The thermal header in `source/zedbsd/` is zedBSD's own (Zlib).

Unlike the other directories, these two files are not an upstream's binaries:
zedBSD compiles them from the unmodified Linux sources in `source/` (below),
and keeps the result here so that a zedBSD build need not fetch and compile
the sources.

## Files

| File | Size | SHA-256 |
| --- | ---: | --- |
| `jh7110-starfive-visionfive-2-v1.2a.dtb` | 31655 | `e76b80a6ea4e3f1642865b0d7205ae20aa0195c1e218936150ba594e11fc39d0` |
| `jh7110-starfive-visionfive-2-v1.3b.dtb` | 32040 | `1826e14d92c1ca336919f810f8f6c98102ed0065a9b9581087cf933b27f347ac` |
| `LICENSE` | 1654 | `720f9755f679ff22a7486de0df13309bf6394e9c17b1966a3ddd0538dbf61823` |

## Device tree source

`source/` holds, with the paths they have in
[torvalds/linux](https://github.com/torvalds/linux) at commit
`adc218676eef25575469234709c2d87185ca223a` (v6.12), the two board `.dts`
files, the `.dtsi` and headers they include, `COPYING` and the
`LICENSES/preferred/` texts their SPDX lines name. The files are unmodified;
zedBSD's `platform/riscv64/visionfive2/dts.sources` lists their sizes and
SHA-256. Linux's `include/dt-bindings/thermal/thermal.h` (GPL-2.0-only) is
not used: `source/zedbsd/include/dt-bindings/thermal/thermal.h` supplies the
one value the device tree takes from it.

With the C preprocessor and dtc 1.7.2, these commands make files identical,
byte for byte, to the ones in this directory:

```sh
cd source
for board in v1.2a v1.3b; do
    name=jh7110-starfive-visionfive-2-$board
    cpp -nostdinc -I zedbsd/include -I include -I arch/riscv/boot/dts/starfive \
        -undef -D__DTS__ -x assembler-with-cpp \
        arch/riscv/boot/dts/starfive/$name.dts |
        dtc -q -I dts -O dtb -o $name.dtb -
done
```
