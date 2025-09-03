## To install qmk firmware:

1. `brew install qmk/qmk/qmk`
1. `brew install --cask gcc-arm-embedded`
1. `brew install avr-gcc`
1. `qmk setup`

## To install vial-qmk firmware:

1. `git clone https://github.com/vial-kb/vial-qmk`
1. `cd vial-qmk`
1. `make git-submodule`
1. `qmk compile -kb sofleplus2 -km tps65-403c`
1. or `make sofleplus2`

## To configure keyboard:

1. In keymaps/tps65-403c/config.h set `#define EE_HANDS` for right keyboard and `#define MASTER_LEFT` for left keyboard
1. Build firmware using: `make sofleplus2`
1. On bottom of keyboard double-tap reset button to enter bootloader
1. Open Finder and drag and drop .build/sofleplus2_tps65-403c.uf2 to the newly mounted drive
1. In Vial set `Tapping Term` to 100 and `Quick Tap Term` to 50 to enable tap-hold without lag
1. In Vial turn off `Hold On Other Key Press` to prevent tap-hold button to be stuck in a triggered state when typing using tap-hold button too often

### Links:

-   [Firmware Compilation](https://xcmkb-docs.gitbook.io/doc/troubleshooting/wired-build#firmware-compilation)
-   [QMK Getting Started](https://docs.qmk.fm/newbs_getting_started#set-up-your-environment)
-   [Porting to Vial](https://get.vial.today/docs/porting-to-vial.html

### Additional links

-   [Vial Documentation](https://vial-kb.gitbook.io/vial/)
-   [Vial GitHub](https://github.com/vial-kb/vial)
-   [QMK Documentation](https://docs.qmk.fm)
-   [QMK GitHub](https://github.com/qmk/qmk_firmware)
