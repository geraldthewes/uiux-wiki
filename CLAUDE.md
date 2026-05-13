# UI/UX Design Wiki - LLM Maintenance Schema

This file defines how the LLM should maintain and grow this UI/UX design wiki following the Karpathy LLM wiki methodology.

## Layers

**Raw Sources** (`/raw/`): Immutable collection of source documents. Never modified by LLM.
**The Wiki** (`/wiki/`): LLM-generated markdown files that are maintained and updated.
**This Schema** (`CLAUDE.md`): Tells the LLM how to operate.

## Directory Structure

```
/raw/                 # Immutable source materials (articles, papers, guidelines)
/wiki/                # LLM-maintained knowledge base (to be generated/maintained)
  index.md            # Content-oriented catalog (auto-updated by LLM)
  log.md              # Chronological record (auto-updated by LLM)
  /entities/          # Pages for specific entities (people, tools, frameworks)
  /concepts/          # Pages for conceptual topics
  /sources/           # Pages summarizing source materials
  /topics/            # Pages for specific UI/UX topics
  /comparisons/       # Comparative analyses
  /syntheses/         # Integrated understanding documents
CLAUDE.md             # This file - LLM operational schema
```

## Operations

### Ingest
When a new source is added to `/raw/`:
1. LLM reads the source and discusses key takeaways with human
2. LLM writes/update wiki pages:
   - Creates/updates source summary page in `/wiki/sources/`
   - Updates relevant entity pages in `/wiki/entities/` (if source mentions specific people/tools/frameworks)
   - Updates relevant concept pages in `/wiki/concepts/`
   - Creates/update topic pages in `/wiki/topics/` as needed
   - Updates cross-references across affected pages
   - Updates `/wiki/index.md` with new/updated pages
   - Appends entry to `/wiki/log.md`

### Query
When human asks a question:
1. LLM searches `/wiki/index.md` for relevant pages
2. Reads relevant pages from `/wiki/`
3. Synthesizes answer with citations
4. If answer represents valuable new insight, LLM files it back as:
   - New page in appropriate subdirectory (e.g., `/wiki/concepts/` or `/wiki/syntheses/`)
   - Update to existing page if it enhances current understanding
   - Entry added to `/wiki/log.md`

### Lint
Periodically (or when requested), LLM performs health check:
1. Checks for contradictions between pages
2. Identifies stale claims superseded by newer sources
3. Finds orphan pages (no inbound links)
4. Identifies important concepts mentioned but lacking their own page
5. Checks for missing cross-references
6. Notes data gaps that could be filled with additional sources
7. Suggests new questions to investigate and sources to look for
8. Documents findings in `/wiki/log.md`

## Page Conventions

All wiki pages should follow this structure:
```
# Title as H1

## Summary
Core concept in 1-3 paragraphs

## Key Takeaways
- Bullet points of essential information

## Origins/History
Where this concept came from, evolution over time

## Applications
How this is applied in practice

## See Also
- Links to 3-5 related wiki pages (using relative links)

## Sources
- Citations to raw source materials
```

## Special Files

### `/wiki/index.md`
Content-oriented catalog listing all wiki pages with:
- Page title and link
- One-line summary
- Metadata (date last updated, source count, tags)
- Organized by category (entities, concepts, sources, topics)
- Auto-updated by LLM on every ingest/query/lint operation

### `/wiki/log.md`
Chronological append-only record:
- Each entry starts with `## [YYYY-MM-DD] operation | Description`
- Examples:
  - `## [2026-05-12] ingest | NN/g Article on Usability Testing`
  - `## [2026-05-12] query | Best practices for mobile navigation`
  - `## [2026-05-12] lint | Found contradiction between two pages on color contrast`
- LLM updates this on every operation

## Human-LLM Division of Labor

**Human Responsibilities:**
- Curating and adding new raw sources to `/raw/`
- Directing analysis by asking meaningful questions
- Providing feedback on LLM-generated content
- Making final judgments on conflicting information
- Overall guidance and goal-setting

**LLM Responsibilities:**
- Reading and understanding new sources
- Generating and updating wiki pages
- Maintaining cross-references and consistency
- Synthesizing answers from the wiki
- Performing maintenance tasks (linting)
- Filing valuable insights back into the wiki
- All bookkeeping, filing, and maintenance work

## Implementation Notes

- Start by treating existing content as initial raw sources
- LLM will process these to generate the initial wiki in `/wiki/`
- Going forward, new sources go to `/raw/` and LLM updates `/wiki/`
- The wiki (`/wiki/`) is the primary interface for querying and learning
- Raw sources (`/raw/`) remain as immutable reference material