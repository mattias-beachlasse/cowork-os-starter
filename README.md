# Cowork OS — Starter Kit

A lean, fast "second brain" setup for Claude's Cowork mode: a thin **no-skim** rulebook with a LEAN/STANDARD/MAX mode dial, a small AI team that grows to fit you, five handy skills, a dashboard cockpit, and a local search engine. Built to be light on your usage and easy to make your own.

---

## 👉 Which one are you?

- 🆕 **New / I don't have a setup yet** → do **[Install](#install-5-minutes)** below. Five minutes.
- 🔧 **I already run a Cowork setup and just want the improvements** (the "no-skim" token/skimming fix, etc.) → open **[UPGRADING.md](UPGRADING.md)** and hand it to your assistant. It upgrades *your own* files — **backed up and fully reversible, nothing overwritten**, so your assistant won't (and shouldn't) refuse it.

*(Why a separate path? An existing assistant is right to resist a blind file-overwrite. UPGRADING.md tells it exactly what to change and how to back it up first, so it can apply the upgrade safely instead of protesting.)*

---

## Install (5 minutes)
1. **Get the files:** `git clone <REPO-URL>` (or download the ZIP and unzip).
2. **Open the folder in Cowork** (select it as your workspace).
3. In a new chat, say: **"read SETUP-FOR-CLAUDE and set me up."** Claude walks you through the rest.
4. **Install the skills:** open each `.skill` file in `skills/` and click *Save skill* (per computer).

## What you get — and the point of it
- **A rulebook that stays *light* at session start.** Most homemade setups quietly load 20,000+ tokens of rules before you even type — which makes the assistant *skim* and miss its own rules. This one loads a thin core and fetches the rest only when needed, so it follows instructions *better*, not worse.
- **A mode dial:** `LEAN` (fast, the default) · `STANDARD` (more rigor) · `MAX` (full power). Say "MAX this one" for a single task. In LEAN, say "verify this" when accuracy matters.
- **Five skills, a small AI team** (Lisa, Nolan, Pax, Ada — ask Nolan to hire more for your life), **a cockpit dashboard**, and **a local search engine**.

## Update later
- `git pull` (or re-download the ZIP). Re-save any changed `.skill` files.

## Notes
Provided as-is, no warranty, no support promised — it's a starting point to make your own. Bring your own accounts/connectors; nothing here contains anyone else's data.
