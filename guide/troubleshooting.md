# Troubleshooting

Here are the snags people hit most, and how to get past them.

## macOS says the app is damaged, or still won't open it

First try the steps in [The first time you open it](install-mac.md#the-first-time-you-open-it).
If macOS still refuses, or says the app is damaged, run this in Terminal:

```bash
xattr -dr com.apple.quarantine "/Applications/Pat In Key.app"
```

Then open the app again.

## Windows says "Windows protected your PC"

That's because the app isn't code-signed.
Choose **More info**, then **Run anyway**.
You only need to do this once.

## The app can't update itself

The app has to be able to write to its own folder.
On a Mac, move `Pat In Key.app` into **Applications** before you open it.
On Windows, keep the `Pat In Key` folder somewhere like Documents, not `Program Files`.
If it still can't write there, it says so and offers the download page instead.
[Updating](updating.md) has the rest.

## Tracks show as missing in rekordbox, Serato or Traktor

Those apps find tracks by file name and folder.
So a track you renamed shows as missing until you relink it in that app.
For tracks already in your library, untick **Rename files** in **Settings** and only write tags.
[First steps](first-steps.md#before-your-first-real-run) explains more.

## rekordbox doesn't show the new key or BPM

rekordbox needs to read the tags again.
Select the tracks, right-click and choose **Reload Tags**.

## rekordbox swaps the key for its own

Leave **KEY** unticked in rekordbox's **Preferences > Analysis**, and in any Analysis Setting box.

## Importing into rekordbox replaced my cues

Export your rekordbox collection first, and pick it with **Choose XML...** in **Settings**.
Pat In Key then leaves the tracks you cued alone.
[Cues for rekordbox](rekordbox-cues.md#keep-the-cues-you-already-set) has the steps.

## A stick is refused

The export dialog says why, and nothing on the stick has changed.
A stick that already holds a rekordbox library is always refused, so use a spare one.
[USB sticks](usb.md) has more.

## A sync is refused

Close Serato, Traktor or Engine DJ first.
A sync is refused while the other app is open.

## I want to take an Apply back

**Undo last Apply**, the round arrow beside **Export to USB...**, puts the old names and tags back.
