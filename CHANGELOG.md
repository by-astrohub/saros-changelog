# Changelog

All notable changes to Saros. Format based on [Keep a Changelog](https://keepachangelog.com).
Saros is in beta. Beta builds are unsigned previews for Apple Silicon; each one has
release notes and downloads under [Releases](../../releases). Beta 01 and Beta 02
went to private testers only; Beta 03 is the first public build.

## [Unreleased]

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

[Unreleased]: ../../compare/v0.1.0-beta.03...HEAD
[0.1.0-beta.03]: ../../releases/tag/v0.1.0-beta.03
