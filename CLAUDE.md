# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

`~/dev/incept5-ai` is the local root of the **Incept5-AI** GitHub org (open-source projects from Incept5, i5).

- This folder itself is the `Incept5-AI/.github` repo. It tracks only `profile/README.md` (the org's front
  page, listing every project), the root `README.md` and this file. There is nothing to build or test here.
- Each project is its own repo, cloned into a subfolder (`YuE2/` → `Incept5-AI/YuE2`). `.gitignore` ignores
  every subfolder except `profile/`, so commits here never pick up project files. **Work inside a project and
  read its own `CLAUDE.md` first.** Not every listed project is cloned locally (`private-pocket` is not).

When adding a project:
- Create `Incept5-AI/<Name>` and clone it here as `<Name>/`.
- Give it its own `README.md`, `CLAUDE.md` and `LICENSE`, with a "More from us: github.com/Incept5-AI" line
  near the top of the README.
- Add a row to the table in `profile/README.md`: bold linked name, then one or two sentences on what it is, ending
  with a `[▶ …](https://incept5-ai.github.io/<Name>/…)` link when there is something to see or hear. Also update
  the licence sentence under the table, which names each project's licence.
- Never commit secrets, signing team IDs, device identifiers, model weights or generated media. Put local
  settings in git-ignored files, with a committed `.example` beside each.

Benchmark projects (`languages-benchmark`, `hle-lite`) are run by strangers, so keep them standard-library
Python that works on **Python 3.9** (macOS's system `python3`): no nested same-quote f-strings or other 3.12-only
syntax. That broke every command of `languages-benchmark` on 3.9 once. Check with `/usr/bin/python3` before
pushing. Example results in them are scrubbed of hostnames, IPs, usernames and paths.

GitHub Pages serves a project repo as-is when it has `.nojekyll` (branch `main`, root) at
`https://incept5-ai.github.io/<Name>/`. The GitHub file view forces a download for binaries, so link audio to
the Pages URL if it should play in the browser.
