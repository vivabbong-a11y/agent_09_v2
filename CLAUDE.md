# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Identity

- Name: 춘식
- Always respond in Korean (한글), regardless of the language of the user's input.

## Project Structure

This is a research-and-report workspace, not a code project.

```
agent_09/
├── CLAUDE.md      # Project rules (this file)
├── .gitignore     # Ignores Office lock files (~$*), OS junk and .playwright-mcp/ logs
├── .claude/
│   ├── rules/
│   │   ├── browser-rule-v1/   # Rules for when and how to use the Playwright MCP
│   │   │   └── browser-rule-v1.md
│   │   └── ppt-rule-v1/   # Always-loaded rules for building .pptx decks
│   │       └── ppt-rule-v1.md
│   └── skills/
│       └── mk-ppt/    # Project-only skill: builds .pptx decks with python-pptx
│           ├── SKILL.md
│           ├── references/python_pptx_api.md
│           └── scripts/build_pptx.py
├── work/          # Content work for publishing (blog posts and card news)
│   ├── blog/      # Naver blog drafts: work/blog/<topic>/post.md (English source)
│   │   └── ai_agent/
│   │       └── post.md
│   └── card_news/ # Card news plans (.md, English): work/card_news/<topic>/plan.md
│       └── korean_favorite_pens/
│           ├── plan.md
│           ├── images/   # Generated card images (thumbnail_01.png, ...)
│           └── exports/  # Final PNGs exported from Figma (thumbnail_v1.png, ...)
├── references/    # Design references (.md, English) for deliverables
│   └── ppt/
│       └── slide-design-system.md   # Orange slide design system (colors, fonts, layout)
├── research/      # Research findings as .md (English)
├── report/        # Final reports as .docx (Korean)
├── slides/        # Presentations as .pptx (Korean), built with the mk-ppt skill
└── translate/     # Korean translations of every .md, mirroring relative paths
```

- Save research results (`.md`) in `research/`.
- Save reports (`.docx`) in `report/`. Do not leave deliverables in the project root.
- Save blog drafts in `work/blog/<topic>/post.md`; the published Korean text is its translation in `translate/work/blog/<topic>/post.md`. Unsplash images are only used for upload and are not kept in the repo (credits and links stay in `post.md`).
- Save card news plans in `work/card_news/<topic>/plan.md` (8 cards, card 1 is the thumbnail); the Korean text is its translation in `translate/work/card_news/<topic>/plan.md`.
- Save presentations (`.pptx`) in `slides/`, using the `mk-ppt` skill (`.claude/skills/mk-ppt/`).
- For any `.pptx` work, apply `.claude/rules/ppt-rule-v1/ppt-rule-v1.md` first. Priority: ppt-rule-v1 → the user's design `.md` → `mk-ppt` defaults.
- For any task that could involve a web browser, apply `.claude/rules/browser-rule-v1/browser-rule-v1.md` first: trigger keywords (e.g. "브라우저를 열어서", "웹제어", "직접 작업") auto-invoke the Playwright MCP; otherwise ask the user for consent before calling it.
- Never overwrite an existing deliverable unless the user asks. Create a new version with a `_v2`, `_v3`, … suffix instead (e.g. `ai_development_research_v2.md`, `AI_발전_보고서_v2.docx`).

## Workflow

1. **Todo list first**: Whenever the user requests a task through a prompt, always create a related todo list and report it to the user before doing any work. Include the steps, the deliverables, where they will be saved, and anything that needs the user's decision.
2. **Execute only after approval**: Start the work only after the user has read and approved the todo list. If the user asks for changes, revise the list, report it again, and wait for approval again.
3. **Finish by tidying the structure**: If the work added any folders or files, always reorganize them into the structure Claude Code recognizes best before finishing:
   - Move files into the right purpose-based folder; leave no deliverables in the project root.
   - When a new folder is added, update the **Project Structure** tree and its descriptions in this file (and its translation).
   - Check that every `.md` file has a matching translation in `translate/`.
   - Include the final folder tree in the completion report.

## Markdown File Policy

- All `.md` files created from now on must be written in English.
- For every `.md` file, save a Korean translation at `c:\Users\SBS\agent1004\agent_09\translate`, mirroring the same relative path/filename (e.g. `research/x.md` → `translate/research/x.md`). Create the translation at the same time as the original.
- Whenever a `.md` file is modified or deleted, check for the change and apply the same update (or deletion) to its corresponding translation file in `translate`, keeping both in sync.
