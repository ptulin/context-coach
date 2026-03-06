# 🧠 Context Coach

**A Claude skill for power users on a budget.**

Context Coach helps you work smarter and longer with whatever Claude plan you have. It activates at the start of every project, monitors your session for token-burning patterns, steps in proactively, and gives you an efficiency report at the end showing estimated savings vs. an uncoached session.

---

## What it does

- **Project Kickoff Protocol** — asks 3 scoping questions before starting any work to prevent scope creep and wasted context
- **Pattern detection** — spots and flags expensive habits in real time: re-explaining context, multi-topic pile-ons, giant unscoped file uploads, scope creep mid-session
- **Response style defaults** — enforces concise, answer-first responses throughout the session
- **Checkpoints** — every ~4 major steps, checks in on context health and recommends when to wrap up or start fresh
- **Handoff summaries** — when context gets long, generates a paste-ready summary for a fresh conversation
- **Session Efficiency Report** — end-of-session report showing estimated tokens used, estimated baseline without coaching, savings, and a plain-English summary

---

## Example output

```
📋 SESSION BRIEF
Goal: Build a landing page for my photography portfolio
Out of scope: Blog section, shop, mobile-only features
Key files: brand-guidelines.pdf (uploaded)
Efficiency mode: ON
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📊 SESSION EFFICIENCY REPORT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

| Metric                  | This Session | Without coaching |
|-------------------------|--------------|-----------------|
| Exchanges               | 12           | ~17             |
| Estimated tokens used   | ~8,400       | ~13,200         |
| Tokens saved            | ~4,800       | —               |
| Efficiency gain         | ~36%         | —               |

In plain English:
This session used roughly 8,400 tokens. Without scoping and
pattern detection, a similar session typically runs ~13,200 tokens.
You got the same output for ~36% less context spend.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Installation

### Option A: Install the .skill file (easiest)

1. Download [`context-coach.skill`](./context-coach.skill) from this repo
2. Open the **Claude desktop app**
3. Go to **Settings → Extensions**
4. Drag and drop the `.skill` file into the extensions panel
5. Done — Context Coach is now active

### Option B: Manual install

1. Copy the contents of [`SKILL.md`](./SKILL.md)
2. In the Claude desktop app, go to **Settings → Extensions → Create Skill**
3. Paste the content and save

### Option C: Install from this repo path (for developers)

Find your Claude skills directory:
```bash
find ~/Library/Application\ Support/Claude -name "SKILL.md" 2>/dev/null | head -5
```

Copy `SKILL.md` into a new folder there:
```bash
mkdir -p "~/Library/Application Support/Claude/.../skills/context-coach"
cp SKILL.md "~/Library/Application Support/Claude/.../skills/context-coach/SKILL.md"
```

---

## Requirements

- Claude desktop app (Cowork / local agent mode)
- Works with any Claude plan — designed specifically for users on Free or Pro plans who want to stretch their usage

---

## Philosophy

Most token optimization tools are built for developers running API calls. This is for everyone else — designers, researchers, writers, and knowledge workers who use Claude for real projects and want to get more done without hitting limits.

The core idea: **Structure beats brute force.** A well-scoped 12-exchange session beats a wandering 20-exchange session every time. Context Coach builds that structure in automatically.

---

## Roadmap

- [ ] Pre-session project brief templates (v2)
- [ ] Obsidian MCP integration for persistent project memory across sessions
- [ ] Model routing hints (flag when a task could use a smaller/cheaper model)
- [ ] Skills/extensions overhead awareness (alert when too many skills are loaded)
- [ ] Post-session notes export

---

## Contributing

This is an open skill — fork it, remix it, improve it. If you make a better version, open a PR.

---

## License

MIT — do whatever you want with it.

---

*Built by [@ptulin](https://github.com/ptulin) with Claude.*
*Part of the "power users on a budget" toolset.*
