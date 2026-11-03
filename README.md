# OCAD Runner – test builds

OCAD Runner is an orienteering game and training tool. You play on Terrain Areas made from OCAD maps (or from made-up maps) in its own Terrain Area Editor: run a Course with the map and a compass, then analyse your Runs against the Perfect Race.

This is a **pre-alpha** program for testing. Things are unfinished, change between versions and will break. Saved files from one version may not open in the next.

This repository holds only the test builds, the documents for testers and the place to report what you find. The program's source is not public.

## Get it

Download the newest build for your computer from [Releases](../../releases/latest):

| Computer | File |
|---|---|
| Linux (x86_64) | `OCAD_Runner-<version>-linux-x86_64.tar.gz` |
| Windows (x86_64) | `OCAD_Runner-<version>-windows-x86_64.zip` |
| macOS (Apple Silicon and Intel) | `OCAD_Runner-<version>-macos-universal.zip` |

### Opening it

Unzip or unpack the file into a folder of its own (on Windows and Linux the program comes with two library files that must stay beside it), then start `OCAD_Runner` (`OCAD_Runner.exe` on Windows). The builds are not signed, so Windows and macOS warn before they run it:

- **Windows:** if "Windows protected your PC" appears, click **More info**, then **Run anyway**.
- **macOS:** if it says the app cannot be opened, right-click (or Control-click) the app and choose **Open**, then **Open** again. Or open **System Settings → Privacy & Security** and click **Open Anyway** by the message about OCAD Runner.
- **Linux:** make the file runnable first if needed (`chmod +x OCAD_Runner.x86_64`). It needs the Cairo and Fontconfig libraries, which most desktops have (`libcairo2` and `libfontconfig1` on Debian and Ubuntu).

## Read

- [Install](docs/install.md): what you need, the warnings, and where your files are.
- [User manual](docs/manual.md): how to do the common tasks, and what each window holds.
- [Keys and mouse](docs/controls.md) during a Run.
- [Glossary](docs/glossary.md): the terms in capitals.
- [Roadmap](docs/roadmap.md): the versions so far and the ones to come.
- [Reporting](docs/reporting.md): how to tell the author what you find.

## Tell us what you find

Use [Issues](../../issues/new/choose): one for a bug, one for feedback. Say which version and computer you use, and what you did.

## Terms

By using a build you accept the [terms](TERMS.md): all rights reserved, for testing only.
