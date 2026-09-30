# AI Wardrobe Stylist (working name)
 
## What this is
A mobile app that acts as a personal stylist. Users add their own clothes; the app suggests
outfits from what they actually own, based on context (college/office/event), weather,
fit, wear history and availability (laundry).
 
Core differentiator vs ChatGPT: it knows and learns the user's real wardrobe, what fits,
and what they wore recently.
 
## Users
18–30 year olds in India who go to college or office. Key moments: weekday outfits
(decided mostly the NIGHT BEFORE) and festivals/traditional events (sharpest pain).
 
## V1 scope
IN: progressive onboarding, photo → auto-tagged item, fit status per item, skip feedback,
wear history, laundry awareness, weather, context input, bags as a category.
OUT (for now): jewelry, avatar, gap analysis, purchase size prediction, custom ML models,
social features.
Full reasoning: `docs/DECISIONS.md`.
 
## Architecture principles
- Data model is category-based. An outfit is a SET of items (supports sarees, dresses,
  kurta sets), never hardcoded "top + bottom".
- Rules before ML. Use simple rules until real data proves a model is needed.
- Collect personal data only when it visibly improves a suggestion. Photos and body data
  are sensitive (India DPDP Act 2023).
- Every feature must be measurable. Track: day-7 return rate, % suggestions worn,
  opens without notification.
## Stack
NOT DECIDED YET. Do not choose a framework, backend, or AI provider on your own.
Ask the user and record the decision.
 
## How to work with me (Claude Code)
- Use plan mode for anything non-trivial. Show the plan before writing code.
- Keep tasks small and scoped. Do not explore the whole repo unless asked.
- If a task requires a decision not covered here or in `docs/DECISIONS.md`, STOP and ask.
- When the user makes a decision, append an entry to `docs/DECISIONS.md` (next number,
  same format) and update this file only if scope or principles change.
- Keep this file short. Detailed reasoning belongs in `docs/DECISIONS.md`.
- For structural changes, update the Mermaid diagram in `docs/ARCHITECTURE.md`.