# ARC Raiders compatibility

Current packages: **0.2.0-alpha9** for every route.

**YouTube setup video:** [Watch on YouTube](https://www.youtube.com/watch?v=5emn-mqPV5A)

Choose **one** ZIP matching your CrossOver version and how you launch Steam.

| Package | What you use |
| --- | --- |
| CrossOver 26.3 — CrossOver Steam bottle | Windows Steam inside CrossOver. |
| CrossOver 26.3 — NotProton Steam native | Native macOS Steam with NotProton. |
| CrossOver Preview 27.0.0.41073 — CrossOver Steam bottle | Windows Steam inside CrossOver Preview 20261015. |
| CrossOver Preview 27.0.0.41073 — NotProton Steam native | Native macOS Steam with NotProton's runner for CrossOver Preview 20261015. |

**Requirements:** Apple Silicon, macOS 27.x, Rosetta, the matching CrossOver
version, and a Steam copy of ARC Raiders. The native Steam route also requires NotProton 1.2.1.
For Preview, download `crossover-preview-20261015.zip` from CodeWeavers' Preview Center (not the `arm64` one).

Extract the whole ZIP, open `Install.command`, and choose **Install / update**.

- **CrossOver Steam bottle:** Launch **ARC Raiders (Patched)** inside your selected bottle.
- **NotProton Steam native:** Restart Steam, select **ARC Raiders - CrossOver 26.3** or **ARC Raiders - CrossOver Preview 27.0.0.41073** as the compatibility tool, and click **Play**. No CrossOver Steam bottle is needed.

The installer creates a private runtime and leaves your installed CrossOver app
and game files unchanged. Verification and rollback are included.

Each ZIP includes setup and technical documentation, plus source and licenses in
`Support`. ZIP checksums are in `SHA256SUMS.txt`.

## Game specific information

- **Ray tracing (CrossOver Preview):** turned off by default, because it currently fails on this Preview build. To test it anyway, add `D3DM_SUPPORT_DXR=1` before `%command%` in Steam's Launch Options (NotProton) — expect a crash if it is still unsupported.
- **Freeze after long play:** if ARC Raiders freezes after loading in (audio keeps playing) and then shows an "Unhandled page fault" popup, the D3DMetal shader cache has grown too large for the Apple GPU driver. The launcher now clears that cache automatically once after such a hang. You can also clear it yourself: quit the game, open `Install.command` and choose **5 Clear D3DMetal shader cache**, or run `rm -rf "$(getconf DARWIN_USER_CACHE_DIR)d3dm/PioneerGame.exe"`. It rebuilds by itself; expect some stutter for the first session or two.

<details>
<summary><strong>Changelog</strong></summary>

**0.2.0-alpha9 (October 2026)**

- **Fixed:** the Preview NotProton download needed a Preview build (July, 27.0.0.40734) that official NotProton never supported, so it could not be set up on other Macs. Both Preview downloads now target **CrossOver Preview 20261015 (27.0.0.41073)**, which NotProton supports.
- NotProton downloads now require **NotProton 1.2.1**.
- Ray tracing is turned off on the Preview (see Game specific information).
- **Fixed:** freezes after long play caused by an oversized D3DMetal shader cache: the launcher clears the cache once after such a hang, and `Install.command` has a new **5 Clear D3DMetal shader cache** option.
- The Steam compatibility tool is now simply named **ARC Raiders - CrossOver &lt;version&gt;**.
- Installer improvements shared with THE FINALS (safer runtime copy, CPU-check fix, clearer NotProton messages).
- Tested: Preview + NotProton and 26.3 + CrossOver bottle launch correctly. The other two downloads use the same fixes but were not separately launch-tested.

</details>

If you'd like to support the compatibility work and ongoing maintenance:

<p>
  <a href="https://ko-fi.com/andreiii22"><img src="docs/images/support-kofi.svg" alt="Support on Ko-fi" width="250" height="64"></a>&nbsp;
  <a href="https://github.com/sponsors/zzoko"><img src="docs/images/github-sponsors.svg" alt="Support through GitHub Sponsors" width="250" height="64"></a>
</p>
