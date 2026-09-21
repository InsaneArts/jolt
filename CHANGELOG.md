# Changelog

Every released version of Jolt, newest first, with the download on the [releases page](https://github.com/InsaneArts/jolt-app/releases). Jolt updates itself, so you are on the latest version unless you turned that off.

## [0.2.0](https://github.com/InsaneArts/jolt-app/releases/tag/v0.2.0) — 18 September 2026

- Show the row that a query means: Jolt opens the System Settings pane, scrolls to the row, and puts a ring on it for three seconds. It does the same in the settings window of an app that has a sidebar.
- Name the Control Center pane "Menu Bar" on macOS 26, and say in its hint that it hides the menu bar.

## [0.1.0](https://github.com/InsaneArts/jolt-app/releases/tag/v0.1.0) — 18 September 2026

The first release.

- Two scopes, switched with Tab: the menus of the app you are in, and the commands of the Mac — your installed apps, the System Settings panes, and a few actions.
- Plain-language search through Jev, with your own TypeSafe API key. The local name match answers first on every keystroke, and Jev's answer arrives on its own.
- Three ways in: the `[` key, Option-Space, and Control-Option-J.
- Jolt counts what you run: the count breaks ties, and an empty query lists what you run most.
- Keyboard: Control-N and Control-P move the selection, Command-1 to Command-8 run a row, Page Up and Page Down jump to the first or last row, and the first Escape clears the query.
- An Edit menu, so select all, copy, paste, cut, and undo work in the search field.
- Automatic updates through Sparkle, checked once a day.
