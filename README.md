# PURRRGE
<img width="1100" height="400" alt="logo1" src="https://github.com/user-attachments/assets/b5935c36-a53f-4975-b03e-c9bb6924c6a0" />

**PURRRGE makes secure deletion, cleaning free space, and zeroing disks safer and more discoverable while preserving the full power of the SDelete CLI.** <br>

**PURRRGE is a desktop front‑end for Microsoft Sysinternals SDelete v2.05.**

<img width="959" height="503" alt="image" src="https://github.com/user-attachments/assets/d9712bea-f7be-4a0a-9db4-9d7cd1d3adb4" />

<img width="255" height="188" alt="image" src="https://github.com/user-attachments/assets/16da8cc5-971f-43e0-a293-d862c4d8e9e7" />



Highlights
- Full coverage of core SDelete flags (passes, recursion, read‑only removal, quiet mode, treat drive letters, clean `-c`, zero `-z`, and automatic `-nobanner`).
- Queue‑based execution with live status, exit codes, elapsed time, aggregate progress, and ETA.
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
- The app tries to auto‑detect SDelete at startup and shows the resolved path in the status bar.
- If detection fails, open Settings and browse to your SDelete executable.

Quick Usage
1. Choose a mode: Secure Delete, Clean Free Space, or Zero Free Space.
2. Configure passes and flags as needed.
3. Add files/folders/drives/disks to the queue.
4. Review the Command Preview; type the confirmation phrase (default: `ERASE`).
5. Start and watch live output in the docked console. Cancel will stop the current job and mark remaining as cancelled.

Elevation and Safety
- Cleaning/Zeroing often requires administrator privileges. PURRRGE can relaunch itself via UAC when needed.
- Cleaning/Zeroing can consume all available disk space during execution and may impact system stability until completion.
- Zeroing physical disks is destructive. Ensure no mounted volumes exist on the target disk.
- Always maintain verified backups before performing secure deletion tasks.

Logs and Privacy
- Logs are written to the configured logs directory and rotate to prevent unbounded growth.
- Each entry includes timestamp, command line (with optional `%USERNAME%` redaction), stdout, stderr, exit code, and duration.
- PURRRGE does not send telemetry.

Troubleshooting
- “SDelete executable not found” — Place `sdelete64.exe` next to `PURRRGE.exe`, add it to PATH, or select it in Settings.
- SmartScreen warnings — Click “More info” and “Run anyway” if you trust the build, or build locally from source.
- High startup time for single‑file builds — Prefer the one‑folder build for snappier startup.

Licensing and Acknowledgements
- PURRRGE is a GUI wrapper around Microsoft Sysinternals SDelete, which remains subject to its own licensing and EULA. Review the official SDelete documentation and license before use.
- SDelete is a trademark of Microsoft.
