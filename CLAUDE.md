# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Sentry's documentation site built with Next.js 15, TypeScript, and MDX. The site serves both user-facing documentation and developer documentation with different build configurations.

## Architecture

### Documentation Structure

- **User docs**: `/docs/` - Product documentation for Sentry users
- **Developer docs**: `/develop-docs/` - Internal engineering documentation
- **Platform includes**: `/platform-includes/` - SDK-specific code snippets and configurations
- **Includes**: `/includes/` - Reusable content snippets

### Key Directories

- `/app/` - Next.js 15 App Router pages and API routes
- `/src/` - Core application code
  - `/components/` - React components organized by feature
  - `/mdx/` - MDX processing and remark/rehype plugins
  - `/styles/` - Global styles and Tailwind configuration

### Build Modes

- **User docs**: Default mode for sentry.io/docs
- **Developer docs**: Enabled with `NEXT_PUBLIC_DEVELOPER_DOCS=1`

## Development Commands

### Setup

```bash
make develop  # Install dependencies and setup git hooks
cp .env.example .env.development  # Configure environment
```

### Development

```bash
yarn dev                    # Start user docs dev server
yarn dev:developer-docs     # Start developer docs dev server
yarn dev:minimal           # Start without sidecar services
```

### Build & Deploy

```bash
yarn build                 # Build user docs
yarn build:developer-docs  # Build developer docs
yarn start                 # Start production server
```

### Testing & Linting

```bash
yarn test                  # Run vitest tests
yarn test:ci               # Run tests in CI mode
yarn lint                  # Run all linting
yarn lint:ts              # TypeScript type checking
yarn lint:eslint          # ESLint
yarn lint:prettier        # Prettier formatting
yarn lint:fix             # Auto-fix linting issues
```

### Environment Variables

- `NEXT_PUBLIC_DEVELOPER_DOCS=1` - Enable developer docs mode
- `NEXT_PUBLIC_ALGOLIA_APP_ID` - Algolia search app ID
- `NEXT_PUBLIC_ALGOLIA_SEARCH_KEY` - Algolia search API key
- `NEXT_PUBLIC_SENTRY_DSN` - Sentry DSN for error tracking

## Key Technologies

- **Next.js 15** with App Router
- **TypeScript** with strict configuration
- **MDX** for markdown processing with custom plugins
- **Tailwind CSS** for styling with custom design system
- **Vitest** for testing
- **Yarn** with Volta for Node.js version management

## MDX Processing

The project uses extensive MDX processing with custom remark/rehype plugins:

- `remark-code-tabs.js` - Code tab generation
- `remark-code-title.js` - Code block titles
- `remark-toc-headings.ts` - Table of contents generation
- `remark-variables.js` - Variable substitution
- `rehype-slug.js` - Heading anchor generation

## Platform-Specific Content

Content is organized by platform with dynamic loading:

- Platform definitions in `/src/data/platforms.yml`
- Platform-specific includes in `/platform-includes/`
- Dynamic platform routing in `/app/platform-redirect/`

## Testing

Tests use Vitest with TypeScript support:

- Unit tests for utilities and components
- MDX processing tests
- Platform routing tests

## Deployment

- **Vercel** deployment with custom headers and security policies
- **Codecov** integration for bundle analysis
- **Sentry** integration for error tracking and performance monitoring
