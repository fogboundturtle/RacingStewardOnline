# Racing Steward

Ever had a contact in mid-race and wondered who was actually at fault? **Racing Steward** is an automated collision analyzer for sim racers. It runs quietly alongside **RaceRoom Racing Experience**, **Le Mans Ultimate** or **Automobilista 2** (experimental), records your session, detects on-track contacts and breaks down who was responsible. It also replays the incident and the whole race, from above in 2D or in first person in 3D, and gives league stewards the tools to rule on incidents and write a report.

# **RACING STEWARD**

**Reconstruct the incident.**  
**Trace the chain of events.**  
**Understand the responsibility.**

**No AI. Local analysis. Your rules. Explainable decisions.**

**Private by design.** Racing Steward has no server, no account and no tracking. Your recordings are analysed on your own PC and stay there unless you share a file yourself.

Two optional features use the network. Both are off until you turn them on:

- **Update check:** asks GitHub whether a newer version exists.
- **Live penalty sending (league stewards):** sends a penalty to the steward's own RaceRoom dedicated server, only to the address they enter.

## Main features

- **Fault split:** a clear percentage breakdown for every contact (e.g. You 70% / Opponent 30%), with a data-quality score. When the data cannot decide a contact, the tool says "needs steward review" instead of guessing.
- **Plain-English reconstruction:** a step-by-step story of how the incident unfolded, and a timeline of the chain of events.
- **Evidence:** the rules that counted, in readable names ("Rear-end hit", "No braking before the hit"), with the values measured from the game's physics data.
- **Top-down incident replay:** an overhead view of the contact, synced with brake, throttle and steering inputs, with mouse-wheel zoom.
- **First-person 3D view (prototype):** see the incident through a driver's eyes, in the seat or orbiting the car with the mouse, with a rear-view mirror. Switch between the two drivers, and use it in the whole-race replay too. The road, ground and cars follow the elevation recorded by the game, with a sky, lighting and distance fog. If the graphics card cannot run it, the program falls back to a simpler drawing.
- **Whole-race replay:** every car on the circuit, live standings with gaps and pit stops, a timeline with the incidents marked, zoom, and "follow this car". Formation-lap overlaps (when the game has car collisions off) are marked so they are not mistaken for missed contacts.
- **Steward tools:** judge every driver by name, record decisions with a ruling, split, penalty and reason (the tool's own number is kept beside yours, and earlier decisions stay in the history), and write a one-page **incident report** for your league.
- **Statistics:** laps, incidents and fault, your driving, tracks, cars, drivers met and hotspots, added up over all your recordings, plus your **best lap on each track for a car class you pick**, with how it improved and a "Show lap" button.
- **Road-aware fault rules:** the tool works out which way the road points from the cars that drive it, so it can tell a lane change on a straight from a turn-in at a corner, and it does not blame a driver for a spin another car caused.
- **The line the field drives:** from all the cars of a recording the tool works out the usual line through each stretch of the track, and in a side contact it measures who moved toward whom against that line, so in a corner a car that moved away and left room is not blamed for the other car closing the gap.
- **Field of view:** the incident replay can shade what the two drivers could see (in view, the blind spot, the mirrors), and the tool uses it to judge how well a driver knew of the other car. It is an assumption (a cockpit view), not the driver's real camera.
- **Import:** open the recordings someone exported for you (File > Import test data...); they are kept apart from your own and are not counted in your statistics.
- **Classes and flags:** each car's class in multi-class races, and blue and yellow flags shown as context for each incident.
- **Built-in help:** press **F1** for instructions inside the program.

## 🚨 Early alpha notice

Think of Racing Steward's verdicts as a digital second opinion, not absolute truth. **It will get things wrong!** It is not an official steward, and human league stewards can override any verdict inside the app (the original score and the human verdict are both saved side by side).

> This repository hosts downloads and release notes only. Racing Steward is not open source.

## 📥 Download and installation

1. Download the latest installer (`RacingSteward-Setup-*.exe`) from the [Releases page](https://github.com/fogboundturtle/RacingStewardOnline/releases).
2. Want to double-check the download? The SHA-256 hash is listed in each release's notes.
3. Run the setup file to install.

### ⚠️ Windows warning

Because the installer is not code-signed yet, Windows SmartScreen will show a "Windows protected your PC / Unknown publisher" warning. Click **More info**, then **Run anyway**. If your antivirus is cautious about unsigned software, you can run the installer through VirusTotal and compare the SHA-256 before launching.

## 💻 Requirements and game setup

- **OS:** 64-bit Windows 10 or 11. No extra frameworks to install.
- **RaceRoom Racing Experience:** no setup. It shares its data automatically.
- **Le Mans Ultimate:** go to **Settings > Gameplay**, turn on **Enable Plugins**, and restart the game. Without it the tool cannot read the game's data.
- **Automobilista 2 (experimental):** go to **Options > System > Shared Memory**, set it to **Project CARS 2**, and restart the game. Without it the tool cannot read the game's data. Support is new and was checked on very little data.

## 🚀 Quick start

1. **Launch** Racing Steward, read the data notice and agree.
2. **Drive.** Start your sim and race. The app detects the game and records by itself (the line under the menu shows **REC**). Offline AI races are great for testing.
3. **Close the game when you are done.** The app waits 60 seconds without data, then saves the recording and works out the track data from it by itself. The line under the menu counts it down.
4. **Review.** On the **Recordings** tab, click a recording: it unfolds to its incidents. Click an incident for the replay, the chain of events, the verdict and the evidence. Drag the thin bars between the panels to make the replay bigger.
5. **Watch the whole race.** The **Race replay** tab shows every car, the standings and a timeline. Space plays and pauses, the mouse wheel zooms, dragging moves the map.
6. **Find things.** The search box, the Game / Track / Class filters and "Sort by" find a recording among many. **Statistics** adds up everything.

**Menus:** File (open, manage, export and import recordings), View (screens, text size), Tools (learn, steward view, incident report), Settings (alert, storage, recordings folder), Help (instructions, shortcuts, about).

**Shortcuts:** F1 help · Ctrl+O find a recording · Ctrl+1 / 2 / 3 the three tabs · F5 refresh · Ctrl + plus / minus text size.

### Optional: alert over the game

Tick **Settings > Alert after a contact** to get a short alert over the game a few seconds after each contact. It needs the game in **Borderless** or **Windowed** mode (it will not show over exclusive full screen). It never takes the mouse, the keys or the focus.

### League stewards

Turn on **Tools > Steward view (all drivers)** to judge driver-to-driver incidents impartially, by name. Record your decision on the **Steward decision** tab of each incident. When the race is reviewed, **Tools > Incident report...** writes one page for the league: every incident, your decision first (ruling, split, penalty, reason), pictures before, at and after the contact, and the tool's own analysis below as supporting data. Incidents you did not review say "Not reviewed". The page opens in your browser and is saved on the desktop.

## 💾 Disk space

- Recordings take about 10 to 40 MB each. **File > Manage recordings...** shows the size of each and can zip a recording (3 to 5 times smaller, and it still opens) or move it to the Recycle Bin.
- **Settings > Recordings folder...** chooses where recordings are kept (for example on a bigger drive). It asks whether to move the recordings you already have, and the new folder is used from the next start.
- Recordings you have not touched for 7 days are **zipped automatically** (**Settings > Zip old recordings...**). Nothing is lost, and you can change the number of days or turn it off.
- **Both games record every car.** In **RaceRoom** this makes recordings about 4 times bigger (roughly 10 MB per minute of racing, about 300 MB for a 30-minute stint, and about 60 to 100 MB once zipped), and the first screen says so. If you are short of space, **Settings > Record every car (RaceRoom)...** turns it off: only the cars within about 150 m of you are kept then, and the whole-race replay shows few cars. A change applies from the next recording.

## 🔒 Privacy and local data

- **100% local processing.** All recordings, track profiles and preferences live in `%LOCALAPPDATA%\RacingSteward`. Racing Steward contains no tracking and never sends your data to any server of ours (there is none). It has two optional network features, both off until you turn them on. One: the live steward view can send a penalty to the steward's own RaceRoom dedicated server, only to the address they type (this PC by default). The other is the update check: it asks GitHub whether a newer release exists (Help > Check for updates), runs only if you allow it, and sends none of your data.
- **What is recorded:** the driver names, track positions and inputs of the cars in the session, as given by the game (with "Record every car" off in RaceRoom, only the cars near you). None of it leaves your machine unless you share a file yourself.
- **Sending feedback:** found a strange verdict? Use **File > Export test data...** to make an anonymized ZIP (your name becomes "Tester", steward names become "Steward") and send it yourself.
- **Uninstalling** leaves your data folder. For a clean wipe, delete `%LOCALAPPDATA%\RacingSteward` by hand.

## ⚠️ Known alpha limitations

- **Verdict accuracy:** the rules are not perfect yet. The goal of this public alpha is to catch edge cases to improve the analyzer.
- **First laps and the live view:** the road and the usual line are worked out from the cars that drive during the session. A saved recording has them from the first lap, but the live view and the first moments of a session judge with the older rules.
- **Big recordings:** a 30-minute race with every car is a big file. How long it takes to open, and how much it costs the game while recording, is not measured yet; please tell us if you notice either.
- **Telemetry depth:** RaceRoom gives brake, throttle and steering for your car only. Le Mans Ultimate gives them for every car, so its evidence is richer.
- **Flags:** shown for your car in RaceRoom and for every car in Le Mans Ultimate, as context only. They do not change the fault split, and they appear in a saved recording, not in the live view.
- **Formation lap:** RaceRoom has car collisions off during the formation lap and countdown, so overlaps there are not counted as contacts.
- **Lap times:** a clean lap is timed, valid and not in or out of the pits. In Le Mans Ultimate the first lap of a session is not timed.
- **Le Mans Ultimate calibration:** car sizes and collision thresholds are still being tuned.
- **Automobilista 2:** experimental. The game gives other cars' position and speed but no inputs, and a collision strength only for your car, so verdicts rest on less data. Thresholds and car sizes are first guesses.
- **Track mapping:** RaceRoom gives no track layout, so the app builds it as you drive and it improves over several laps.
- **Not fully tested yet:** VR, clean Windows installs, exclusive full screen, and very long sessions.

## 🐛 Reporting issues

Found a bug or an incorrect verdict? Open a public GitHub Issue describing the track, the game and what went wrong. **Do not attach raw telemetry or recordings to public issues**, because they contain driver names. If your anonymized ZIP is needed, we will reach out.

## 📄 Legal and attribution

See [TERMS.md](TERMS.md) for the full terms. Racing Steward is an independent project and is not affiliated with or endorsed by Sector3 Studios (RaceRoom), Studio 397 (Le Mans Ultimate) or Reiza Studios (Automobilista 2). All product and brand names belong to their respective owners.

Third-party libraries used in this build (Dear ImGui, nlohmann/json, RaceRoom shared-memory headers) and their licenses are listed in `THIRD-PARTY-NOTICES.txt` in the installation folder.
