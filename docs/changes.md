# What's new and changed in 0.12.0-prealpha

Everything that is new or different since 0.11.0, one short line each. The release notes have the summary. Terrain Areas built by an earlier version should be built again to get the new ground and Props in 3D.

## Orienteering Types

- A Course has an **Orienteering Type**, chosen in the Course Settings: Normal, Score, Window, Corridor, Line, Memory, Compass only, Place the flags or Mirrored.
- **Score:** Controls in any order within a time limit (30 min at first), points per Control (10 at first), 5 points lost per started minute over. A Points column and **Points by code tens** set the points.
- **Score:** the map shows circles only, with code and points. A Control already punched is drawn faded.
- **Score:** the Perfect Race is the order that scores most within the limit. It is found much faster than before.
- **Window:** the map only within a circle (75 m at first) round the Start, each Control and the Finish.
- **Corridor:** the map only in a band (80 m at first) along the Course's line. **Show the course line** is off at first.
- **Line:** only a line on the map, which you follow. Controls are punched in order, a missed one costs 5 min, and its rings can be hidden, shown as found, or shown all the time.
- **Line:** the line is always drawn with Black overprint, 1 mm wide, with gaps cut where it crosses a stream.
- **Memory:** the map readable only within 15 m of the last Control, and/or for 10 s on each Leg.
- **Compass only:** blank paper but for the Course, the north lines and the map's border. Each Leg's length is written beside it.
- **Place the flags:** no flags in the forest. You place each Control's flag with the Place flag key (P). Each metre off costs 2 s. An optional question asks before placing.
- **Mirrored:** the map and the 3D ground mirrored left to right, the map's text removed.
- New Flag Size **No flag**: no flags in the terrain, and a Control is punched within 5 m of its place.
- Dragging a Corridor or Line Course's line adds bends. A right click removes one, and **Straighten Leg** puts a Leg back.
- The Course Settings are in tabs (Course, Map, Run, and one for the Type's own settings).
- **Settings for all Courses…** changes several Courses at once. A field where they differ shows Mixed.
- Changing a Course's Type makes a new Course Version.
- Analyse replays the map as the runner saw it, with a **Full map** box.
- Analyse has new columns by Type: Points, Missed, Distance from the line, Within 20 m, Average error.
- Analyse marks on the slider when the map could be read (Memory), the worst stretch (Line), and the placed flags with their errors.

## Event Editor

- The Course's rows are an **IOF description sheet** that you edit in place, with row letters and the Start as the IOF symbol.
- Panels collapse out of the way: two buttons on the map, Ctrl+B and Ctrl+Alt+B.
- **Undo and Redo** sit on the Map Tools row, and the tools work in Preview.
- **Preview Course** shows the map as the Course's Run will, for its Type.
- **Export to PDF** from a right-click on the map: map only, with Course, with hillshade, Runnability map or Slope Direction.
- **Export Course:** every complete Course as IOF XML 3.0 or 2.0.3.
- The map's right-click menu also has Show full map, Zoom in and Zoom out. The keys + and − zoom.
- A Line Course's bends **snap** to paths, streams and stone walls (the magnet button, or hold Alt).
- An Event with a Course that cannot be run is **not saved**. The faults are marked on the map and named in a dialog.
- Starts and Finishes get the same checks as Controls: outside the map, in impassable ground, near the edge.
- **Import Courses** reports flags on boulders, cliffs or impassable ground instead of moving them.
- **Make a Course** has a **Characteristic**: Direction changes, Varied leg length, Homogenous leg length, Butterfly or Course crossing.
- **Add Controls:** Leg length limit (was Longest Leg), never on a vegetation boundary, and a question to keep the Controls when no Course can be made.
- A Course has **Allow other Profiles to play the Course** (on at first).
- New Courses are named Course 1, Course 2 and so on.
- Computing the Perfect Race shows a busy window with a bar and the seconds.
- Other Controls' opacity and Default difficulty are Profile options.

## Terrain Area Editor

- **Saved Slope Directions:** contours you corrected are remembered for other cutouts of the same map. **Saved Slopes…** lists and deletes them.
- Slope Directions: ◀ ▶ browse the uncorrected lines, and F turns the highlighted line.
- The Boundary's polygon mode: drag from an edge to add a corner, Delete removes one, click the first corner to close.
- The right-click menu has **Export to PDF** and, with Diagnostic Tools on, **Diagnostics** (copy a position, enter coordinates).
- **Generate Random Map…:** Open forest areas, Power lines, and the progress bar names the step.
- Random maps now have small ruins, more power lines turning corners, and walls that stop short of shores.

## Run screen and the Run

- Each Course is a row with its Type, difficulty colour, first Run or rerun, and day or night.
- Start is larger, Game speed sits above it, and an Event with one Course selects it.
- The map is centred on the Start, still zoomed to show the whole Course.
- **Third-Person View** is the default for new Profiles, and you see the runner through trees and bushes in front.
- A tree or boulder that pushes you aside turns your heading a little.
- The punch message shows the Control's points and your total (Score).
- The F3 debug line is readable on any background.

## Profile options

- Tabs: Game, Keyboard, Mouse, Compass, Analyse, Edit, Sound. The window is narrower.
- **Tree distance** (Edit tab) for the 3D views, **Take screenshots with F4**, and Edit tab sections.
- A **Swedish** translation. Choosing a language shows at once in the main menu.

## The ground and Props in 3D

- Each vegetation Symbol (open land, forest, green areas, marshes, fields, orchards) has its own ground, and grass, sedge, reeds and heather grow near you.
- Marshes have pools. 310 has wet ground only.
- Streams and waterholes have water. **Footbridges** can be walked over, not under.
- **Power lines** have wood poles, pylons and wires. Hunting towers and cairns have shapes of their own.
- **Dry stone walls** are piles of rounded stones with moss. Ruined walls have gaps, and the ends close.
- **Small ruins** are low mossy walls with a doorway and rubble.
- Bare rock, gardens (lawn), narrow rides and other ground have their own look.
- Cliffs show rock on their faces. Footpaths are wider on the ground and their ends are rounded.
- Trees are drawn in four steps by distance: forest maps run about two to three times faster.
- Fences have wire between thin posts.
- The 3D map ends at the map's edge, with blank paper beyond.

## Running and the map

- **Running speed retuned** (Speed Model 3): 3:30 min/km on flat open ground, a gentler uphill penalty.
- **508** narrow rides run and look as their outline says (yellow, white, green).
- Roads and paved lanes open a way through a settlement. Narrow alleys between walls are passable.
- Impassable lines end flat, so gaps between hedges are runnable.
- A new Map Type, **No footpaths**: the map without footpaths and small paths.
- A form line drawn twice on top of a contour is dropped.
- Where you can run is worked out on 0.5 m cells, twice as fine as before, so a narrow alley is two cells wide.

## Fixed

- The Terrain Area Editor's 3D View and the map end where the map ends.
- The description sheet no longer shifts right under All Controls.
- The Finish's instruction picker shows its symbols in full.
- The Start/Finish row in the sheet turns red when it has a fault.
- The Profile options' OK refreshes the main menu's language.
- A click on the open symbol list's cell closes the list.
- Stone wall ends were open and see-through.
- Auto-placed Controls on knolls stay inside their territory.

## Main menu

- Play (Run, Analyse, Drills) and Create (Terrain Area Editor, Event Editor) in two framed groups.
- A Drills button opens the Drills screen, where Leg Practice now lives.
- The Terrain Area Editor's button has its own picture.
- Dialogs have a fixed size, except the Profile options, which can be made taller.
