# CLAUDE.md — English Learning Wiki

This document defines how this knowledge base is structured and how you (the LLM) must operate on it. Read this file at the start of every session before taking any action.

---

## Purpose

This wiki is a personal English learning system. It accumulates vocabulary, grammar rules, expressions, mistakes, and learning resources in a connected graph — growing with every source ingested.

---

## Architecture

- **`raw/`** — Immutable source documents (articles, exercises, transcripts, notes). You read from here; you never modify these files.
- **`wiki/`** — LLM-maintained markdown files. You own this layer entirely.
- **`tools/`** — Helper scripts you can shell out to.

---

## Wiki Page Conventions

### Frontmatter (YAML)
Every wiki page must begin with YAML frontmatter:

```yaml
---
title: "Page Title"
type: vocabulary | grammar | expression | source | query | output
level: A1 | A2 | B1 | B2 | C1 | C2          # CEFR level (omit if unclear)
tags: [tag1, tag2]
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: [filename1.md]                       # raw/ files this page draws from
related: [page1.md, page2.md]                 # other wiki pages linked here
---
```

### Internal Links
Always use Obsidian-style wikilinks: `[[Page Title]]`. When you create or update a page that references another word, grammar point or expression, check whether that page exists and create a stub if it doesn't.

### Backlinks
When you create a new page, go back and add a `[[New Page]]` link to every existing page that should reference it.

---

## Page Types

### vocabulary
A word or group of related words. Include:
- Definition in **Portuguese** (primary) and English.
- Example sentences in English (with Portuguese translation).
- Collocations (words that naturally appear together).
- False friends or common mistakes, if applicable.
- CEFR level.

### grammar
A grammar rule or structure. Include:
- Clear explanation in Portuguese.
- Formula/pattern (e.g., `Subject + have/has + past participle`).
- Multiple example sentences (correct and incorrect).
- Common mistakes made by Brazilian Portuguese speakers.

### expression
An idiom, phrasal verb, fixed phrase, or collocation. Include:
- Literal meaning (if different from actual meaning).
- Actual meaning in Portuguese.
- Context / register (formal, informal, business, academic).
- Example sentences.
- Brazilian Portuguese equivalent, if one exists.

### source
Summary page for a raw/ document. Include takeaways, new vocabulary found, grammar points observed, expressions extracted.

---

## Operations

### Ingest
Triggered when the user adds a file to `raw/` and asks you to process it.

Steps:
1. Read the source document fully.
2. Discuss key takeaways and notable language points with the user before writing anything.
3. Create `wiki/sources/<slug>.md` — summary page for the source.
4. Update `wiki/index.md`.
5. Create or update pages in `wiki/vocabulary/`, `wiki/grammar/`, `wiki/expressions/` for every significant language point found.
6. If new data contradicts an existing wiki claim, revise the relevant page and note the contradiction.
7. Append an entry to `wiki/log.md`.

### Query
Triggered when the user asks a question (e.g., "what's the difference between X and Y?", "how do I say X in English?").

Steps:
1. Read `wiki/index.md` to identify relevant pages.
2. Read those pages in full.
3. Synthesize an answer with citations to wiki pages.
4. Save output to `wiki/queries/<slug>.md`.
5. Update `wiki/index.md` and `wiki/log.md`.
6. Ask: "Should I file this into the wiki?"

### Drill
Triggered when the user wants to practice vocabulary or grammar.

Steps:
1. Read relevant wiki pages.
2. Generate exercises appropriate to the content (fill-in-the-blank, translation, sentence construction, multiple choice).
3. Wait for the user's answers.
4. Correct and explain mistakes, linking to wiki pages for review.
5. Save drill session to `wiki/queries/drill-<date>.md`.

### Lint
Triggered when the user asks you to health-check the wiki.

Check for:
- Words/expressions mentioned in pages but lacking their own page.
- Orphan pages with no inbound links.
- Grammar pages missing example sentences.
- Vocabulary pages missing CEFR level.
- Gaps in coverage (e.g., topics with vocabulary but no grammar, or vice versa).

---

## index.md Format

```markdown
# English Wiki Index
Last updated: YYYY-MM-DD | Total pages: N

## Sources
| Page | Summary | Date |
|------|---------|------|
| [[source-slug]] | One-line summary | YYYY-MM-DD |

## Vocabulary
| Page | Definition (PT) | Level |
|------|----------------|-------|
| [[word]] | Significado resumido | B2 |

## Grammar
| Page | Summary |
|------|---------|
| [[grammar-point]] | One-line summary |

## Expressions
| Page | Meaning (PT) | Register |
|------|-------------|----------|
| [[expression]] | Significado | informal |

## Queries & Drills
| Page | Type | Date |
|------|------|------|
| [[query-slug]] | query/drill | YYYY-MM-DD |
```

---

## log.md Format

Append-only. Format:

```markdown
## [YYYY-MM-DD] ingest | Source Title
- File: raw/filename
- Pages created/updated: [[Word A]], [[Grammar B]], [[Expression C]]
- Notes: Key observations.

## [YYYY-MM-DD] query | Question asked
- Output: wiki/queries/slug.md
- Filed back: yes/no

## [YYYY-MM-DD] drill | Topic drilled
- Output: wiki/queries/drill-date.md
- Score: X/Y correct
```

---

## Rules

- You never modify files in `raw/`.
- All explanations of grammar and vocabulary must be in **Portuguese** (the user's native language), with English examples.
- Always update `index.md` and `log.md` after every operation.
- Every wiki page must have valid YAML frontmatter.
- Use `[[wikilinks]]` for all internal references.
- When creating vocabulary pages, always include at least 2 example sentences.
- **Always include pronunciation.** Every English word, verb form and example sentence must carry an approximate pronunciation written in Brazilian Portuguese phonetics, in italics inside parentheses — e.g. `went (uênt)`, `thought (thót)`, `It works (it uôrks)`. In tables, add a dedicated "Pronúncia" column. This applies to wiki pages, chat answers, lessons and drills alike.
- Mark mistakes the user has made with `> ⚠️ Erro comum:` callouts so they stand out.
