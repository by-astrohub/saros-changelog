# Changelog

All notable changes to Saros. Format based on [Keep a Changelog](https://keepachangelog.com).
Builds are for Apple Silicon and are not yet signed or notarized; each one has
release notes and downloads under [Releases](../../releases). Beta 01 and Beta 02
went to private testers only; Beta 03 was the first public build.

## [Unreleased]

## [1.3.0] - 2026-10-05

### Added
- Settings > Agents connects Claude Code, Codex and Claude usage with one Connect all, and
  opens on its own the first time Saros starts. Each agent shows whether it is connected,
  needs an update, or (for Codex) is waiting for you to trust the hooks in `/hooks`
- Open Saros at login, and Uninstall, which takes Saros out of every agent and moves the
  app to the Trash while your plan stays
- Saros offers to move itself into Applications when it is opened straight from the disk image

### Changed
- Agents reach Saros through a link Saros keeps pointed at the installed app, so moving or
  updating the app no longer disconnects them
- Connecting no longer needs the ZIP or Python; the ZIP's `.command` files still work
- The disk image window shows where to drag Saros and how to approve the first open

## [1.2.1] - 2026-10-05

### Fixed
- Saros 1.2.0 downloaded from the website opened as "damaged" and macOS offered only Move to Trash.
  The app is now signed as a whole bundle, so the first open works as described in the install steps

## [1.2.0] - 2026-10-05

### Added
- Saros Lite and Saros Pro: every install runs Pro for 2 months, then becomes Lite.
  Pro features lock instead of disappearing, and clicking one opens a paywall
- A plan line at the top of the gear, right-click and menu bar menus, which now share one menu
- Settings > Plan (was License) with the plan, trial days left and a Lite / Pro comparison
- License keys are entered in place in Settings > Plan, with the reason shown when a key is rejected

### Changed
- Get Saros Pro… asks before opening the mail app

## [1.0.1] - 2026-10-04

### Added
- `Install Claude Hooks.command` in the ZIP connects Claude Code in one step: it backs up
  `~/.claude/settings.json`, keeps every other hook, updates hand-written Saros entries in place,
  and takes them out again with `--remove`

## [1.0.0] - 2026-10-04

First release. Same features as Beta 03.

### Changed
- The app's bundle identifier is now `com.astrohub.saros`. After replacing a beta,
  macOS asks once more for Automation permission. Trial, license and settings carry over.
- Install steps for macOS 15 and newer, where Control-click > Open no longer bypasses Gatekeeper

### Known limitations
- Claude Code hooks are added to `~/.claude/settings.json` by hand; the release notes have the entries to copy.
  Codex has an installer (`Install Saros Monitoring.command`).
- Not signed or notarized yet.
- No launch at login yet.

## [0.1.0-beta.03] - 2026-10-02

### Added
- Answer an agent's question from the notch, not only Allow / Deny
- Approve from the notch, and help text for every setting
- Usage tab in the notch: five-hour and weekly limits, with plan names
- Show usage in the notch, an edge rail, both, or neither
- Choose which display the panel lives on
- Settings window with three panes, opened from the gear in the expanded notch
- Right-click menu on the notch and a confirmed Quit
- Open VS Code sessions from their row
- 60-day trial and license keys

### Changed
- Summary rows name the session instead of its latest command
- Usage stays on screen until its window resets
- Full-bleed app icon for macOS 26

### Fixed
- Auto-mode calls are no longer held waiting for a decision
- The panel only redraws when something moves, so it idles at near-zero CPU

## 0.1.0-beta.02.1 - 2026-09-28

### Fixed
- Panel resources load from inside `Saros.app`

## 0.1.0-beta.02 - 2026-09-22

### Added
- Codex usage from local session logs: five-hour and weekly percentages with reset countdowns
- Opt-in Claude Code usage through a status line collector
- Codex monitoring, installed by `Install Saros Monitoring.command` with a dated backup of your hooks
- Packaged as a DMG with a Finder-launchable app and a demo mode

## 0.1.0-beta.01

### Added
- Notch panel with collapsed, summary and decision states
- Claude Code and Codex adapters
- Allow / Deny permission requests from the notch
- Live status per agent with elapsed time
- Terminal jump from a row to its exact window
- File-level collision warnings across worktrees
- Floating glass pill on displays without a notch

[Unreleased]: ../../compare/v1.2.0...HEAD
[1.2.0]: ../../releases/tag/v1.2.0
[1.0.1]: ../../releases/tag/v1.0.1
[1.0.0]: ../../releases/tag/v1.0.0
[0.1.0-beta.03]: ../../releases/tag/v0.1.0-beta.03
