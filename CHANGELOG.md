# Changelog

## 0.1.0-alpha.7
- New: File > Import test data... takes the zip someone made with Export test data and adds its recordings to a separate Imported list (tagged "imported"; a box under the filters shows all, yours or imported). They are kept apart from your own: they are not counted in your statistics or best laps. A name already in use gets "(2)" after it; nothing is overwritten.
- New: Settings > Recordings folder... chooses where recordings are kept. It asks whether to move the recordings you already have, and the new folder is used from the next start. If the chosen folder is not there at start (a drive that is not connected), the default folder is used and the program says so.
- New: best laps. The Tracks tab of Statistics shows your best lap on each track and layout for a car class you pick in a drop-down, how it improved over the sessions, and "Show lap" to open that lap in the replay. Statistics is counted again after this update (open a recording, or press "Count them now").
- New: in the race replay, "Follow the selected car" keeps the car you picked in the middle while you zoom; pick another car and it follows that one.
- Better fault judgement, using the road: the tool learns which way the road points from the cars that drive it. On a straight, a car that moves sideways into another is blamed, whoever was ahead; the 100 m before a corner count as the braking zone, where the car ahead keeps its line. A car ahead that moves into a faster car holding its line close behind, or that has just caused another contact, is blamed for it (a faster car that dives sideways into the car ahead still is). A car that was already level with the other car's middle is no longer blamed for "no braking". A car sent into a spin by another car is not blamed for what it then hits. In the first laps of a session the road is not known yet and the older rules apply.
- Fixed: the program no longer saves an empty "probe_..." recording when the game shares its data in the menus before any session has started. Empty recordings of that kind left by older versions are removed when the program starts.
- Fixed: a recording whose name ends in "(2)" (two sessions in the same minute) showed "(no date)"; it now shows its date.
- Better: the tester notes describe the new menus and the fault rules.

## 0.1.0-alpha.6
- New: a Help window (Help > How to use Racing Steward, or F1) with topics: getting started, recordings and incidents, race replay, steward decisions and the report, statistics, storage, the alert, shortcuts, and what to do when something goes wrong. The About box is rewritten.
- New: you can change the size of the panels by dragging the thin bars between them: the replay can be made much taller, and the widths of the list, replay and verdict can be changed. Double-click a bar for the default. The sizes are remembered.
- New: the mouse wheel zooms the incident replay, as it does on the race replay map.
- New: the race replay marks the formation lap. When RaceRoom has car collisions off (formation lap and countdown) and cars drive through each other, amber marks on the timeline and a note under the map say so. It is not counted as a contact.
- Better: the recordings list is easier to read: each recording is its own card, and the open one has an orange edge and its incidents inside it.
- Better: the race replay zoom and moving of the map are easier to find (Map + / - / Fit).

## 0.1.0-alpha.5
- New: a menu bar (File, View, Tools, Settings, Help) and tabs instead of a row of buttons, with keyboard shortcuts (Ctrl+O, Ctrl+1/2/3, F5, Ctrl+plus/minus). Greyed-out items say what they need.
- New: Recordings and incidents are one tab. The list shows each recording as a card; the open one unfolds to its incidents, and the incident you click is shown beside it. Search, Game / Track / Class filters and a "Sort by" dropdown.
- New: Race replay tab: the whole race from above with every car, the standings with gaps and pit stops, and a timeline with the incidents marked. Play, pause and speed up to 32x, follow a car, zoom with the mouse wheel and move the map by dragging.
- New: RaceRoom can record every car, so the race replay shows the whole field (Settings > Record every car (RaceRoom)). It is off until you agree to a warning: recordings become about 4 times bigger (roughly 10 MB for each minute of racing). Le Mans Ultimate always records every car.
- New: the league incident report (Tools > Incident report..., steward view): one page for the browser with every incident, the steward's decision first, pictures of the contact, and the tool's analysis as supporting data.
- New: recordings that have not been touched for 7 days are zipped by themselves (Settings > Zip old recordings... changes the days or turns it off). Recordings with a steward decision stay as they are.
- Better: the tester notes describe the new window.

## 0.1.0-alpha.4
- New: a Statistics screen ("Statistics..." in the top bar) with overview, driving, tracks, cars, drivers, trends and hotspots, counted from all your recordings. Recordings are counted when you open them; "Count them now" counts the rest.
- New: a darker, racing-style look, and an incident screen that needs no scrolling: replay on the left, verdict on the right, tabs (Evidence, Timeline, Steward decision, Each contact) underneath.
- New: the incident list shows cards with the other driver, the verdict, the time, lap and speed, and a fault bar. Rules in the Evidence table have plain names.
- New: in the replay, the driver you pick turns blue and the other cars turn grey. The car picker wraps onto several rows, and "Each contact" follows the driver you picked.
- New: in a race with several classes, each car's class is shown (card, verdict and replay).
- New: flags are shown as context for each incident (blue and yellow flag, wrong way, cutting the track). They do not change the fault split. Le Mans Ultimate gives them for every car; RaceRoom for your car only. They appear in a saved recording, not in the live view.
- Better: after the game closes, the top bar says "No data from the game for N s, saving in M s" while the recording waits to be saved.


## 0.1.0-alpha.3
- New: an optional alert over the game a few seconds after each contact, with who is at fault and the split. Off by default: tick "Alert after a contact" in the top bar. It only shows over a game in **borderless or windowed** mode, not over true full screen, and it never takes the mouse, the keys or the focus.
- New: a "Test alert in 8 s" button, so you can switch to the game and see whether the alert appears over it.
- The top bar and the tester notes now say the game must be in borderless or windowed mode for the alert.

## 0.1.0-alpha.2
- New: Le Mans Ultimate support (turn on *Settings > Gameplay > Enable Plugins* in the game). The road is drawn from the track edges the game reports.
- New: steward view for league stewards: every driver judged by name, with the steward's own decision, reasons and history kept beside the tool's number.
- New: a Recordings screen with search, filters and sorting (it copes with hundreds of recordings), and an "Analysing" popup with a progress bar.
- New: Manage recordings: the size of each recording, zip (about 3 to 5 times smaller, it still opens) and move to the Recycle Bin, with a warning when the tool has not learned from a recording yet.
- New: brake (red), throttle (green) and steering shown under the replay for you, and for the other car when the game reports them (Le Mans Ultimate: every car; RaceRoom: your car only).
- New: the road is remembered between sessions for each track layout; a kerb found once stays found, and the replay road stops at kerbs.
- Better: choosing the recording that is already open no longer analyses it again, and the previous recording is cleared as soon as you pick another, so nothing of it shows while the new one loads.
- Better: larger, more readable text (A- / A+), session types (practice, qualifying, race) kept apart, ground surfaces coloured.

## 0.1.0-alpha.1
- First test build: RaceRoom recording, collision detection, fault split with reasons, replay, test-data export.
