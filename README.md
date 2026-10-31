Racing Steward

Ever had a contact in mid-race and wondered who was actually at fault? Racing Steward is an automated collision analyzer built for sim racers. Running quietly alongside RaceRoom Racing Experience or Le Mans Ultimate, it detects on-track contacts and breaks down responsibility.

When a collision happens, it provides a complete incident breakdown:

Fault Split: A clear percentage breakdown (e.g., You 70% / Opponent 30%).

Plain-English Reconstruction: A step-by-step story of how the incident unfolded.

Telemetry & Evidence: Hard data pulled directly from the physics engine.

Top-Down Replay: An overhead visual synced with brake, throttle, and steering inputs.

🚨 Early Alpha Notice

Think of Racing Steward’s verdicts as a digital second opinion, not absolute truth. It will get things wrong! It is not an official steward, and human league stewards can easily override any verdict inside the app (the original score and human verdict are both saved side-by-side).

Note: This repository hosts downloads and release notes only. Racing Steward is not open source.

📥 Download & Installation

Download: Grab the latest installer (RacingSteward-Setup-*.exe) from the Releases page.

Want to double-check the download? You'll find the SHA-256 hash listed alongside each release note.

Launch: Run the setup file to install.

⚠️ Windows Warnings Notice

Because the installer isn't code-signed yet, Windows SmartScreen will display a "Windows protected your PC / Unknown publisher" warning.

Click More info, then click Run anyway.

If your antivirus is overly cautious with unsigned software, feel free to run the installer through VirusTotal to compare the SHA-256 before launching.

💻 Requirements & Game Setup

OS Requirements

OS: 64-bit Windows 10 or 11.

No extra frameworks or dependencies need to be installed manually.

Simulator Setup

RaceRoom Racing Experience: Zero setup required! It broadcasts shared data automatically.

Le Mans Ultimate: Go to Settings > Gameplay, enable Enable Plugins, and restart the game. The tool cannot read collision data without this turned on.

🚀 Quick Start Guide

Launch: Open Racing Steward, review the initial data notice, and agree to proceed.

Drive: Fire up your simulator and hit the track. The app auto-detects telemetry and begins recording (indicated by a REC icon in the top bar). Offline AI sessions are great for testing!

Review Incidents: A few seconds after a bump or crash, the incident will populate in your list. Click it to inspect the telemetry replay, event chain, and fault verdict.

Manage Archives:

Use Recordings... to search, filter, and sort past sessions.

Use Manage recordings... to check disk usage, archive sessions into compressed .zip files (reducing size by 3x–5x without breaking playback), or send old files to the Recycle Bin.

In-Game Overlay (Optional): Check Alert after a contact to get a quick popup notification over your screen after an incident.

Note: Requires running your game in Borderless or Windowed mode (will not render over Exclusive Fullscreen).

League Steward View: Looking to steward a league race? Switch to Steward view (all drivers) to analyze driver-to-driver incidents impartially by name rather than from a single player's perspective.

🔒 Privacy & Local Data

100% Local Processing: All telemetry recordings, track profiles, and user preferences live locally in %LOCALAPPDATA%\RacingSteward. Racing Steward contains zero tracking or network code and never sends data to external servers.

Session Details: Telemetry captures nearby driver names, track positions, and inputs as output by the game engine. None of this leaves your machine unless you share it yourself.

Sending Feedback: Found a weird verdict? Click Export test data... to generate an anonymized ZIP file. This automatically strips out player identities (replacing your name with "Tester" and stewards with "Steward") so you can safely send it over for debugging.

Uninstalling: Removing the application leaves your user data folder intact. If you want a completely clean wipe, simply delete the %LOCALAPPDATA%\RacingSteward folder manually.

⚠️ Known Alpha Limitations

Verdict Accuracy: The math isn't perfect yet. The primary goal of this public alpha is catching edge-case collisions to train the analyzer engine.

Telemetry Depth: RaceRoom only exposes telemetry (brake, throttle, steering) for your vehicle. Le Mans Ultimate provides full telemetry across all nearby cars, making its evidence breakdowns significantly richer.

LMU Calibration: Vehicle hitboxes and collision thresholds for Le Mans Ultimate are still undergoing tuning.

Track Mapping: Because RaceRoom doesn't supply map layouts, the app builds track geometry dynamically as you drive. Layout precision improves over multiple laps.

Untested Scenarios: VR setups, clean Windows installs without developer packages, and Exclusive Fullscreen modes have not been fully verified yet.

🐛 Reporting Issues

Found a bug or an incorrect verdict?

Open a public GitHub Issue describing the track, game, and what went wrong.

Do not attach raw telemetry or log files to public issues as they contain driver names.

If we need your anonymized ZIP or telemetry files to investigate, we will reach out with a secure upload link or email.

📄 Legal & Attribution

Check out TERMS.md for full terms. Racing Steward is an independent project and is not affiliated with or endorsed by Sector3 Studios (RaceRoom) or Studio 397 (Le Mans Ultimate). All product and brand names belong to their respective owners.

Third-party libraries used in this build (Dear ImGui, nlohmann/json, RaceRoom shared-memory headers) along with their corresponding licenses are detailed in THIRD-PARTY-NOTICES.txt located in the installation folder.
