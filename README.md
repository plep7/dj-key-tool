# Pat In Key

Pat In Key finds the key and BPM of your DJ tracks, writes them into the files, and gives each file a tidy name.
Drop a folder of music on the window, check the results, and press Apply.

![Pat In Key with six analysed tracks, each with its key, BPM and energy](images/02-tracks.png)

- **Key and BPM:** each track gets a Camelot key (8A) or a musical key (Am), a tempo, and an energy estimate from 1 to 10.
- **Tags and names:** Apply writes the key, BPM, artist and title that rekordbox, Serato, Traktor and Mixxx read, and can rename files to `8A - 124 - Artist - Title.mp3`.
- **Beat grids:** a grid for every track, written for rekordbox, which follows the tempo when a track speeds up or slows down.
- **Cue points:** hot cues A to H, memory cues, loops and cue comments for rekordbox.
- **Waveforms, phrases, loudness and vocals:** a coloured waveform per track, its phrases (Intro, Up, Chorus, Down, Outro), its loudness, and a hint of where the vocals are.
- **Track list:** search it, choose its columns and row height, and press Space to hear the selected track.
- **Track editor:** hear a track, and set its beat grid, cues and phrases by ear.
- **Library:** playlists, folders and intelligent playlists, with rating, colour, genre, label, year and My Tag, imported from rekordbox, Apple Music or playlist files if you like.
- **Export to USB:** write a stick that CDJ and XDJ players read, with no rekordbox needed (new, see below).
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
Run Pat In Key on new tracks before you import them, and for tracks already in your library, untick **Rename files** in **Settings** and only write tags.

1. **Add tracks.** Drag tracks or whole folders onto the window, or use **Add files** or **Add folder**. Each track is analysed straight away, and results are remembered, so adding the same file again is instant.
2. **Open Settings.** **Settings...** at the top of the sidebar opens them in their own window, as does Cmd+comma on a Mac or Ctrl+comma on Windows. A change takes effect at once.
3. **Pick a key format.** Choose **Camelot (8A)** or **Musical (Am)**.
4. **Choose what Apply does.** **Write tags** and **Rename files** are on to start with. Pick your BPM range too: the first setting suits house and D&B, and **Hip-hop / downtempo** suits slower crates.
5. **Check the table.** A flag in the **Check** column marks a track worth a listen; press the **?** beside that heading for what each flag means. Press Space to hear the selected track, and Space again to pause it. Double-click a title to fix it, or select the track and press Return on a Mac or F2 on Windows. The artist sits beside the title: double-click it to fix it, or where it says *Add artist*.
6. **Press Apply.** A message says what is about to change, and the line under the heading then says what Apply did. **Undo last Apply**, the round arrow beside **Export to USB...**, puts the old names and tags back.

![Settings: key format, BPM range, file names, what Apply does and the rekordbox collection](images/09-settings.png)

![The table after Apply, with each track's cues ready for rekordbox](images/04-applied.png)

**Finding your way round the table:**

- **Search:** type in the box over the table, or press Cmd+F on a Mac or Ctrl+F on Windows, to show only the tracks that match every word, by title, artist, file name, key, BPM, genre, label or comment. Esc clears it.
- **Columns:** right-click a column heading, or open **View > Columns**, to show or hide a column. Drag a heading to move it, and drag the line between two headings to resize. **Reset columns** puts them back.
- **Rows:** **View > Rows** switches between compact rows, one line each, and comfortable rows, with the artist under the title and the old file name under the new one.

After Apply, your DJ app needs to read the tags again.
In rekordbox, select the tracks, right-click and choose **Reload Tags**.
Leave **KEY** unticked in rekordbox's **Preferences > Analysis** and in any Analysis Setting box, or rekordbox replaces the key with its own.

### Cue points for rekordbox

In **Settings**, tick **Make rekordbox cues** and choose **Hot cues** or **Memory cues**.
The **Waveform** column then shows each track's waveform with where each cue will go, and comfortable rows count the cues under it.
Audio files are not changed for this: Apply writes the cues to a file for rekordbox to import.

![Comfortable rows, with five cues over each track's waveform](images/03-cues.png)

If your tracks are already in rekordbox, export your collection first (**File > Export Collection in xml format**) and pick it with **Choose XML...** in **Settings**.
Pat In Key can then see the cues you set, and leaves those tracks alone.
Without it, importing a track replaces its cues.

To set up rekordbox once:

1. In **Preferences > Advanced > Database > rekordbox xml**, set **Imported Library** to the cue file. **Show cue file** in the app's **Settings** shows you where it is.
2. In **Preferences > View > Layout**, turn on **rekordbox xml**.

Then after each Apply:

1. Refresh **rekordbox xml** in rekordbox's tree.
2. Open **Playlists > Pat In Key cues** and select its tracks.
3. Right-click and choose **Import To Collection**.
4. If rekordbox says a track already exists, choose **Yes** to give it these cues.

## Your library

Every track you analyse joins your library, which stays between sessions.
The sidebar's **Library** shows **This batch** (what you added since opening the window), **Collection** (everything), and your own folders and playlists.
Apply works on what the table shows, so a batch is how you tag a few new tracks without touching the rest.

![A playlist in the library, with its related tracks in the panel beside the table](images/07-library.png)

- **Playlists and folders:** press **New...** under **Library** and choose **New playlist** or **New folder**, then drag tracks onto them. Drag folders and playlists to rearrange them.
- **Intelligent playlists:** choose **New intelligent playlist** from **New...** and set its filters, as in rekordbox, for example BPM above 125 and key 8A. It keeps itself up to date.
- **Track details:** rating, colour, genre, label, year, comment and My Tag, in the table and in what goes to rekordbox.
- **Import:** **Import playlists...** brings in a rekordbox XML (tracks, playlists, cues and grids), an Apple Music library export, or M3U, PLS and TXT playlists.
- **Related tracks:** the **Related tracks** tab over the right of the table opens a panel beside it, listing what goes with the selected track, such as tracks that mix in key or sit near its tempo. **Track suggestion** and **Hot cue banks** open there too. Press the tab again, or the panel's X, to close it.
- **Missing files and duplicates:** **Library > Missing files...** finds tracks whose files moved and points them at their new place. **Library > Find duplicates...** groups copies of the same song. Nothing is deleted without asking.
- **Backup:** **Library > Back up library...** saves everything Pat In Key keeps about your library in one zip, and **Library > Restore library...** brings it back.

## Track editor

Select a track and press E, double-click its waveform or cover, or press **Edit track**, to open the editor.
Return opens it too on Windows, and Cmd+Down on a Mac.
The back arrow or Esc goes back to the table.

![The track editor, with the beat grid, five cues and the track's phrases](images/08-editor.png)

The editor's buttons show icons, as a player's do. Hover over one for its name and key.

- **Play**, the round white button, runs the track, and Space plays or pauses. Click the waveform to move the playhead, and zoom with the magnifier buttons or **+** and **-**.
- **Click**, the metronome button, adds a metronome, so you can hear whether the grid sits on the beat.
- **BPM**, **÷2**, **×2**, **Tap**, the two arrows (5 ms earlier or later), **Beat here**, **Bar here** and **Turns** fix the grid.
- Add, move and name cues, and cut, relabel or clear phrases.
- Every change is kept at once. **Undo**, **Redo** and **History**, the round arrows and the clock beside the key, take changes back.

While Apply or Undo is writing files, the editor waits for it to finish.

## Export to USB

**Export to USB...** beside **Apply** writes the table's tracks to a stick that CDJ and XDJ players read, with their grids, cues, waveforms and phrases, and no rekordbox involved.
It is made for the XDJ-RX3 and CDJ-3000.

**It is new.** No real player has read a Pat In Key stick yet, so use a spare stick with nothing on it you need.
The [USB stick test kit](USB-TEST-KIT.md) shows how to make a test stick, and has a page to send a friend who tries it on their player.

It keeps your stick safe: you choose the stick yourself, only removable drives are offered, nothing is ever formatted, and a stick that already holds a rekordbox library is refused.
Tracks a player cannot play (Opus, Ogg, WMA) stay off the stick, and the dialog says why.

![The export dialog with a stick chosen](usb-test-kit/02-export.png)

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

After updating from 1.1.0, each track is analysed once more the first time you open it, to add its waveform, phrases, loudness and vocals.

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
The Windows window is the same, with its menus above the heading.
