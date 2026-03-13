# ZMK port for silent_display_3x3

This folder contains a standalone ZMK shield/config scaffold for the 3x3 macropad.

## Included

- 3x3 matrix on RP2040 GPIO pins GP2..GP7
- EC11 encoder on GP8/GP9
- Encoder button on GP10
- SSD1306 OLED over I2C (SDA GP0, SCL GP1, address 0x3C)
- RGB underglow key bindings
- 9 total layers (0..8)

## Build (local ZMK checkout)

1. Copy or symlink this shield folder into your ZMK config/module.
2. Build for a Seeed XIAO RP2040 target:

   west build -p -b seeeduino_xiao_rp2040 -- -DSHIELD=silent_display_3x3

If you use a different RP2040 board definition in ZMK, update the board name accordingly.

## Notes

- The display integration in this port is configured as SSD1306.
- The original QMK behavior for "hold encoder button + rotate = cycle layer" is not replicated one-to-one; layer selection is provided on Layer 5 and by direct layer keys.
