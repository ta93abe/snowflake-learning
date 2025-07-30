# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev presentation project for Snowflake learning materials. Slidev is a markdown-based presentation framework designed for developers that combines Vue.js components with slide content.

## Development Commands

- **Install dependencies**: `pnpm install`
- **Start dev server**: `pnpm dev` (opens at http://localhost:3030)
- **Build for production**: `pnpm build`  
- **Export slides**: `pnpm export` (exports to PDF, PPTX, PNG, or static site)

## Architecture

### Slide Content
- **Main slides**: `slides.md` - Primary presentation content in Markdown with YAML frontmatter
- **Imported slides**: `pages/imported-slides.md` - Additional slide content that can be imported
- Slides support Vue components, animations, LaTeX, diagrams (Mermaid/PlantUML), and interactive elements

### Components
- **Custom components**: `components/` directory contains Vue SFC components usable in slides
- **Counter.vue**: Example interactive counter component demonstrating Vue integration in slides
- Components use UnoCSS utility classes for styling

### Code Snippets
- **External code**: `snippets/external.ts` - Reusable TypeScript code that can be imported into slides using `<<< @/snippets/external.ts#snippet` syntax
- Supports code highlighting, TypeScript hover information, and live coding features

### Configuration
- **Theme**: Currently using `seriph` theme (configurable in slides.md frontmatter)
- **Deployment**: Configured for both Netlify (`netlify.toml`) and Vercel (`vercel.json`)
- **Package manager**: Uses pnpm with lockfile

## Key Features
- Markdown-based slides with Vue component integration
- Built-in code highlighting with TypeScript support
- Interactive elements and animations
- Diagrams and LaTeX support  
- Multiple export formats
- Live development with hot reload