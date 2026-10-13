# Troubleshooting

## The Max device controls the ES-1, but the ES-1 does not control the Max device

Check the incoming MIDI path:

```text
ES-1 MIDI OUT → MIDI interface IN → Ableton MIDI track → Electribe ES-1 Bridge
```

Make sure:

- the correct MIDI input port is selected;
- the correct MIDI channel is selected;
- Track input monitoring allows the device to receive ES-1 MIDI data.

A MIDI Monitor placed before the device is useful for confirming whether the ES-1 is actually transmitting data.

## The ES-1 controls the Max device, but Max does not control the ES-1

Check:

```text
Ableton MIDI track → MIDI interface OUT → ES-1 MIDI IN
```

Make sure the correct output port is selected and the ES-1 is receiving on the expected MIDI channel.

## Audio sounds doubled

This is normally an audio-monitoring issue rather than a MIDI issue.

If using **External Instrument**, do not also monitor the same physical ES-1 input through a separate audio track or another parallel input path.

## Effect Type jumps, skips values or gets stuck

The Effect Type parameter range is 0–10.

Use a MIDI Monitor before Electribe ES-1 Bridge and move the physical Effect Type selector.

If the incoming Data Entry values themselves are missing or unstable, the problem is upstream of the Max device.

On older ES-1 units, a worn Effect Type potentiometer can cause:

- skipped effect positions;
- sudden jumps to Wah;
- unstable intermediate values;
- values only registering when pressure is applied to the shaft.

If MIDI Monitor already shows incorrect values, investigate the ES-1 hardware.

## Delay controls appear inactive

Test Delay while the pattern is running.

Delay Depth and Time are global pattern parameters, and BPM Sync changes how Delay Time relates to tempo.

## The device loads but assets are missing

Use the frozen release build of the `.amxd`.

See `DOCS/FREEZE_AND_RELEASE.md`.

## Hardware → Max works only when Track Monitor is set to In

The device must receive the incoming MIDI stream from the ES-1.

If changing Track Monitor to **In** causes doubled audio, correct the audio path separately rather than disabling the MIDI receive path.

Use External Instrument or a single dedicated audio return so that MIDI monitoring and audio monitoring do not create duplicate audio paths.
