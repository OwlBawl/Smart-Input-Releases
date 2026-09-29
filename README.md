# Smart Input 🦉

**Smart Input** is a lightweight macOS menu-bar utility that fixes text typed with the wrong keyboard layout. It can correct words automatically while you type or convert the current word or selected text on demand.

![macOS](https://img.shields.io/badge/macOS-14.6+-blue.svg?style=flat-square)
![License](https://img.shields.io/badge/license-All%20Rights%20Reserved-red.svg?style=flat-square)

## What it does

You type using the wrong keyboard layout:

> ntcn

Smart Input converts the same physical keystrokes to the intended layout:

> тест

It works with the keyboard layouts already configured in macOS and can use more than two enabled layouts.

## Main features

- **Automatic wrong-layout correction** — correct the current word when you press an enabled trigger key.
- **Independent trigger keys** — Space, Tab, and Enter can each be enabled or disabled separately.
- **Manual conversion** — double-tap the configured modifier to convert the current word at any time.
- **Selected-text conversion** — when there is no current word to convert, select text and use the same double-tap shortcut.
- **Configurable shortcut** — use double Shift, Control, Option, or Command.
- **Configurable double-tap timing** — tune the shortcut interval to your typing style.
- **Multiple keyboard layouts** — enable exactly the macOS layouts Smart Input should use.
- **Automatic layout switching** — after a successful conversion, the active keyboard layout follows the converted text.
- **Per-app exclusions** — disable Smart Input in applications where you do not want it to act.
- **Ignored words** — keep names, abbreviations, technical terms, or other chosen words from being auto-corrected.
- **Optional conversion sound** — play a sound when conversion succeeds.
- **Launch at Login** — start Smart Input automatically with macOS.
- **English and Ukrainian interface**.
- **Built-in updates** — automatic update checks/downloads plus a manual **Check for Updates** action.

## Less-obvious features

### Undo an automatic conversion

If Smart Input automatically changes a word and you did not want that conversion, immediately use the manual double-tap shortcut. Smart Input restores the previous text and previous keyboard layout.

### Repeated manual conversion

After a successful manual conversion, the converted word remains available for another immediate double-tap. This lets you continue switching the same current word through your enabled layouts without retyping it.

### Smart layout priority

When the same keystrokes could make sense in more than one enabled layout, Smart Input prefers layouts according to your recent actual layout usage. Layouts you really switch to naturally move forward in that priority.

### Typing inside an existing word

In compatible editors, after moving the caret with the mouse or arrow keys into an existing word, Smart Input can use the neighboring letters to choose the appropriate layout before the first new character is inserted.

### Selected text in difficult editors

Smart Input can convert manually selected text even in many applications and web editors that behave differently from standard macOS text fields.

Select the text, use your configured double-tap shortcut, and Smart Input will use the safest available method to convert it while preserving your current selection and surrounding text.

### Manual conversion remains useful when automatic conversion is suppressed

Actions such as Backspace or a manual layout change can be configured to stop automatic correction for the current editing context without removing the ability to use the manual double-tap conversion.

### Safe handling of passwords and sensitive fields

Smart Input avoids conversion and text tracking in secure/password input contexts. Excluded applications are also left alone.

### One running instance

Opening Smart Input again does not intentionally start another competing keyboard monitor. The existing app is reused and its Settings window can be brought forward.

## Menu-bar controls

Smart Input normally lives in the macOS menu bar rather than the Dock.

From the menu you can quickly:

- see the current keyboard layout;
- switch between enabled layouts;
- invoke conversion;
- open Settings;
- check for updates;
- quit Smart Input.

The Settings window appears in the Dock while it is open and returns the app to menu-bar-only operation when closed.

## Settings

### General

- App language: **English** or **Українська**
- Accessibility permission status and repair/grant action
- Launch at Login
- Conversion sound
- Background Auto-Conversion
- Cancel automatic conversion after manual layout changes
- Cancel automatic conversion after Backspace
- Space / Tab / Enter trigger switches
- Enabled keyboard layouts
- Application exclusions
- Ignored words

### Hotkeys

Choose the modifier used for manual conversion:

- ⇧ Shift
- ⌃ Control
- ⌥ Option
- ⌘ Command

You can also adjust the double-tap interval from **200 ms to 800 ms**.

### Updates

Smart Input can:

- check for updates automatically;
- download updates automatically;
- check manually at any time.

## Diagnostics and logs

Debug Logging is optional and off by default.

When you need troubleshooting data, Smart Input provides:

- a configurable log folder;
- a **Choose…** button for selecting the folder;
- **Use Default** to return to the standard location;
- **Open Logs Folder**;
- an optional **Overwrite Log on App Start** switch;
- daily log rotation and retention of recent logs;
- automatic Debug Logging expiry after 30 days so detailed diagnostics are not accidentally left enabled forever.

Debug mode can contain detailed editor/input diagnostics, so it should be enabled only while troubleshooting. Secure/password fields remain protected.

## Installation

1. Open [Smart-Input-Releases](https://github.com/OwlBawl/Smart-Input-Releases).
2. Download the newest `SmartInput-<version>-<build>.zip`.
3. Unzip it and move **Smart Input.app** to **Applications**.
4. Launch Smart Input.
5. Grant **Accessibility** permission when macOS asks for it.

Smart Input requires **macOS 14.6 or newer**.

After installation, future versions can be installed through the built-in updater.

## Basic use

### Automatic

1. Enable **Background Auto-Conversion**.
2. Enable the trigger keys you want: Space, Tab, and/or Enter.
3. Type normally.
4. When a word clearly belongs to another enabled layout, Smart Input converts it and follows the converted layout.

### Manual

1. Type a word in the wrong layout.
2. Double-tap your configured modifier — Shift by default.
3. Smart Input converts the current word.

For arbitrary existing text:

1. Select the text.
2. Double-tap the configured modifier.
3. Smart Input converts the selection when the editor provides a safe conversion path.

## Compatibility philosophy

Smart Input uses the safest conversion method currently available in the active editor. If an editor exposes less information, Smart Input can use bounded compatibility fallbacks for current-word or explicitly selected-text conversion.

If Smart Input cannot establish a safe conversion path, it prefers leaving the user's text unchanged rather than guessing.

## License & copyright

Copyright © 2026 **OwlBawl**. All rights reserved.

Smart Input is provided for personal use only.

- You may not redistribute, modify, or sell this software without explicit written permission from the author.
- Reverse engineering or unauthorized distribution of binary artifacts is prohibited.

## Author

Built with vibe for macOS by **OwlBawl**.
