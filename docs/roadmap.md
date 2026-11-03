# Roadmap

Where OCAD Runner has been and where it is going, one short paragraph per version. Versions are named `X.Y.Z-stage`: the middle number goes up for each step below, and the stage is `prealpha`, then `alpha`, then `beta`. No dates are planned. What is not built yet may change.

The test builds in this repository start at 0.11.0.

## Released

**0.1** The first workflow, end to end: Profiles, the Terrain Area Editor, the Event Editor, Runs with Leg Practice and the Run menu, and an analysis with Time Loss and comparison.

**0.2 Saved data you can trust.** Renaming a Course no longer splits its Runs. Punching is automatic at a flag. Terrain Areas are limited to 4000 m across. All text is ready for translation.

**0.3 The Terrain Area Editor redesigned.** A Symbol Links window with a map preview, and guesses of what a Symbol is from how it looks, not its number. Older Mapping Standards (ISOM 2000, ISSOM 2007) open too. A proper Save and Open window with notes about each map.

**0.4 Terrain you can trust.** The Slope Direction editor for contours drawn the wrong way round, cliffs that work as walls of rock, new Runnability values, Terrain Styles (named sets of rules, such as "Nordic forest"), and a 3D View of the built ground.

**0.5 Profile options.** Keys and mouse set per Profile, key setups, a language choice, and Game speed (1x to 4x).

**0.6 The compass and viewing the map.** A thumb compass in many models, the map held up in front of you with a tilting head, shaking and bouncing as you run, three Map Types (normal, contours only, contours with cliffs), full screen, and the user manual.

**0.7 The Event Editor redesigned.** Several Starts, Controls, Finishes and Courses per Event, Events saved and opened like Terrain Areas, Allowed Aids per Course, Highlight n legs, cut circles and lines, Undo and Redo, flag sizes, and a 3D View of the Event.

**0.8 Analyse.** Replay Runs in 2D and 3D with a time slider, the Perfect Race (the quickest possible Run) compared with yours, Time Loss and Loss to Perfect per Leg, a Legs table of all Runs, and the runner's view of a Run.

**0.9 Keys, the map and Profiles.** The two Catching Features key setups, turning the map while it is away, overprint (the map's black over the Course), and Profiles that can be renamed and own their files.

**0.10 A first look at realism.** Realistic trees and bushes, textures on the ground, cliffs and boulders, a performance test, and a first test of **Generate Random Map…**: a made-up map and terrain from a few settings.

**0.11 Importing Courses and training.** Courses imported from OCAD's course setting and from IOF XML, with cut circles and Leg lines. Add Controls by Difficulty, and ready-made random Courses made to your settings. Sound options (Silent Mode, Start Countdown, Punching), keys copied from a ready-made setup, a language asked for with a new Profile, and the automatic Control Descriptions looked at again.

## Being built

**0.12 Orienteering modes.** Score orienteering, corridor, window and memory orienteering, a relocation drill, a route choice drill, and line orienteering. A setting for how far away trees are drawn in the 3D views comes with it.

## Planned

**0.13 Analyse's Numbers.** The Numbers tab filled in: facts about a Run, time spent looking at the map, time lost to each kind of mistake, and your progress over time with graphs.

**0.14 Realistic world.** Realistic assets in place of the placeholders, an animated runner in the Third-Person View with clothes to choose from, graphics quality settings aimed at 60 fps on a mid-range gaming PC, water plants, weather for a Course, and Terrain Rules and Prop Rules edited in the Terrain Styles window.

**0.15 The runner's senses.** Footsteps that depend on the ground, the rustle of bushes, a finish sound and ambient sound, and a text status line while running.

**0.16 Night Orienteering.** Runs in the dark by the light of a headlamp, with reflective flags.

**0.17 Contours and Symbol guesses across the maps.** Correct 3D contours and good Symbol guesses on every map tested, so fewer corrections are needed by hand.

**0.18 Choosing what to run.** The screen where you pick an Event and a Course redesigned: what each Course tells you before the Run, your own record on it, finding a Course among many, and Leg Practice chosen more plainly.

**0.19 Ready for others.** Sharing Terrain Areas and Events, a first-run path that brings a new player to a Run without help, a keys overview in the game, and Linux packaging.

**0.20 UI and testing pass.** A pass over the whole workflow, with tests and checklists for each part.

## Alpha (from 0.21)

All major features in place with reasonable polish. Alpha releases fix what testing finds, and no known bug may lose or split saved data. The **Costume Designer** lets you design the runner's clothes.

## Beta (from 0.22)

Starts when the file formats are stable, so older files are converted when found. Planned for beta: Windows and macOS releases tested on each system, gamepads, translations, editing Collision Outlines and single Props by hand, progress over time across Courses, a ghost runner showing an earlier Run, other runners in the forest simulated by the computer, export of a Run as GPX, printing a Course on its map to PDF, and perhaps a demo Terrain Area if a club allows its map to be used.

## The Map Generator

Made-up orienteering maps, drawn in a chosen Mapping Standard from a recipe learned from real maps, with contours, roads, water and marsh, rock and cliffs, vegetation and paths, never the same twice. It is built as a project of its own. **Generate Random Map…** in the Terrain Area Editor is its first test in the game, and more of it arrives as it is finished.

## Not planned

Multiplayer, online results and rankings (the game is single player and offline), and a personal pace per player (it would stop Runs from being compared).
