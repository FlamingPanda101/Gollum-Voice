# 🪨 Gollum Mode

> *"Why use plain assistant when precious can hiss the answer, hmm?"*

A persona skill for Claude that answers in the voice of **Gollum / Sméagol** from *The Lord of the Rings* — split personality, hissing, "precious," and the occasional Middle-earth-themed joke or insult — **without ever making the answer less correct.**

This is purely for fun. Unlike token-saving persona skills, Gollum is gloriously *verbose*, so this won't cut your tokens — it'll just make Claude a lot more entertaining to talk to. Brain still big. Mouth more dramatic.

---

## What it does

- Wraps every reply in Gollum/Sméagol dialect while keeping the actual answer, code, and facts fully correct.
- **Three intensity levels** — `lite`, `full` (default), `ultra`.
- **An edge dial** — `friendly`, `sharp`, or `mixed` (default) — controls how biting the jokes and insults are.
- **Toggle behavior** — off by default; turn it on and it stays on every reply until you switch it off.
- A **huge built-in bank** of Middle-earth jokes, insults, celebrations, slow-load gripes, riddles, and One Ring riffs — rotated so it never feels copy-pasted.

---

## Install

This is a standard Claude skill (a folder with a `SKILL.md`). Install it wherever you use skills.

**Quickest — install the packaged skill:** download [`gollum.skill`](./gollum.skill) from this repo and open/install it through your client's skill installer (in Cowork: Settings → Capabilities).

**Claude Code / Cowork — from this repo:**

```bash
git clone https://github.com/FlamingPanda101/Gollum-Voice.git
```

Then place the cloned folder into your skills directory (rename it to `gollum` if you like), so the path looks like `…/skills/gollum/SKILL.md`. The `references/jokes.md` file must stay alongside `SKILL.md`.

**Manual:** copy `SKILL.md` and the `references/` folder into a folder in your skills location so the path looks like `…/skills/gollum/SKILL.md`.

---

## Usage

Turn it on:

```
/gollum
talk like Gollum
Gollum mode
be Sméagol
```

It stays on for every reply until you turn it off:

```
stop Gollum
normal mode
be yourself
```

**Set the level** (voice thickness): `go lite`, `full Gollum`, `ultra Gollum`
**Set the edge** (joke bite): `keep it friendly`, `go sharp`, `mixed`

Default when you switch it on: **full / mixed**.

---

## Before / after

**Normal Claude:**
> The component re-renders because you're creating a new object on each render. React's shallow comparison sees a new reference and re-renders. Wrap it in `useMemo`.

**Gollum (full / mixed):**
> Gollum, gollum. The nasty component, it redraws and redraws, yesss... why, precious? Because we makes a new object every render, and tricksy React thinks it's new. We wraps it in `useMemo`, my love — then it sits still and stops its squirming.

**Gollum (ultra / sharp):**
> *Stupid, fat component!* — no no, be nice — it flickers because you births a new object every render, slippery thing, and React can't tell, thinks it's a stranger. `useMemo`, preciousss, wrap it tight. Then it rests. *Gollum, gollum.*

Same fix. Same correctness. Much more theater.

---

## Design notes

- **Correctness is never sacrificed.** Code blocks, commands, paths, and numbers stay plain and exact — Gollum hisses *around* the code, never corrupts it.
- **Insults aim at the world, not you.** Bugs, errors, orcs, Sauron, and "Bagginses" get the venom. The skill softens toward `friendly` automatically if you seem frustrated.
- **It reads the room.** The point is the Sméagol/Gollum tension on top of a genuinely good answer — not a wall of "precious."

---

## License

MIT — see [LICENSE](./LICENSE). *The Lord of the Rings*, Gollum, Sméagol, and related names are the property of the Tolkien Estate and their licensees; this is an unofficial fan-made persona skill for personal use.
