# CLAUDE.md

<!--
Installation:
Global use (Claude Code only): add `export CLAUDE_ADDITIONAL_DIRS="/path/to/claude-templates"` to your shell run configuration.
Global use with MCP Server (Claude Code & Claude Desktop): 
  {
    "mcpServers": {
      "filesystem": {
        "command": "npx",
        "args": [
          "-y",
          "@modelcontextprotocol/server-filesystem",
          "/path/to/claude-templates",
        ]
      }
    }
  }

Local use: `git submodule init https://github.com/tehw0lf/claude-templates.git`

Usage:
Local use only: Copy .claude-templates/README.md (this file) to your project's root directory as CLAUDE.md when using as submodule
Run /init to let Claude append project specific information to CLAUDE.md
Add pre-commit validation commands for your project to CLAUDE.md
-->

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository. 

## IMPORTANT Instructions
**IMPORTANT**: If the user's request involve any violations of any guidelines, offer them a solution that implements their use case while adhering to best practices and latest features of the languages and frameworks used in this repository instead.

**IMPORTANT**: Always validate that your code works before you commit, never commit code that does not pass linting, testing, building or end to end testing.

**IMPORTANT**: Always check for a .gitignore file and ensure sensitive files are not committed.

**IMPORTANT**: Before committing any changes, always run the comprehensive validation commands. Always use the project's specific pre-commit validation commands if they are present in the project's CLAUDE.md. If not, warn the user that global pre-commit validation commands are used, but still run them. Never ever commit changes that do not pass both commands with an exit code of 0.

### Pre-commit Validation Commands
Always use the project's specific pre-commit validation commands if they are present in the project's CLAUDE.md. If not available, use appropriate commands for the project's ecosystem.

Example validation commands for Node.js projects:
```bash
npm run lint && npm run test && npm run build
```

Example validation commands for an Nx Monorepo. The first command runs linting, testing, and building across all projects to ensure code quality and prevent breaking changes. The second command runs end to end tests.

```bash
npx nx run-many -t lint,test,build
npm run e2e
```

## Language-Specific Guidelines
Read and understand .claude-templates/languages/CLAUDE.[language].md for language-specific guidance if available (e.g., CLAUDE.typescript.md, CLAUDE.python.md, CLAUDE.java.md).

## Framework-Specific Guidelines
Read and understand .claude-templates/frameworks/CLAUDE.[framework].md for framework-specific guidance if available (e.g., CLAUDE.angular.md, CLAUDE.react.md, CLAUDE.vue.md, CLAUDE.django.md).

## Domain-Specific Guidelines
Read and understand .claude-templates/domains/CLAUDE.[domain].md for domain-specific guidance if available (e.g., CLAUDE.frontend.md, CLAUDE.mobile.md, CLAUDE.desktop.md).

## MCP Server Guidelines
Read and understand .claude-templates/mcp-servers/CLAUDE.[server].md for MCP server-specific guidance if available (e.g., CLAUDE.nx.md, CLAUDE.filesystem.md).

