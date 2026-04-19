# Chattrvox Docs: Claude Code Instructions

## About this project

This is the documentation site for Chattrvox, a white-label AI voice platform for agencies, MSPs, BPOs, and VoIP providers.

- Framework: [Mintlify](https://mintlify.com)
- Pages: MDX files with YAML frontmatter
- Navigation: `docs.json`
- Preview locally: `mintlify dev`
- Check links: `mintlify broken-links`
- Source of truth for all feature claims: the platform source code at `../chattrvox-production-saas`

Never guess at feature behavior. If you're unsure how something works, read the platform source before writing about it.

---

## Terminology

Use these terms consistently across every page:

| Use this | Not this |
|----------|----------|
| Agent (in UI references) | Bot, chatbot, robot |
| Assistant (acceptable in prose) | — |
| Workspace | Project, account, org |
| Contact | Lead, user, prospect |
| Campaign | Dialing run, outreach |
| Workflow | Automation, zap, flow |
| Composer | Workflow builder, canvas |
| Partner plan | Enterprise, reseller plan |

---

## Writing tone

The goal: a capable person reads this once and knows exactly what to do.

Write like Apple writes. Not a manual. Not a brochure. Direct, human, confident.

**Do this:**
- Short sentences. One idea each.
- Start with what the user can do: "Build a voice agent in minutes."
- Use second-person imperative: "Click **New Agent**" not "The user clicks New Agent."
- State facts plainly: "Chattrvox transcribes every call automatically."
- Trust the reader. Skip the hand-holding.

**Never do this:**
- Passive voice: "An SMS is sent" → "Chattrvox sends an SMS"
- Hedging: "you may want to", "consider", "it's possible to"
- Editorializing: "powerful", "intuitive", "intelligent" — describe what it does, not how great it is
- Filler: simply, easily, just, quickly
- Em dashes — use periods, commas, parentheses, or colons instead
- Banned words: leverage, utilize, streamline, cutting-edge, game-changing, robust, synergy, optimize, revolutionize, empower, seamless, holistic, actionable insights, best-in-class, paradigm shift, deep dive, comprehensive guide

**Formatting:**
- Sentence case for all headings
- Bold all UI element names: **New Agent**, **Settings**, **Composer**
- No Oxford-comma debates — use it

---

## Page structure

Every page follows this order. No exceptions.

1. **Opening sentence** — one sentence, plain statement of what this thing does. Never start with "In this guide" or "This page explains."
2. **How it works** — steps or concepts in second-person imperative voice
3. **Key configuration** — what the user needs to decide, what the options are
4. **Next steps** — one internal link to where the user goes next

**Example — BEFORE (wrong):**
> "The platform supports four primary automation types including post-call messaging and CRM synchronization."

**Example — AFTER (right):**
> "Workflows run automatically after calls end. Use them to send SMS follow-ups, update HubSpot, trigger new outbound calls, or route contacts based on call outcome."

---

## Mintlify components

Use these components correctly. Wrong component choices make docs harder to scan.

| Component | Use for |
|-----------|---------|
| `<Steps>` | Any sequential process. Never use numbered lists in prose. |
| `<CardGroup cols={2}>` | Parallel options or use cases. Max 4 cards per group. |
| `<AccordionGroup>` | Reference material users don't always need open. |
| `<Note>` | Important context the user might miss. |
| `<Tip>` | A non-obvious shortcut or best practice. |
| `<Warning>` | Something that causes data loss or irreversible action. |

Use `<Note>`, `<Tip>`, and `<Warning>` sparingly. If every other paragraph has a callout box, none of them land.

Always:
- Add language tags to every code block: ` ```bash `, ` ```json `, etc.
- Add alt text to every image
- Use relative paths for internal links

---

## Content rules

- Search existing docs before adding anything new
- Make the smallest change that achieves the goal
- Every page ends with a next step or related link
- Don't document pricing — link to [waverunner.digital/pricing](https://waverunner.digital/pricing)
- Don't document internal Wave Runner admin or operator features
- Don't make feature claims that aren't verified in the platform source

---

## Git workflow

- Never use `--no-verify`
- Branch per page: `docs/rewrite-page-name`
- Commit per page, not in bulk
- Run `mintlify broken-links` before pushing
- Commit message format: `docs(page-name): short description of change`
