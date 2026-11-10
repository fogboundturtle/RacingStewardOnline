# Changelog

## 0.1.0-alpha.18
- New: Help > Check for updates (opt-in, one question at first start). It installs the new version after checking GitHub's checksum. Testers on alpha.17 or older install this one by hand.
- New: Settings > Acceleration unit (m/s², g or km/h/s) for braking figures.
- New: the recordings list can be folded away (arrow at its top right).
- New: a quick move across toward a car beside or behind counts extra, and so does a path steeper toward the other car over the approach (Settings > analysis rules > Side contact).
- Changed: who moved toward whom is measured across the road where it is known, and small moves count for less.
- Changed: the overtaker's blind-spot blame shrinks when the car ahead swerved across abruptly.
- Changed: steering counts only when known for both cars, so the player alone is not blamed for it.
- Changed: the split reads "Estimated responsibility", rounded to 5% (exports keep exact numbers).
- Changed: Statistics are recounted; some verdicts change.

## 0.1.0-alpha.17
- New (EXPERIMENTAL): Assetto Corsa EVO support. Checked on one practice and one race against AI only, game version 0.9.1.
- AC Evo: other cars are named "Car 1", "Car 2" ...; their speed, heading and track position are worked out from their positions.
- AC Evo: the game gives no impact reading, so contacts come from the cars overlapping plus a sudden speed change. Pit lane and ground surface are not read yet.
- Changed: a car that moves across in front of you, then brakes hard for a corner just ahead, counts as a lane change (half weight), not a cut-off. Switch: Settings > analysis rules > Cut-off and vision.
- Changed: the top line says "Waiting for a game to load".

## 0.1.0-alpha.16
- Fixed: random crash (memory error) while recording or switching recordings.
- Changed: a closed game ends the recording after 15 s without data (was 60). A pause longer than 15 s also ends it.
- Known: edges between ground pictures (grass, gravel, sand) look stepped in the 3D view.

## 0.1.0-alpha.15
- New: first person view picks a random sky (day, dusk or night) by the recording's time of day.
- New: pit lane and grandstands placed from OpenStreetMap data for 51 RaceRoom and Le Mans Ultimate circuits (file circuits.rsc, nothing is downloaded). Falls back to the old guess if the map does not fit.
- New: sand, gravel and dirt ground pictures; gravel strip along road edges; sand round desert circuits and Laguna Seca.
- New: painted concrete walls on the Mount Panorama (Bathurst) mountain section. Placed by a rule, not exact.
- Changed: road at the start line joins the end of the lap (no bare gap).
- Fixed: first person view froze on big circuits (Laguna Seca); pit entry and exit join the track; pit lane lines no longer cross it.
- Known: crash when switching recordings during a replay (seen twice, cause not found). Map data checked by eye on a few circuits only.
- Data: pit lanes and grandstands (c) OpenStreetMap contributors, ODbL (https://www.openstreetmap.org/copyright). Sand, gravel and dirt pictures: CC0, Poly Haven.

## 0.1.0-alpha.14
- New: first person view has car models by class (GT3/DTM, GT4, touring, stock car, open wheel), turning wheels, glossy paint and brake lights.
- New: tarmac, grass and sky pictures instead of flat colour.
- New: distance boards (200, 150, 100, 50 m) before corners. View menu switch.
- New: start gantry, grandstands, pit lane with garages and barriers on the start straight, placed from the road and parked cars (a guess). View menu switch.
- Changed: model and picture files ship with the program (about 3 MB more). A missing file is drawn plain.
- Known: frame rate with a full field not measured; tell us if the first person view is slow.

## 0.1.0-alpha.13
- New: first person view (3D prototype): View > First person in the incident and race replay. Sit in the car or orbit it with the mouse. Needs DirectX 11, otherwise a simpler drawing is used.
- New: Live steward view (Tools > Live steward view) for spectating a RaceRoom dedicated server: collisions as they happen, decisions saved with the recording.
- New: Settings > Penalty server... sends penalties to the steward's own dedicated server. OFF until turned on; the only thing the program ever sends over the network.
- New: Settings > Automatic penalties... proposes penalties by confidence and hit strength. Only tried against a test stand-in, not real players: prefer "In game" or "Countdown" over "Automatic".
- Changed: new look (colours, fonts, icons), more polished track map and incident picture.

## 0.1.0-alpha.12
- New: mark a moment while driving. Settings > Marker button... sets a key or a wheel/joystick button. Shown on the overlay and as a cyan pin on the race replay timeline. Only tried with a keyboard: tell us if your wheel button works.
- New: "Help me tune ..." in Settings > Analysis rules: pick a goal in plain words (15 goals) and get the settings to change; preview on the open recording; add to draft or save as preset. Amounts are first guesses.

## 0.1.0-alpha.11
- New (EXPERIMENTAL): Automobilista 2. In the game set Options > System > Shared Memory = "Project CARS 2" and restart. Checked on one race of light contacts only: please send recordings of hard and wall hits (File > Export test data).
- New: each game (RaceRoom, Le Mans Ultimate, Automobilista 2) has its own settings and presets in Settings > Analysis rules; a recording uses its own game's settings. Existing rules.json is copied to all three.
- Changed: Standard rules slightly less sensitive (velocity-change trigger 1.0 to 1.3 m/s, RaceRoom impact 8 to 10, Le Mans Ultimate impact 200 to 260, squeeze 0.8 to 1.0 s, push 1.0 to 1.2 s). Hard racing and Strict unchanged. Reopened recordings can show fewer incidents; Statistics are recounted.
- Changed: each session (practice, qualifying, race, restart) gets its own recording folder. Existing recordings unchanged.
- New: RaceRoom class names learned from recording folder names and a small list, so "DTM 2024" shows instead of "Class 13136".
- New: program icon (shield and magnifier).
- New: chain rule: a driver at fault for every later contact in a chain (at least 2) is at fault for the first contact in full. Two new values in the Control & chain tab. Changed one incident on our recordings.

## 0.1.0-alpha.10
- New: Settings > Analysis rules... lists every value used to find contacts and split fault (about 120 values, 10 tabs, search box). Changes stay in a draft until Apply; changed values are orange and can be reset.
- New: presets Standard, Hard racing and Strict (untested guesses). Save your own under a name.
- New: settings saved in rules.json; Export and Import let a league share the same rules.
- New: results made with changed rules show "Custom rules" (or the preset name) under the tabs and in the incident report.
- Fixed: zip from File > Export test data looked empty in Windows Explorer. Older zips: open with 7-Zip or File > Import test data.
- Known: Statistics use whatever rules are active when a recording is opened, so totals can mix rules.

## 0.1.0-alpha.9
- New: RaceRoom records every car by default (about 10 MB per minute, 300 MB for 30 min). Settings > Record every car (RaceRoom)... turns it off (then cars within about 150 m are kept, was 50 m).
- New: the incident replay can show both drivers' field of view (View > Field of view). An assumption (cockpit view). The evidence says how the other car was seen.
- Better: fault in corners is judged against the line the field drives (recordings only, not the live view).
- Better: a car steering across into a car holding its line is blamed, also at a race start.
- Fixed: a tight corner (hairpin) no longer counts as a spin, which had forced 50/50 verdicts.
- Fixed: a recording with no incident opens on the race, not the grid.
- Faster: big recordings open about a third faster.
- Statistics are recounted (open a recording or "Count them now"). Some old verdicts change; tell us when one looks wrong.

## 0.1.0-alpha.8
- New fault rule: slow drift into another car's lane on a straight (last 10 s, against the road, not in the 100 m before a corner). The car ahead is blamed; the car behind is not blamed for the blind spot.
- Statistics are recounted after this update.

## 0.1.0-alpha.7
- New: File > Import test data... adds a zip from Export test data to a separate "imported" list, kept out of your statistics and best laps. Nothing is overwritten.
- New: Settings > Recordings folder... chooses where recordings are kept and can move existing ones. If the folder is missing at start, the default is used.
- New: best laps in Statistics > Tracks, per car class, with "Show lap" to open it in the replay. Statistics are recounted.
- New: race replay "Follow the selected car" keeps it centred while zooming.
- Better: fault judged against the road the cars drive: sideways moves on a straight are blamed on the mover; the 100 m before a corner is a braking zone; a car sent spinning is not blamed for what it hits. Not in the first laps (road unknown).
- Fixed: empty "probe_..." recording saved from the game's menus. Old ones are removed at start.
- Fixed: a recording named "(2)" showed "(no date)".

## 0.1.0-alpha.6
- New: Help window (Help > How to use Racing Steward, or F1); About box rewritten.
- New: drag the bars between panels to resize them (double-click resets); sizes are remembered.
- New: mouse wheel zooms the incident replay.
- New: race replay marks the formation lap (RaceRoom collisions off); not counted as contacts.
- Better: recordings list is one card per recording; easier map zoom (Map + / - / Fit).

## 0.1.0-alpha.5
- New: menu bar (File, View, Tools, Settings, Help), tabs and keyboard shortcuts (Ctrl+O, Ctrl+1/2/3, F5, Ctrl+plus/minus).
- New: Recordings and incidents in one tab, with search, Game / Track / Class filters and sorting.
- New: Race replay tab: whole race from above, standings with gaps and pit stops, timeline with incidents; speed up to 32x, follow a car, zoom, drag.
- New: RaceRoom can record every car (Settings > Record every car (RaceRoom)); off until you accept a warning (about 10 MB per minute). Le Mans Ultimate always does.
- New: league incident report (Tools > Incident report..., steward view): one browser page with every incident, steward decision first.
- New: recordings untouched for 7 days are zipped (Settings > Zip old recordings...). Recordings with a steward decision stay.
- Better: tester notes describe the new window.

## 0.1.0-alpha.4
- New: Statistics screen: overview, driving, tracks, cars, drivers, trends, hotspots. Recordings are counted when opened; "Count them now" counts the rest.
- New: darker racing look; incident screen with replay left, verdict right and tabs (Evidence, Timeline, Steward decision, Each contact).
- New: incident cards (other driver, verdict, time, lap, speed, fault bar); plain names for rules.
- New: in the replay the picked driver is blue, the others grey.
- New: each car's class shown in multi-class races.
- New: flags as context (blue, yellow, wrong way, track cut); they do not change the split. Le Mans Ultimate: every car; RaceRoom: your car only; saved recordings only.
- Better: the top bar counts down while a closed game's recording waits to be saved.

## 0.1.0-alpha.3
- New: optional alert over the game after each contact (who is at fault, split). Off by default ("Alert after a contact" in the top bar). Borderless or windowed mode only; never takes mouse, keys or focus.
- New: "Test alert in 8 s" button.
- Changed: top bar and tester notes say the game must be borderless or windowed.

## 0.1.0-alpha.2
- New: Le Mans Ultimate (turn on Settings > Gameplay > Enable Plugins in the game). Road drawn from the track edges.
- New: steward view: every driver judged by name, with the steward's own decision, reasons and history.
- New: Recordings screen with search, filters and sorting; "Analysing" popup with progress.
- New: Manage recordings: sizes, zip (3 to 5 times smaller), move to the Recycle Bin.
- New: brake, throttle and steering under the replay (Le Mans Ultimate: every car; RaceRoom: yours).
- New: road remembered per track layout; kerbs stay found.
- Better: reopening the open recording does not analyse it again; the previous one clears at once.
- Better: larger text (A- / A+), session types kept apart, coloured ground surfaces.

## 0.1.0-alpha.1
- First test build: RaceRoom recording, collision detection, fault split with reasons, replay, test-data export.
