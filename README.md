# PURRRGE
<img width="1100" height="400" alt="logo1" src="https://github.com/user-attachments/assets/b5935c36-a53f-4975-b03e-c9bb6924c6a0" />

**PURRRGE makes secure deletion, cleaning free space, and zeroing disks safer and more discoverable while preserving the full power of the SDelete CLI.** <br>
**PURRRGE is a desktop front‑end for Microsoft Sysinternals SDelete v2.05.**

Highlights
- Full coverage of core SDelete flags (passes, recursion, read‑only removal, quiet mode, treat drive letters, clean `-c`, zero `-z`, and automatic `-nobanner`).
- Queue‑based execution with live status, exit codes, elapsed time, aggregate progress, and ETA.
- Responsive UI via per‑job QProcess with streamed stdout/stderr to a dockable console.
- Command Preview pane and a typed confirmation phrase to prevent accidents.
- Admin awareness with optional UAC elevation for operations that require it.
- Persistent settings (paths, passes, logs folder, theme, confirmation phrase, geometry).
- Rotating audit logs with optional username redaction.
- Built‑in dialogs to pick files, folders, logical drives, and enumerated physical disks.

System Requirements
- Windows 10 or later (x64 recommended).
- Python not required for the packaged build; Python 3.10+ required only for running from source.
- Microsoft Sysinternals SDelete v2.05 (64‑bit preferred): `sdelete64.exe` or `sdelete.exe`.

Download and Run
1. Download the portable build from the Assets section of this release (the `PURRRGE.zip`).
2. Unzip anywhere you like (for example, `C:\Tools\PURRRGE`).
3. Place `sdelete64.exe` (or `sdelete.exe`) next to `PURRRGE.exe` inside the unzipped folder, or ensure it is on your PATH.
4. Double‑click `PURRRGE.exe` to launch.

Notes
- The About dialog title is “PURRRGE (SDelete)”.
- The app tries to auto‑detect SDelete at startup and shows the resolved path in the status bar.
- If detection fails, open Settings and browse to your SDelete executable.
