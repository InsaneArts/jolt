# Jolt

Jolt is a macOS launcher that understands plain language. Type an app name and it behaves like any launcher. Say what you want instead — "why is my fan so loud", "bring back the tab I just closed" — and Jolt finds the command that does it, even when no word of the query is in the command's name.

**[usejolt.app](https://usejolt.app)** · [Download](https://usejolt.app) · [Changelog](CHANGELOG.md) · [Discussions](https://github.com/InsaneArts/jolt-app/discussions) · [Report a bug](https://github.com/InsaneArts/jolt-app/issues/new/choose)

This repository is where Jolt is discussed in public: bug reports, feature requests, questions, and the changelog. Jolt's source code lives elsewhere and is not part of this repository.

## What Jolt does

Press `[`, Option-Space, or Control-Option-J. Type, move with the arrow keys, press Return to run the row. Tab switches between three scopes.

**The menus of the app you are in.** "wipe the old compiled files" in Xcode presses Product › Clean Build Folder. A row shows its menu path and its keyboard shortcut.

**The commands of the Mac.** Installed apps, System Settings panes, and built-in actions. "my disk is full" finds the Storage pane, and Jolt opens it, scrolls to the row, and puts a ring on it. Actions that take a value read it from the query: "keep awake for 35 minutes", "volume 20", "screenshot window in 5s". Scriptable apps bring their own actions: "spotify next", "dark mode on".

**Your files.** "my resume" finds `Tornike_CV_2026.pdf`; "all my movies" lists the films and leaves out the screen recordings. Files are indexed only in folders you pick yourself.

The Mac scope also searches the web. "watch the new dune trailer" finds YouTube, "directions to heydar aliyev center" finds Google Maps, and bangs work as in DuckDuckGo: `!yt lofi beats`, `alan turing !w`.

The understanding comes from [Jev](https://typesafe.ai), TypeSafe's System One model. Jolt asks it one multiple-choice question whose options are every command, and reads back a probability for each. The name match never waits for it: every keystroke matches names locally in microseconds, and Jev's answer arrives about a third of a second later.

## Requirements

macOS 14 or later. A release build updates itself with Sparkle and checks for updates once a day. Jolt needs Accessibility permission to read the menus of other apps; without it, it opens on the commands of the Mac.

An active trial or license is required to open the launcher. The 14-day trial needs no email and no key.

## Privacy

Jolt writes no query to disk and logs none. Queries shorter than three characters stay on the Mac, as do one- and two-word name prefixes. File contents, sizes, and dates are never sent. Menu titles that look like documents or addresses — recent files, browser tabs — stay on the Mac by default. The full account of what leaves your Mac, scope by scope, is on [usejolt.app](https://usejolt.app).

## Getting help

- **Something is broken** → [open a bug report](https://github.com/InsaneArts/jolt-app/issues/new/choose)
- **Something is missing** → [open a feature request](https://github.com/InsaneArts/jolt-app/issues/new/choose)
- **A question, or an idea to talk through** → [Discussions](https://github.com/InsaneArts/jolt-app/discussions)
- **A security issue** → [SECURITY.md](SECURITY.md), not a public issue

Jolt is made by [InsaneArts](https://github.com/InsaneArts).
