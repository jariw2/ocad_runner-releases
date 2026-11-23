# What's new and changed in 0.14.0-prealpha

Everything that is new or different since 0.13.0, one short line each. The release notes have the summary. **Build your Terrain Areas again** to get the new ground, Props and houses in 3D; Terrain Areas built by an earlier version keep working but look as before, and a new build gives their Courses new Course Versions.

## Terrain Styles

- Terrain Styles are now whole files you can look at and change in the **Terrain Styles** window: **Default** (a summer forest) and the Stock Styles, such as Beech, autumn. A style is made from a Base and its own changes.
- Each Standard Symbol has a page with its **Props** (what stands on it, in slots: models, weights, sizes, density or spacing), its **Surfaces** (the ground's look, also by the ground beneath) and its speed. Slots and Surfaces fold up.
- **Tweaks** change a look without a new build, and **Update looks from style** in the Terrain Area Editor applies them to a built Terrain Area.
- A 3D preview in the window, with a hover preview of models and textures, hillshade and a background for points and lines.
- **Copy props from** and **Carbon copy props from** (right-click a 3xx or 4xx Symbol) copy one Symbol's Props to another.
- The Standard Symbols have their icons as the standard draws them, and Swedish names.
- Marsh versions: white, open and green versions of the marshes (406-410) with their own trees, bushes, Surfaces and speed.
- Watercourses get **Depth** and **Width**, the waterhole (303) a **Water level**, the marshes a **Pools** option, and narrow marsh (309) a width.
- Ways (footpaths, tracks, roads) take their ground by the ground beneath, and paved areas and roads are split by their circumstance (road, yard, built-up).
- The Terrain Area Editor has collapsible sections, a **Houses** layer, a **Settlement areas** layer and a **Slowness** layer (the Slowing Zones of trees and bushes).
- **Graphics Detail** (Profile options, Display tab): a slider from 1 to 10 for weaker computers, and water reflections on Ultra.

## Trees, bushes and plants

- New tree models: many Scots pines (young too), silver birches (and autumn birches), beeches (forest, open and young, also in autumn), apple trees (blossom, summer, autumn, winter), uprooted trees with their pits (419) and high stumps. The trunks have their own tints and bark.
- New bushes: Scots pine and Norway spruce bushes, rhododendrons, boxwood, garden bamboo, heather, blueberry, lingonberry and ferns. Hedges are built of bushes that suit hedges, one model all along a hedge.
- Water plants on shores and water: reeds, sedge, reedmace, white and yellow water lilies, pondweed.
- Ground plants can be as dense as 10 000 a hectare.
- Props no longer pop out close by.

## Props and buildings

- **Realistic houses**: houses, schoolhouses, churches and dwellings with roofs, doors, windows, balconies and staircases, lit windows at night, and a hand pick for a building's look, colour and roof.
- **Settlement areas (520)** by kind: garden, graveyard (gravestones in rows, groves), playground, schoolyard, sports ground, industrial yard, flower bed, farmyard.
- Lamp posts and benches (several models) along the ways, with night lights.
- Fences: roundpole (also ruined), 2 m wire, wildlife, chain-link (1 m and 2 m) and farm plank fences. Brick and plank walls (nine models), canopies and passages between buildings.
- Boulders in five shapes, the boulder cluster (207) and boulder fields (208, 209) as 3D models, the cairn as a pile of small boulders, wells, high and small towers, a fodder rack, ruins, stumps in six models, logs (birch, beech, pine) and mushrooms (chanterelle, fly agaric, russula, porcini).
- Edge lines on the wide roads (502).
- Other Symbols with no model yet have a placeholder.
- Stones, logs and stumps are walked on, passable stone walls are walked over, and stumps are low enough to step onto.

## Water and ground

- Watercourses flow from their higher end, stop at the ways they cross, are carved into the ground at their depth and end rounded; no stub of water under 3 m.
- New ground textures drawn for the game: sand, grass, beech leaves, ways, corrugated iron, concrete, asphalt and wood.
- Sandy ground ends sharply, and no orange bands show beside paved areas and houses.
- Passable cliffs have the same rock as impassable ones, and run a little faster.

## In a Run

- **Enter** switches between First- and Third-Person View. **Z** jumps (Alt in both Catching Features setups).
- A new Run starts zoomed so the first Leg fits the map's height. **Leg Alignment** puts the Leg's start at the bottom middle.
- The map stops at the map's edge. The Third-Person camera no longer goes inside a hill.
- A **loading screen** with a progress meter from the Start button on.
- **Save and exit…** in the Run menu puts a Run aside. **Show Position** is always listed in the menu.
- Closing the window during a Run asks first. A Run cut off by a crash or power cut is kept as Did Not Finish with its track up to the last checkpoint.
- A Leg is no longer First Sight from the moment the Start Countdown begins. Flag codes show only within 5 m of the flag.
- The Profile option **Show running time** (off at first) shows the time in the corner.
- The line of keys is hidden while the map is held up.
- The compass needle settles by default. Compass models have a tip corner, **Size**, and turn/zoom to the tip.
- Profile options: **Full screen** moved to a new **Display** tab, a defaults button on each tab, and the Catching Features #1 setup is the default.

## Analyse, Event Editor and menus

- Analyse's Progression line is in the Perfect Race's blue; Course opacity is 80 % at first; the Legs table lines up times, differences and placed errors.
- The main menu's Analyse and Run buttons are cards.
- The Run screen shows Events on the left, the Courses, and a framed **About this Event** panel.
- The New Event and Open Terrain Area windows show the map as a preview.
- The right button no longer removes Controls, Starts or Finishes in the Event Editor.
- **Keys boxes** in the editors' 2D and 3D Views list the keys and mouse actions; they fold up.
- **Generate Random Map** is a menu: Forest map…, City sprint map…, Maze map….
- Export to PDF: Houses with contours and Settlement areas with contours.
- Every control has a tooltip, kept short; longer help is in the manual. Tooltips and pop-up panels are on solid paper.
- Names are in italics and dark blue in info text. Swedish translation brought up to date.

## Speed and other fixes

- Terrain Areas build faster: planting the forest, the ground, paved areas and the Props are done in the game's extension. The Terrain Styles window opens about twice as fast.
- Many leaks at exit and several crashes fixed (uprooted pits, an empty Profile id).
- Windows: checked that a Run's checkpoint replaces the earlier one.
