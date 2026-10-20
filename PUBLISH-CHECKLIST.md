# Publish Checklist — open-model-cheatsheet (public GitHub repo)

> ⚠️ **This task does NOT run any `git push`. No push is authorized yet.**
> The package below is publish-ready; pushing happens only after the user
> completes the two manual steps and explicitly confirms.

## Package contents (this directory)

- [x] `README.md` — finalized from the pre-research draft; version v1.25, data as of 2026-10-20
- [x] `open-model-cheatsheet.en.md` — full English translation of the Chinese source v1.25
- [x] `LICENSE` — CC BY 4.0 full text (document license only; model weights keep their own licenses)
- [x] `PUBLISH-CHECKLIST.md` — this file
- [x] `BUILD-NOTES.md` — source version, translation conventions, daily-sync notes

## Step 1 — User: create the empty public repo (GitHub, ~2 min)

- [ ] Go to https://github.com/new
- [ ] Repository name: `open-model-cheatsheet`
- [ ] Visibility: **Public**
- [ ] Description (suggested): `Daily-updated selection guide for open-weight AI models — strengths, benchmarks, size, local-deployability`
- [ ] Do **NOT** add a README, .gitignore, or license in the web UI (the repo must start empty; this package supplies them)
- [ ] Create repository

## Step 2 — User: authenticate the GitHub CLI on this VM (device flow, ~3 min)

- [ ] In a terminal on this VM, run: `gh auth login`
- [ ] Choose: `GitHub.com` → `HTTPS` → `Login with a web browser`
- [ ] Copy the one-time device code shown, open https://github.com/login/device in any browser, enter the code, and authorize
      (the token stays in the VM's `gh` credential store — it is never pasted into chat or saved to memory)
- [ ] Verify: `gh auth status` shows the account as logged in

## Step 3 — Main agent (only after Steps 1–2 and user confirmation)

- [ ] Copy this package's `README.md`, `open-model-cheatsheet.en.md`, and `LICENSE` into a clean working clone directory
- [ ] `git init`
- [ ] `git add README.md open-model-cheatsheet.en.md LICENSE`
- [ ] `git commit -m "Open Model Cheatsheet v1.25 (data as of 2026-10-20)"`
- [ ] `git branch -M main`
- [ ] `git remote add origin https://github.com/<user-account>/open-model-cheatsheet.git`
- [ ] `git push -u origin main`  ← **requires explicit user confirmation at that time; not done in this task**

## Step 4 — After the first push

- [ ] Confirm the repo renders: README shows version v1.25 / data as of 2026-10-20, and the link to `open-model-cheatsheet.en.md` works
- [ ] From then on, the daily sync cron updates the Chinese source first, then the English file is updated incrementally per `BUILD-NOTES.md`, committed, and pushed

## Explicitly out of scope for this build task

- No GitHub connection, no `gh auth`, no `git init/commit/push` was performed while building this package
- The Chinese source file was not modified
