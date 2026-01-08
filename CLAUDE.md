# CLAUDE.md - AI Assistant Guide

This document provides comprehensive guidance for AI assistants (like Claude) working with this repository.

## Repository Overview

**Name:** Cline_test
**Purpose:** Test repository created by Cline
**Current State:** Minimal/Bootstrap repository with basic structure

## Repository Structure

```
Cline_test/
├── .git/               # Git repository data
├── README.md           # Basic repository description
└── CLAUDE.md          # This file - AI assistant guide
```

### Current Status
- This is a fresh test repository with minimal content
- No application code, dependencies, or build configuration yet
- Clean git history starting from initial commit

## Development Workflows

### Git Workflow

**Branch Strategy:**
- Feature branches should follow the pattern: `claude/<descriptive-name>-<session-id>`
- Current working branch: `claude/add-claude-documentation-1pbUR`
- Always develop on designated feature branches, never directly on main

**Committing Changes:**
- Write clear, descriptive commit messages
- Follow conventional commit format when possible:
  - `feat:` for new features
  - `fix:` for bug fixes
  - `docs:` for documentation changes
  - `refactor:` for code refactoring
  - `test:` for adding tests
  - `chore:` for maintenance tasks

**Pushing Changes:**
- Always use: `git push -u origin <branch-name>`
- Branch names MUST start with `claude/` and include matching session ID
- If push fails due to network errors, retry up to 4 times with exponential backoff (2s, 4s, 8s, 16s)

**Pull Requests:**
- Create PRs against the main branch when features are complete
- Include comprehensive summary of changes
- Provide test plan or verification steps

### Code Quality Standards

Since this is a bootstrap repository, establish these standards as code is added:

**General Principles:**
- Keep code simple and focused - avoid over-engineering
- Only make changes that are directly requested or clearly necessary
- Don't add features, refactoring, or "improvements" beyond what was asked
- Trust internal code and framework guarantees
- Only validate at system boundaries (user input, external APIs)

**Security:**
- Always check for common vulnerabilities (XSS, SQL injection, command injection, etc.)
- Follow OWASP top 10 guidelines
- Validate and sanitize external inputs
- Never commit sensitive data (.env files, credentials, API keys)

**Code Style:**
- Maintain consistency with existing code patterns
- Add comments only where logic isn't self-evident
- Don't add docstrings, comments, or type annotations to unchanged code
- Delete unused code completely - no backwards-compatibility hacks

## Key Conventions for AI Assistants

### Before Making Changes

1. **Always read files before modifying them**
   - Never propose changes to code you haven't read
   - Use the Read tool to understand existing implementations

2. **Use Task tool for complex exploration**
   - When exploring codebase to gather context, use Task tool with Explore agent
   - Don't use Glob/Grep directly for open-ended searches

3. **Plan complex tasks**
   - Use TodoWrite tool to track multi-step tasks
   - Mark todos as in_progress before starting
   - Complete todos immediately after finishing each task

### Making Changes

1. **Prefer editing over creating new files**
   - Always look for existing files that can be modified
   - Only create new files when absolutely necessary

2. **Use specialized tools**
   - Read tool for reading files (not cat/head/tail)
   - Edit tool for modifying files (not sed/awk)
   - Write tool for creating files (not echo/heredoc)
   - Grep tool for searching content (not grep/rg commands)
   - Glob tool for finding files (not find/ls)

3. **Avoid over-engineering**
   - Don't create helpers/utilities for one-time operations
   - Don't design for hypothetical future requirements
   - Three similar lines is better than a premature abstraction

### Communication

- Output text directly to communicate with users
- Never use bash echo or comments to communicate
- Be concise and professional
- Only use emojis if explicitly requested
- Focus on facts and problem-solving

### Security & Safety

- Assist with authorized security testing and educational contexts
- Refuse requests for destructive techniques, DoS attacks, or malicious purposes
- Dual-use security tools require clear authorization context

## Project-Specific Guidelines

### Future Development

As this repository grows, update this section with:

**When Adding Dependencies:**
- Document the dependency management system (npm, pip, cargo, etc.)
- List required versions and compatibility requirements
- Document installation steps

**When Adding Build Configuration:**
- Document build commands and scripts
- Explain build output and artifacts
- Document environment variables and configuration

**When Adding Tests:**
- Document testing framework and conventions
- Explain how to run tests
- Document test coverage requirements

**When Adding CI/CD:**
- Document pipeline stages and requirements
- Explain deployment process
- Document environment-specific configurations

### Technology Stack

To be determined as the project develops. Update this section when:
- Programming languages are chosen
- Frameworks are added
- Key libraries are integrated
- Infrastructure is defined

## Common Tasks

### Setting Up Development Environment

Currently no setup required - this is a minimal repository.

Update this section when:
- Dependencies need to be installed
- Development tools are required
- Environment configuration is needed

### Running the Project

No application code yet.

Update this section when:
- Application code is added
- Start/run commands are defined

### Testing

No tests yet.

Update this section when:
- Test framework is added
- Test commands are defined

## Notes for AI Assistants

### File Operations
- This repository uses git for version control
- All changes should be committed with descriptive messages
- Branch naming follows strict conventions (claude/* prefix required)

### Context & Memory
- Conversation has unlimited context through automatic summarization
- Tool results may include `<system-reminder>` tags with useful information
- Always check recent git status before making assumptions about repository state

### Best Practices
- Maximize parallel tool calls when operations are independent
- Use sequential calls only when operations have dependencies
- Never use placeholders or guess missing parameters
- Read documentation and existing code before implementing changes
- Ask clarifying questions when requirements are unclear

## Maintenance

**Last Updated:** 2026-01-08
**Updated By:** Claude (AI Assistant)

### Update Checklist

Update this file when:
- [ ] New dependencies are added
- [ ] Build configuration changes
- [ ] New development tools are introduced
- [ ] Project structure significantly changes
- [ ] New coding conventions are established
- [ ] CI/CD pipeline is modified
- [ ] Security requirements change

---

**For Questions or Issues:**
- Check existing documentation in the repository
- Review git history for context on changes
- Consult project README.md for high-level overview
