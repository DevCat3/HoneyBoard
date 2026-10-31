# Samsung Keyboard (HoneyBoard) for AOSP

The stock **Samsung Keyboard** (One UI 4.1 Core build, `com.samsung.android.honeyboard`) patched to run on AOSP and
GSI ROMs. It installs as a normal app: **no root, no Magisk module, no system partition changes.**

> Made By DevCat3 · [github.com/DevCat3](https://github.com/DevCat3)

## Features

- Full Samsung layout, animations and toolbar
- All Settings pages
- Language download, word prediction and suggestions
- Clipboard: open, paste, delete and pin
- Translation, search and the privacy-policy dialog
- Size and transparency, including the *Show keyboard* button
- **Tablet mode switch** in the keyboard settings (details below)
- Save screenshots to clipboard
- Dark clipboard
- Fast paste after copying any text

## Download

Get the latest APK from the [Releases](https://github.com/DevCat3/HoneyBoard/releases/) page.

## Install

1. Install the APK like any other app. If a differently signed build is already installed, uninstall it first.
2. Open *Settings → System → Languages & input → On-screen keyboard → Manage keyboards*, enable **Samsung Keyboard**,
   then select it as your keyboard.

## Tablet / phone mode

The keyboard chooses its layout when it starts:

1. If you flipped the **Tablet mode** switch (bottom of the main Settings page), your choice is used.
2. Otherwise it auto-detects the device: tablet when the system declares it or the smallest screen width is at least
   600dp, phone otherwise.

Changing the switch restarts the keyboard, because the layout is read once at startup.
Tablet mode shows extra keys such as Ctrl + arrows.

## Known limitations

- **Handwriting is not available.** It depends on Samsung's separate handwriting service app, which does not exist on
  AOSP, so the toolbar button is removed.
- Features that depend on other Samsung system apps or services do not work.

## Tested on

- Galaxy Tab A7 (SM-T509), DerpFest 13 GSI (Android 13)
- Phones running Android 16 and Android 17 (reported by testers)
- HyperOS 3

## Reporting a bug

Open an issue with your device, ROM, Android version and the crash log:

```sh
adb logcat -d -b crash
```

## Disclaimer

Samsung Keyboard and One UI are the property of Samsung Electronics. This project is not affiliated with or endorsed
by Samsung and is provided as-is, without warranty, for personal use. If you are a rights holder and want the file
removed, open an issue and it will be taken down.

### Credits
- [Helicopterr](https://github.com/real-omar)
- [MrDeard](https://github.com/omarheshambadr)
