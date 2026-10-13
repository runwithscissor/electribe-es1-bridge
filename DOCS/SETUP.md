# Setup

## Hardware connections

For full bidirectional control, both MIDI directions are required:

```text
Korg ES-1 MIDI OUT  ─────►  MIDI interface IN
Korg ES-1 MIDI IN   ◄─────  MIDI interface OUT
```

Audio routing is independent from MIDI routing.

Connect the ES-1 audio outputs to your audio interface as usual.

## Ableton Live track setup

1. Create a MIDI track for the ES-1.
2. Load `Electribe_ES-1_Bridge.amxd` on the track.
3. Set **MIDI From** to the MIDI input receiving data from the ES-1.
4. Select the ES-1 MIDI channel.

The factory default ES-1 MIDI channel is **11**.

5. Route MIDI output from the track to the MIDI interface port connected to the ES-1 MIDI IN.

## Bidirectional control test

### ES-1 → Ableton Live

Move a physical ES-1 control such as Filter or Level.

The corresponding control in Electribe ES-1 Bridge should move.

### Ableton Live → ES-1

Move the same control in Electribe ES-1 Bridge.

The ES-1 should respond immediately.

Repeat the test with:

- Effect On / Off
- Reverse
- Effect Type
- Edit 1
- Edit 2
- Delay Depth
- Delay Time
- BPM Sync

## Part View

The Part View selector can display:

- Show All
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

Part View changes what is visible in the interface; it does not alter the ES-1's underlying MIDI parameter mapping.

## Audio monitoring

If you use Ableton Live's **External Instrument** device for the ES-1, use its audio return as the primary monitoring path.

Avoid monitoring the same ES-1 audio input through a second parallel Ableton input path at the same time, otherwise the signal may sound doubled or phasey.

## Recommended first-session check

After loading the device:

1. Test one part's Filter and Level.
2. Test Effect and Reverse.
3. Test Effect Type across all 11 positions.
4. Test Edit 1 and Edit 2.
5. Start the pattern and test Delay Depth and Time.
6. Enable and disable BPM Sync.
7. Confirm control works in both directions.
