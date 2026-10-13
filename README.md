# Electribe ES-1 Bridge

**Bidirectional Max for Live controller for the Korg Electribe ES-1**

Electribe ES-1 Bridge brings the main controls of the Korg Electribe ES-1 into Ableton Live while preserving hands-on control from the hardware itself.

The device provides **bidirectional MIDI/NRPN communication**: changes made on the ES-1 are reflected in Max for Live, and changes made in the Max for Live device are sent back to the ES-1.

> Independent community project. Not affiliated with or endorsed by Korg, Ableton, or Cycling '74.

## Features

- Bidirectional ES-1 ↔ Max for Live control
- Individual control for:
  - Part 1
  - Part 2
  - Part 3
  - Part 4
  - Part 5
  - Part 6A
  - Part 6B
  - Part 7A
  - Part 7B
  - Slice
- Per-part controls:
  - Pitch / Speed
  - Filter
  - Level
  - Pan
  - Effect On / Off
  - Reverse On / Off
- Global Effect section:
  - Effect Type
  - Edit 1
  - Edit 2
- Global Delay section:
  - Depth
  - Time
  - BPM Sync
- Custom presentation-mode interface
- Part View selector for focused editing
- Hardware feedback from incoming MIDI/NRPN data

## Requirements

- Korg Electribe ES-1
- Ableton Live with Max for Live
- MIDI interface with MIDI IN and MIDI OUT
- Two standard 5-pin MIDI cables for full bidirectional operation

### Tested with

- Ableton Live 12
- Max 8.6.5
- Windows x64
- Korg Electribe ES-1 mk1

Other configurations may work but have not yet been formally tested.

## Installation

1. Download `Electribe_ES-1_Bridge.amxd`.
2. Copy it into your Ableton User Library or any folder indexed by Ableton Live.
3. Connect the ES-1 MIDI OUT to your MIDI interface IN.
4. Connect the MIDI interface OUT to the ES-1 MIDI IN.
5. Load the device on the MIDI track used for the ES-1.
6. Configure the track MIDI input so the device receives data from the ES-1.

For the full setup procedure, see [DOCS/SETUP.md](DOCS/SETUP.md).

## MIDI channel

The ES-1 factory MIDI channel is **11**.

If your ES-1 uses another MIDI channel, set Ableton Live to receive from the channel currently configured on the hardware.

## Effect section

Electribe ES-1 Bridge exposes all 11 ES-1 effect types:

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

The ES-1 uses one global effect type per pattern. Each part can independently enable or disable its Effect switch.

## Delay section

Delay is global to the pattern and provides:

- Depth
- Time
- BPM Sync

BPM Sync links Delay Time to the current pattern tempo.

## Documentation

- [Setup](DOCS/SETUP.md)
- [Troubleshooting](DOCS/TROUBLESHOOTING.md)
- [Freeze & release workflow](DOCS/FREEZE_AND_RELEASE.md)
- [MIDI implementation notes](DOCS/MIDI_NOTES.md)
- [Credits & provenance](CREDITS.md)
- [Changelog](CHANGELOG.md)
- [Contributing](CONTRIBUTING.md)
- [License](LICENSE.md)

## Versioning

The project follows semantic-style versioning:

- `v1.0.0` — first stable public release
- `v1.0.1` — bug fix
- `v1.1.0` — backwards-compatible feature update
- `v2.0.0` — major revision or breaking change

The distributed device remains named:

`Electribe_ES-1_Bridge.amxd`

Versions are tracked through Git tags and GitHub Releases rather than appended to the filename.

## Project status

**v1.0.0 — first public release**

Core bidirectional control, effect handling, delay handling and per-part control have been tested in a real ES-1 + Ableton Live setup.

## Acknowledgements

Electribe ES-1 Bridge is based on and substantially reworks **Electribe ES1 Full Kontrol v1.25** by **okan**, originally published on maxforlive.com in 2010 under an **AttributionNonCommercial** license.

Original device:
https://maxforlive.com/library/device/335/electribe-es1-full-kontrol

The original device provided the starting point for ES-1 control in Max for Live. Electribe ES-1 Bridge adds a redesigned interface, direct bidirectional MIDI/NRPN handling, updated routing logic, expanded hardware feedback, documentation, troubleshooting and a modern release workflow.

See [CREDITS.md](CREDITS.md) for full provenance.

## License

Electribe ES-1 Bridge is distributed for **non-commercial use** under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license.

Portions derived from **Electribe ES1 Full Kontrol v1.25** remain subject to the original AttributionNonCommercial terms under which that device was published.

See [LICENSE.md](LICENSE.md).

## Author

Project redevelopment, interface redesign and documentation by [runwithscissor](https://github.com/runwithscissor).

Feedback, bug reports and compatibility reports are welcome through GitHub Issues.
