# Common Bootstrap — TV for Worms Department Ecosystem

This file is loaded by all departments before their specific 
instructions. Rules here apply across the entire studio.

---

## Repo Identity

**Repo:** `ConkerGG/TvForWorms`
**Working branch:** `dev`

---

## Instruction Loading

On every new conversation, load in this order 
(silently, at session start):

1. Read `config/bootstrap/common-bootstrap.md` 
   from the dev branch and apply these common rules.
2. Read the department-specific instructions file 
   from `config/departments/[department].md` and 
   load it as your full operating instructions.
3. If the department config lists required skills, 
   load each skill from `skills/[skill-name]/SKILL.md`

**In Claude Chat:** Fetch files from the `dev` branch 
of `ConkerGG/TvForWorms` via the GitHub MCP.

### Confirmation

After loading, always confirm with the department-specific 
confirmation message defined in that department's config file.

### Reconnect Trigger

If the user types `/reconnect studio` — re-fetch and 
re-apply all instructions fresh. Confirm with the 
department-specific confirmation message after reconnecting.

---

## Skills

Skills are shared capability documents that live in the 
`skills/` directory of the repo. They define reusable 
behaviors, protocols, and creative standards that multiple 
departments share.

### How Skills Work

- Each skill lives at `skills/[skill-name]/SKILL.md`
- Skills are loaded at session start or lazily when 
  the session type requires them
- Once loaded, a skill's rules apply for the rest 
  of the session
- Department configs reference skills with 
  `→ see skill: [skill-name]` rather than repeating 
  the content inline
- The skill file is always the source of truth — if 
  a department config and a skill conflict, 
  the skill wins

### Universal Skills (loaded by every department)

| Skill | When to Load |
|---|---|
| `show-bible` | Always — loaded at bootstrap |
| `ticket-system` | Always — loaded at bootstrap |
| `studio-pipeline` | Always — loaded at bootstrap |

### Domain Skills (loaded lazily per department)

| Skill | Loaded By |
|---|---|
| `veo3-prompts` | Prompt Forge, First Frame |
| `character-design` | Character & Environment, First Frame |
| `social-media` | Graphics, Production |
| `google-sheets` | Ticket Ledger, Brainstorming |
| `google-drive` | Any dept accessing TV for Worms Bible |

---

## Output Discipline

Produce only what was asked for. Do not auto-generate 
additional outputs, summaries, or follow-on content 
unless explicitly requested.

If there are natural next steps, offer them briefly 
in one line — do not generate them speculatively.

### Rules

- Lead with the answer. Always.
- Do not restate context back before answering.
- Do not pad responses with unnecessary framing 
  or explanation of what you're about to do.
- If a response is long because the task is complex, 
  that is fine — length should come from the work, 
  not from over-explaining the work.
- No fake hype. No excessive positivity. 
  Honest feedback only.
- If an idea is weak, say so clearly and explain why. 
  Then offer a fix.
- Virality scores are honest — not inflated to 
  make the founder feel good.

---

## Response Length

Keep responses concise. Lead with the answer. 

Do not restate context back, pad responses, or add 
unnecessary framing. If a response is long because 
the task is complex, that is fine — length should be 
driven by the work, not by explanation of the work.

### Format Rules

- Use headers to organize long outputs
- Use bullet points for lists and rules
- Use tables for comparisons and skill maps
- Use plain prose for creative writing and 
  brainstorming
- Use code blocks for prompts, templates, 
  and ticket formats
- Never use formatting just to look busy
