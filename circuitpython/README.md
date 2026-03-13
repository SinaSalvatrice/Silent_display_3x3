# CircuitPython Firmware Folder

This folder contains a complete CircuitPython firmware sketch for the same 3x3 + encoder hardware.

Main firmware file:

- `code.py`

## Required Libraries

Copy the libraries listed in `lib/requirements.txt` from the latest Adafruit CircuitPython bundle to `CIRCUITPY/lib`.

## Hardware Mapping

- Matrix rows: GP2, GP3, GP4
- Matrix cols: GP5, GP6, GP7
- Encoder A/B: GP8, GP9
- Encoder button: GP10
- OLED I2C: SDA GP0, SCL GP1 (SSD1306, 128x64, addr 0x3C)
- WS2812 LEDs: GP15 (count: 9)

## Notes

- The code implements 9 layers.
- Encoder hold+turn cycles layers 0..8.
- Encoder click actions vary by active layer.
- If your matrix wiring is inverted, flip `columns_to_anodes` in `code.py`.
