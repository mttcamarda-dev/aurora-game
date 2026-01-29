# CLAUDE.md - Aurora Game

This file provides guidance for AI assistants working with the Aurora Game codebase.

## Project Overview

Aurora Game is a game project. This repository is currently in its initial setup phase.

## Repository Structure

```
aurora-game/
├── CLAUDE.md          # AI assistant guidelines (this file)
└── (project files to be added)
```

## Development Setup

### Prerequisites

- Node.js (recommended: LTS version)
- npm or yarn package manager
- Git

### Getting Started

```bash
# Clone the repository
git clone <repository-url>
cd aurora-game

# Install dependencies (once package.json is added)
npm install

# Start development server (once configured)
npm run dev
```

## Development Workflow

### Branch Naming Convention

- Feature branches: `feature/<description>`
- Bug fixes: `fix/<description>`
- AI-assisted development: `claude/<session-id>`

### Commit Message Guidelines

Use clear, descriptive commit messages:
- `feat: add new game feature`
- `fix: resolve collision detection bug`
- `refactor: improve rendering performance`
- `docs: update README`
- `test: add unit tests for player module`

### Code Style

- Use consistent indentation (2 or 4 spaces, to be determined)
- Follow established patterns in the codebase
- Write clear, self-documenting code
- Add comments only when logic isn't self-evident

## Testing

Run tests with:
```bash
npm test
```

## Building

Build for production:
```bash
npm run build
```

## Key Conventions for AI Assistants

1. **Read before modifying**: Always read existing files before making changes
2. **Minimal changes**: Make focused, targeted changes without over-engineering
3. **Security first**: Avoid introducing vulnerabilities (XSS, injection, etc.)
4. **Test changes**: Run tests after modifications when applicable
5. **Follow patterns**: Match existing code style and conventions
6. **No unnecessary files**: Don't create files unless absolutely necessary

## Project Status

This project is newly initialized. Update this document as the codebase develops with:
- Actual directory structure
- Framework-specific conventions
- Build and deployment procedures
- API documentation
- Game-specific architecture details

---

*Last updated: 2026-01-29*
