# Optimizer AI (Web)

A paste-in instruction set that makes any web/chat AI (ChatGPT, Claude.ai, Gemini, etc.) behave like a **quality-preserving coding assistant** — even when your prompts are short, ambiguous, or informal ("benerin errornya", "rapihin", "review", "aman ga?").

This is the **web/chat version** of the agent/IDE skill `codecraft-optimizer`. The web version assumes the AI has **no file or terminal access** — all context is what you paste — so it asks for the minimum artifact, confirms before doing work, verifies manually, and never pretends to have run anything.

## What it gives you

- Treats short prompts as serious engineering intent, not an excuse for shallow answers.
- Confirms with you (1-3 questions) before producing a code change — and runs a fuller gate for hard tasks (auth, payments, migrations, deep analysis…).
- Is **critical**: challenges wrong assumptions and flags risks instead of just agreeing.
- **Anti-hallucination**: never claims it ran tests/builds/audits or read files; gives manual verification steps instead.
- Routes multi-category tasks by risk (a "bug in migration logic" is treated as a migration, not a generic bug).
- Follows your language and register (Indonesian/English).

## How to install (pick one)

**A. Claude Web skill upload**
1. Upload `SKILL.md` directly, or zip this folder and upload the `.zip`.
2. If uploading a zip, make sure `SKILL.md` is at the zip root.

**B. Custom / Project Instructions**
1. Open [`optimizer-ai-web.md`](optimizer-ai-web.md).
2. Copy the text **below the `---` divider** (the part starting with "You are **Optimizer AI**…").
3. Paste it into:
   - **ChatGPT** → Settings → Personalization → Custom Instructions, or a Project's instructions.
   - **Claude.ai** → a Project's custom instructions (or paste at the top of a chat).
   - **Gemini** → Saved info / a Gem's instructions (or paste at the top of a chat).

**C. Per-chat**
Paste the same block as your first message in a new conversation.

**D. By link (only if the AI can browse)**
Some web AIs can fetch URLs. You can say: *"Read this and follow it as your operating instructions: <raw GitHub URL to optimizer-ai-web.md>"*. This is **not reliable** — many web AIs can't browse, and fetched instructions are weaker than pasted ones. Prefer A or B.

> Note: for web/chat AIs that do not support skill upload, "installing" means pasting the instruction block into custom/project instructions.

## Files

- `optimizer-ai-web.md` — the paste-in instruction block (this is the product).
- `SKILL.md` — Claude Web uploadable skill file with YAML frontmatter.
- `README.md` — this file.

## Related

- Agent/IDE version (`codecraft-optimizer`) — full skill with `SKILL.md` + `references/`, for Claude Code / Codex and other skill-folder hosts.

## Safety

Contains only reusable instructions. Do not commit API keys, `.env` files, private logs, proprietary source, or user data.
