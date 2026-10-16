# ARC Raiders compatibility — 0.2.0-alpha7

**YouTube setup video:** Coming soon.
<!-- YouTube video URL: -->

Choose **one** ZIP matching your CrossOver version and how you launch Steam.
Extract it completely, read its setup guide, then open `Install.command`.

| Package | What you use |
| --- | --- |
| CrossOver 26.3 — CrossOver Steam bottle | Windows Steam inside a CrossOver bottle; launch the added **ARC Raiders (Patched)** icon. |
| CrossOver 26.3 — NotProton Steam native | Native macOS Steam with NotProton; download and launch ARC in native Steam. No CrossOver bottle needed. |
| CrossOver Preview 27.0.0.40734 — CrossOver Steam bottle | Windows Steam in a bottle created/imported by this exact older Preview build. |
| CrossOver Preview 27.0.0.40734 — NotProton Steam native | Native macOS Steam with NotProton's runner for this exact older Preview build. No CrossOver bottle needed. |

**Requirements:** Apple Silicon, Rosetta, macOS 27.x, your own matching CrossOver
copy, Steam and ARC Raiders. Stable means **26.3.0.39832** (GPTK3). Preview means
the specific **27.0.0.40734 July build** (GPTK4), not the latest Preview.
The installer checks actual Rosetta compatibility; it does not require one exact
macOS build. It explains and requests any needed startup authorization.

The native Steam packages need an existing NotProton setup for the chosen
CrossOver build. NotProton 1.1.7's launch interface is tested; compatibility is
checked against actual input files rather than the app's version label alone.
No Windows Steam client or CrossOver-managed bottle is required for that route.
Reusing game files already recognized by native Steam is also supported by the
launcher; the game location comes from Steam, not a hard-coded bottle path.

All packages contain the startup, CPU NT-flag and allocator corrections. They
create a private runtime and preserve the installed CrossOver app and game files.
The runtime binaries are the same confirmed builds as before this documentation
cleanup. No full CrossOver, Steam, NotProton or Apple runtime is distributed.

These remain experimental releases. Stable bottle and personal Preview/NotProton
gameplay have been confirmed. Stable/NotProton and Preview/bottle still need full
gameplay confirmation. A fresh native-Steam-only download and a second Mac have
not received end-to-end gameplay testing. Each ZIP's README describes its own route.

Only these ZIPs are intended for sharing. The parent project's Runtime and Launcher
folders are personal recovery files. Source, rebuild instructions and licenses
are retained under each ZIP's `Support` folder. `SHA256SUMS.txt` lists ZIP hashes;
each ZIP also contains checksums and release metadata.
