# BOB · start here

BOB is built and handed over. On 29 October 2026 Ash handed it to Alicia, Mags and Lukas. Everything a new owner needs is in two files:

1. `docs/TEAM-HANDOVER.md`: who owns what, the honest state, how a change ships, and the first decision (keep, cut back or stop).
2. `ONBOARDING.md`: ask Claude, in the Claude desktop app's Code tab on a folder called `BOB` in your home folder, to follow it. It installs BOB, runs one half-hour session on a small real idea with you, and records your verdict.

The install line, for reference: `claude plugin install bob --marketplace sip-stepchange/bob --scope project`, then quit and reopen the Claude app.

## What is in this repository

| Path | What it is |
|---|---|
| `CLAUDE.md` | What Claude Code reads first in any session on this repository |
| `docs/TEAM-HANDOVER.md` | The handover: owners, state, next decision |
| `docs/product/intent.md` | What BOB is for, in Ash's words; the top of the brief |
| `docs/product/mags-first-session.md` | The pass and fail rule for a first real session |
| `docs/project-status.md` | The build log, newest verdicts at the top |
| `docs/handoff.md` | Every decision and landmine from the build |
| `hooks/` | The plugin: pane, gates, map and status pages, and its tests (`bob.test.tsx`) |
| `skills/` | The two skills BOB ships: `design-with-bob` and `adopt-under-bob` |
| `bob/` | BOB's own records (it governs its own repository) and `schema.json`, the one home for every record shape and state |
| `.github/workflows/gate.yml` | The five checks every pull request must pass |
| `references/` | Read-only source material; never edited |

This file replaced the original start-pack guide on 30 October 2026; that version is in the git history.
