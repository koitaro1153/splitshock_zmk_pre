# splitshock46 ZMK

ZMK firmware configuration for splitshock46.

This configuration targets a fully wireless split build using nice!nano v2
controllers.

## Build targets

The GitHub Actions build matrix in `build.yaml` produces:

- `splitshock46_left`
- `splitshock46_right`
- `splitshock46_settings_reset`

## Source

The layout and behavior were ported from the QMK `splitshock46_qmk`
configuration:

- 5 row x 7 column matrix per half
- COL2ROW diode direction
- base and number layers
- `-` / `@` tap dance
- Enter layer-tap for the number layer
- caps word toggle
- EC11 encoder support on both halves

## Pin notes

The original QMK project used RP2040 `GPx` pin names. This ZMK port maps those
as direct nice!nano nRF GPIO port 0 pins for the first pass. If your PCB wiring
uses Pro Micro header labels instead of MCU GPIO labels, update the GPIO
references in:

- `boards/shields/splitshock46/splitshock46.dtsi`
- `boards/shields/splitshock46/splitshock46_left.overlay`
- `boards/shields/splitshock46/splitshock46_right.overlay`

See `docs/pin-notes.md` for the current mapping.
