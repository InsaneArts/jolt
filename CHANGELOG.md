# Changelog

Every released version of Jolt, newest first, with the download on the [releases page](https://github.com/InsaneArts/jolt/releases). Jolt updates itself, so you are on the latest version unless you turned that off.

## [0.3.3](https://github.com/InsaneArts/jolt/releases/tag/v0.3.3) — 22 September 2026

- Rows no longer show Jev's percentage beside the result.

## [0.3.2](https://github.com/InsaneArts/jolt/releases/tag/v0.3.2) — 22 September 2026

- Files searches only the folders you choose, and nothing until you choose them: Choose Folders… in the Files scope, or Add Folder… in Settings › Privacy. Folders from 0.3.0 and 0.3.1 have to be chosen again.
- A folder that Jolt can no longer read offers Choose Again… and Remove.
- Folders are results too. Return opens a folder or previews a file, and Option-Return shows either in Finder.

## [0.3.1](https://github.com/InsaneArts/jolt/releases/tag/v0.3.1) — 21 September 2026

Jolt has a new bundle identifier, `com.insanearts.jolt`, so macOS sees it as a new app. After this update:

- Allow Jolt again in System Settings › Privacy & Security › Accessibility. The old Jolt entry there can be removed.
- Settings are back to their defaults, the shortcut to Command-Space among them, and the counts of what you run start over.
- Check Launch at login in Settings › General.

## [0.3.0](https://github.com/InsaneArts/jolt/releases/tag/v0.3.0) — 21 September 2026

The public beta. Jolt is free while it lasts, and you no longer need a TypeSafe API key.

- Plain-language search works without a key of your own: Jolt asks Jev through its own service. The `api-key` file of 0.2.0 is no longer read, and you can delete it.
- Files, a third scope. Tab moves between the menus of the app you are in, the Mac, and Files, and a space in an empty field goes straight to Files. Find a file by its name, or turn on Find files with Jev in Settings › Privacy to describe it. Command-C copies the file, Command-Shift-C copies its path, and you can drag a row out of the panel.
- Web search: "!g", "!yt", "!w" and the other bangs search Google, YouTube, Wikipedia, GitHub, Stack Overflow, Amazon, Reddit, Maps, X, IMDb, Spotify, or DuckDuckGo in your browser. Jev picks the site when you describe the search instead.
- Actions that take a value: "keep awake for 35 minutes", "volume 20", "screenshot window in 5s". The value is read on the Mac.
- Actions of your apps, read from their scripting dictionaries: "spotify next", "dark mode on", "make the dock hide itself". Jolt never offers one that deletes, erases, quits, or logs out.
- A Lock Screen action.
- A settings window, from the bolt menu or with Command-Comma, with Launch at login.
- One shortcut to open Jolt, Command-Space unless you record another in Settings › General. The `[` key, Option-Space, and Control-Option-J no longer open it. If Spotlight still has Command-Space, change one of the two.
- Menu items that are your data, such as recent documents, history, bookmarks, and window names, stay on the Mac and out of the requests to Jev. Turn this off in Settings › Privacy.
- The panel starts small and grows with the results, takes the color of the app in front, and remembers where you moved it on each display.
- An app you install shows up without restarting Jolt.

## [0.2.0](https://github.com/InsaneArts/jolt/releases/tag/v0.2.0) — 18 September 2026

- Show the row that a query means: Jolt opens the System Settings pane, scrolls to the row, and puts a ring on it for three seconds. It does the same in the settings window of an app that has a sidebar.
- Name the Control Center pane "Menu Bar" on macOS 26, and say in its hint that it hides the menu bar.

## [0.1.0](https://github.com/InsaneArts/jolt/releases/tag/v0.1.0) — 18 September 2026

The first release.

- Two scopes, switched with Tab: the menus of the app you are in, and the commands of the Mac — your installed apps, the System Settings panes, and a few actions.
- Plain-language search through Jev, with your own TypeSafe API key. The local name match answers first on every keystroke, and Jev's answer arrives on its own.
- Three ways in: the `[` key, Option-Space, and Control-Option-J.
- Jolt counts what you run: the count breaks ties, and an empty query lists what you run most.
- Keyboard: Control-N and Control-P move the selection, Command-1 to Command-8 run a row, Page Up and Page Down jump to the first or last row, and the first Escape clears the query.
- An Edit menu, so select all, copy, paste, cut, and undo work in the search field.
- Automatic updates through Sparkle, checked once a day.
