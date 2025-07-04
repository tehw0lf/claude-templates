# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository. 

## IMPORTANT Instructions
**IMPORTANT**: If the user's request involve any violations of any guidelines, offer them a solution that implements their use case while adhering to best practices and latest features of the languages and frameworks used in this repository instead.

**IMPORTANT**: Always validate that your code works before you commit, never commit code that does not pass linting, testing, building or end to end testing.

## Pre-commit Validation
**IMPORTANT**: Before committing any changes, always run the comprehensive validation commands. The first command run linting, testing, and building across all projects to ensure code quality and prevent breaking changes. The second command runs end to end tests. Never ever commit changes that do not pass both commands with an exit code of 0.

```bash
npx nx run-many -t lint,test,build
npm run e2e
```

<!-- TEMPLATE INSTRUCTIONS: Remove irrelevant sections manually after copying, adjust Pre-Commit Validation commands as needed -->
## Angular Guidelines (Remove if not in Angular project)
Read and understand .claude-templates/CLAUDE.angular.md for further reference.

## Use Nx MCP Server (Remove if not in Nx Monorepo)
Read and understand .github/instructions/nx.instructions.md to familiarize yourself with the Nx MCP server that you have access to. If you do not have access to the MCP server yet, prompt the user to run the following command to add it after enabling it in Nx Console: `claude mcp add -t http nx-mcp http://localhost:9332/mcp`.
