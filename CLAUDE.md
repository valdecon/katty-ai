# CLAUDE.md

This file provides guidance for AI assistants (Claude Code and similar tools) working in this repository.

## Project Overview

**katty-ai** is a project in its earliest stages. As of the initial commit, no technology stack, source code, or configuration has been established. This document will be updated as the project evolves.

- **Repository**: `valdecon/katty-ai`
- **Owner**: valdecon <roman.beni@hotmail.com>

## Current State

The repository contains only:
- `README.md` — project title placeholder
- `CLAUDE.md` — this file

No language, framework, dependencies, or source structure have been chosen yet.

## Git Workflow

### Branch Naming

Feature branches follow the pattern:
```
claude/<description>-<random-suffix>
```

Example: `claude/add-claude-documentation-eW7Rd`

### Development Branches

Always develop on the designated feature branch. Never push directly to `main` without explicit instruction.

### Commit Style

Use clear, descriptive commit messages in the imperative mood:
- `Add initial project structure`
- `Fix authentication bug in login handler`
- `Update CLAUDE.md with new conventions`

### Push Workflow

Always push with upstream tracking:
```bash
git push -u origin <branch-name>
```

Retry on network failure with exponential backoff (2s, 4s, 8s, 16s — max 4 retries).

## Conventions for AI Assistants

### General Principles

- Read files before modifying them
- Prefer editing existing files over creating new ones
- Do not add features or refactoring beyond what is explicitly requested
- Do not add comments unless logic is genuinely non-obvious
- Do not add error handling for impossible scenarios
- Do not speculate about future requirements — implement only what is asked

### Security

- Never introduce command injection, XSS, SQL injection, or other OWASP Top 10 vulnerabilities
- Validate only at system boundaries (user input, external APIs)
- Never commit secrets, credentials, or `.env` files

### File Creation

Only create files when strictly necessary. Do not create documentation (`.md`) files unless explicitly requested.

### Code Quality

- Match the style and conventions of surrounding code
- Do not add type annotations, docstrings, or comments to code you did not change
- Do not introduce backwards-compatibility shims for unused code paths
- Three similar lines of code is better than a premature abstraction

## Updating This File

This file should be updated whenever:
- A technology stack is chosen (add setup and run instructions)
- Project structure is established (add directory descriptions)
- Build, test, or deploy workflows are defined (add commands)
- New conventions are agreed upon (document them here)

The goal is to keep this file accurate and useful — not exhaustive.
