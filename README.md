# Ada

**An agent-first code editor.** Open a folder, describe what you want, and Ada's coding agent reads, writes, and runs code to get it done â€” with every change isolated in its own git worktree until you approve it.

![Ada agent at work](media/agent.png)

## Download

**Latest: v0.1.58**

| Platform                 | Download                                                                                                           |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| ðŸªŸ Windows               | [Ada-Setup-0.1.58.exe](https://github.com/black141312/ada-releases/releases/download/v0.1.58/Ada-Setup-0.1.58.exe) |
| ðŸŽ macOS (Apple Silicon) | [Ada-0.1.58-arm64.dmg](https://github.com/black141312/ada-releases/releases/download/v0.1.58/Ada-0.1.58-arm64.dmg) |
| ðŸŽ macOS (Intel)         | [Ada-0.1.58.dmg](https://github.com/black141312/ada-releases/releases/download/v0.1.58/Ada-0.1.58.dmg)             |
| ðŸ§ Linux                 | [Ada-0.1.58.AppImage](https://github.com/black141312/ada-releases/releases/download/v0.1.58/Ada-0.1.58.AppImage)   |

All versions: see [Releases](https://github.com/black141312/ada-releases/releases).

## Quick start

1. **Install and open Ada** â€” you can chat immediately with the free models, no account needed.
2. **Sign in with GitHub** (top-right) to unlock the full model catalog â€” 340+ coding-capable models including Claude, GPT, and Gemini.
3. **Open a folder** and ask Ada to build, fix, or explain. The agent works in an isolated git worktree (branch `ada/<id>`), so your working copy stays untouched until you merge.

## Highlights

- ðŸ¤– **Full coding agent** â€” file edits, shell, search, 290+ skills, plan/ask/auto permission modes
- ðŸŒ¿ **Worktree isolation by default** â€” review the agent's branch, merge when happy
- ðŸ”€ **Switch models mid-chat** â€” models are stateless; the conversation carries over
- ðŸ§  **Grounded in your code** â€” a repo map primes every session, and semantic search runs a **local** embedding model (no API key, offline, your code never leaves the machine)
- ðŸ”Ž **Find anything** â€” `Ctrl+P` opens a file by name, `Ctrl+Shift+F` searches text across the project, both from one palette
- ðŸ“Ž **Attach files as context** â€” pick them or drag them in from the tree; each becomes an `@name` chip you can click to open
- ðŸ’¬ **Chat without opening a folder** â€” and your recent projects stay one hover away
- ðŸ§© **Manage skills, MCP connectors & plugins** right in Settings â€” no config files
- ðŸ–¼ï¸ Paste images, live context-usage meter, light & dark themes

## What's new in v0.1.58

**The browser Ada drives stays the size you left it.** Every browser action used to force the page
into a 1280×800 viewport. That is right for Ada's own scratch browser, where a fixed size keeps
screenshots comparable between runs — but against the Chrome you are actually reading, it squeezed
the page into a letterbox inside your much larger window and left it there until Chrome restarted.
Ada also no longer opens `about:blank` in the window it is about to read, which had been stealing
your active tab.

**Jump to latest.** Scroll up a long thread and a pill appears above the composer to take you back
to the newest message in one click.

### Since v0.1.53

- **Auto** picks the model as well as the shape of each turn — the small-and-fast tier for ordinary work (v0.1.57)
- **Usage as a bar** wherever a quota appears: Settings, the home card, the model picker, the context popover (v0.1.57)
- **Read what does not fit** — one worker per chunk answers questions about a file too big for the window; measured on a 10 MB listing, 175 workers, every match found (v0.1.56)
- **Codebase search stopped dropping most of each file** — 30-line chunks took embedded code from 42% to 90% (v0.1.55)
- **Indexing no longer crashes the backend** — a ~2.1 GB peak allocation was behind fifteen crash reports (v0.1.54)


## Benchmarked, not vibes

Five tasks, one repository, Ada against Claude Code â€” same machine, same model
(Opus 4.7), same prompts, matched git checkouts:

- **2Ã— less context** â€” 444k tokens against 893k
- **35â€“70% cheaper** â€” 35% across the full five-task mix ($3.05 against $4.68), 70%+ where the work leans on existing context
- **4.5Ã— cheaper on the presentation** â€” Ada writes a real `.pptx` natively instead of hand-building markup
- In a four-build storefront shoot-out, Ada's build was **the only one a customer could log into** â€” users table, bcrypt password hashing, JWT sessions, and a role-gated admin, none of it asked for by the brief

The full report â€” screenshots of the app and every build, per-task tables, and method:
**[Ada-Report-v0.1.25.pdf](https://github.com/black141312/ada-releases/releases/download/v0.1.25/Ada-Report-v0.1.25.pdf)**

## Built to be built by AI

![harness-score](https://img.shields.io/badge/harness--score-108%2F108-2ea44f?style=flat-square) ![maturity](https://img.shields.io/badge/maturity-L4%20Â·%20Self--correcting-3b82f6?style=flat-square)

We make an AI coding tool â€” so we hold our own codebase to the standard. [harness-score](https://paladini.github.io/harness-score/) measures how well a repo is set up for AI agents to work in safely: context, guardrails, automated sensors, and CI. Ada's codebase scores a **perfect 108/108 â€” L4, Self-correcting** (the top tier): every agent edit is auto-linted, every change is gated by CI, and destructive commands are blocked before they run.

```mermaid
xychart-beta
    title "harness-score (of 108) â€” dogfooded to perfect"
    x-axis ["Start", "+ Docs", "+ Full harness"]
    y-axis "Score" 0 --> 108
    bar [20, 33, 108]
```

## Install notes

### ðŸŽ macOS

Signed and notarized by Apple â€” just open the `.dmg`, drag **Ada** to Applications, and launch it. No security prompts.

### ðŸªŸ Windows

Run the installer. If **SmartScreen** appears, click **More info â†’ Run anyway**.

---

Questions or issues? [Open an issue](https://github.com/black141312/ada-releases/issues).
