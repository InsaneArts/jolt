# Jolt

Jolt is a macOS launcher that understands plain language. Type an app name and it behaves like any launcher. Say what you want instead — "why is my fan so loud", "bring back the tab I just closed" — and Jolt finds the command that does it, even when no word of the query is in the command's name.

**[usejolt.app](https://usejolt.app)** · [Download the latest release](https://github.com/InsaneArts/jolt-app/releases/latest) · [Changelog](CHANGELOG.md) · [Discussions](https://github.com/InsaneArts/jolt-app/discussions) · [Report a bug](https://github.com/InsaneArts/jolt-app/issues/new/choose)

This repository is where Jolt is discussed in public: bug reports, feature requests, questions, and the changelog. Jolt's source code lives elsewhere and is not part of this repository.

## What Jolt does

This describes **0.2.0**, the current release. Jolt is early, and the changelog is where each version says what changed.

Press `[`, Option-Space, or Control-Option-J. Type, move with the arrow keys, press Return to run the row. Escape closes the panel. Tab switches between two scopes.

**The menus of the app you are in.** "wipe the old compiled files" in Xcode presses Product › Clean Build Folder. Other launchers match menu items by name only. A row shows its menu path and its keyboard shortcut.

**The commands of the Mac.** Your installed apps, the System Settings panes, and a few actions. "my disk is full" finds the Storage pane — and Jolt then shows you where the setting is: it opens the pane, scrolls to the row, and puts a ring on it for three seconds. It does the same in the settings window of an app that has a sidebar.

Jolt counts what you run. The count breaks ties, and an empty query lists what you run most.

The understanding comes from [Jev](https://typesafe.ai), TypeSafe's System One model. Jolt asks it one multiple-choice question whose options are every command, and reads back a probability for each. The name match never waits for it: every keystroke matches names locally in microseconds, and Jev's answer arrives about a third of a second later, on its own.

## Download

Every release is on the [releases page](https://github.com/InsaneArts/jolt-app/releases), newest first. Take the `.dmg`, open it, and drag Jolt to Applications. The `.zip` beside it holds the same build in the form Sparkle installs an update in; you do not need it to install Jolt.

Jolt has no Dock icon. Look for the bolt in the menu bar.

## Requirements

macOS 14 or later.

**Accessibility permission.** Jolt reads the menus of other apps through the Accessibility API and presses the item you choose. It reads the rows of a System Settings pane the same way. Allow it in System Settings › Privacy & Security › Accessibility, or from the bolt menu. Without the permission, Jolt opens on the commands of the Mac.

**A [TypeSafe](https://typesafe.ai) API key, for plain-language search.** In 0.2.0 you bring your own key, in a file that only you can read:

```sh
mkdir -p ~/Library/Application\ Support/Jolt
printf '%s' "apikey_..." > ~/Library/Application\ Support/Jolt/api-key
chmod 600 ~/Library/Application\ Support/Jolt/api-key
```

Without a key Jolt still works, as a launcher that matches names.

## Updates

A release build updates itself with [Sparkle](https://sparkle-project.org). It checks once a day, and the bolt menu has Check for Updates. The update request holds the version of Jolt and nothing about you.

## What leaves your Mac

When Jolt asks Jev, the request goes to the TypeSafe API. In the menu scope it holds your query, the name of the app, and the titles of the app's enabled menu items — and a menu title can be the name of a recent document or a browser tab. In the Mac scope it holds your query, the names of your installed apps, and the built-in list of panes and actions. When Jolt shows a row of a System Settings pane, a second request holds your query, the name of the pane, and the labels of its rows; for the settings window of an app, one more holds the names of its sidebar sections. A label can be the name of an app, a network, or a device.

A query of one or two words that is a name prefix stays on the Mac. So does a query shorter than three characters, and everything when there is no API key.

Jolt writes no query to disk and logs none. It stores only the counts of what you run.

## Getting help

- **Something is broken** → [open a bug report](https://github.com/InsaneArts/jolt-app/issues/new/choose)
- **Jolt found the wrong command** → [report the query](https://github.com/InsaneArts/jolt-app/issues/new/choose), with the row you expected
- **Something is missing** → [open a feature request](https://github.com/InsaneArts/jolt-app/issues/new/choose)
- **A question, or an idea to talk through** → [Discussions](https://github.com/InsaneArts/jolt-app/discussions)
- **A security issue** → [SECURITY.md](SECURITY.md), not a public issue

[CONTRIBUTING.md](CONTRIBUTING.md) says what makes a report easy to act on.

Jolt is made by [InsaneArts](https://github.com/InsaneArts).
