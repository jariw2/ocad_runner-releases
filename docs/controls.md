# Keys and mouse during a Run

Every key and mouse action a Run uses, with its default. Keep this list in step with the code: a change to a binding changes this file in the same commit. Each Profile can set its own in the Profile options, opened from the main menu (see design.md): it chooses a key setup, Default (the keys listed here), Catching Features #1 or Catching Features #2 (the two key sets of that game, listed [below](#catching-features-setups)) or Custom, where every named action below can have up to two keys of the Profile's own; turning with the mouse has a sensitivity and can look up and down inverted, the left button can run (on by default), and the right button can walk backwards. Only keys are chosen: the mouse is otherwise fixed for now, and so is Walk on Shift, which no other action can have. The camera view is chosen there too, never switched during a Run. Esc stays as listed.

Named actions and their defaults are in `profile/controls.gd` (`Controls.DEFAULTS`); the rest is read directly where noted.

Punching needs no key: a Punch happens on its own when the runner comes within 1.2 m of a flag, as with touch-free electronic punching, and the next only after being 10 m from that flag (see design.md). On a Place the flags Course, which has no Control flags, Place flag (P) places them instead.

## Running and looking

| Action | Default | Notes |
|---|---|---|
| Run | Up; left button | Held: runs the way the runner faces. Action `run`. The left mouse button, held, runs too, the mouse still turning the runner meanwhile, with "Use left button to run" in the Profile options (on by default); not while the Run menu has the mouse. `run/runner.gd`. |
| Walk | Shift | Held with Run: caps the speed at about a third of Full Speed. Fixed: not in the Profile options, and Shift cannot be chosen for anything else. Action `walk`. |
| Walk backwards | Down | Held, without Run: walks backwards at walking speed; the runner stops before turning between forwards and backwards. Action `walk_back`. With "Use right button to walk backwards" in the Profile options, also the right mouse button while the map is away or held up with Space (off by default; with the map up otherwise it drags the map). `run/runner.gd`. |
| Turn left, turn right | Left, Right | Held: turns the runner, 120° a second. Actions `turn_left`, `turn_right`. |
| Jump | Z (Alt in the Catching Features setups) | Pressed afresh (holding it does not jump again): a jump rises 1 m in an arc and lasts about 0.9 s (`Runner.JUMP_HEIGHT`, gravity 9.8 m/s²), over and onto the stones, logs and stumps whose tops are no higher than that (a stone wall is climbed on foot as before). The runner keeps the speed and direction of the take-off in the air (turning only turns the view; standing, it jumps on the spot), takes no footsteps there, and is stopped in the air by Solid Cores, impassable ground and Props above the feet as on the ground; the next jump needs a landing first. No cost: the speed goes on at landing. In Third-Person View the camera stays where the ground puts it while the runner rises. Allowed in every Course and with the map up. Action `jump`. `run/runner.gd`. |
| Turn head left, turn head right | none | Held, in First-Person View with the map away: turns the head, not the runner, 180° a second as far as 80°; let go, the head turns back to straight ahead, as it does when the map comes up. No keys by default. Actions `look_left`, `look_right`. |
| Turn and look | Mouse movement | The runner turns left and right, looks up and down. Not while the right button drags the map. Sensitivity and inverted looking in the Profile options. `run/runner.gd`. |
| Place flag | P | Place the flags Courses only: places the next Control's flag where the runner stands, once each, in the Course's order, with the Punch's beep and "Control 1 is placed"; not until the runner has been 10 m from the last flag placed ("Not yet: 10 m from the last flag placed first"). With the Course's **Ask before placing**, it first asks "Place Control 1 here?" over a covered screen with the clock stopped: Yes (Enter, or P again) or No (Esc); Left and Right move between them (`run/place_question.gd`). Does nothing elsewhere, during the Start Countdown, or once every flag is placed. In the line of keys only on these Courses. Action `place_flag`. `run/play.gd`. |
| First- or Third-Person View | Enter | Switches the camera during a Run (not during the Start Countdown); the Profile's Camera choice is only the view each Run begins in. A Run put aside keeps the view and resumes in it. Action `toggle_view`. No key in the Catching Features setups. |
| Debug line | F3 | Shows pace, Runnability, slope, height, position and the Speed Model version, and a row on performance: frames per second, frame time and its CPU part, draw calls, triangles and objects drawn, video memory and memory; for development. Action `toggle_debug`. |
| Copy position | F7 | Only with Diagnostic Tools in the Profile options (Edit tab, off by default): copies where the runner stands and the way the runner faces to the clipboard as one line, `X, Y, D` (real-world east and north where the map has them, else `Paper X, Y` in mm, D degrees clockwise from map north), with "Position copied"; at any time, the Start Countdown and the Run menu too. Fixed: F7 cannot be chosen for anything else. `run/play.gd`, `map/diagnostic_position.gd`. |
| Enter position | F8 | Only with Diagnostic Tools, on a rerun ("Not on a first Run" otherwise) while running: not in the Start Countdown, the Run menu or after the Finish. Asks for a place, a line as F7 copies it pasted whole into any field, and puts the runner there, turned to the direction given or keeping its way; not outside the Terrain Area Boundary, anywhere inside it. The clock stops while it asks; Cancel or Esc changes nothing. A Run moved so is never kept: the Run menu's Save and exit becomes Exit… (nothing saved), and at the Finish or on Abandon "Moved with F8: this Run is not kept" shows for 3 s before the main menu, with no Run record, no Analyse and its Legs still First Sight. Fixed: F8 cannot be chosen for anything else. `run/play.gd`. |

## Map View

| Action | Default | Notes |
|---|---|---|
| Map up or away | M, Tab | Not during the Start Countdown. Action `map`. |
| Map up while held | Space | Brings the map up while held and puts it away when let go; the Map View's keys work meanwhile, except that keys shared with running, walking backwards and turning keep doing those and do not move the map, and with "Use right button to walk backwards" the right button walks backwards instead of dragging the map. With the map already up it does nothing. Action `map_hold`. |
| Screenshot | F4 | Only with "Take screenshots with F4" in the Profile options (off by default): saves the whole game window, whatever screen or dialog, as a png named by the time in the Profile's `screenshots` folder, the window then flashing white like a camera. Fixed. `game.gd`. |
| Compass up while held | C | Brings the compass up alone, without the map, low at the hand's side over the 3D view, while held; when it is up is recorded with the track. Not with the map up, which has the compass on its paper, nor during the Start Countdown; does nothing for a Profile that does not run with the compass, or on a Course whose Allowed Aids leave out the compass. Action `compass`. |
| Turn the map | Q (left), E (right) | Held, with the map up, or also with it away when the Profile options' Game tab has **Turn the map while it is away** on (off by default); ends Heading Alignment. Actions `rotate_map_left`, `rotate_map_right`. |
| Align current leg | R | With the map up, or also away with **Turn the map while it is away** on: Leg Alignment to the Leg being run. Not on a Score Course, which has no Legs: there it does nothing and is left out of the line of keys. Action `align_leg`. |
| Align next leg | F | With the map up, or also away with **Turn the map while it is away** on: Leg Alignment to the Leg after the one being run (on the last Leg, to that one). Not on Score, as Align current leg. Action `align_next_leg`. |
| North up | N | With the map up. Action `north_up`. |
| Heading Alignment (Assistance) | none | No key by default; one can be set in the Profile options. Does nothing, and is left out of the line of keys, on a Course whose Allowed Aids leave it out. Action `align_heading`. |
| Zoom in, zoom out | Keypad +, keypad −; mouse wheel | With the map up, in steps; out no further than the map fills the view (a soft click at either end, Map edge click in the Profile options). Actions `zoom_map_in`, `zoom_map_out`; the wheel is fixed (`run/map_view.gd`). |
| Drag the map | Right button, dragged | With the map up, moves the map in the hand instead of turning the runner, no further than the map's edge (a soft click there). Fixed. `run/map_view.gd`. |
| Move the map up, down, left, right | W, S, A, D | Held, with the map up: moves the map in the hand that way on the screen, no further than the map's edge (a soft click there). While the map is up these keys move the map only, not the runner, except while it is held up with Map up while held, when they run and turn only; they are the only keys two actions may share (with running, walking backwards and turning). Actions `move_map_up`, `move_map_down`, `move_map_left`, `move_map_right`. |

## Catching Features setups

Two key setups as in Catching Features (`Controls.CATCHING_FEATURES`), named as that game names them and never translated, chosen in the Profile options and not changed there. Its moving left and right is turning here. An action not listed has no key in that setup; Walk stays on Shift and the mouse as above. Keypad keys are taken by place, whether Num Lock is on or not.

| Action | Catching Features #1 | Catching Features #2 |
|---|---|---|
| Run | Up | W |
| Walk backwards | Down | S |
| Turn left, turn right | Left, Right | A, D |
| Jump | Alt | Alt |
| Map up while held | Space | Space |
| Map up or away | M | M |
| Move the map up, down, left, right | W, S, A, D | Keypad Up (8), Down (2), Left (4), Right (6) |
| Zoom in, zoom out | 1, 2 | Keypad +, keypad − |
| Turn the map left, right | Q, E | Keypad Home (7), Prior (9) |
| Align current leg | R | Keypad Begin (5) |
| Align next leg | F | none |
| Place flag | P | P |

## Run menu

| Action | Default | Notes |
|---|---|---|
| Open or close the Run menu | Esc | Also during the Start Countdown, without Show Position; never with it on a Course whose Allowed Aids leave it out. From Show Position, back to the menu. Godot's `ui_cancel`. |
| Resume, Show Position, Abandon, Save and exit…, Profile options… | Left click; Up, Down and Enter | The menu's buttons. Profile options… opens the Profile options (keys, mouse, the rest) with the clock still stopped; OK keeps them on the Profile and the Run follows at once (the keys, the map and compass, the description row's side), but the camera view, the language and the game speed stay as the Run began. The menu lists, in its lower part below a line, every key of the game as it is now set, in groups (Running, Looking, The map, Turning the map, Zoom and move the map, Other), with the fixed ones (Walk on Shift, Esc, the mouse); only those the Course has (Place flag on Place the flags, no Leg alignment on Score, Heading Alignment and the compass only when allowed). Up and Down move among them (wrapping round), Enter or Space presses; Godot's `ui_up`, `ui_down`, `ui_accept`. Abandon asks "Are you sure?": Yes or No (Left and Right move between them, Esc says No). Save and exit… (only with a Profile) asks "Save the Run and go to the main menu? You can resume it later." the same way. |
| Zoom in Show Position | Mouse wheel | About the mouse. `run/run_menu.gd`. |
| Move the map in Show Position | Left or right button, dragged | `run/run_menu.gd`. |
