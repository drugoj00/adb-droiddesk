[English](README.md) · [Українська](README.uk.md) · [Русский](README.ru.md)

🌐 All our programs: https://drugoj00.github.io/

Description and screenshots: https://drugoj00.github.io/phone-in-window-with-sound/adb-droiddesk.html

<img src="screenshots/icon_128.png" alt="" width="96" align="right">

# ADB DroidDesk

Android and Android TV from your PC: install any app, adapt apps for a TV box, and the screen and files of another PC.

A free Windows program for phones, tablets and Android TV boxes over USB and Wi-Fi. The focus is Android TV: put anything on a box without a file manager, switch on accessibility services where the system blocks them, adapt a phone app for TV, make a banner. Plus “Remote desk”: the screen of another computer in the program window and a two-pane “this PC ⇄ that PC” file manager. The rest is in one window: screen with sound, apps, files, adb console, cleaner, backups. adb and scrcpy are inside, nothing else to install.

⭐ If the program is useful, please star this repository: it costs nothing and helps other people find it.

## Download

**Version 4.0.** [ADBDroidDesk-4.0.exe](https://github.com/drugoj00/adb-droiddesk/releases/latest) (Assets) · [Releases](https://github.com/drugoj00/adb-droiddesk/releases)

SHA-256: `811627f309e8755f5c5c67def80339cf82989f7473e3e146ba1c2746888b1d98`

## What's new in 4.0

- “Remote desk” tab: the screen of another computer opens in the program window (monitor choice, fit to window, clipboard); the other computer must confirm “Allow?”.
- A two-pane “this PC ⇄ that PC” file manager next to it: copy, move, delete, rename, F5–F8, Tab, drag and drop, progress and cancel, a choice on name conflicts.
- [Long Scissors](https://drugoj00.github.io/phone-in-window-with-sound/long-scissors.html) moved out into a separate program ([GitHub](https://github.com/drugoj00/long-scissors)): the installer is smaller.
- A device screenshot is saved to “Pictures\ADB DroidDesk” and copied to the clipboard.
- Fixed: no separate fixes in this version.

## Features

### Android TV

- Install on a box without a file manager: APK, APKS, APKM, XAPK, ZIP with game data (OBB).
- Sources: files, a folder, drag and drop, F-Droid with all old versions, a link to a file.
- The right package parts are chosen for the device CPU, screen density and language.
- Install an older version over a newer one; where Android 12+ refuses, a replace with a backup and rollback (data is deleted).
- Old apps on Android 14: bypass of the “target SDK too old” block.
- Accessibility: enable a service and “restricted settings” with adb commands (Android 13–14).
- Adapt for TV: Android TV launcher entry, no touchscreen requirement, 64-bit libraries from another build, signing.
- Banners 320×180, 640×360, 1280×720; icon and cover images from Google Play.
- Remote: arrows, OK, Back, Home, volume, text input; to several devices at once.

### Connection over the internet

- “Connect” tab: Tailscale network devices, link type (direct or relay), ADB connection, link check.
- Wizard: Tailscale on the PC and on an Android device, sign-in by key; file sending (Taildrop).
- Invitations by program code: bring a person into your network, accept an invitation; keys are one-time, valid for an hour.
- Video call without a browser: call a person from the list, a “Calling…” window, sound, speaker and camera buttons.
- “Remote desk” tab: the screen of another computer in the program window (monitor choice, fit to window, clipboard) with a two-pane “this PC ⇄ that PC” file manager next to it (F5–F8, Tab, drag and drop, progress and cancel); the other computer must confirm “Allow?”. “Access to this screen” is switched on there.
- Auto-connect of known devices over the home network and through Tailscale.

### Everything else

- Device screen in a tab: sound (Android 10 too), video recording, screenshot, rotation, a mini window in the screen corner.
- Apps: names and icons, uninstall and disable system apps with an APK copy, permissions, batch actions.
- Files: two panes (PC, device, another computer), copy, move, delete, drag and drop.
- adb console with highlighting and history, logcat with filters.
- Cleaner with a database of known bloatware and rollback; app backups.
- Device overview like CPU-Z: CPU, memory, battery, display, cameras, sensors; a “This computer” tab does the same for the Windows PC itself.
- Several devices at once, USB and Wi-Fi, pairing by code; tray icon; Russian, Ukrainian, English; light and dark theme.

## Screenshots

![Android TV → Install: any APK, APKS, APKM, XAPK, ZIP with OBB](screenshots/en/01_androidtv_установка.png)

![Android TV → Adapt an app for TV](screenshots/en/03_androidtv_подстройка.png)

![Device overview](screenshots/en/05_обзор.png)

![This computer](screenshots/en/11_этот_компьютер.png)

![Apps](screenshots/en/06_приложения.png)

![Files](screenshots/en/07_файлы.png)

![Cleaner](screenshots/en/08_очистка.png)

![Backups](screenshots/en/09_копии.png)

![adb console](screenshots/en/10_консоль.png)

## Requirements

Windows 10 or 11 (64-bit); an Android phone or box with debugging on (USB or network). Administrator rights are optional; the internet is needed only for F-Droid and Google Play search.

## Quick start

1. Download ADBDroidDesk-4.0.exe and run it; Windows asks for permission (if declined, the program goes into your user folder).
2. On the device: Developer options → USB debugging (a box: network debugging); connect the cable and allow debugging.
3. A box over Wi-Fi: “+ Wi-Fi” → IP and port, usually 5555.
4. Android TV → Install: drop app files into the window and press Install.

## Limits

- Any version can be downloaded from F-Droid; Google Play is used only for banner images, not for downloading apps.
- A downgrade on Android 12+ and a signature change are possible only by deleting the app data: the system allows nothing else.
- Adapting for TV changes the app signature: store updates will not apply to the copy; split apps are not supported yet; remote control cannot be added to an app.
- Tested on Android 10 and 15 phones; accessibility services have not been tested on a real Android TV 14 box yet.
- Android 10 sound goes through sndcpy; Android 11+ sends sound by itself.
- The installer is not signed with a publisher certificate: Windows may show a SmartScreen warning (“More info” → “Run anyway”).
- The program is unofficial; adb (Google) and scrcpy (Genymobile) are inside, Apache-2.0.
- The video call goes directly between devices (Tailscale on both or one network is needed, there is no relay) and uses WebView2 from Windows 10 and 11.
- “Remote desk”: Tailscale is needed on both computers (or one network), “Access to this screen” must be on at the other computer and its “Program code” entered; the screen does not open without the “Allow?” confirmation.
