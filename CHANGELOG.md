# Changelog

Unreleased

- Add a localized plus-with-shield action that opens a separate sudo login shell using normal DSM sudo authentication and existing session persistence rules.

- Terminate foreground/background jobs and nested child sessions when a shell tab closes, unless the user explicitly enabled background persistence. Escalate unresponsive jobs after a grace period.

- Recover stalled metrics streams without waiting for the close handshake; ignore late socket events and use browser-valid close codes for malformed messages.

- Retry temporary DSM authentication failures without treating them as revoked sessions.
- Reposition open metric details on resize and close them when their widget is hidden.
- Use a monotonic graph clock, stream identity, and sample sequence numbers to handle clock corrections and service restarts.

- Added localized, automatically scaled header histories for each logical CPU core, RAM, NAS volume usage, fan speed, and available drive temperatures.
- Added an authenticated metrics WebSocket with a shared sampler, periodic session validation, and bounded timestamped history with gaps on reconnect.
- Pause hidden monitors and expose all per-core readings in a scrollable, keyboard-accessible detail panel.

v1.2.0

- Fixed Escape handling so closing terminal search does not close the DSM window.
- Added the installed package version to the shell footer.
- Changed drag-and-drop uploads to use the shell's current directory without inserting file paths into the terminal.
- Added filename checks before uploading, with Override, Keep both, and Cancel choices for conflicts.
- Upload files individually; a later failure no longer deletes previously completed uploads.
- Bound upload authorization to the user, session, and checked directory; changing directories requires a new upload check.
- Hardened upload commits against directory targets and filename options, and added process timeouts and cleanup for write failures.
- Route drops to the hovered split pane, with animated target highlighting, shell name, and pane-local upload progress.
- Removed the old 100 MiB cumulative upload quota; per-file and per-request limits remain.

v1.1.1

- Added a package icon and clickable maintainer, project, and support links for Package Center.
- Corrected the package maintainer and canonical Go module path.

v1.1.0

- Added renameable shell sessions, terminal search, secure file uploads, and split views.
- Hardened uploads and polished the shell workspace controls.

v1.0.1

- Added multiple shell tabs and persistent shell sessions.

v0.1.0

- First release of DiskShell.
- Added automated SPK releases with checksums.
