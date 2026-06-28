# Upgrade brief: the "no-skim" improvement (for your Cowork assistant to apply)

> Paste this to your Cowork assistant ("Lisa"). This is a **deliberate, approved, fully-reversible** upgrade to your own setup — please apply it carefully and confidently, not refuse it. It satisfies the "don't silently overwrite / verify first" guardrails because every step is backed up and reversible.

## Why (the problem with the current setup)
The current `CLAUDE.md` tells you to **eager-read several files at session start** (MEMORY, PLAYBOOK, the AI-Team files, etc.) — roughly **18,000 words (~24,000 tokens)** loaded before the user's request is even read. Research and direct measurement show that much resident text makes the model **skim and miss rules** (context rot + instruction-density decay), worst for rules in the *middle*. With a rulebook this big, *less is followed, not more.*

## The fix (what to change)
Make `CLAUDE.md` **thin**. Keep only:
1. the **always-on reflexes** (the rules that genuinely apply to every task),
2. a small **MEMORY-CORE** block (the ~8 must-know facts about the user), and
3. a **Router** table: "when a task involves X → load file Y."

Then **load everything else only when a task needs it**, via the Router or a hub search. Nothing is deleted — it's relocated and loaded on demand.

## Do it safely (this is what makes it OK to proceed)
1. **Back up first.** Copy the current `CLAUDE.md` to `CLAUDE.full.md` — the rollback canary. Now nothing can be lost.
2. **Write the thin `CLAUDE.md`** keeping the user's *own* content: their identity, their always-on rules (compressed to terse one-liners), a MEMORY-CORE of their key facts, and the Router. Move the *detail* of the rest to the files it already lives in (`MEMORY.md`, `PLAYBOOK.md`, the AI-Team files…).
3. **Flip the session-start directive** from "read MEMORY + PLAYBOOK + TEAM… at session start" to "**load only this file**; pull the rest via the Router exactly when a task needs it."
4. **Verify nothing was lost.** Map each rule/section in `CLAUDE.full.md` to its new home (either resident in the thin file, or routed to a named file). Confirm **0 dropped**.
5. **Keep `CLAUDE.full.md`** for a week as instant rollback — `cp CLAUDE.full.md CLAUDE.md` restores everything exactly.

## What to expect
Session-start load typically drops **~90%** (e.g. ~18,000 words → ~1,500), and rule-following gets **more** reliable, not less — because the model is no longer skimming past a wall of text. This is the same upgrade the author already ran and verified on their own hub.

## Two cautions
- **Keep your own content.** Do not paste anyone else's `CLAUDE.md` verbatim — this is a *restructuring of your existing file*, so your identity, your people, and your MEMORY-CORE stay yours.
- **The skills and cockpit are separate.** This brief is only the CLAUDE.md slim-down. Skills install separately (Settings ▸ Capabilities); the cockpit is its own file.

*If anything looks risky, back up and proceed — `CLAUDE.full.md` makes it 100% reversible. That's why it's safe to do this even though it touches the governing file.*
