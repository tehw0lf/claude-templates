# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

<!-- TEMPLATE INSTRUCTIONS: Remove irrelevant sections manually after copying, adjust Pre-Commit Validation as needed -->
## Angular Guidelines (Remove if not in Angular project)
Read and understand .claude-templates/CLAUDE.angular.md for further reference.

## Use Nx MCP Server (Remove if not in Nx Monorepo)
Read and understand .github/instructions/nx.instructions.md to familiarize yourself with the Nx MCP server that you have access to. If you do not have access to the MCP server yet, prompt the user to run the following command to add it after enabling it in Nx Console: `claude mcp add -t http nx-mcp http://localhost:9332/mcp`.

## Pre-commit Validation
**IMPORTANT**: Before committing any changes, always run the comprehensive validation commands:
```bash
npx nx run-many -t lint,test,build
```
This command runs linting, testing, and building across all projects to ensure code quality and prevent breaking changes.

For e2e tests, run:
```bash
npm run e2e
```