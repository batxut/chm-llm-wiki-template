# LLM Wiki Template

A structured knowledge base framework for **Obsidian + Claude Code (LLM Agent)**.

This template provides the schema (`CLAUDE.md`) and directory structure to turn an Obsidian vault into an LLM-maintained wiki — where you curate sources, and the LLM handles summarization, cross-referencing, and incremental updates.

## Quick Start

1. **Clone or fork** this repository
2. **Open in Obsidian** as a vault
3. **Configure Claude Code** in this directory
4. Follow the workflows in `CLAUDE.md`:
   - **Ingest** — drop a source into `原始资料/`, tell the LLM to process it
   - **Query** — ask questions against the wiki
   - **Lint** — periodically health-check the wiki

## Prerequisites

- [Obsidian](https://obsidian.md)
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) or any LLM agent

## Recommended Plugins

| Plugin | Purpose |
|--------|---------|
| Obsidian Git | Auto-commit and sync |
| Local Images Plus | Download external images locally |
| Marp Slides | Generate presentations from wiki content |
| Dataview | Dynamic queries over frontmatter |

## Structure

```
CLAUDE.md              # Schema — defines how the LLM maintains the wiki
原始资料/              # Source documents (LLM read-only, you manage manually)
知识库/                # Wiki content (LLM maintains)
├── 来源/              # Source summaries
├── 概念/              # Concept pages
├── 实体/              # Entity pages (people, organizations, products)
├── 对比/              # Comparisons and analysis
├── 媒体/              # Media files (copied from sources)
├── index.md           # Content index
├── 领域索引.md         # MOC by knowledge domain
└── log.md             # Operation log
```

## License

MIT
