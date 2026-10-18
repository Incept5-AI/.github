# CLAUDE.md

`~/dev/incept5-ai` is the local root of the **Incept5-AI** GitHub org (open-source projects from Incept5, i5).

- This folder itself is the `Incept5-AI/.github` repo. `profile/README.md` is the org's front page and lists
  every project.
- Each project is its own repo, cloned into a subfolder (`YuE2/` → `Incept5-AI/YuE2`). Those subfolders are
  git-ignored here. **Work inside a project and read its own `CLAUDE.md` first.**

When adding a project:
- Create `Incept5-AI/<Name>` and clone it here as `<Name>/`.
- Give it its own `README.md`, `CLAUDE.md` and `LICENSE`, with a "More from us: github.com/Incept5-AI" line
  near the top of the README.
- Add a row to the table in `profile/README.md`.
- Never commit secrets, signing team IDs, device identifiers, model weights or generated media. Put local
  settings in git-ignored files, with a committed `.example` beside each.

GitHub Pages serves a project repo as-is when it has `.nojekyll` (branch `main`, root) at
`https://incept5-ai.github.io/<Name>/`. The GitHub file view forces a download for binaries, so link audio to
the Pages URL if it should play in the browser.
