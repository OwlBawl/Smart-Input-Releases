# Smart Input 🦉

**Smart Input** is a lightweight, professional macOS utility designed to solve the "wrong keyboard layout" problem. It automatically detects when you've typed text in the wrong language and allows you to convert it instantly, either manually or automatically.

![Swift](https://img.shields.io/badge/Swift-5.0-orange.svg)
![macOS](https://img.shields.io/badge/macOS-14.6+-blue.svg)
![License](https://img.shields.io/badge/license-All%20Rights%20Reserved-red.svg?style=flat-square)

## ✨ Key Features

- **Double-Shift Conversion:** Tap the Shift key (or Control/Option/Command) twice quickly to convert the last typed word or selection to the correct layout.
- **Auto-Conversion:** Automatically detects and corrects the layout as you type (triggered by Space, Enter, or Tab).
- **Intelligent Layout Detection:** Support for multiple languages (English, Ukrainian, etc.) with deterministic layout matching.
- **Smart Exceptions:** 
  - **App Blacklist:** Disable conversion in specific apps (e.g., Terminal, IDEs).
  - **Word Whitelist:** Define specific words that should never be converted.
  - **Correction Awareness:** Stops converting if you press Backspace or manually change the layout.
- **Modern UI:** A sleek, native macOS menu bar interface built with SwiftUI.
- **Seamless Updates:** Built-in auto-update system powered by Sparkle.

## 🚀 Getting Started

### Installation
1. Download the latest version [released](https://github.com/OwlBawl/Smart-Input-Releases/) version or just autoupdate it if in use already.
2. Drag **Smart Input.app** to your `Applications` folder.
3. Launch the app and grant the required **Accessibility Permissions** so it can detect keystrokes and perform text replacement.

### Usage
- **Manual:** Just type. If you realize you typed in the wrong layout, double-tap **Shift**.
- **Automatic:** Enable "Background Auto-Conversion" in Settings. The app will detect wrong-layout patterns and fix them as soon as you hit Space.

## 🛠 Development

### Prerequisites
- Xcode 15.4+
- macOS 14.6+

## ⚖️ License & Copyright

Copyright © 2026 **OwlBawl**. All rights reserved.

**Smart Input** is provided for personal use only. 
- You may not redistribute, modify, or sell this software without explicit written permission from the author.
- Reverse engineering or unauthorized distribution of the binary artifacts is strictly prohibited.

## 🦉 Author
Built with vibe for macOS by **OwlBawl**.
