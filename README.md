# ARC Raiders compatibility — 0.2.0-alpha7

**YouTube setup video:** Coming soon.
<!-- YouTube video URL: -->

Choose **one** ZIP matching your CrossOver version and how you launch Steam.

| Package | What you use |
| --- | --- |
| CrossOver 26.3 — CrossOver Steam bottle | Windows Steam inside CrossOver. |
| CrossOver 26.3 — NotProton Steam native | Native macOS Steam with NotProton. |
| CrossOver Preview 27.0.0.40734 — CrossOver Steam bottle | Windows Steam inside that exact Preview build. |
| CrossOver Preview 27.0.0.40734 — NotProton Steam native | Native macOS Steam with NotProton's runner for that exact Preview build. |

**Requirements:** Apple Silicon, macOS 27.x, Rosetta, the matching CrossOver
version, and a Steam copy of ARC Raiders. The native Steam route also requires NotProton.

Extract the whole ZIP, open `Install.command`, and choose **Install / update**.

- **CrossOver Steam bottle:** Launch **ARC Raiders (Patched)** inside your selected bottle.
- **NotProton Steam native:** Restart Steam, select the game’s compatibility tool, and click **Play**. No CrossOver Steam bottle is needed.

The installer creates a private runtime and leaves your installed CrossOver app
and game files unchanged. Verification and rollback are included.

Each ZIP includes setup and technical documentation, plus source and licenses in
`Support`. ZIP checksums are in `SHA256SUMS.txt`.

If you'd like to support the compatibility work and ongoing maintenance:

<p>
  <a href="https://ko-fi.com/andreiii22"><img src="docs/images/support-kofi.svg" alt="Support on Ko-fi" width="250" height="64"></a>&nbsp;
  <a href="https://github.com/sponsors/zzoko"><img src="docs/images/github-sponsors.svg" alt="Support through GitHub Sponsors" width="250" height="64"></a>
</p>
