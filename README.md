# Pat In Key

Pat In Key finds the key and BPM of your DJ tracks, writes them into the files, and gives each file a tidy name.
Drop a folder of music on the window, check the results, and press Apply.

![Pat In Key with six analysed tracks, each with its key, BPM and energy](images/02-tracks.png)

- **Key and BPM:** each track gets a Camelot key (8A) or a musical key (Am), a tempo, and an energy estimate from 1 to 10.
- **Tags and names:** Apply writes the key, BPM, artist and title that rekordbox, Serato, Traktor and Mixxx read, and can rename files to `8A - 124 - Artist - Title.mp3`.
- **Cue points:** it can make hot cues or memory cues for rekordbox.
- **Track editor:** hear a track, and set its beat grid and cues by ear.
- **Cover art:** tracks with no cover can get one looked up online.
- **Undo:** **Undo last Apply** puts the old names and tags back.

It reads MP3, WAV, AIFF, FLAC, M4A/AAC, Ogg and Opus.
Your music stays on your computer: only artist, title and album are sent, for the cover art lookup, and you can turn that off.

## Download

Get the latest version from the [releases page](https://github.com/plep7/dj-key-tool/releases/latest).

| Computer | Download | Needs |
| --- | --- | --- |
| Mac | [`Pat-In-Key-mac.zip`](https://github.com/plep7/dj-key-tool/releases/latest/download/Pat-In-Key-mac.zip) | Apple silicon (M1 or later), macOS 14.4 or later |
| Windows | [`Pat-In-Key-win64.zip`](https://github.com/plep7/dj-key-tool/releases/latest/download/Pat-In-Key-win64.zip) | 64-bit Windows 10 or 11 |

Nothing else needs installing: the download carries everything the app uses.

### Check the download (optional)

Each zip has a `.sha256` file beside it on the releases page, which proves the download arrived intact.
Put both files in one folder and run this there.

On a Mac, in Terminal:

```bash
shasum -a 256 -c Pat-In-Key-mac.zip.sha256
```

It should print `Pat-In-Key-mac.zip: OK`.

On Windows, in PowerShell:

```powershell
(Get-FileHash -Algorithm SHA256 Pat-In-Key-win64.zip).Hash.ToLower()
Get-Content Pat-In-Key-win64.zip.sha256
```

The two long strings of letters and numbers should match.

## Install on a Mac

1. Double-click `Pat-In-Key-mac.zip` to unzip it.
2. Drag `Pat In Key.app` into your **Applications** folder. Do this before opening it, or the app cannot update itself later.
3. Open it from Applications, as below.

### The first time you open it

The app is not signed by an Apple-registered developer, so macOS stops it the first time.
You only need to do this once.

On macOS 14:

1. Right-click `Pat In Key.app` in Applications and choose **Open**.
2. Choose **Open** again in the message that appears.

On macOS 15 or later, or if the steps above do not offer **Open**:

1. Double-click the app, and choose **Done** when macOS says it was not opened.
2. Open **System Settings > Privacy & Security** and scroll down to **Security**.
3. Next to the line about Pat In Key, choose **Open Anyway**, and confirm with your password or Touch ID.

If macOS still refuses, or says the app is damaged, run this in Terminal and open it again:

```bash
xattr -dr com.apple.quarantine "/Applications/Pat In Key.app"
```

## Install on Windows

1. Right-click `Pat-In-Key-win64.zip`, choose **Extract All**, and pick any folder you can write to, such as Documents. Avoid `Program Files`, where the app cannot update itself.
2. Open the extracted `Pat In Key` folder and double-click `Pat In Key.exe`.

The app is not code-signed, so Windows may say **Windows protected your PC** the first time.
Choose **More info**, then **Run anyway**.
You only need to do this once.

## First use

![The empty window, ready for tracks](images/01-start.png)

Before your first real run, try it on a copy of 20 or 30 tracks you know well, and keep a backup of your music.

**Renaming and your DJ library:** rekordbox, Serato and Traktor find tracks by file name and folder.
If you rename tracks already in your collection, they show as missing there until you relink them.
Run Pat In Key on new tracks before you import them, and for tracks already in your library, untick **Rename files** and only write tags.

1. **Add tracks.** Drag tracks or whole folders onto the window, or use **Add files** or **Add folder**. Each track is analysed straight away, and results are remembered, so adding the same file again is instant.
2. **Pick a key format.** Choose **Camelot (8A)** or **Musical (Am)** in the sidebar.
3. **Check the table.** A flag in the **Check** column marks a track worth a listen; press the **?** beside that heading for what each flag means. Double-click an artist or title to fix it, or select it and press Return on a Mac or F2 on Windows.
4. **Choose what Apply does.** **Write tags** and **Rename files** are on to start with. Pick your BPM range too: the first setting suits house and D&B, and **Hip-hop / downtempo** suits slower crates.
5. **Press Apply.** A message says what is about to change, and the table then shows each track as applied. **Undo last Apply** puts the old names and tags back.

![The table after Apply, with each track marked applied](images/04-applied.png)

After Apply, your DJ app needs to read the tags again.
In rekordbox, select the tracks, right-click and choose **Reload Tags**.
Leave **KEY** unticked in rekordbox's **Preferences > Analysis** and in any Analysis Setting box, or rekordbox replaces the key with its own.

### Cue points for rekordbox

Tick **Make rekordbox cues** and choose **Hot cues** or **Memory cues**.
The **Waveform** column then shows each track's waveform with where each cue will go.
Audio files are not changed for this: Apply writes the cues to a file for rekordbox to import.

![The Waveform column, showing five cues over each track's waveform](images/03-cues.png)

If your tracks are already in rekordbox, export your collection first (**File > Export Collection in xml format**) and pick it with **Choose XML**.
Pat In Key can then see the cues you set, and leaves those tracks alone.
Without it, importing a track replaces its cues.

To set up rekordbox once:

1. In **Preferences > Advanced > Database > rekordbox xml**, set **Imported Library** to the cue file. **Show cue file** in the app shows you where it is.
2. In **Preferences > View > Layout**, turn on **rekordbox xml**.

Then after each Apply:

1. Refresh **rekordbox xml** in rekordbox's tree.
2. Open **Playlists > Pat In Key cues** and select its tracks.
3. Right-click and choose **Import To Collection**.
4. If rekordbox says a track already exists, choose **Yes** to give it these cues.

## Updating

You do not need to come back here for new versions.
When one is out, the app says so as it opens.

![The update window, with what is new and the choices Update now, Later and Skip this version](images/05-update.png)

- **Update now** downloads it, checks it, swaps it in and restarts the app.
- **Later** asks again the next time you open the app.
- **Skip this version** stays quiet until a newer one is out.

![The update window showing a progress bar and a Cancel button](images/06-update-download.png)

An update waits for a running analysis or Apply to finish.
A restart empties the table, so if it holds tracks you have not applied, the app asks once more first.
Apply first to keep any names you fixed.

To look for an update yourself, choose **Check for updates** in the **Pat In Key** menu on a Mac, or the **Help** menu on Windows.
**Check for updates at launch**, in the same menu, turns the automatic look off.
If the app is in a folder it cannot write to, it says so and offers this page instead, so you can download the new version by hand.

## Uninstall

On a Mac, drag `Pat In Key.app` from Applications to the Trash.
On Windows, delete the `Pat In Key` folder.

That leaves your settings, remembered results, cue history and Apply logs behind, in case you come back.
To remove those too, delete this folder:

- Mac: `~/Library/Application Support/Pat In Key`
- Windows: `%APPDATA%\Pat In Key`

Deleting it also removes what **Undo last Apply** needs.
Your music keeps its tags and names.

## Licence

Pat In Key is free software under the GNU AGPL-3.0.
Its licences and source code travel with the app: in the `licenses` and `source` folders on Windows, and inside the app on a Mac, under `Contents/Resources`.

The screenshots show generated test tones, on a Mac.
The Windows window is the same, with its menu above the heading.

## USB stick test kit

Pat In Key 1.2.0 can write a USB stick that CDJ and XDJ players read, with no rekordbox needed.
It is new, so use a spare stick, and follow the [USB stick test kit](USB-TEST-KIT.md) for making a stick and the page to send a friend who tries it on their player.
