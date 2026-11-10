# What's new and changed in 0.13.0-prealpha

Everything that is new or different since 0.12.0, one short line each. The release notes have the summary. Terrain Areas built by an earlier version should be built again to get the new ground and Props in 3D.

## Analyse: the Numbers tab

- The Numbers tab, empty until now, has two tabs: **This Run** and **Progression**.
- **This Run** gives the selected Run's numbers in groups, never compared with other Runs. The Perfect Race is the yardstick.
- **Result:** the time, the Result, the Orienteering Type, the game speed, and the penalty with the result including it.
- **Against the Perfect Race:** its time, Loss to Perfect, Route Choice Loss and Execution Loss (seconds and % of the time), and the number of Execution Loss spots.
- **Distance:** the distance run, Extra distance (beyond the straight lines from place to place, so it can be below 0), the pace run and the pace over the Course length.
- **Stops:** the times standing still, as on Analyse's map (under 0.3 m/s for 3 s or more), per Leg and per km.
- **The map:** the time with the map up, the number of looks (raises less than 1 s apart count as one), the average and longest look, how much of the map time you stood still or moved, the time with the compass up and in Third-Person View.
- **Mistakes and aids:** Wrong Punches, Missed Controls and Show Position uses.
- Below the groups, a table of the Legs, one per row, with First Sight's eye. Selecting a Leg selects it on the Map tab too, and a Leg clicked again selects the whole Course.
- A Mispunch's Legs after its missing Control show "–".
- A **Basic / Extended** switch, kept on the Profile, chooses the short or the full list of numbers and columns.
- **Progression** shows the Profile's Runs over time. Choose the number, the period (Last 30 days, Last 90 days, Last year, All time), the Orienteering Type, **First Sight only** and **Leg Practice**.
- A dot per Run along a date axis, so breaks in your training show, and a dashed, slightly transparent line through the average of the last 5 Runs. The line has one point per day, so it never runs straight up or down.
- The selected Run's dot is ringed. Hover a dot to see the Run, and click it to open that Run in Analyse.
- Below the main graph, always, each Run's time and Course length, as a longer Course changes the other numbers.
- **Training time per day** and **Training length per day** show bars, with the period's totals above them.
- Each Run's numbers are saved with the Runs, and worked out again when the way they are worked out changes. Runs from before are worked out the first time Progression opens, below a progress bar.
- The Runs list can be filtered by **Orienteering Type**.

## Orienteering Types

- Window, Corridor, Memory, Compass only, Place the flags and No flag have been played through as Runs and in Analyse, and fixed where needed.
- Window and Corridor: the map's north lines are drawn whole on the blank paper, as on Compass only. This also holds in Analyse, Preview Course and Export to PDF.
- The north lines take their colour from the finest tiles, where a black line used to come out grey.
- Place the flags: a placed flag stands on the ground where it was placed, in the Run and in Analyse's Runner's view.
- Place the flags: each Leg's flag error is in the Legs table, and the Start Countdown's line wraps within the screen.
- Place the flags: the question before placing, and the Run menu, are on the theme's background.
- No flag: you are told before the Start, in the Course's tooltip and under the Start Countdown.

## Event Editor

- Nothing can be placed or moved outside the Terrain Area's boundary. A dragged Control goes back, and a click there does nothing.
- **Add Controls:** the progress window shows at last, with the steps (Reading the map, Looking for landforms, Choosing places) and the time elapsed. **Smallest Control angle** is 50° at first.
- **Import Courses:** imported places are described as Add Controls describes them (junctions, crossings, bends, spurs, re-entrants, column C).
- **Import Courses:** a flag within 0.5 m of a cliff or bank line is put at its foot, and one within 0.5 m of an area's edge at the edge.
- **Show control codes when editing a Course** (Profile options, Edit tab, on at first): the map labels Controls with their codes. Only Preview Course shows 1, 2, 3.

## Run screen and the Run

- **Profile options…** in the Run menu (last, set apart) opens the Profile options over the paused Run, and the Run follows your changes at once.
- Every key of the game is listed in groups, each drawn as a key cap.
- The Profile options always open on the leftmost tab, Game.
- Long tooltips wrap, and Analyse's Legs table columns are as wide as their text.

## The ground and Props in 3D

- Every tree and bush is now grown by a program from photos of Swedish trees, in place of the models from before. Ground textures are as before.
- New: birch, with an old birch (darker, greyer bark) and a weeping birch.
- New Scots pine, with a low-crowned pine. New Norway spruce and juniper.
- Settlements' Runnability is 0.5 where it was set to 0 (a converter fix).

## Main menu and other

- A Swedish translation covers the new texts.
