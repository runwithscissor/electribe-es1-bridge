# MIDI implementation notes

Electribe ES-1 Bridge uses the Korg ES-1 MIDI implementation, including NRPN-based parameter communication.

## NRPN structure

The ES-1 uses:

- CC 99 — NRPN MSB
- CC 98 — NRPN LSB
- CC 6 — Data Entry MSB
- CC 38 — Data Entry LSB

The ES-1 uses the Data Entry MSB value for parameter control.

## Global Effect and Delay NRPN parameters

| NRPN | Parameter | Range |
|---|---|---:|
| 05 60 | Delay Depth | 0–127 |
| 05 61 | Delay Time | 0–127 |
| 05 62 | Effect Type | 0–10 |
| 05 63 | Effect Param 1 | 0–127 |
| 05 64 | Effect Param 2 | 0–127 |
| 05 65 | BPM Delay Sync | 0–1 |

The NRPN bytes above are shown in hexadecimal notation, following the ES-1 MIDI implementation documentation.

For example, `05 62` means:

- NRPN MSB = `0x05`
- NRPN LSB = `0x62` = decimal `98`

The Effect Type value itself is carried by Data Entry MSB (CC 6) in the range 0–10.

## Effect Type values

| Value | Effect |
|---:|---|
| 0 | Reverb |
| 1 | Flanger / Chorus |
| 2 | Phaser |
| 3 | Ring Modulator |
| 4 | Pitch Shifter |
| 5 | Compressor |
| 6 | Distortion |
| 7 | Decimator |
| 8 | Isolator |
| 9 | Resonant Filter |
| 10 | Wah |

## Debugging advice

When troubleshooting hardware → Max behavior, inspect the raw MIDI data before changing the patch.

If the expected NRPN selector is present but the CC 6 value is wrong or missing, the Max device is receiving incorrect hardware data and cannot reconstruct the intended parameter value.
