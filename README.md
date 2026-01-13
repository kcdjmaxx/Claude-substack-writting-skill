# Substack Writing Assistant

A [Claude Code](https://claude.ai/code) skill that helps writers craft Substack articles. It provides structure, synthesis, and feedback—without writing the article for you.

## Philosophy

This skill empowers writers rather than replacing them. It will:
- Synthesize your research into usable themes
- Generate outlines and structure suggestions
- Propose headlines and CTAs
- Provide editorial feedback on your drafts

It will **never** write your article for you.

## Installation

1. Create a `.claude/skills/` directory in your project
2. Copy `SKILL.md` into that directory
3. The skill will be available as `/substack` in Claude Code

```
your-project/
└── .claude/
    └── skills/
        └── substack/
            └── SKILL.md
```

## Usage

### Commands

| Command | Description |
|---------|-------------|
| `/substack new <name>` | Create a new article directory structure |
| `/substack research` | Synthesize all materials in `research/` folder |
| `/substack outline` | Generate a detailed outline from research |
| `/substack structure` | Get article format recommendations |
| `/substack headlines` | Generate title and subtitle options |
| `/substack edit` | Get editorial feedback on your draft |

### Workflow

```
1. /substack new "my-article"
2. Add notes, sources, and quotes to research/
3. /substack research
4. /substack structure (optional)
5. /substack outline
6. Write your draft in draft.md
7. /substack headlines
8. /substack edit
9. Revise and publish
```

### Directory Structure

Each article gets its own directory:

```
my-article/
├── research/        # Your source material (skill reads from here)
│   ├── notes.md
│   ├── sources.md
│   └── quotes.md
├── outline.md       # Generated outline
└── draft.md         # Your writing
```

## Features

### Research Synthesis
Reads all markdown files in your `research/` directory and extracts:
- Core themes and arguments
- Key points with source references
- Usable quotes and statistics
- Gaps and questions to address
- Potential angles for the article

### Outline Generation
Creates a dual-format outline with:
- Suggested thesis/angle
- Multiple hook options
- Section-by-section breakdown with purpose, bullet points, and narrative flow
- Evidence mapping from your research
- CTA options for the closing

### Headline Options
Generates 5-10 title options across styles:
- Direct/Clear
- Curiosity/Hook
- Bold Claim

Each paired with a subtitle (email preview text) and engagement notes.

### Editorial Feedback
Provides developmental feedback without rewriting:
- Strengths to keep developing
- Structure and flow observations
- Clarity questions (not answers)
- Energy drop identification
- Generic phrasing alerts
- Voice pattern notes

## Requirements

- [Claude Code](https://claude.ai/code) CLI

## License

MIT License - see [LICENSE](LICENSE) for details.

## Contributing

Contributions welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## Author

Max Ross
