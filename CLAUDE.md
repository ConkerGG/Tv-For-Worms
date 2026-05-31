# TV for Worms — Claude Code Reference

**Repo:** `ConkerGG/TvForWorms`
**Working branch:** `dev` — never push directly to `main`

---

## Project

TV for Worms is an AI-powered surreal short-form series. 
South Park meets Robot Chicken on Adult Swim — with the 
soul of a TikTok fever dream.

The show is set in a dystopian claymation world built on 
early 2000s nostalgia — CRT TVs, familiar homes, that warm 
glitchy glow — but populated by worms, bugs, and small 
creatures — clay and toy versions of them — living alongside 
androids, AI, and robots. Big corporations compete for one 
thing: everyone's attention. Every adult is zombified by 
short-form content on TVs and phones. Every adult except 
a gang of kids still living in the real world.

Episodes follow the kids through their daily shenanigans — 
South Park-style chaos and heart. Mid-episode, one kid gets 
hypnotized by a screen and enters a trance state. That's 
where we cut into the skit block — a relentless, anything-
goes sequence of short-form content. Funny, gross, shocking, 
scary, artistic, absurd — no rules, no consistency, just 
the pure randomness of the scroll. Then we snap back to the 
kids and finish the episode.

The show is a symbolic mirror of today. The trance is real. 
Everyone knows what it feels like to get sucked in and 
wake up twenty minutes later. TV for Worms just puts it 
on screen.

This repo manages department instructions, show assets, 
production skills, automation scripts, and the full 
multi-department creative studio system built on Claude.

---

## Department System

Departments are configured in `config/departments/`. Each 
loads its instructions at session start via 
`config/bootstrap/common-bootstrap.md`. Skills live in 
`skills/` and are the source of truth for shared protocols 
— if a skill and a department config conflict, the skill 
wins.

Key files:
- `config/bootstrap/common-bootstrap.md` — universal rules for all departments
- `skills/show-bible/SKILL.md` — show identity, tone, and creative standards
- `config/departments/production.md` — top-level studio operations

---

## Git Workflow

All sessions follow the two-gate push pattern:

1. Present plan → wait for approval
2. Draft changes
3. Self-improvement check
4. Present push confirmation → wait for explicit yes
5. Push to `dev`

Never skip gates. Approval at gate 1 does not authorize 
the push at gate 4.

---

## Credentials

All credentials live in `.env` only. Never hardcode in 
scripts, configs, or commit messages. Required variables 
are documented in `.env.example`.
