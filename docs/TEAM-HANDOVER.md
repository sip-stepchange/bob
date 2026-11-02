# BOB is yours: Alicia, Mags and Lucas

Handed over by Ash on 29 October 2026, 10:40 pm. Ash is out. You three own BOB from here: Alicia holds its foundations and adoption, Mags makes the call on whether it is kept, cut back, or stopped, and Lukas supports Mags with Alicia. Nobody needs Ash's approval for any of it. This page is the whole handover; everything else it points to is in this repository.

## Who holds what (Ash's ruling, 29 October 2026, 11:25 pm)
- Alicia owns BOB's foundations and its adoption: getting it onto Step Change ground (a Step Change GitHub organisation instead of Ash's personal account, with the team able to reach it), and making sure it is optimised, briefed and used. Claude Code in this repository transfers it once Alicia names the organisation.
- Mags decides BOB's future (keep, cut back, or stop) and is the person it is for: she uses it as the foundation for what she builds.
- Lukas, with Alicia, supports Mags in using it.
- Ash is out. He asked for the result, not the report.

## What BOB is
BOB (Build Optimisation Buddy) is a Claude Code plugin. It sits as a pane beside the chat in the Claude desktop app's Code tab. A person says an idea in a sentence; Claude designs it with them in plain questions; BOB draws a picture of what is being built and lights each part as it is proven; then the build runs in rounds where no round starts without the person's Approve press and none ends without proof on file. The person types nothing but their idea and their answers; every ask is a button in the pane.

Ash's intent, in his words, is in `docs/product/intent.md`. Read that first.

## Honest state on handover
- The gates work. BOB refused Claude's own shortcuts several times on 29 October: an unapproved edit, a round ending unproven, a "proven" claimed without a person's look, a person's look written by Claude instead of a press. None of that can be faked by prose.
- The picture works. The home page is a flowchart of the product, drawn from the records only, and a person can edit it in MindNode and BOB reads the edit back by itself (seen live, 29 October, 4:47 pm).
- The experience does not yet work for the person it is for. Ash's day with it was relaunches, presses that did nothing, screenshot requests and long reports. BOB was built using BOB, which is the worst test of it: the product under construction was the machinery itself. No real project has been through it yet.
- Rebuild promises on the demo project (`bob-demo`, on Ash's Mac, not in this repository): 17 of 21 proven. The three left need a real repo adopted and a real person's first project.
- Fixed on 30 October 2026 (plugin 0.19.5): every step the pane, the status page and the map gave a person said "Ash needs to", so BOB told whoever was using it that Ash had to act. Person steps now read "You need to", an approval is recorded and announced under the approver's own name, and a test fails if Ash's name comes back.
- Added on 2 November 2026 (plugin 0.20.0), borrowing the best of Addy Osmani's agent-skills (MIT): Claude designs with one question at a time, each with its best guess, then plays the idea back with what the first version will not do and waits for a clear yes; and a new build-with-bob skill tells Claude how to run an approved round (thin slices proven one by one, nothing outside the round, stop and fix the cause when something breaks, two fresh-eyes reviewers before it closes). Pressing Approve now starts the round under that skill.
- Known open faults: two "I've seen this" presses wrote nothing straight after a plugin install mid-session (the same presses worked after the app was reopened); MindNode Classic's save-as picker when the picture is edited; a new plugin version loads only after the app is quit and reopened.

## Where everything is
- This repository: https://github.com/sip-stepchange/bob (public; it was `sip-stepchange/bob`, and that address still works). `CLAUDE.md` is what Claude Code reads first here; `docs/handoff.md` has the landmines; `docs/project-status.md` is the build log.
- The method and the records: `bob/schema.json` (every state and transition), `hooks/` (the plugin), `hooks/bob.test.tsx` (135 tests, all green at 0.20.0), and the three skills: `skills/design-with-bob` (designing an idea), `skills/build-with-bob` (running an approved round) and `skills/adopt-under-bob` (bringing an existing repo under BOB).
- What Ash asked for: `docs/product/intent.md`. What was there before the reset and what was kept: `docs/product/reconcile.md`. Why the first build failed him: `docs/product/post-mortem.md`.
- The first real test, written for Mags's thirty-minute session: `docs/product/mags-first-session.md`. It is the pass or fail rule Ash set before handing over; keep it or write your own.

## How to get it running (Claude does this with you)
Open the Claude desktop app, Code tab, on a folder called `BOB` in your home folder, and ask Claude to follow `ONBOARDING.md` from this repository. It installs BOB with this one command, tested on 29 October 2026 in a fresh folder:

    claude plugin install bob --marketplace sip-stepchange/bob --scope project

Then quit and reopen the app, open the Code tab on your BOB folder, press Turn them on when asked about mods, and the pane appears with one question. The step not re-tested on a fresh Mac is adding the marketplace for the first time; if the install says the marketplace is unknown, `claude plugin marketplace add sip-stepchange/bob` comes first. (On 30 October 2026 that command added the marketplace by itself and installed 0.19.4 in an empty folder, from both the new and the old address, on a Linux test machine with engine 2.1.314. A Mac with the desktop app is still the real test.)

## How a change ships
Branch, pull request, five required checks (secret scan, plugin validate and test, personal-data grep, no runtime Babel, schema and fixtures agree), squash merge, then `claude plugin tag . --push`, `claude plugin marketplace update bob`, and `claude plugin update bob@bob --scope project` in each workspace. Claude Code in this repository knows the sequence; ask it.

## Rules that travel with it
- No client material in this repository. It is public.
- No key, password or token in any file, log or chat.
- No state from prose: a promise is proven only by an evidence record pointing at a file.
- Name the doer on every action line, one step at a time for a person, never a list of to-dos.

## Your first decision
Each of you runs one small real idea through it (half an hour; `docs/product/mags-first-session.md` says what pass and fail look like). Then Mags decides, with Alicia's and Lucas's notes in front of her, and writes the decision at the top of `docs/project-status.md` in this repository:
- Keep: run the next real project through it the same way.
- Cut: strip it to the gates and the picture; drop the status page, the proof counts in the pane and the reviewer ceremony.
- Stop: archive the repository. Nothing else depends on it.

Ash does not need to be told. He asked for the result, not the report.
