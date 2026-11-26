# Installing the Mitsumete Knight R: Daibouken-hen English translation (v1.0)

The download contains only the changes to the game's disc image, not the game. You need your
own disc image of Mitsumete Knight R - Daibouken-hen (Japan), the Redump version.

## What you need

- The Redump version of **Mitsumete Knight R - Daibouken-hen (Japan)** (product code
  SLPM-86134): one `.cue` and one `.bin`. The disc has a single data track.
- The file that gets patched must be exactly:

  | File | Size | SHA-1 |
  |---|---|---|
  | `Mitsumete Knight R - Daibouken-hen (Japan).bin` | 747,764,304 bytes | `4f4f9aadbe78d00b4b71c026325b5c59d6c82bd6` |

  With any other file the patch refuses to apply.
- xdelta3, or a front end for it such as Delta Patcher or xdelta UI. Rom Patcher JS in a web
  browser also applies `.xdelta` files. The download does not include a patching program.
- A PlayStation emulator. Tested in DuckStation. Not tested on real hardware.

## What is in the zip

| File | What it is |
|---|---|
| `MitsumeteKnightR-EN-v1.0.xdelta` | The patch |
| `Mitsumete Knight R (English).cue` | Optional cue sheet, only for the side-by-side alternative below. Most people do not need it |
| `README.txt` | The release notes |

## How to apply

Patch the `.bin` with the `.xdelta`. Keep the file name, and open your usual `.cue`. That is all.

### With Delta Patcher

1. Original file = your `Mitsumete Knight R - Daibouken-hen (Japan).bin`
2. XDelta patch = `MitsumeteKnightR-EN-v1.0.xdelta`
3. Tick Backup original file in the settings, then Apply patch.

### With the command line

xdelta3 writes a new file, so rename the original first:

```
ren "Mitsumete Knight R - Daibouken-hen (Japan).bin" "original.bin"
xdelta3 -d -s "original.bin" MitsumeteKnightR-EN-v1.0.xdelta "Mitsumete Knight R - Daibouken-hen (Japan).bin"
```

### Check the result

The patched file is 747,764,304 bytes with this SHA-1 checksum:

| File | SHA-1 after patching |
|---|---|
| Patched `.bin` | `2b2832293e6e83badca6a848300a05d723e8e1ee` |

## Alternative: keep the Japanese and English discs side by side

Leave your file alone, save the patched file as `Mitsumete Knight R (English).bin` in the same
folder, and open `Mitsumete Knight R (English).cue` from the zip.

## After patching

Start a new game. A save made with the Japanese game stores the hero's name in Japanese
letters, which the English game cannot show properly. A save state made on the Japanese game
keeps the old program and text in memory, so load the game normally instead.

Controls: Circle confirms, Cross cancels, Triangle opens the menu, the D-pad moves.
