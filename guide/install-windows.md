# Install on Windows

You need 64-bit Windows 10 or 11.
Download [`Pat-In-Key-win64.zip`](https://github.com/plep7/dj-key-tool/releases/latest/download/Pat-In-Key-win64.zip) from the [releases page](https://github.com/plep7/dj-key-tool/releases/latest).

## Install it

1. Right-click `Pat-In-Key-win64.zip` and choose **Extract All**.
2. Pick any folder you can write to, such as Documents.
   Steer clear of `Program Files`, because the app can't update itself there.
3. Open the extracted `Pat In Key` folder and double-click `Pat In Key.exe`.

## The first time you open it

The app isn't code-signed, so Windows may say **Windows protected your PC** the first time.
Choose **More info**, then **Run anyway**.
You only need to do this once.

## Check the download (optional)

Each zip has a `.sha256` file beside it on the releases page.
It proves the download arrived intact.
Put `Pat-In-Key-win64.zip` and `Pat-In-Key-win64.zip.sha256` in one folder, open PowerShell there, and run this:

```powershell
(Get-FileHash -Algorithm SHA256 Pat-In-Key-win64.zip).Hash.ToLower()
Get-Content Pat-In-Key-win64.zip.sha256
```

You'll see two long strings of letters and numbers, and they should match.

## Next

Head to [First steps](first-steps.md) for your first run.
