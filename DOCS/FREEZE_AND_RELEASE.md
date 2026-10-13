# Freeze and release workflow

The public `.amxd` should be frozen before distribution.

## Why freeze the device?

Freezing prepares a Max for Live device for distribution by embedding the files it depends on into the `.amxd`.

This helps avoid missing images, abstractions, JavaScript files, external assets or other patch dependencies.

## Recommended working files

Keep a separate development copy and release copy:

```text
Electribe_ES-1_Bridge_DEV.amxd
Electribe_ES-1_Bridge.amxd
```

Use the DEV file for future editing.

Use the frozen file for GitHub Releases and public downloads.

## Freeze procedure

1. Open the release copy in the Max for Live editor.
2. Save a development backup first.
3. Click **Freeze Device** (snowflake icon) in the Max patcher toolbar.
4. Choose **File → Save**.
5. Close the Max editor.
6. Reload the device in Ableton Live.

## Release validation

Before publishing:

- [ ] Device is frozen and saved
- [ ] Device reloads correctly after closing Live
- [ ] No missing-file errors
- [ ] ES-1 → Max control works
- [ ] Max → ES-1 control works
- [ ] Parts 1–5 work
- [ ] Parts 6A / 6B work
- [ ] Parts 7A / 7B work
- [ ] Slice works
- [ ] Effect On / Off works
- [ ] Reverse works
- [ ] Effect Type covers 0–10
- [ ] Edit 1 works
- [ ] Edit 2 works
- [ ] Delay Depth works
- [ ] Delay Time works
- [ ] BPM Sync works
- [ ] Part View works
- [ ] Audio routing does not create doubled monitoring
- [ ] README is current
- [ ] CHANGELOG is current
- [ ] Screenshot added to `IMAGES/`
- [ ] License and original attribution are present
- [ ] Git tag created
- [ ] GitHub Release created

## Suggested first release

Tag:

`v1.0.0`

Release title:

`Electribe ES-1 Bridge v1.0.0`

Attach the frozen:

`Electribe_ES-1_Bridge.amxd`
