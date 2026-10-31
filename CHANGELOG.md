# Changelog

## 0.1.0-alpha.3 (built, not yet published)
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
