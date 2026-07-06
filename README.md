# 🪨 Gollum Voice

> *"Why use plain assistant when precious can hiss the answer, hmm?"*

A persona skill that makes your AI agent answer in the voice of **Gollum / Sméagol** from *The Lord of the Rings* — split personality, hissing, "precious," and Middle-earth jokes and insults — **without ever making the answer less correct.**

Purely for fun. Unlike token-saving persona skills, Gollum is gloriously *verbose*, so this won't cut your tokens — it just makes your agent far more entertaining. Brain still big. Mouth more dramatic.

---

## Before / after

**Normal:**
> The component re-renders because you create a new object each render. Wrap it in `useMemo`.

**Gollum (full):**
> Gollum, gollum. The nasty component, it redraws and redraws, yesss... why, precious? A new object every render, and tricksy React thinks it's new. We wraps it in `useMemo`, my love — then it sits still and stops its squirming.

Same fix. Same correctness. Much more theater.

---

## What it does

- Wraps every reply in Gollum/Sméagol dialect while keeping the answer, code, and facts fully correct.
- **Three intensity levels** — `lite`, `full` (default), `ultra`.
- **An edge dial** — `friendly`, `sharp`, `mixed` (default) — how biting the jokes are.
- **Toggle** — off by default; on with "talk like Gollum"; stays on until "stop Gollum".
- A **575-line joke bank** across 32 categories (`skills/gollum/references/jokes.md`), rotated so it never feels copy-pasted.

---

## Install

**Quickest (Cowork / any skill host):** download [`gollum.skill`](./gollum.skill) and install it through your client's skill installer (in Cowork: Settings → Capabilities).

### Claude Code

```
/plugin marketplace add FlamingPanda101/Gollum-Voice
/plugin install gollum@gollum-voice
```

(Send as two separate prompts.)

### Works with many agents (same ruleset, native format)

This repo ships the Gollum ruleset in each tool's native rules location, so it works far beyond Claude Code. Copy the matching file into your project or global config:

| Agent | File to use |
| --- | --- |
| **Codex / OpenCode / Zed / Aider / CodeWhale / VS Code (Codex)** | [`AGENTS.md`](./AGENTS.md) (read automatically from project root) |
| **Cursor** | [`.cursor/rules/gollum.mdc`](./.cursor/rules/gollum.mdc) |
| **Windsurf** | [`.windsurf/rules/gollum.md`](./.windsurf/rules/gollum.md) |
| **Cline** | [`.clinerules/gollum.md`](./.clinerules/gollum.md) |
| **GitHub Copilot** | [`.github/copilot-instructions.md`](./.github/copilot-instructions.md) |
| **Kiro** | [`.kiro/steering/gollum.md`](./.kiro/steering/gollum.md) |
| **Claude Code (skill only)** | [`skills/gollum/`](./skills/gollum) |

All of these are copies of one source: [`rules/gollum-rules.md`](./rules/gollum-rules.md). The Claude Code plugin bundles the full skill (with the 575-line joke bank); the rules-file adapters carry the compact ruleset plus a joke sample.

---

## Usage

Turn it on: `talk like Gollum` · `Gollum mode` · `/gollum` · `be Sméagol`
Turn it off: `stop Gollum` · `normal mode`

**Level:** `go lite` · `full Gollum` · `ultra Gollum`
**Edge:** `keep it friendly` · `go sharp` · `mixed`

Default when switched on: **full / mixed**.

---

## Design notes

- **Correctness is never sacrificed.** Code, commands, paths, and numbers stay plain and exact — Gollum hisses *around* the code.
- **Insults aim at the world, not you** — bugs, orcs, Sauron, "Bagginses." The skill softens toward `friendly` if you seem frustrated.
- It reads the room: the point is the Sméagol/Gollum tension on top of a genuinely good answer.

---

## Repo layout

```
Gollum-Voice/
├── skills/gollum/          # the full skill (SKILL.md + references/jokes.md)
├── .claude-plugin/         # Claude Code plugin + marketplace manifest
├── rules/gollum-rules.md   # canonical compact ruleset (source for all adapters)
├── AGENTS.md               # always-on rule for AGENTS.md-aware agents
├── .cursor/ .windsurf/ .clinerules/ .github/ .kiro/   # per-agent rule copies
├── gollum.skill            # packaged one-click install
├── README.md
└── LICENSE
```

---

## License

MIT — see [LICENSE](./LICENSE). *The Lord of the Rings*, Gollum, Sméagol, and related names are the property of the Tolkien Estate and their licensees; this is an unofficial fan-made persona skill.
