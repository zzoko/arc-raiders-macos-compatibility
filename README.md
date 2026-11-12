# ARC Raiders compatibility

**Check compatibility <img src="docs/images/compatibility-status-red-v2.svg" alt="status" width="49" height="20"> in the main repository before downloading or opening an issue.** [View compatibility status ↗](https://github.com/zzoko/mac-gaming-compatibility#readme)

**YouTube setup video:** [Watch on YouTube](https://www.youtube.com/watch?v=5emn-mqPV5A)

<br><br>

Choose **one** ZIP matching your CrossOver version and how you launch Steam.

| Package | Version |
| --- | --- |
| CrossOver Preview 27.0.0.41303 — NotProton Steam native | 0.2.0-alpha14.1 |
| CrossOver Preview 27.0.0.41303 — CrossOver Steam bottle | 0.2.0-alpha14.1 |
| CrossOver 26.3 — NotProton Steam native | 0.2.0-alpha14.1 |
| CrossOver 26.3 — CrossOver Steam bottle | 0.2.0-alpha14.1 |

**Requirements:** Apple Silicon, macOS 27.x, Rosetta, the matching CrossOver
version, and a Steam copy of ARC Raiders. **macOS 27.2 or 27.2.1 is required to use the improved Wine performance optimization.** The native Steam route also requires NotProton 1.2.5.
For Preview, download `crossover-preview-20261111.zip` from CodeWeavers' Preview Center (not the `arm64` one).

Extract the whole ZIP, open `Install.command`, and choose **Install / update**.

- **CrossOver Steam bottle:** Launch **ARC Raiders (Patched)** inside your selected bottle.
- **NotProton Steam native:** Restart Steam, select **ARC Raiders - CrossOver 26.3** or **ARC Raiders - CrossOver Preview 27.0.0.41303** as the compatibility tool, and click **Play**. No CrossOver Steam bottle is needed.

The installer creates a private runtime and leaves your installed CrossOver app
and game files unchanged. Verification and rollback are included.

Each ZIP includes setup and technical documentation, plus source and licenses in
`Support`. ZIP checksums are in `SHA256SUMS.txt`.

## Game specific information

- **Shader-cache recovery:** for recurring graphics freezes, quit the game and try **5 — Clear D3DMetal shader cache** in `Install.command`. It rebuilds automatically; expect shader-compilation stutter.

<details>
<summary><strong>Changelog</strong></summary>

**0.2.0-alpha14.1 (12 November 2026)**

- Fixes initialization with CrossOver Preview 20261111.
- Supports CrossOver Preview 20261111 (27.0.0.41303), retaining the startup and window-cleanup repairs.
- Updates native Steam integration to NotProton 1.2.5 while preserving saved graphics and synchronization choices.
- Supports the Wine performance optimization on macOS 27.2.1.

**0.2.0-alpha13 (7 November 2026)**

- Clearer installer selection and confirmation across all downloads.
- CrossOver bottle installers now find custom bottle and Windows Steam locations.
- Thanks to [@alex-paradeyev](https://github.com/alex-paradeyev) for the installer contribution in [ARC Raiders #8](https://github.com/zzoko/arc-raiders-macos-compatibility/pull/8).

**0.2.0-alpha12 (5 November 2026)**

- Reduces CPU overhead from frequent system calls while preserving Wine's normal results and instrumentation callbacks.
- Thanks to [@NidaleNieve](https://github.com/NidaleNieve) for the performance report and initial investigation in [#3](https://github.com/zzoko/arc-raiders-macos-compatibility/pull/3).

**0.2.0-alpha11.1 (30 October 2026)**

- Restores startup after the ARC Raiders 2.03 update and repairs a window-cleanup hang.
- Preserves caller-relative native library loading and the existing CPU/memory fixes.
- NotProton integration updated to 1.2.3; explicit launch options take priority over saved settings, followed by fallback defaults.

**0.2.0-alpha10 — Preview downloads (26 October 2026)**

- Updated Preview graphics defaults.
- Added shader-cache recovery guidance. CrossOver 26.3 downloads remain at alpha9.

**0.2.0-alpha9 (October 2026)**

- **Fixed:** the Preview NotProton download needed a Preview build (July, 27.0.0.40734) that official NotProton never supported, so it could not be set up on other Macs. Both Preview downloads now target **CrossOver Preview 20261015 (27.0.0.41073)**, which NotProton supports.
- NotProton downloads now require **NotProton 1.2.1**.
- **Fixed:** freezes after long play caused by an oversized D3DMetal shader cache: the launcher clears the cache once after such a hang, and `Install.command` has a new **5 Clear D3DMetal shader cache** option.
- The Steam compatibility tool is now simply named **ARC Raiders - CrossOver &lt;version&gt;**.
- Installer improvements shared with THE FINALS (safer runtime copy, CPU-check fix, clearer NotProton messages).

</details>

If you'd like to support the compatibility work and ongoing maintenance:

<p>
  <a href="https://ko-fi.com/andreiii22"><img src="docs/images/support-kofi.svg" alt="Support on Ko-fi" width="250" height="64"></a>&nbsp;
  <a href="https://github.com/sponsors/zzoko"><img src="docs/images/github-sponsors.svg" alt="Support through GitHub Sponsors" width="250" height="64"></a>
</p>
