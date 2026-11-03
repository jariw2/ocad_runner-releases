# OCAD Runner user manual

How to do the common tasks in OCAD Runner, and what each of its major windows holds. Terms in capitals (Terrain Area, Course, Assisted Run) are explained in the [glossary](glossary.md).

Keys and mouse buttons marked **(configurable)** are defaults that each Profile can change in its Profile options, under Keys and mouse. All other input is fixed. The full list of a Run's keys and mouse actions is in [controls.md](controls.md).

## Getting started

OCAD Runner needs a screen of at least 1280 × 800 pixels, not counting the system's panels. On a smaller screen it says so and exits.

The game always starts in a window, on the Profile screen. A Profile with **Full screen** on makes the game full screen once it is chosen.

The way from an OCAD map to a Run:

1. Make a **Terrain Area** from the OCAD map in the Terrain Area Editor.
2. Make an **Event** with a Course on that Terrain Area in the Event Editor.
3. **Run** the Course from the main menu's **Run** window.
4. Look at the **analysis**, which opens after the Run, or later from **Analyse**.

## Tasks

### Make or choose a Profile

1. On the Profile screen ("Who is playing?"), write a name under **New Profile** and press **Create**.
2. Choose the Profile's **Language** and press **OK**. The new Profile is made and chosen, and the game goes on to the main menu in that language. The Profile options can change the language later. **Cancel** makes no Profile.
3. To play an existing Profile, select it in the list and press **Select**.

To change Profile later, press **Change Profile** in the main menu. To rename one, select it and press **Rename…**: its Runs, Terrain Areas and Events stay its own.

### Set the Profile options

1. In the main menu, press **Options…** (beside Change Profile).
2. Change what you want on the tabs: **Keys and mouse**, **Game**, **Compass**, **Analyse**, **Edit** or **Sound**. On **Edit**: **Warn about Controls near the map edge** (on at first), the Event Editor's outline and warning for Controls too close to the edge of the drawn map; and **Diagnostic Tools** (off at first), which shows Copy code and Paste code in the Terrain Area editor and turns on its map keys P, L and Backspace (go to, copy and clear a place). On **Analyse**: **Course opacity**, how strongly the Course shows on Analyse's map; **Inactive Legs' opacity**, how strongly the other Legs show while a Leg is selected; **Selected Run's opacity**, how strongly the selected Run's track (the one with the marks) shows, and **Other Runs' opacity**, the other Runs' tracks shown with it, both 70% at first; **Replay at actual speed** (off at first), which replays a Run as fast as it was played; and **Open on**, the tab Analyse opens on, Map (at first) or Numbers. Analyse's other choices are not here: Analyse keeps them itself, as you left them. On **Sound**: **Silent Mode** (off at first) turns every sound off; below it **Start Countdown**, the start clock's beeps, and **Punching**, the beeps at the Controls and the Finish (both on at first), greyed while Silent Mode is on.
3. Press **OK** to keep the changes, or **Cancel** to drop them. **All defaults** sets every tab back to its defaults.

### Change a key

1. In the Profile options, on **Keys and mouse**, choose **Custom** under Keys. Only Custom's keys can be changed. To start from a ready-made setup, press **Copy keys from…** beside it and choose Default, Catching Features #1 or Catching Features #2: Custom gets its keys.
2. Click the slot beside the action, then press the new key. Esc cancels the wait.
3. Right-click a slot to clear it. **Default** sets that action's keys back.
4. If another action had the key, it is taken from that action, and a note says so.

### Make a Terrain Area from an OCAD map

1. In the main menu, press **Terrain Area Editor**, then **OCAD File…**, and choose the `.ocd` file. Until a file is open, the map area is white and says how to open one.
2. The **Symbol Links** window opens. Check the Mapping Standard, then go through the unresolved Symbols at the top of the list. Tick a guess to confirm it, or right-click the Link for other choices. You can also use **Confirm guesses** and **Skip unguessed** to handle them all at once. Press **Done**.
3. Draw the **Terrain Area Boundary**. **Draw** draws a shape: click the corners and double-click to finish. **Draw rectangle** draws a rectangle from two opposite corners. **OCAD's export area** takes the export area set in OCAD.
4. Choose the **Terrain Style** and check the **Contour Interval**, then press **Build Terrain Area**.
5. If some contours' uphill side is unclear, the **Slope Direction editor** opens first. Fix the red lines (see below), then press **Build**.
6. Check the result in the layers or the **3D View**. Under the Build button, the editor says which contour ends were left open and where the ground drops or rises sharply over a long stretch, often a contour drawn on two levels. Both are marked on the **Contour Model** layer: open ends with rings, sharp drops and rises with a ring and a cross. Fix such contours in OCAD and open the file again, or draw the boundary round another part of the map.
7. Press **Save As…**, write a name (and the text about the map if you like), and save.

### Make a Terrain Area from a random map

A first test of the Map Generator: a made-up orienteering map, and its terrain, with no OCAD File.

1. In the Terrain Area Editor, press **Generate Random Map…**.
2. Choose the **Map Recipe** (what the map is made like), the **Size** in metres, the **Scale**, the **Contour Interval**, the **Steepness** from Flat to Steep, how much **Level ground** (at most 50 %, 30 % at first), and whether it has **Settlements** (on at first) and **Water bodies** (off at first), how much **Dense vegetation** there is, how **Dry hilltops** are, how many **Footpaths** and how many **Stone walls** there are (sliders from 0 to 3, 1 as the Map Recipe has it; dry hilltops have rough open land and bare rock). The **Seed** picks the map: the same seed and settings always make the same map, and **New seed** draws another.
3. Press **Generate**. Making the map takes up to a minute.
4. The map opens with its boundary already set and its Symbols linked, so there is no Symbol Links window and no Slope Direction editor. The panel says what it was made with.
5. To try another map with the same settings, press **Generate new**, which draws another seed and makes the map again. For other settings, press **Generate Random Map…** again.
6. To keep or share exactly this map, press **Copy code**: the clipboard then holds the map's Settings Code, one string with the generator's exact version and every setting. **Paste code** makes the map again from a code on the clipboard (the settings shown are then those of the code). A code only works with the generator version that made it; a Terrain Area saved before codes existed has none until it is generated again.
7. Choose the **Terrain Style** and press **Build Terrain Area**, then **Save As…**, as for an OCAD map. The Terrain Area keeps its map, so it opens again with **Terrain Area…** without any file.

If **Generate Random Map…** is greyed out, the Map Generator is not installed with this game.

### Fix slope directions

1. In the Slope Direction editor, red lines have issues. The arrows point downhill.
2. Click a line to turn its direction. Shift+click accepts it as it is. Either way the line turns green.
3. Press **Check again** to see whether your changes raised new issues.
4. Press **Build** once no red line is left.

To review the directions later, press **Slopes…** beside the Build button.

### Open, change or delete a saved Terrain Area

1. In the Terrain Area Editor, press **Terrain Area…**.
2. Select one, then press **Open** (or double-click it) or the bin (🗑, Delete…). Deleting moves the file to the system's trash.
3. After changes, press **Save…** to save over it, or **Save As…** for a new Terrain Area. Rebuilding a Terrain Area that has Events gives their Courses new Course Versions.

### Make a Terrain Style

1. In the Terrain Area Editor, press **Terrain Styles…**.
2. Select a style and press **New…**. The new style starts as a copy of the selected one.
3. Change values on the **Runnability** and **Roughness** tabs. Changes are saved at once.
4. Press **Close**. The selected style is now chosen for the next build.

### Make an Event and a Course

1. In the main menu, press **Event Editor**. Until an Event is open, the map area is white and says how to make or open one.
2. Press **New Event…**, select the Terrain Area, optionally write an **Event description** (free text about the Event) under the list, and press **New Event** (or double-click the Terrain Area). The new Event has one Course, A. The description can be changed when saving.
3. Under **Courses**, choose **All Controls**. Under **Map Tools**, choose **Add Start** (the triangle), **Add Control** (the circle) or **Add Finish** (the double circle), and click on the map to place it. A Control placed where something is wrong with it, such as its flag in impassable ground, is placed, and a box by where you clicked says what, until you click again. A Control closer than 8 mm on the map to the edge of the drawn map, where the ground is less exact, also has an orange ring round its circle; a Terrain Area built before version 0.7.0 does not know its edge until it is built again in the Terrain Area Editor. One too close to another is not placed, and a box by where you clicked says why, until you click again: Controls' flags at least 30 m apart (15 m on sprint maps), a Start or Finish at least as far from every flag; a Start at least 100 m from every other Start, and a Finish from every other Finish. New Controls get codes from 31, never 66, 68, 69, 86, 89, 96, 98 or 99. An Event can have several of each. Right-click removes what is under the mouse, from the Event and every Course; a Control a Course visits only after asking (see below). Drag to move the map, and use the wheel to zoom; the map always fills the view, as in Analyse.
4. To move a Control, Start or Finish, choose **Move** (the mouse arrow) and drag it: the flag goes along with its circle. A place too close to another goes back, and a box by where you let go says why until you click again. A click or drag anywhere inside a circle, triangle or the Finish's outer ring takes it. In a Course, Move also drags a Control's number to where you want it on the map; right-click a moved number to let it place itself again. Numbers not moved go by themselves at the side with most room, clear of the rest of the Course. To move a Control's flag away from its circle's centre, choose **Move Flag** (the flag with a small arrow): select the Control and click where the flag stands, or drag the flag. Only a point object's flag (a boulder, a knoll, a pit…) can stand apart from its circle; for lines and areas it stays at the centre. In the Add modes a drag moves the map.
5. Check each Control's **Control Description**. It is guessed from the map, but only when the guess says where the Control is: a point feature, a line at a junction, crossing, bend or end, or an area with a side, edge, corner or part. Otherwise only the code is filled in. Cliffs and earth banks are never described by their end: above one, with **Top**; at the foot of a long one (30 m or more), with the foot and its direction; at a shorter one, the cliff alone or the earth bank with **Foot**. A cliff at its foot and a boulder get their height in column F, measured on the 3D terrain to the nearest 0.5 m (a boulder at least 1 m). A Control on a knoll gets **Top**. To change a column, click it in the description row and choose its symbol (in column F, also a size); a click anywhere else closes the choice without changing anything. A description you change is **Locked**: moving the Control keeps it. Untick **Locked**, or press **Suggest from map**, to have it guessed again.
6. Under **Courses**, choose a Course, or press **New Course**. With **Add Control** chosen under **Map Tools**, click the Controls on the map in running order. Each goes in after the selected row of the Course, or before the Finish when no row is selected. A click on empty ground places a new Control into the Course. A Control may come more than once, never twice in a row.
7. With **Start** or **Finish** chosen, click one of the Event's Starts or Finishes to make it the Course's, or on empty ground to place a new one for it.
8. Change the order with ▲ and ▼ on a row, and take a Control off the Course with ✕, or by right-clicking it on the map.
9. Where a Course's line or circle covers important map detail, choose **Cut** under **Map Tools** (the circle and line with scissors) and drag along the line or round the circle (or either of the Finish's rings, which are cut together): the part dragged over is cut out, on every map of this Course. Cuts that overlap join. Right-click a cut to close it. A click still selects, and a drag elsewhere moves the map. Cuts on Legs or circles the Course no longer has are dropped when the Event is saved.
10. Press **Course Settings…** to rename the Course, set its **Difficulty**, **Course setter** and **Course description**, tick **Guided Punching**, choose the **Allowed Aids**, the **Flag Size** or the **Map Type**, or untick **Show Full Course** to highlight the next legs, and press **OK**.
11. Press **Save As…**, write the Event's name, and save. Every Course needs a Start, at least one Control and a Finish, and a name of its own. Saving computes the Perfect Race.

To delete a Control, Start or Finish from the Event, choose **Delete** under **Map Tools** (the circle with a ✕) and click it, under All Controls or in a Course. One no Course uses goes at once. Otherwise a question names the Courses first (five at most, then "(and more)"), and **Yes** deletes it, **No** keeps it: a Control is taken off the Courses visiting it; Courses starting or finishing at a deleted Start or Finish move to the first one left, which the question names, or have none. Right-clicking under **All Controls** asks the same. **Undo** brings it back.

**Duplicate** copies the chosen Course under a new name, the bin (🗑) deletes it (its Runs are kept), and ▲ and ▼ next to **New Course** change the order the main menu lists the Courses in.

To see the flags where the runner will meet them, press **3D View** at the bottom left of the map. The Course is drawn on the ground. Click a Control's row, or a Control on the 2D map before switching, and the camera goes to its flag, so you can check that it stands where the description says. The Map Tools work only in the **2D View**.

### Import Courses from a course-setting program

Courses set in OCAD or Purple Pen can be brought into an Event, when they were set on the map the Terrain Area was made from.

1. In Purple Pen, export the Courses as IOF XML (version 3.0 or 2.0.3). From OCAD, the course-setting project's OCAD File itself can be imported, or its IOF XML export. Of a relay or leg variation, the first branch is imported.
2. In the Event Editor, make or open the Event, press **Import Courses…** under the Courses, and choose the file.
3. A window lists the file's Courses, each with its number of Controls and its length. Tick the Courses to import (**All** ticks every one, **None** clears them), and press **Import**. Nothing is ticked at first, and Import stays off until a Course is.
4. A window says which Courses were imported, which were left out and why, which Controls got new codes, and the warnings. A Course is left out when it does not lie wholly within the Terrain Area, when one of its Controls, Starts or Finishes is too close to another (the same rules as placing them: see above), when it lacks a Start or a Finish (as OCAD's routes for putting out the Controls do), or when the Event already has it. A Control with a code the game never uses (66, 68, 69, 86, 89, 96, 98 or 99), or a code another Control of the Event has, gets a new code. A Control closer than 100 m to the edge of the Terrain Area is warned about. A file whose Controls all lie outside the Terrain Area is refused.
5. Check the imported Controls' descriptions and flags, and save. An OCAD File's descriptions come with its Controls; IOF XML has none, so those are guessed from the map once. Either way **Locked** is ticked, so moving a Control keeps its description. Circles and lines cut in an OCAD File (OCAD 2018 or later) are cut the same way in the game; IOF XML holds no cuts. A flag that would stand on a boulder, a cliff or impassable ground is moved off it, the way the description says (a boulder's east side to its east, a cliff's foot to the lower ground, its top to the higher), and the window says how far.

A Control, Start or Finish within 5 m of one of the Event's, a Control with the same code, is taken as that one, so importing the same file again adds nothing new. In a new Event, the imported Courses take the place of the empty Course A. **Undo** takes the whole import away again, its Courses too, and **Redo** brings it back.

### Add Controls by Difficulty, and a random Course

The game can put Controls in the forest for you, on features that suit a Difficulty.

1. In the Event Editor, make or open the Event, and press **Add Controls…** beside Import Courses….
2. Choose the **Difficulty** (the chosen Course's at first, then the one you last added with) and how many **Controls**, up to 50 at a time, and press **Add**.
3. A window says which Controls were added. When too few places suit the Difficulty, fewer are added than asked for.
4. To have a Course made as well, tick **Make a Course** before pressing Add. Give it a **Name**, an **Ideal length** and an **Ideal number of Controls** (both filled in for the Difficulty when you choose it), how many **Line crossings** it may have (0 to 4), the **Smallest Control angle** between the Leg coming in and the Leg going out at a Control, and whether **Butterflies** are allowed (one Control visited twice). The number of Controls to add can then be 0, to use only those the Event has. When the options can never make a Course, the dialog says why and Add is off.

The Course is made of all the Event's Controls that suit the Difficulty, those on other Courses too, and the Event's Start and Finish; when the Event has none, they are placed for it. It comes as near the ideal length and number of Controls as those Controls allow, and never passes through another of its Controls' circles. The window then says how long it came out, with how many Controls, and how often its lines cross, and the new Course is chosen. **Undo** takes it away with the Controls added.

Green puts them on paths, at junctions, bends and ends, and where a path crosses a stream, ditch or stone wall (a wall that ends at a path and goes on at its other side crosses it); White on line features such as paths, streams, ditches, walls and fences; Yellow on them or on a clear feature right beside one; Orange on clear features, such as a ruin, a large boulder, a cliff or a pond, near a line feature; Violet on clear features anywhere; Blue and Black on any feature, small ones too, away from the paths when they can, and most often on spurs and re-entrants, on the distinct bends of the map's contours (on form lines only now and then) (a Terrain Area built before version 0.11.0 has to be built again for them). A cliff is used at its foot, with its height, never on top; a point feature's circle, such as a boulder's, is on it and the flag beside it, on the side the description says (a knoll's at its foot). From Orange up, none is on a road or path, and none is ever on a less distinct small path. Where more features like the Control's lie in its circle, such as two boulders or two path junctions, column C says which (the northern, the south-western, the middle, …); Green and White use such places only when no other is left (a Terrain Area built before version 0.11.0 has to be built again for the small paths and the wall crossings). They keep 60 m (30 m on a sprint map) from every other Control, Start and Finish, and 100 m from the edge of the Terrain Area. The new Controls are in no Course: add them to Courses as any other. Areas, such as clearings and buildings drawn as areas, are not used for now, nor single dots of stony ground, boulder fields or broken ground. Their descriptions are guessed from the feature, a path branching off another described as a junction, and are not Locked. **Undo** takes them all away again.

### Open, change or delete a saved Event

1. In the Event Editor, press **Open…**.
2. Select one, then press **Open** (or double-click it) or the bin (🗑, Delete…). Deleting moves the file to the system's trash; its Runs can still be analysed.
3. After changes, press **Save…** to save over it, or **Save As…** for a new Event under another name. The Save window says when a Course with Runs gets a new Course Version.

Leaving an Event with changes not saved (New Event…, Open…, the house (⌂, Back to menu) or closing the window) asks first whether to discard them.

**Undo** (↶, Ctrl+Z) and **Redo** (↷, Ctrl+Y or Ctrl+Shift+Z), at the top left of the right panel, step through the changes to the Controls, Starts and Finishes and to the Courses' rows, cuts and numbers since the Event was made or opened; a whole drag is one step. Managing the Courses (New Course, Duplicate, Delete, ▲ ▼) and the Course Settings are not undone.

A click on a Control, Start or Finish selects it, to see or edit its description, whichever Map Tool is chosen; in a Course, with **Control** chosen, a click on a Control adds it to the Course instead.

### Run a Course

1. In the main menu, press **Run**. In the Run screen, choose an Event, then a Course. A Course's tooltip names its Map Type when it is not the normal map, whether the map highlights the next legs, and the aids it does not allow, such as the compass.
2. Optionally choose one Leg for **Leg Practice** instead of the Whole Course, and a **Game speed** (1x to 4x; the Profile options set the one offered first, 2x for a new Profile).
3. Press **Start**, or double-click the Course. After the five-second Start Countdown the clock starts.
4. Find the Controls in order. A Punch happens on its own when you come within 1.2 m of a flag. It beeps, and **Punched** with the Control's code shows at the top of the screen, where the Start Countdown was, for two seconds before it fades away.
5. The Run ends at the Finish, and the analysis opens.

To pause, press Esc for the Run menu. From there, **Abandon (DNF)** ends the Run as Did Not Finish.

### Read the map while running

1. Press M or Tab **(configurable)** to bring the map up or put it away, or hold Space **(configurable)** to hold it up only while the key is down.
2. Turn the map with Q and R **(configurable)**, or press F **(configurable)** to align it to the current Leg, or N **(configurable)** for north up.
3. Zoom with the mouse wheel, or keypad + and − **(configurable)**. Drag the map with the right button.
4. Hold C **(configurable)** to look at the compass alone, without the map.

### Look at a Run again

1. In the main menu, press **Analyse**.
2. Under **Order** at the top right, choose **Newest first** or **Best time first** for the Runs of each Course Version. The list keeps your choice.
3. Double-click a Run in the list to open its analysis. To delete a Run, select it and press the bin (🗑) below the list, or the Delete key, and answer **Delete**: it moves to the system's trash and cannot be analysed again. Analyse opens with the choices you left it with last time: Show, the boxes, the legend, the replay's speed and Tail, Text or 3D, Runner's view and Trees.

### Compare Runs

1. In the analysis, look at the **Legs table** below the map. Its rows are every Run of the Course Version, yours and other Profiles', its columns the Legs and the Total.
2. Above it, under **Show**, choose **Split Times**, **Time Loss** (behind the fastest Run shown on each Leg) or **Loss to Perfect** (behind the Perfect Race). Untick **Perfect Race** to hide its row, or tick **Only First Sight Runs** or **Only my Runs** to see fewer Runs.
3. Select a Run's name to analyse that Run instead, or one of its times to analyse that Run on that Leg. Select a Leg's title to see that Leg of the selected Run.
4. Tick Runs to see their tracks on the map, each in its own colour, which it keeps whatever you select.

### Replay Runs

1. In the analysis, tick the Runs to replay in the Legs table (none ticked: the selected Run alone). To replay one Leg, select it; the Runs then start the Leg together.
2. Press **Play** (the triangle) in the bar above the Legs table, or drag the time slider. Choose how fast it runs (10x at first; 1x to 4x match the game speeds) beside it, and the **Tail**, how much track is drawn behind each runner, at the right.
3. On the slider, a line with a golden star on top is where the fastest of the Runs finished, a line with a pointer at the bottom the selected Run, and blue dashes the Perfect Race, while the Legs table shows it. Drag the slider to its end to see the whole analysis again.
4. To watch it in 3D as well, press **3D** under the legend beside the map. The 3D view takes the place of the text beside the map, the tracks drawn on the ground, and its camera follows the selected runner. Right-drag to turn and tilt it, drag to move, and use the wheel to go farther or closer; the other keys of the editors' 3D View work after a click in it. Press **Text** to get the text back.
5. Untick **Trees** below the 3D view to see the ground without them. To see what the selected Run's runner saw, tick **Runner's view** beside it: First- or Third-Person View as run, the head's turns, the map and the compass when they were up, and the next Control's description, the 3D view shaped as the game's screen. The lines on the ground are left off, and dragging no longer moves the camera. Runs from before 0.8.0 look straight ahead (down at the map while it is up), the map not moved in the hand.

## Windows

### Profile screen

"Who is playing?": the list of Profiles, **Select**, **Rename…**, and **New Profile** with a name field and **Create**, which asks the new Profile's language. It is always in English, as no Profile's language is chosen yet.

While any dialog is open over a screen (a question, a report, a file dialog or an options window), the screen behind it is darkened.

### Main menu

- **Playing as** the current Profile, with **Change Profile** and **Options…**.
- **Run**, opening the Run screen, and **Analyse** side by side; below them **Event Editor** (with a small course on it) and **Terrain Area Editor** side by side; the four as large as each other; then **About** and **Quit**.

### Run screen

The house (⌂, **Back to menu**) on a row of its own at the top left, the Events, the chosen Event's Terrain Area and its text about the map, the Event's Courses, Leg Practice, Game speed, and **Start**. A note says when a Course's Perfect Race are out of date.

### Profile options

- **Keys and mouse**: the key setup (Default, Catching Features #1 or #2, or Custom, your own, with **Copy keys from…** to start Custom from one of the others), every action of a Run with two keys each, and the mouse: turning speed, inverted looking, the left button to run, and the right button to walk backwards.
- **Game**: Language, Full screen, Camera (First-Person View or Third-Person View), Game speed, Map size, Map shake, Description row (top left or top right), tilting the map, and turning the map while it is away (off by default: the turn keys then work only with the map up). A preview shows the Map View's layout.
- **Compass**: the hand that holds it, the Model, the Needle (Exact or Settling), and whether to run with a compass. A preview shows the compass on a piece of map, its north lines leaning as on the tilted paper when the Game tab tilts the map.
- **Analyse**: Course opacity, Inactive Legs' opacity, Selected Run's opacity, Other Runs' opacity, Replay at actual speed, and Open on (Map or Numbers).
- **Edit**: Warn about Controls near the map edge (on) and Diagnostic Tools (off).
- **Sound**: Silent Mode at the top, set apart by a line; then Start Countdown and Punching, greyed while Silent Mode is on.

### A Run

- **The 3D view**: the terrain, seen from the runner's eyes or from behind (Third-Person View).
- **The Control Description row**: the next Control's row of the IOF pictorial descriptions, at the top right or the top left, as the Profile options choose. During the Start Countdown it is the Start's row, and on the last Leg the Finish's instruction with its distance.
- **The Map View**: the map on paper with your Course, held up in front of the 3D view, with the thumb compass at the hand's side. A line at the top of the screen says how the map is turned and lists its keys.
- **The Run menu** (Esc): **Resume**, **Show Position (Assisted Run)**, which shows where you are, with a wedge for what your eyes see, but makes the Run an Assisted Run (the arrow ← at its top left, Back to the menu, goes back to the Run menu), and **Abandon (DNF)**, which asks "Are you sure?" first.

Keys and mouse during a Run (the full list is in [controls.md](controls.md)):

| Action | Default | |
|---|---|---|
| Run | W, Up; left button held | Keys configurable; the left button is an option |
| Walk | Shift, held with Run | Fixed |
| Walk backwards | Down; right button | Key configurable; the right button is an option, off by default |
| Turn | Left, Right; mouse | Keys configurable; the mouse's speed is an option |
| Turn the head | none | Configurable; First-Person View only |
| Map up or away | M, Tab | Configurable |
| Map up while held | Space | Configurable |
| Compass up while held | C | Configurable |
| Turn the map | Q, R | Configurable |
| Align current leg, next leg | F, none | Configurable |
| North up | N | Configurable |
| Heading Alignment (Assistance) | none | Configurable |
| Zoom the map | Keypad +, −; wheel | Keys configurable; the wheel is fixed |
| Move the map | Arrow keys; right button dragged | Keys configurable; dragging is fixed |
| Run menu | Esc | Fixed |

### Analysis

- **The top row**, at the screen's top left: the house (⌂, **Back to menu**), or the arrow (←, **Back to Runs**) when the analysis was opened from the Runs list.
- **The tabs**: **Map**, with everything below, and **Numbers**, empty for now (it is filled in a later version). The Profile options choose which one Analyse opens on. The bottom row stays below both.
- **The map**: the Course, the Perfect Race in blue dashes on a white edge, unlike any Run's track, and the selected Run's track coloured by speed: red at half speed or slower, green at Full Speed. Grey dots mark map reading; across them, every 5 seconds the map was up and each time it came up, an arrow shows the way the map's north pointed in the terrain, straight up when the map was turned to fit the ground: orange, teal where it was aligned to the Leg, magenta for Heading Alignment. White dots ringed in black compass looks, short dark lines where the head was turned and which way, rings stops, red circles Execution Loss, on the line between the Controls, and magenta squares Show Position. The legend beside the map has a box for each of them and for the Perfect Race (no compass or head box, and no arrow colour for Leg or Heading Alignment, when no Run in the Legs table has any): untick one to hide it, or tick **Hillshade** to shade the ground. The **Perfect Race** box shows it on the map and as the Legs table's top row. With a Leg selected, everything on the other Legs is drawn faded. Drag to move the map, and use the wheel to zoom.
- **The panel** beside the map: the map's legend with its boxes in two columns at the top, then **Text** and **3D**. Text shows the selected Run's result (the time or DNF, the game speed, the Profile and when it was run), and for the selected Leg its Split Time, the Perfect Race's time, the Loss to Perfect with its Route choice and Execution parts, and where time was lost; with no Leg selected, the same for the whole Course. 3D shows the replay in 3D in its place (see the replay bar).
- **The bottom row**, at the screen's bottom right: **Rerun Course** (or **Rerun Leg**), which asks before starting a new Run.
- **The replay bar** across the screen above the Legs table: **Play**, a triangle (two bars, **Pause**, while it plays), its speed (1x, 2x, 3x, 4x, 5x, 10x at first, 30x or 60x; with Replay at actual speed in the Profile options, the selected Run's game speed, not to be chosen), the time slider with the time and the slider's length beside it, and **Tail**: 30 s, 1 min (at first), 90 s, 2 min or Full Course. The Runs on the map start together, at the Start, or at the selected Leg's start with a Leg selected; each is drawn up to the slider's time, its tail only, with a dot in its track's colour where the runner was and a line the way it faced; the selected Run's dot is larger, ringed in yellow, and the map moves to keep it in sight. The slider reaches the longest time of those Runs; a line with a golden star on top marks where the fastest finished, a line with a pointer at the bottom the selected Run, and blue dashes the Perfect Race while the Legs table shows it. At the slider's end the whole analysis shows, as before the replay. With **3D** pressed under the legend (Text at first), a 3D view of the ground as in a Run takes the place of the Run's and the Leg's text: the Course, the Perfect Race, the tracks and the marks drawn on the ground as on the map, and while replaying each runner standing where it was in its track's colour, the selected one with a yellow ball over its head; the camera follows the selected runner, and keeps the way and distance you turn it to. **Runner's view**, beside Text and 3D, shows the 3D as the selected Run's runner saw it, with the map, the compass and the Control Description row over it as in the Run, scaled down; the Course's flags stand on the ground and the lines are left off. **Trees** beside it (on at first) shows or hides the trees in the 3D view.
- **The Legs table** below the map: every Run of the Course Version down, as First Sight Runs, Later Runs and Assisted Runs, fastest first, and the Legs and the Total across, both scrolling. **Show** chooses Split Times (the best in green, the others' time behind it) Time Loss (behind the fastest Run shown on each Leg, whatever its group, the fastest 0:00 in green) or Loss to Perfect. The blue **Perfect Race** row at the top is every Leg run the quickest way, which no Run can beat; the legend's Perfect Race box hides it. Legs that were First Sight are on pale blue, and a First Sight Run has an open blue eye before its name. **Only First Sight Runs** and **Only my Runs** filter the Runs, but never hide the selected one. The selected Run's row is yellow and bold, and the Run you just ran or opened is marked » in dark blue; select another Run, one of its times or a Leg's title to analyse it. A tick puts a Run's track on the map in its own colour. Drag the bar above the table to make it taller or shorter.

### Runs list (Analyse)

The house (⌂, **Back to menu**) on a row of its own at the top left. Your Runs, in smaller text so more of them fit, by Event and Course Version, newest first, or best time first within each Course Version with **Order** at the top right set to **Best time first** (finished Runs by time, then Mispunches, then DNF), the Event and Course rows bold on darker bands so the Runs stand out between them: when each was run, the Result, the Time (DNF for a Run that Did Not Finish), the Speed, and whether it was a First Sight Run (an open blue eye and **First Sight** in bold blue on pale blue) or Assisted. Double-click one to analyse it. Below the list the bin (🗑) deletes the selected Run, asking first; the Delete key does the same.

### Terrain Area Editor

- **The map**: the OCAD map, or with **3D View** the built terrain. In the 2D View, the wheel zooms and dragging moves the map; the map always fills the view. P goes to a map position, L copies what the mouse window says, and Backspace removes a position's mark. A small window beside the mouse gives the map position, and the height and Runnability when those layers are shown.
- **The panel**: the house (⌂, Back to menu) on a row of its own, opening (**OCAD File…**, **Terrain Area…**, **Generate Random Map…**), **Symbol Links…** with the state of the links, the **Terrain Area Boundary** buttons, **Terrain Style** with **Terrain Styles…**, **Contour Interval** with **Build Terrain Area** and **Slopes…**, the **Layers** to show (Map, Hillshade, Contours, Slope Direction, Contour Model, Runnability, Props), and **Save…** and **Save As…**.
- **For a random map**, the panel has in place of the Symbol Links, the boundary, the Contour Interval and Slopes… a line saying what the map was made with, and the **Seed** with **Generate new**, and **Copy code** and **Paste code**.
- **Generate Random Map window**: Map Recipe, Size, Scale, Contour Interval, Steepness, Level ground, Settlements, Water bodies, Dense vegetation, Dry hilltops, Footpaths, Stone walls and Seed with New seed; **Reset to defaults** (all but the seed; your settings are kept for next time); **Generate** and **Cancel**.
- **The 3D View**: the ground with the map draped over it, with boxes for 2D Map, Hillshade, Trees (off at first), Props and Buildings. Tab switches between orbiting a point and flying freely, after a click on the view. A box at its top left lists its keys, which are fixed.

### Symbol Links window

The OCAD File's Symbols with Objects in the map, each linked to a Standard Symbol of the Mapping Standard, skipped, hidden or unresolved. Beside each are its guess and Match (solid, by appearance, by number, mismatch, conflict). A preview of the map shows the selected Symbol's Objects, and can show only the linked, unlinked, Skipped or mismatched Symbols. **Done** returns to the editor.

### Slope Direction editor

Every contour and form line with downhill arrows. Red lines have issues, green ones you changed. **Check again**, **Build** and **Cancel**, or **Done** when opened from Slopes….

### Terrain Styles window

The styles (Default is built in and cannot be changed), with **New…**, **Rename…** and the bin (🗑) to delete, and the selected style's **Runnability**, **Roughness**, **Terrain Rules** and **Props** by Standard Symbol. Only Runnability and Roughness can be changed so far.

### Course Settings window

The chosen Course's name, which no other Course of the Event may have; its **Type**, where only **Normal** can be chosen so far (the others are listed with the version they come in, and OK is disabled while one is chosen); its **Difficulty** in the Swedish colour system, Green to Black, Orange for a new Course; the **Course setter**, your Profile's name for a new Course; a **Course description**; **Night orienteering**, kept with the Course but not yet used in Runs (they are in daylight until Night Orienteering comes); **Guided Punching** (a Punch at a wrong Control gets no response and is not recorded), and the **Allowed Aids**: the compass, Show Position and Heading Alignment; a new Course allows only the compass. An aid not ticked is not there in a Run of the Course: no compass, no Show Position in the Run menu, no Heading Alignment key. The **Flag Size** of the Course's flags in a Run, **Small**, **Normal** (a new Course's), **Large** or **Huge**, with a preview of the flag on its whole stand against the forest's colour to its right (the stand lighter and thicker there than in a Run, to be seen); the stand is as tall at every size, a larger flag reaching further down and wider. The **Map Type** the Course is run and analysed on: the normal map, contours only, or contours and cliffs, with a preview of a piece of map to its right, with a sample Control on a knoll, pit or small depression near the Course's first Control; it shows the Control's code with its number when **Show control codes** is ticked. A Terrain Area saved before Map Types shows the normal map instead until it is saved again in the Terrain Area Editor; the window says so. **Show control codes** (off for a new Course) prints each Control's code with its number on the map, as 1-31. **Black overprint** (on for a new Course) prints the map's black over the Course on the 2D maps, as on a printed map, so cliffs, boulders and other black details show through the purple; the preview shows it. A Terrain Area saved before Black overprint draws the Course over the map until it is saved again in the Terrain Area Editor; the window says so. **Show Full Course** (on for a new Course) shows the whole Course in full colour; untick it for **Highlight the next n legs** (1 to 9, 4 at first), greyed out while Show Full Course is on: the Run's map shows only the Leg being run and the next ones, n in all, and their Controls in full colour, and the rest of the Course toned down; it moves on as you punch. Changing Guided Punching, the Allowed Aids, the Flag Size, the Map Type, Show Full Course, Highlight or Black overprint on a Course with Runs warns that saving makes a new Course Version.

### Save window

In the Event Editor: the Event's name, fixed for **Save…**, the **Event description** (free text about the Event, shown when opening it, changeable with either button), **Other Profiles may open, edit and save it**, and what saving does to Courses with Runs.

In the Terrain Area Editor: the Terrain Area's name, its text about the map: creator, club, mapper(s), map year, permission and notes, and **Other Profiles may open, edit and save it**.

**Other Profiles may open, edit and save it** (on by default) can be changed only by the file's owner, the Profile that saved it first; for others it is greyed. With it off, other Profiles see the file in the Open window but cannot open or delete it; they can still run its Events.

### Event Editor

- **The map** of the Terrain Area, with the Course and, when **Show** is ticked, its Perfect Race.
- **The map** under **All Controls**: every Start, Control and Finish. With a Course chosen: the Course, the Event's other places toned down.
- **2D View** and **3D View** at the bottom left of the map. The 3D View shows the ground with the map and the Course draped over it, every flag with its code, and the Starts and Finishes; for looking only. Its keys are those of the Terrain Area Editor's 3D View, listed at its top left. Boxes for 2D Map, Hillshade, Trees (off at first), Props and Buildings show under **Course Settings…** while it is shown.
- **The left panel**: the house (⌂, Back to menu) on a row of its own, **New Event…**, **Open…**, **Save…** and **Save As…**, with the Terrain Area's text about the map; **Courses** (All Controls and the Courses, ten shown, scrolling for more; **New Course**, **Duplicate**, the bin (🗑) to delete, ▲ ▼; a Course with warnings in orange, the chosen one too), **Import Courses…** and **Add Controls…** (by Difficulty), and **Course Settings…** for the chosen Course.
- **The right panel**: ↶ and ↷ for Undo and Redo at the top; **Map Tools** (Add Start, Add Control and Add Finish on one row; Move, Move Flag, Cut and Delete on the next); for the chosen Course its rows (Start, the Controls with ▲ ▼ ✕, Finish; ten shown, scrolling for more; a place with warnings on the map in orange), its length, and along the Perfect Race its length, climb and time, and **Compute Perfect Race**; the warnings, under a Course only about that Course (its places, name and Perfect Race), under All Controls the first ten; the selected Control's **Control Description**, or with the Start or Finish row selected, the **Start Description** or the **Finish Instruction** (taped route, navigate to the funnel, or navigate with no tapes; click the row to choose).
- **The status line**, under both panels.

### About

The version, and the credits and licence notices.
