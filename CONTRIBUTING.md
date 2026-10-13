# Contributing

Bug reports, compatibility reports and improvements are welcome.

## License condition

Contributions must be compatible with this project's **non-commercial** distribution terms and with the attribution requirements inherited from the original **Electribe ES1 Full Kontrol v1.25** by okan.

By submitting a contribution, you confirm that you have the right to contribute that material to this project under those terms.

## Bug reports

Please include:

- Ableton Live version
- Max version
- operating system
- MIDI interface
- ES-1 MIDI channel
- affected parameter
- whether the issue occurs:
  - ES-1 → Max
  - Max → ES-1
  - both directions
- steps to reproduce
- MIDI Monitor output when relevant

## Pull requests

Keep changes focused.

Any changes to MIDI/NRPN handling should be documented and tested in both directions.

Before submitting a pull request, verify:

- per-part controls;
- Effect Type;
- Edit 1 / Edit 2;
- Delay controls;
- Part View;
- hardware feedback.

## Release builds

Do not replace the public release `.amxd` without testing a frozen build.

See `DOCS/FREEZE_AND_RELEASE.md`.
