# Alt Text Generator — Exercise

A before/after comparison of AI-generated alt text for BBC Visual Journalism graphics, produced as part of the **Advanced Prompt Engineering for Journalists** MOOC (Joe Amditis / Center for Cooperative Media).

## What this exercise explores

Can a `CLAUDE.md` context file meaningfully improve the quality of AI-generated alt text? This exercise tests that by running the same task twice — once with no context, once with a set of domain-specific conventions — and comparing the results.

## Graphics

Four BBC Visual Journalism assets in `images/`:

| File                     | Type              | Subject                                                   |
| ------------------------ | ----------------- | --------------------------------------------------------- |
| `chart_ai_responses.png` | Stacked bar chart | AI chatbot accuracy on health questions (BMJ Open, 2025)  |
| `chart_fertiliser.png`   | Calendar chart    | When fertiliser shortages could be felt — UK, US, India   |
| `graphic_co2.png`        | Infographic       | How a CO2 shortage could hit food supplies                |
| `map_louisiana.png`      | Locator map       | Brompton Lane, Bossier Parish, near Shreveport, Louisiana |

## Outputs

| File                 | Description                                                            |
| -------------------- | ---------------------------------------------------------------------- |
| `without_context.md` | Alt text generated with no additional instructions — Claude's baseline |
| `with_context.md`    | Alt text generated after `CLAUDE.md` conventions were in place         |
| `comparison.md`      | Side-by-side table and analysis of what changed between the two runs   |

## What changed with context

The `CLAUDE.md` file gave Claude four conventions. Each one produced a measurable difference:

- **Start with graphic type** — both runs did this; the convention reinforced existing behaviour.
- **Lead with the key finding** — without context, alt text described visual structure first (legend colours, numbered steps, row/column layout). With context, the journalistic takeaway leads.
- **Stay under 300 characters** — without context, all four alt texts ran 480–607 characters. With context, all four came in under 255.
- **Omit implicit sources and map details** — without context, BBC and Google were credited and map scale bars and locator insets were described. With context, only third-party sources (BMJ Open) appear, and map conventions are applied.

## How to replicate

1. Place source images in `images/`.
2. Run Claude Code in this directory **without** a `CLAUDE.md` file and ask for alt text suggestions. Save output to `without_context.md`.
3. Add a `CLAUDE.md` with your alt text conventions.
4. Run the same prompt again. Save output to `with_context.md`.
5. Ask Claude Code to compare the two files and generate `comparison.md`.

## Course context

This is a Module 1 exercise from the MOOC, covering how context files shape model behaviour. The key lesson: a well-written `CLAUDE.md` acts as a standing brief — it encodes domain knowledge (accessibility conventions, source attribution rules, length constraints) that would otherwise have to be re-stated in every prompt.
