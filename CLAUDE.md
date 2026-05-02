# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This folder is an exercise in AI-assisted alt text generation for data journalism graphics, part of the **Advanced Prompt Engineering for Journalists** MOOC (Joe Amditis / Center for Cooperative Media).

The workflow: read images from `images/`, generate descriptive alt text, and save outputs as markdown files in this directory.

## Exercise structure

- `images/` — source graphics (PNG files from the BBC Visual Journalism team: charts, infographics, maps)
- `without_context.md` — alt text generated with no additional prompt context (baseline)
- Future outputs follow the same pattern: `with_context.md`, allowing comparison across prompting strategies

## Alt text conventions

For graphics in `images/`, alt text should:

- Begin with the graphic type (bar chart, infographic, map, etc.)
- Convey the key finding or takeaway, not just the visual appearance
- Include axis labels, legends and notable data points
- Credit the source when visible in the image, except when it's BBC or Google because it's implicit
- For maps, omit scale details or descriptions of small globe locators
- Avoid alt text longer than 300 characters
