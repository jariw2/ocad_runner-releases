# Keys and mouse during a Run

Every key and mouse action a Run uses, with its default. Keep this list in step with the code: a change to a binding changes this file in the same commit. Each Profile can set its own in the Profile options, opened from the main menu (see design.md): it chooses a key setup, Default (the keys listed here), Catching Features #1 or Catching Features #2 (the two key sets of that game, listed [below](#catching-features-setups)) or Custom, where every named action below can have up to two keys of the Profile's own; turning with the mouse has a sensitivity and can look up and down inverted, the left button can run (on by default), and the right button can walk backwards. Only keys are chosen: the mouse is otherwise fixed for now, and so is Walk on Shift, which no other action can have. The camera view is chosen there too, never switched during a Run. Esc stays as listed.

Named actions and their defaults are in `profile/controls.gd` (`Controls.DEFAULTS`); the rest is read directly where noted.

Punching needs no key: a Punch happens on its own when the runner comes within 1.2 m of a flag, as with touch-free electronic punching, and the next only after being 10 m from that flag (see design.md).

## Running and looking

| Action | Default | Notes |
|---|---|---|
| Run | W, Up; left button | Held: runs the way the runner faces. Action `run`. The left mouse button, held, runs too, the mouse still turning the runner meanwhile, with "Use left button to run" in the Profile options (on by default); not while the Run menu has the mouse. `run/runner.gd`. |
| Walk | Shift | Held with Run: caps the speed at about a third of Full Speed. Fixed: not in the Profile options, and Shift cannot be chosen for anything else. Action `walk`. |
| Walk backwards | Down | Held, without Run: walks backwards at walking speed; the runner stops before turning between forwards and backwards. Action `walk_back`. With "Use right button to walk backwards" in the Profile options, also the right mouse button while the map is away or held up with Space (off by default; with the map up otherwise it drags the map). `run/runner.gd`. |
| Turn left, turn right | Left, Right | Held: turns the runner, 120° a second. Actions `turn_left`, `turn_right`. |
| Turn head left, turn head right | none | Held, in First-Person View with the map away: turns the head, not the runner, 180° a second as far as 80°; let go, the head turns back to straight ahead, as it does when the map comes up. No keys by default. Actions `look_left`, `look_right`. |
| Turn and look | Mouse movement | The runner turns left and right, looks up and down. Not while the right button drags the map. Sensitivity and inverted looking in the Profile options. `run/runner.gd`. |
| Debug line | F3 | Shows pace, Runnability, slope, height, position and the Speed Model version, and a row on performance: frames per second, frame time and its CPU part, draw calls, triangles and objects drawn, video memory and memory; for development. Action `toggle_debug`. |

## Map View

| Action | Default | Notes |
|---|---|---|
| Map up or away | M, Tab | Not during the Start Countdown. Action `map`. |
| Map up while held | Space | Brings the map up while held and puts it away when let go; the Map View's keys work meanwhile, except that keys shared with running, walking backwards and turning keep doing those and do not move the map, and with "Use right button to walk backwards" the right button walks backwards instead of dragging the map. With the map already up it does nothing. Action `map_hold`. |
| Compass up while held | C | Brings the compass up alone, without the map, low at the hand's side over the 3D view, while held; when it is up is recorded with the track. Not with the map up, which has the compass on its paper, nor during the Start Countdown; does nothing for a Profile that does not run with the compass, or on a Course whose Allowed Aids leave out the compass. Action `compass`. |
| Turn the map | Q (left), R (right) | Held, with the map up, or also with it away when the Profile options' Game tab has **Turn the map while it is away** on (off by default); ends Heading Alignment. Actions `rotate_map_left`, `rotate_map_right`. |
| Align current leg | F | With the map up: Leg Alignment to the Leg being run. Action `align_leg`. |
| Align next leg | none | With the map up: Leg Alignment to the Leg after the one being run (on the last Leg, to that one). No key by default. Action `align_next_leg`. |
| North up | N | With the map up. Action `north_up`. |
| Heading Alignment (Assistance) | none | No key by default; one can be set in the Profile options. Does nothing, and is left out of the line of keys, on a Course whose Allowed Aids leave it out. Action `align_heading`. |
| Zoom in, zoom out | Keypad +, keypad −; mouse wheel | With the map up, in steps. Actions `zoom_map_in`, `zoom_map_out`; the wheel is fixed (`run/map_view.gd`). |
| Drag the map | Right button, dragged | With the map up, moves the map in the hand instead of turning the runner. Fixed. `run/map_view.gd`. |
| Move the map up, down, left, right | Up, Down, Left, Right | Held, with the map up: moves the map in the hand that way on the screen. While the map is up these keys move the map only, not the runner, except while it is held up with Map up while held, when they run and turn only; they are the only keys two actions may share (with running, walking backwards and turning). Actions `move_map_up`, `move_map_down`, `move_map_left`, `move_map_right`. |

## Catching Features setups

Two key setups as in Catching Features (`Controls.CATCHING_FEATURES`), named as that game names them and never translated, chosen in the Profile options and not changed there. Its moving left and right is turning here. An action not listed has no key in that setup; Walk stays on Shift and the mouse as above. Keypad keys are taken by place, whether Num Lock is on or not.

| Action | Catching Features #1 | Catching Features #2 |
|---|---|---|
| Run | Up | W |
| Walk backwards | Down | S |
| Turn left, turn right | Left, Right | A, D |
| Map up while held | Space | Space |
| Map up or away | M | M |
| Move the map up, down, left, right | W, S, A, D | Keypad Up (8), Down (2), Left (4), Right (6) |
| Zoom in, zoom out | 1, 2 | Keypad +, keypad − |
| Turn the map left, right | Q, E | Keypad Home (7), Prior (9) |
| Align current leg | R | Keypad Begin (5) |
| Align next leg | F | none |

## Run menu

| Action | Default | Notes |
|---|---|---|
| Open or close the Run menu | Esc | Also during the Start Countdown, without Show Position; never with it on a Course whose Allowed Aids leave it out. From Show Position, back to the menu. Godot's `ui_cancel`. |
| Resume, Show Position, Abandon | Left click; Up, Down and Enter | The menu's buttons. Up and Down move among them (wrapping round), Enter or Space presses; Godot's `ui_up`, `ui_down`, `ui_accept`. Abandon asks "Are you sure?": Yes or No (Left and Right move between them, Esc says No). |
| Zoom in Show Position | Mouse wheel | About the mouse. `run/run_menu.gd`. |
| Move the map in Show Position | Left or right button, dragged | `run/run_menu.gd`. |
