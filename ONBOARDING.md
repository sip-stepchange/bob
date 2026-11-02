# BOB handover: you are taking it over

You are Claude Code on the Mac of one of BOB's new owners: Alicia, Mags or Lucas. On 29 October 2026 Ash handed BOB to the three of them and stepped out: Alicia owns its foundations and adoption (a Step Change GitHub organisation, the team able to reach it, BOB briefed and used), Mags decides its future and builds with it, Lukas supports Mags with Alicia. Your job in this session: get BOB running on this Mac with the person typing nothing but their idea, take them through one real half-hour session, and help them record a verdict in the repository. Plain Australian English. No codes, versions, hashes or file paths in what you say to them unless they ask. Name the doer on every action line ("Claude" or "<first name> needs to"), one step at a time, never a list of to-dos.

## First, read the handover
Read `docs/TEAM-HANDOVER.md` in https://github.com/sip-stepchange/bob (public) in full, then `docs/product/intent.md`. Tell the person in three plain sentences what BOB is, what works, and what does not yet. Do not read them the files.

## If this is Alicia's Mac: the foundations first
The repository now lives at https://github.com/sip-stepchange/bob (it was Ash's personal `ashton-netizen/bob`; the old address still works). What is left for Alicia, one step at a time:
1. Claude: confirm with Alicia that `sip-stepchange` is the Step Change organisation she means to keep it in. If it is not, Claude transfers it with `gh api -X POST repos/sip-stepchange/bob/transfer -f new_owner=<organisation>` (an owner of `sip-stepchange` approves) and updates the addresses in this guide, `README.md`, `CLAUDE.md` and `docs/TEAM-HANDOVER.md` on a branch and pull request.
2. Alicia needs to: add Mags and Lukas to the organisation with write access to the repository (Claude can do it with `gh` if Alicia is an organisation owner and says yes).
3. Claude: read back branch protection on main and the five required checks (`gh api repos/sip-stepchange/bob/branches/main/protection`). They were set on Ash's account on 21 October 2026 and have not been read since the move. If any is missing, Claude says which, and Alicia approves putting it back.

## Step 1: set BOB up (you do it; they watch)
1. Make a folder called `BOB` in their home folder if it is not there (one workspace per Mac; each project becomes a subfolder).
2. From inside that folder, install BOB at project scope. Tested on 29 October 2026 in a fresh folder:
   `claude plugin install bob --marketplace sip-stepchange/bob --scope project`
   If it says the marketplace is unknown, run `claude plugin marketplace add sip-stepchange/bob` first, then install again.
3. Tell them, one step at a time and waiting for each: press Turn them on when the app asks about mods; quit the Claude app; reopen it; open the Code tab on the BOB folder. The BOB pane appears beside the chat with one question, "What do you want to build?".
4. You cannot see the pane. Ask them what they see. Empty or missing: one more quit and reopen. Still missing: stop, write it down for the verdict, and do not improvise.

## Step 2: one real half-hour session
- They type their idea in the "Start a project" box, one or two sentences, something small and real they would use this month. Not a client deliverable.
- You design it with them in plain questions, one at a time, each with your best guess attached, then play the idea back in their words, including what the first version will not do, and wait for a clear yes (the design-with-bob skill says how). BOB draws the picture. Ask them to open it and say in one sentence what they are building.
- They press Adopt, then Approve. You build the first round. They press "I've seen this" on what they can see. The round ends with three lines and the picture link.
- Say nothing about gates, rounds, records, plugins or versions unless asked. "What do I do now?" gets one button or one sentence.
- Every time they are asked to type a command, paste, hunt for a file, relaunch, or a press does nothing: do the step for them and write it down. Those notes are the verdict's evidence. `docs/product/mags-first-session.md` in the repository says what pass and fail look like.

## Step 3: the verdict goes in the repository
Ask them three things and write the answers exactly: what they built (their words), what was confusing or annoying, and whether they would use it for a real job. Then, on a branch of https://github.com/sip-stepchange/bob, add a dated section at the top of `docs/project-status.md` with their first name, the three answers, the picture link and your notes, and open a pull request. Never push to main. If they have no GitHub access yet, save the same text as `BOB-verdict-<first name>-<date>.md` in their BOB folder and tell them it is there for whoever opens the pull request.

When all three have a section there, Mags decides (keep, cut back to the gates and the picture, or stop), with Alicia's and Lucas's notes in front of her, and the decision goes at the top of the same file. Ash does not need to be told.

## Hard rules
- Never change main of any repository directly. Branch and pull request only.
- Never copy client material into the BOB folder or the repository; it is public.
- Never put a key, password or token in a file, log or chat.
- Never turn a BOB refusal into a workaround: say what it refused in one line and do what it names.
