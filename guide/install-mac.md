# Install on a Mac

You need a Mac with Apple silicon (M1 or later) and macOS 14.4 or later.
Download [`Pat-In-Key-mac.zip`](https://github.com/plep7/dj-key-tool/releases/latest/download/Pat-In-Key-mac.zip) from the [releases page](https://github.com/plep7/dj-key-tool/releases/latest).

## Install it

1. Double-click `Pat-In-Key-mac.zip` to unzip it.
2. Drag `Pat In Key.app` into your **Applications** folder.
   Do this before you open it, or the app can't update itself later.
3. Open it from Applications, as below.

## The first time you open it

The app isn't signed by an Apple-registered developer, so macOS stops it the first time.
You only need to get past this once.

On macOS 14:

1. Right-click `Pat In Key.app` in Applications and choose **Open**.
2. Choose **Open** again in the message that pops up.

On macOS 15 or later, or if those steps don't offer **Open**:

1. Double-click the app, and choose **Done** when macOS says it wasn't opened.
2. Open **System Settings > Privacy & Security** and scroll down to **Security**.
3. Next to the line about Pat In Key, choose **Open Anyway**.
4. Confirm with your password or Touch ID.

Still stuck, or does macOS say the app is damaged?
[Troubleshooting](troubleshooting.md#macos-says-the-app-is-damaged-or-still-wont-open-it) has the fix.

## Check the download (optional)

Each zip has a `.sha256` file beside it on the releases page.
It proves the download arrived intact.
Put `Pat-In-Key-mac.zip` and `Pat-In-Key-mac.zip.sha256` in one folder, open Terminal there, and run this:

```bash
shasum -a 256 -c Pat-In-Key-mac.zip.sha256
```

It should print `Pat-In-Key-mac.zip: OK`.

## Next

Head to [First steps](first-steps.md) for your first run.
