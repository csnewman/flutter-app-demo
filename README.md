# flutter-app

A desktop app built using flutter & rust.

![screenshot](https://raw.githubusercontent.com/gliheng/flutter-rs/master/www/images/screenshot_mac.png)


- Support Hot reload
- MethodChannel, EventChannel
- Async runtime using tokio
- System dialogs
- Clipboard support
- Cross platform support, Runs on mac, windows, linux
- Support distribution format: (windows NSIS, mac app, mac dmg, linux snap)

# Install requirements

- [Rust](https://www.rust-lang.org/tools/install)

- libglfw:
    - Install on Mac with: `brew install glfw`
    - Install on linux with `apt install libglfw3`
    
- [flutter sdk](https://flutter.io)

# Config flutter engine version
flutter-rs need to know your flutter engine version.
You can set this using any of the following methods.
- If you have flutter cli in your PATH, you're set.
- Set FLUTTER_ROOT environment variable to your flutter sdk path
- Set FLUTTER_ENGINE_VERSION environment variable to your engine version

# Develop

To develop, install [flutter-rs devtools](https://github.com/flutter-rs/psi-cli) with `pip install psi-cli`

**Note:**
Devtools require python3

- Create a flutter-rs app

    `psi create flutter_app`

- Add flutter-rs to existing flutter project

    `psi create .`

- Run a flutter-rs app in dev mode

    `psi run --vscode`

- Bundle a flutter-rs app for distribution

    `psi build {nsis,mac,dmg,snap} --release`

**Note:**
Build on Windows require [NSIS3](https://sourceforge.net/projects/nsis/files/NSIS%203/)

# Caveats
    Ubuntu font is required on linux, otherwise please change the default font using `ThemeData` accordingly.