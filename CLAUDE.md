# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**真理之剑** (Truth's Sword) is a personal blog focused on AI research and independent product development. Built with VitePress, it serves as a static site generator for technical content in Chinese.

## Development Commands

```bash
# Start development server (http://localhost:5173)
npm run docs:dev

# Build for production
npm run docs:build

# Preview production build locally
npm run docs:preview
```

## Architecture

### Tech Stack
- **VitePress 1.6+**: Vue 3-based static site generator
- **TypeScript**: Configuration files use `.mts` extension
- **Markdown**: Content authored in Markdown with Vue component support

### Directory Structure
```
docs/
├── .vitepress/
│   └── config.mts          # Site configuration (title, nav, sidebar, social links)
├── index.md                # Homepage
├── markdown-examples.md    # Markdown feature demos
└── api-examples.md         # Runtime API examples
```

### Site Configuration
- Primary language: Chinese (content and UI)
- Navigation and sidebar configured in `docs/.vitepress/config.mts`
- Uses VitePress default theme with custom GitHub social link

## Speckit Framework Integration

This project uses the Speckit methodology for structured development. Custom slash commands are available:

- `/speckit.specify` - Create feature specifications from natural language descriptions
- `/speckit.plan` - Generate implementation plans with design artifacts
- `/speckit.tasks` - Create executable, dependency-sorted tasks.md files
- `/speckit.implement` - Execute implementation plans by processing tasks.md
- `/speckit.clarify` - Ask targeted clarification questions to improve spec completeness
- `/speckit.analyze` - Perform cross-artifact consistency and quality analysis
- `/speckit.checklist` - Generate custom checklists based on requirements
- `/speckit.constitution` - Create/update project charters
- `/speckit.taskstoissues` - Convert tasks to GitHub issues

Feature branches follow the pattern: `<number>-<short-name>` (e.g., `1-user-auth`).

## Content Conventions

- Blog content is in Chinese
- Technical documentation and code comments in English
- Use VitePress frontmatter for page metadata
- Follow VitePress Markdown syntax for embedding Vue components
