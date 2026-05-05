# MacVisionary

MacVisionary is the macOS companion app for Visionary. It streams live Mac windows to Apple Vision Pro as individual spatial windows, while preserving low-latency keyboard, pointer, scroll, drag, resize, and window-management interactions.

This repository publishes public binary releases of the Mac app. The Visionary visionOS app is currently available through TestFlight and is planned to be distributed through the visionOS App Store.

## Highlights

- Share individual Mac windows as native visionOS windows instead of mirroring the whole desktop.
- Use a Visionary dock on visionOS to open, focus, hide, and restore Mac apps and windows.
- Use unified and per-host docks when working with one or more Macs.
- Launch Finder, Trash, Spotlight, and app windows from visionOS.
- Use the Mac menu bar from inside shared windows.
- Forward keyboard, pointer, click, double-click, right-click, scroll, and drag input to shared Mac windows.
- Use local Visionary shortcuts including app switching, Spotlight, and window cycling.
- Enable a high-quality virtual render display while connected so shared windows can be captured cleanly and quickly.
- Pair devices with pairing-code verification and encrypted local transport.
- Disable Visionary from the Mac menu bar when you need the Mac to immediately stop networking and restore its displays.

## Requirements

- macOS 15 or newer.
- Apple Vision Pro running the matching Visionary visionOS app.
- Both devices on a network that permits local peer discovery, or manual connection settings configured in the Visionary apps.
- Screen Recording and Accessibility permissions on the Mac.
- For now, physically pairing a keyboard and pointing device with Apple Vision Pro is recommended for the best input experience. Universal Control-style input from the Mac is in progress.

## Install

1. Download the latest `MacVisionary-*.zip` from the Releases page or from the `releases/` folder in this repository.
2. Unzip it.
3. Move `MacVisionary.app` to `/Applications` or `~/Applications`.
4. Launch `MacVisionary.app`.
5. Grant Screen Recording and Accessibility permissions when prompted.
6. Restart `MacVisionary.app` after granting permissions if macOS asks you to.

If macOS says the app was downloaded from the internet, choose Open. Release builds are intended to be Developer ID signed and notarized.

## Latest Build

- [MacVisionary-1.0.0-1102.zip](releases/MacVisionary-1.0.0-1102/MacVisionary-1.0.0-1102.zip)
- [SHA-256 checksum](releases/MacVisionary-1.0.0-1102/MacVisionary-1.0.0-1102.zip.sha256)

## Recommended Setup: Virtual Display

For the best visual quality and fastest window sharing, enable MacVisionary's independent virtual display before connecting to Vision Pro.

1. Launch MacVisionary on the Mac.
2. Click the MacVisionary menu bar icon.
3. Choose `Settings`.
4. In `Independent Render Display`, turn on `Use Independent Virtual Display`.
5. Leave `Render Display` set to `6K HiDPI` unless you specifically want a different render resolution.
6. Connect from Visionary on Vision Pro.

When this option is enabled, MacVisionary uses a private high-DPI render display while connected, then restores your normal Mac displays when the session disconnects or the option is turned off. If you ever need an escape hatch, press `Command-Control-Escape` on the Mac to force Visionary into disabled mode and restore the physical display.

## Pair With Vision Pro

1. Launch Visionary on Apple Vision Pro.
2. Launch MacVisionary on the Mac.
3. When a pairing prompt appears, confirm that the Mac name and pairing code match.
4. Accept the pairing request.
5. Once connected, visible Mac windows should appear as shared windows on visionOS.

## Everyday Use

- Tap a dock icon to show or focus that Mac app.
- Tap a shared window to send pointer and keyboard input to it.
- Use the traffic-light overlay for close, minimize, zoom, menu bar access, and window scale options.
- Secondary click works inside shared Mac windows.
- Outside shared Mac windows, use long press or long click for Visionary secondary actions. Dock icons, the dock separator, the Spotlight icon, and the menu/minimize overlay buttons expose secondary actions this way.
- Use natural scroll gestures in shared windows to scroll Mac content.
- Use `Command-Control-Escape` on the Mac as an escape hatch to force Visionary into disabled mode.

## Privacy And Permissions

MacVisionary needs Screen Recording permission to capture the windows you choose to share. It needs Accessibility permission to focus, resize, move, minimize, restore, and send input to Mac windows. Visionary is designed to stream selected app/window content locally between your Mac and Vision Pro.

## Troubleshooting

- If no windows appear, confirm Screen Recording permission is enabled for MacVisionary.
- If input does not work, confirm Accessibility permission is enabled for MacVisionary.
- If pairing fails, disable and re-enable Visionary from the Mac menu bar, then retry pairing.
- If the Mac display stays dark after disconnecting, press `Command-Control-Escape` on the Mac.
- If Bonjour discovery is blocked, configure manual IP/port settings in the Visionary apps.

## Release Notes

See each GitHub Release for build-specific notes and checksums.
