# OCAD Runner

An orienteering game and training tool. The player runs Courses on Terrain Areas made from real orienteering maps, and analyses each run afterwards to improve as an orienteer in real life. Terrain Areas are made in the in-game Terrain Area Editor with the OCAD Converter, whose glossary defines the map, interpretation and terrain terms used here (Terrain Area, Terrain Area Boundary, Terrain Area Editor, Runnability, Prop, Standard Symbol and others).

## Language

### Players

**Profile**:
One person who plays the game, with their own name, Runs and Profile options (their key setup and keys, the mouse, the camera and the language). Several Profiles can share a computer, but only one plays at a time. A Profile is known by an id made with it, not by its name, so it can be renamed and keep its Runs and the Terrain Areas and Events it owns.
_Avoid_: User, account, player (for the stored person)

### Courses

**Owner**:
The Profile that saved a Terrain Area or Event first, kept in the file by the Profile's id. The owner chooses in the Save window whether other Profiles may open, edit and save it (yes by default); anyone may run its Events either way. One saved before 0.9.0 has no owner until it is saved again, and anyone may open it.
_Avoid_: Author, creator (the Terrain Area's creator is free text about the map)

**Event**:
A set of Controls, Starts and Finishes on one Terrain Area together with the Courses that use them, kept as one file. A Terrain Area can have many Events, and they are made in the Event Editor, which can also import Courses into one from a course-setting program's file (IOF XML or OCAD's course setting, from 0.11.0). All of an Event's Controls stand on the ground during a Run, so the runner meets Controls that are not on their Course.
_Avoid_: Course file, competition, race

**Course**:
An ordered sequence of one of its Event's Starts, some of its Controls and one of its Finishes, to be visited in that order. Once it has Runs, a change that would make new Runs incomparable with them, including a changed Terrain Area, makes a new Course Version.

**Course Version**:
One fixed state of a Course. Every Run belongs to one, and only Runs of the same Course Version are compared.
_Avoid_: Revision, edition
_Avoid_: Track, route, map (for the course)

**Event Editor**:
The in-game tool where a user makes Events on a saved Terrain Area, separate from the Terrain Area Editor and never changing the Terrain Area. When a Terrain Area changes, its Events are checked again.
_Avoid_: Course Editor, course planner, course setter (that is a person)

**3D View**:
In the Terrain Area Editor, the built ground and its Props in 3D with the map draped over the ground, shown in place of the 2D map to check the terrain against the map. A similar one comes to the Event Editor.
_Avoid_: 3D preview, terrain view

**Slope Direction editor**:
In the Terrain Area Editor, a window where the user sets which way each contour and form line runs uphill, by clicking its downhill arrows. It opens in place of the build when the evaluation conversion finds direction issues, and from a button at any time; the Terrain Area keeps the user's directions.
_Avoid_: arrow editor, contour editor

**Evaluation conversion**:
The quick first step of building a Terrain Area: the contours and the ground alone, without Props or Runnability, to find the contours and form lines whose direction may be wrong (direction issues) before the real build.
_Avoid_: test build, preview build

**Terrain Style**:
The Runnability Rules, Roughness, Terrain Rules and Prop Rules saved together under a name, such as "Nordic forest" or "Sprint town", chosen when building a Terrain Area. Keyed by Standard Symbols, so one style suits every map of that kind of terrain. A built Terrain Area keeps a frozen copy of it and its name. Default is built in and cannot be changed.
_Avoid_: Preset, profile (that is a player), rule set, theme

**Course Type**:
How a Course is run, chosen in the Course Settings: Normal (the Controls in order), and the planned Score, Corridor, Window and Memory orienteering, Route Choice drill and Relocation drill. Only Normal can be chosen until each of the others is built. Part of what makes Runs of a Course comparable.
_Avoid_: Mode, game mode (for the Course), format

**Difficulty**:
A Course's level in the Swedish colour system, from Green, the easiest, through White, Yellow, Orange and Violet to Blue and Black; Orange for a new Course and one from before it. Information for the runner, not part of what makes Runs comparable. **Add Controls…** in the Event Editor also places Controls to suit one (see Control Site).
_Avoid_: Level (that was a Terrain Area), grade

**Control Site**:
A place that suits a Control of a Difficulty, found among the Terrain Area's describable features by **Add Controls…** (`ControlSites`): Green on paths, White on line features, Yellow on or beside them, Orange and Violet on clear features, Blue and Black on any, and on spurs and re-entrants at the distinct bends of the map's contours; never on a less distinct small path, and column C telling which where more alike lie in the circle.
_Avoid_: Spot, location (for this)

**Random Course**:
A Course made by **Add Controls…** with Make a Course (`RandomCourse`): the Event's Controls that suit a Difficulty, put in an order that comes near an ideal length and number of Controls, with at most the line crossings allowed, no Control angle sharper than allowed, and a Butterfly only when allowed.
_Avoid_: Generated Course, auto Course

**Butterfly**:
A Course visiting one Control twice, looping out from it and back, with at least two other Controls between the visits. Allowed in a Random Course only when asked for.
_Avoid_: Loop, double visit

**Control angle**:
The angle at a Control between the Leg coming in and the Leg going out: 180° straight on, small when the runner turns sharply back.
_Avoid_: Leg angle, turn angle

**Guided Punching**:
A Course setting under which a Punch at a wrong Control gets no response and is not recorded. It is off by default, when every flag responds as a real punching unit does. Called Forgiving Punching until 2026-10-26; Events saved then still read.
_Avoid_: Easy mode, Forgiving Punching (misleading)

**Flag Size**:
A Course setting for how large its flags are in a Run: Small, Normal (the default), Large or Huge. The stand is as tall at every size; a larger flag reaches further down and is wider. Part of what makes Runs of a Course comparable.
_Avoid_: Control size, kite size

**Cut**:
A stretch of a Course's Leg line, Control circle or Finish rings (both together) left out by the course setter, so important map detail under it shows. It belongs to the Course and is drawn wherever its map is. Called Gap until 2026-10-27; Events saved then still read.
_Avoid_: Gap, break

**Map Tool**:
In the Event Editor, one of the buttons that set what a click or drag on the map does: Add Start, Add Control, Add Finish, Move, Move Flag, Cut and Delete. Called Place until 2026-10-27.
_Avoid_: Place mode, Place button

**Control**:
A place in an Event that a runner must visit and punch when it is on their Course, marked on the ground by a flag showing its code. Several Courses of the Event may use it.
_Avoid_: Checkpoint, waypoint, post

**Control Description**:
The description of one Control as one row of the IOF pictorial Control Descriptions, such as the feature, its side and its appearance. The Event Editor guesses it from the map at the flag, only when the guess says where on the feature the Control is, and the course setter can change it, which locks it against guessing again. The Control's circle marks the feature; for a point object the course setter places the flag where the description says it stands, for others it stands at the circle's centre. The Start has a description row too, and the Finish an instruction row.
_Avoid_: Clue, hint, control text

**Start**:
The place where a Course begins. The clock starts there after the Start Countdown.

**Start Countdown**:
The five seconds before a Run, counted down with the traditional start beeps, during which the runner can neither move nor read the map.
_Avoid_: Pre-start, timer

**Silent Mode**:
A Profile option (Sound tab) that turns every sound in the game off, whatever the other sound options say.
_Avoid_: Mute, quiet mode

**Finish**:
The place where a Course ends and the clock stops.
_Avoid_: Goal, end

**Leg**:
The part of a Course between two consecutive places on it: Start to the first Control, Control to Control, or the last Control to the Finish.
_Avoid_: Section, stage, split (that is a time)

### Runs

**Run**:
One go at a Course by one Profile, from the Start to the Finish or until abandoned. Runs on the same Course are comparable whoever plays them, because everyone moves under the same Speed Model.
_Avoid_: Race, attempt, session, try

**Punch**:
The registering of a visit at a Control's flag, or the Finish. It is automatic, as with touch-free electronic punching: it happens when the runner comes within reach of the flag, with no key.
_Avoid_: Check-in, stamp, tag

**Wrong Punch**:
A Punch at a Control that is not the next one on the Course, including one punched too early. It is recorded but does not end the Run, which still counts if the player goes on to the right Control.
_Avoid_: Mispunch (that is a missing Control), error

**Mispunch**:
The result of a Run that reached the Finish with a Control still missing. It has no valid total time, and its Legs after the missing Control are not compared.
_Avoid_: Disqualified, DSQ, Wrong Punch (that is a single Punch)

**Did Not Finish**:
The result of a Run the player abandoned before the Finish. Its completed Legs are still analysed.
_Avoid_: DNF in prose, quit, aborted. DNF is used, never translated, on the Run menu's Abandon (DNF) button and in place of the total time in result lists and the analysis.

**Finished**:
The result of a Run that punched every Control in order and reached the Finish.

**Assistance**:
Anything that gives the player information a real orienteer on the course would not have, such as being shown their position on the map, or the map kept turned to their facing. A Run that used it is an **Assisted Run** and is kept apart in comparisons. Turning or zooming the map, by hand or by Leg Alignment, is not Assistance.
_Avoid_: Help, cheat, hint

**Allowed Aids**:
The aids a Course lets the runner use, chosen by the course setter in the Event Editor's Course Settings: the compass, which every real orienteer has and so is never Assistance, and each kind of Assistance (Show Position, Heading Alignment). All are allowed unless the course setter takes one away; an aid not allowed is not there in the Run at all. Part of what makes Runs of a Course comparable.
_Avoid_: Permitted tools, rules, handicaps

**Show Position**:
The Assistance offered in the menu during a Run: the map with the runner's position and view range, shown while the clock is stopped. Each use is recorded with its place and time.
_Avoid_: Reveal, GPS, you-are-here

**Leg Practice**:
A Run of one Leg alone, starting at the Leg's first place facing a random direction and ending at the Punch of its last.
_Avoid_: Leg run, drill

**Split Time**:
The time a Run took over one Leg.
_Avoid_: Lap time, leg time

**First Sight**:
A Leg run by a Profile who had never seen it before: not in an earlier Run, nor by setting or opening its Event in the Event Editor. A Run whose Legs were all First Sight is that Profile's First Sight Run of the Course, and it is shown apart from later ones.
_Avoid_: Fresh, unseen, blind, on-sight

### Playing

**Speed Model**:
The game's fixed rules for how fast the runner moves: Full Speed slowed by Runnability, slope and reading the map, with gradual acceleration and deceleration. It is the same for every Profile, and each Run stores which version it was played under.
_Avoid_: Pace, physics

**Full Speed**:
The runner's top speed on flat ground of Runnability 1, the same for everyone.
_Avoid_: Base speed, max speed, pace

**Game speed**:
How many times faster a Run goes than real time, 1x to 4x, chosen before each Run. The runner and the clock speed up alike under the same Speed Model, so the Run's times are as at 1x, but the player has less real time to read the map; the runner's footsteps keep real time. Runs at any game speed are compared with each other.
_Avoid_: Running speed (the name until 0.6.0), time scale, fast forward

**First-Person View**:
The camera at the runner's eye height, looking where the runner looks.

**Third-Person View**:
The camera fixed a few metres behind the runner, for players who get motion sick in the First-Person View. Chosen per Profile in its Profile options, never switched during a Run.
_Avoid_: Chase camera, follow camera

**Map View**:
The orienteering map shown on screen while playing, with the Course on it. It looks the same in both camera views, never shows where the runner is, and can be read while running, which slows the runner down. The player can zoom it in steps, like holding the map closer.
_Avoid_: Minimap, overlay, HUD map

**Overprint**:
A Course setting, on by default: the map's full black is printed over the Course on the 2D maps, as on a printed map, so black details show through the purple. Drawn with the Terrain Area's **black plate**, each Map Type's black as the map shows it, so no black is drawn twice.
_Avoid_: Black on top

**Map Type**:
Which map a Terrain Area's map is drawn as: the **normal map**; **contours only**, every Symbol linked to a landform (1xx) with the north lines; or **contours and cliffs**, the same with the impassable and passable cliffs. All three are drawn when the Terrain Area is built and kept in it. From 0.7.0 each Course chooses one, the normal map by default.
_Avoid_: Map style, map mode, layer

**Leg Alignment**:
Turning the Map View once, at a key press, so that a Leg points straight up: the current one (Align current leg) or the one after it (Align next leg). The map stays as turned, and can be turned by hand after, until the next Leg Alignment.

**Heading Alignment**:
Keeping the Map View turned automatically to match the direction the runner faces. It is Assistance, since it works as a compass that never needs reading, and has no key by default.
_Avoid_: Auto-rotate, compass mode

### Analysis

**Perfect Race**:
The quickest way through every Leg of a Course, computed by the game from Runnability and slope under the Speed Model, running throughout without reading the map. Each Leg of it runs from Punch to Punch, as a Run's Leg is timed: from the Start itself, or a Punch's reach (1.2 m) from the last flag, to a Punch's reach from the next. No Run can beat it on any Leg.
_Avoid_: Fastest Route, optimal route, ideal route, best route

**Loss to Perfect**:
How much longer a Run took over a Leg than the Perfect Race. It is the sum of Route Choice Loss and Execution Loss.
_Avoid_: Mistake time, lost time, delay

**Time Loss**:
How much longer a Run took over a Leg than the fastest of the Runs shown on that Leg, as orienteering split analysis has it.
_Avoid_: Time behind

**Runner's view**:
The analysis's 3D replay seen as the selected Run's runner saw it in the Run: First- or Third-Person View, the head's turns and tilt, with the Map View, the compass held alone and the Control Description row over it as they were.
_Avoid_: Replay camera, POV, first-person replay

**Route Choice Loss**:
The part of a Leg's Loss to Perfect caused by the way chosen: how much slower that way is than the Perfect Race when both are run perfectly under the Speed Model.
_Avoid_: Route error, choice time

**Execution Loss**:
The part of a Leg's Loss to Perfect not caused by the way chosen, such as stops, map reading, hesitation, walking and slowing down near the Control.
_Avoid_: Technical error, running loss
