# splitshock46 pin notes

This ZMK port is configured for a fully wireless nice!nano v2 split.

The QMK source used RP2040 `GPx` names. In this first ZMK port those are
translated as direct nice!nano nRF GPIO port 0 numbers:

- Columns, left: P0.14, P0.13, P0.12, P0.11, P0.10, P0.09, P0.08
- Columns, right: P0.08, P0.09, P0.10, P0.11, P0.12, P0.13, P0.14
- Rows: P0.02, P0.03, P0.06, P0.07, P0.28
- Encoder, left: A=P0.26, B=P0.15
- Encoder, right: A=P0.15, B=P0.26

If the PCB was routed by Pro Micro header labels instead of MCU GPIO labels,
replace the GPIO references in the two overlay files and `splitshock46.dtsi`
with `&pro_micro <pin>` references that match the actual nets.
