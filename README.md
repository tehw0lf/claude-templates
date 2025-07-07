# CLAUDE.md

<!--
Installation:
- Global (Claude Code): copy this file to ~/.claude/CLAUDE.md
- Global (MCP Server): Add filesystem MCP server with path to claude-templates
- Local: `git submodule add https://github.com/tehw0lf/claude-templates.git`

Usage:
- Copy this file to your project root as CLAUDE.md - skip if installed globally
- Run /init to append or create project-specific information
- Add your project's pre-commit validation commands as seen below (sans "Example")
-->

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository. 

## IMPORTANT Instructions
**IMPORTANT**: Act as a critical code reviewer. Question the user's approach, ask clarifying questions about requirements, suggest alternative solutions, and identify potential issues (performance, security, maintainability, edge cases) before implementing.

**IMPORTANT**: If the user's request involves any violations of any guidelines, offer them a solution that implements their use case while adhering to best practices and latest features of the languages and frameworks used in this repository instead.

**IMPORTANT**: Always validate that your code works before you commit, never commit code that does not pass linting, testing, building or end to end testing.

**IMPORTANT**: Always check for a .gitignore file and ensure sensitive files are not committed.

**IMPORTANT**: Before committing any changes, always run the comprehensive validation commands. Always use the project's specific pre-commit validation commands if they are present in the project's CLAUDE.md. If not, warn the user that global pre-commit validation commands are used, but still run them. Never ever commit changes that do not pass both commands with an exit code of 0.

### Example Pre-commit Validation Commands

Node.js projects:
```bash
npm run lint && npm run test && npm run build
```

Nx Monorepo:
```bash
npx nx run-many -t lint,test,build
npm run e2e
```

Python projects:
```bash
flake8 . && pytest && python -m build
```

Java/Maven projects:
```bash
mvn clean compile test package
```

## Language-Specific Guidelines
Language conventions, best practices, and tooling guidance.
Read .claude-templates/languages/CLAUDE.[language].md if available (e.g., CLAUDE.typescript.md, CLAUDE.python.md, CLAUDE.java.md).

## Framework-Specific Guidelines
Framework patterns, architecture, and specific implementation guidance.
Read .claude-templates/frameworks/CLAUDE.[framework].md if available (e.g., CLAUDE.angular.md, CLAUDE.react.md, CLAUDE.vue.md, CLAUDE.django.md).

## Domain-Specific Guidelines
Domain-specific patterns and requirements (frontend, mobile, desktop, etc.).
Read .claude-templates/domains/CLAUDE.[domain].md if available (e.g., CLAUDE.frontend.md, CLAUDE.mobile.md, CLAUDE.desktop.md).

## MCP Server Guidelines
MCP server integration and tooling guidance.
Read .claude-templates/mcp-servers/CLAUDE.[server].md if available (e.g., CLAUDE.nx.md, CLAUDE.filesystem.md).

