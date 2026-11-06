# The command line

The command line can do anything the window does to a folder of tracks.
That's handy for scripts and big batches.
The command line runs from the source code, so you'll need Python, Node and ffmpeg.

```bash
python -m app.cli "D:/Music/New" --write-tags --rename --dry-run   # preview the new names and tags
python -m app.cli "D:/Music/New" --csv keys.csv --write-tags --rename
python -m app.cli --undo changes-20260929-141500.csv              # put the old names and tags back
```

Run the commands from the repository's root folder.
`python -m app.cli --help` lists every option.
The command line searches a folder and every folder inside it, all the way down.

## Options by task

| Task | Options | More |
| --- | --- | --- |
| Analyse and keep the results | `--csv FILE` (skips unchanged files), `--reanalyze`, `--jobs N` (default 4), `--max-minutes N` (default 40) | [Analysis](analysis.md) |
| Keys and tempo | `--key-format musical`, `--bpm-range LO HI` (default 89 178), `--no-fold` | [Analysis](analysis.md#how-it-works) |
| Write tags and names | `--write-tags`, `--rename`, `--dry-run`, `--name-format`, `--title-format`, `--energy`, `--replaygain`, `--no-art-lookup` | [Tags, names and Apply](tags.md) |
| Undo | `--undo changes-<time>.csv` | [Undo](tags.md#undo) |
| Your rekordbox collection | `--rekordbox-xml export.xml` keeps listed tracks' names and feeds the cue history | [Cue points](editor.md#cue-points) |
| Cues for rekordbox | `--cues`, `--cue-type hot\|memory\|both`, `--cue-every BARS`, `--cue-loops BARS`, `--first-bar-cue`, `--no-cue-comments`, `--cue-xml XML` | [Cue points](editor.md#cue-points) |
| Cue history | `--restore-cues`, `--restore-cues all`, `--remove-cues` | [Cue history](editor.md#cue-history) |
| Hot Cue Auto Load | `--hot-cue-auto-load on\|off` | [Hot Cue Auto Load](editor.md#hot-cue-auto-load) |
| USB sticks | `--list-usb`, `--export-usb DRIVE`, `--playlist NAME`, `--confirm-stick NAME`, `--my-settings` | [Export to USB](usb.md#export-to-usb) |

The change logs go in the same folder as the `--csv` file.
Without `--csv`, they go in the current folder.
The command line can't see the edits you make in the [track editor](editor.md#track-editor).
It can't see the name formats you set in the window either.
