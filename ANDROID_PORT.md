# Frame Window Counter — Android port

This tree contains the Android32/Android64 portability changes.

## Changes
- Added Android Geometry Dash target `2.2081` to `mod.json`.
- Replaced the Windows-only file dialogs with Geode's cross-platform `geode::utils::file::pick` API.
- File import/export now works through the Android system file picker.
- Audio-file selection now uses the same cross-platform picker.
- Kept the Windows `O` hotkey as a Windows-only feature; mobile continues to use the existing in-game/pause-menu UI.
- No Windows headers or Win32 file-dialog APIs remain in the Android code path.

## Build targets
The project is intended for:
- Android32 (`armeabi-v7a`)
- Android64 (`arm64-v8a`)

The resulting package should contain:
- `c0nscious.frame_window.android32.so`
- `c0nscious.frame_window.android64.so`

along with the normal Geode package metadata/resources.
