# Wingflight Targets

Board configurations for [Wingflight](https://github.com/WingFlight/wingflight-firmware), the
open-source flight controller firmware for fixed-wing aircraft.

Wingflight builds one firmware per MCU family (STM32F405, STM32F411, STM32F7X2, STM32F745,
STM32G47X, STM32H743). What makes it fit a particular flight controller is a configuration applied
on top: the board's sensors, pins, timers and defaults. Those configurations ("custom defaults")
live here.

The Firmware Flasher in the [Wingflight Configurator](https://github.com/WingFlight/wingflight-configurator)
loads its list of boards straight from this repository, so a board added here shows up in the
Configurator without a new release.

## Layout

- `configs/` holds one file per board, named `<MANUFACTURER>-<BOARD>.config`, for example
  `FRSK-VANTAC_RF007.config`. The manufacturer is a four-letter code.
- `tools/` holds scripts for comparing and filtering config files.

## Adding or changing a board

Open a pull request with the board's `.config` file. Say which flight controller it is for and how
you tested it (flashed, sensors detected, outputs working).

## More

- [Flashing the Firmware](https://doc.wingflight.org/getting-started/flashing-the-firmware/)
- [Documentation](https://doc.wingflight.org) · [Discord](https://discord.gg/aEyyAJTXRw)
