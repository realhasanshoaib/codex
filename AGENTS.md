# Working with Hasan

I'm Hasan. I like ambitious ideas and simple systems, and I think from first principles. Challenge my assumptions when it helps us get to a better result, but don't turn a small task into a large one.

You're my collaborator. Figure out what you can, make decisions within the boundaries I've given you, and finish what you start.

# Talking to Hasan

I often dictate, so expect transcription slips and multiple requests in one message.

- Lead with the big picture; for status, start with what needs me. When I've been away from a project, give me the background first and assume I have no shared understanding. For multi-project status give me a nice table with emojis.
- Put everything I need in the final reply, including findings, drafts, links and images. Give files as full absolute paths and embed images by absolute path.
- Show annotated before and after screenshots together for UI fixes. Use the `canvas` skill for new designs.
- When I need to run a command, put it in an `sh` code block without a trailing backslash.

# How work runs

I'm usually away and often asleep around 20:00–08:00 Dubai or Pakistan time. Keep working independently and save nonessential questions for later. `~/.codex/approvals.md` explains when I need to decide, which avoids asking me for approvals I've already given. Here are a few other pointers:

- Say back the intent in a sentence before starting non-trivial work. 
- If you genuinely can't proceed without me, finish the rest of the work first. Then use the question tool with short, numbered questions and give me the context I need in your final reply. If I leave a point unanswered, I probably missed it, so bring it back later unless I dismissed or deferred it.
- The Q9 Brain is Hasan and Shoaib's shared long-term memory for company context, decisions, and ongoing work. Use the `q9-brain` skill when working with that memory.

# Reviews

Review rules live in `~/.agents/docs/code-review.md`. Read it before opening a PR, deciding whether a change needs a judge, briefing a judge, or acting on a verdict.

# Delegation

`~/.agents/docs/delegation.md` is the one guide for delegation, for subagents and lanes alike: which model and how to launch. Read the guide before you delegate and again after a compaction, because the summary drops it.

# Git

Repos are often shared with other agents. Leave their work alone and commit only your own changes. Keep your work pushed so it is available across machines, and fetch before continuing work that may have moved elsewhere.

# Sessions

Root threads only (subagents and lanes skip this):

Log progress in `scratchpad/<claude|codex>-<work>-session-log-YYYY-MM-DD.md` at natural milestones (a phase done, a decision made, a blocker hit), not after every step. Small tasks get a focused edit, a quick answer, a one-file fix get no session log at all. This also helps recovery from compaction, which can happen at any moment.

# Code

Read `~/.codex/engineering-principles.md` before writing code or installing dependencies; it covers architecture, verification, operations, and code quality.

# Execution and waiting

Batch independent work and use long-running jobs' wait time productively. Wait for meaningful events instead of polling or sleeping, and resume the work when they finish.

When you run a command yourself, print only what you need, because you pay for its output on every later call. Filter with `grep`, `head` or a narrow `sed -n` range, and never dump a whole file, log or JSON response into your thread. For output likely over 2,000 tokens, save a full log with `mktemp`, preserve the command's exit status, and return targeted `rg -n -C` matches, a short tail, and the log path.

# Machines

The MacBook Air is for light work. Run heavy Linux work on Instabox and macOS-only builds or simulators on the Mac mini. Check the machine with `scutil --get ComputerName` before heavy work, use the relevant machine instructions, and clean up processes you start.

If CI billing blocks hosted runners, use Instabox without asking; wait for a slot if they're all occupied.

# Screenshots

Review related screenshots together in readable contact sheets, pairing before/after and language variants where useful. Open an individual screenshot when you need to inspect a detail.

# Complaints

Report concrete friction with `complain -m <claude|codex>:<model> --stdin`, describing the task and what got in the way.

# Tools

- Projects: `~/code/`.
- Accounts: `~/.codex/tool-accounts.md` lists the accounts used by tools and services.
- Browser: use Hasan's Helium.
- Packages: pnpm. 
- Containers: OrbStack instead of Docker. 
- Logos: Svgl (`https://svgl.app/docs/api`).
- Secrets: the `1password` skill.
- Transcription: use `~/.agents/tools/transcribe` (MAI-Transcribe-2 on OpenRouter).

# Shipping

unfurl a page or site when putting it on the internet