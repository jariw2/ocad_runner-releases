# Install

## What you need

- A computer with Linux (x86_64), Windows (x86_64) or macOS (Apple Silicon or Intel).
- A screen of at least 1280 × 800 pixels, not counting the system's panels. On a smaller screen the game says so and exits.
- A graphics card and driver with Vulkan support (macOS: Metal, which every Mac that runs a recent macOS has).
- On Linux, the Cairo and Fontconfig libraries. Most desktops have them. On Debian and Ubuntu: `sudo apt install libcairo2 libfontconfig1`.

The game reads OCAD maps (`.ocd` files, OCAD 8 to 2018 and later). To try it without one, use **Generate Random Map…** in the Terrain Area Editor.

## Install

1. Download the file for your computer from [Releases](https://github.com/jariw2/ocad_runner-releases/releases/latest).
2. Unpack it into a folder of its own. On Windows and Linux the program comes with two library files that must stay beside it.
3. Start it:
   - **Windows:** `OCAD_Runner.exe`.
   - **macOS:** the OCAD Runner app.
   - **Linux:** `OCAD_Runner.x86_64`. If it will not start, make it runnable first: `chmod +x OCAD_Runner.x86_64`.

## The warnings

The builds are not signed, so Windows and macOS warn before they run the game. This is expected for a test version.

- **Windows:** if "Windows protected your PC" appears, click **More info**, then **Run anyway**.
- **macOS:** if it says the app cannot be opened, right-click (or Control-click) the app and choose **Open**, then **Open** again. Or open **System Settings → Privacy & Security** and click **Open Anyway** by the message about OCAD Runner.

## Where your files are

Your Profiles, Terrain Areas, Events, Terrain Styles and Runs are kept in the game's user folder, apart from the program:

| Computer | Folder |
|---|---|
| Linux | `~/.local/share/godot/app_userdata/OCAD Runner/` |
| Windows | `%APPDATA%\Godot\app_userdata\OCAD Runner\` |
| macOS | `~/Library/Application Support/Godot/app_userdata/OCAD Runner/` |

Copy that folder to keep a backup. A newer version may not open files saved by an older one: it is pre-alpha.

## Update and remove

To update, unpack the new version into a new folder; your files stay in the user folder above. To remove the game, delete its folder, and the user folder too if you want your files gone.

## Next

Read the [user manual](manual.md) to begin, and see [Reporting](reporting.md) for how to tell the author what you find.
