# CLAUDE.md - AI Assistant Guide for Okinawa Peace Tour

**Last Updated:** 2025-11-18
**Project Status:** New/Initial Setup
**Repository:** komedorobou/okinawa-peace-tour

## Project Overview

This repository is for the Okinawa Peace Tour project. As this is a new repository, specific implementation details will be updated as the project develops.

### Project Purpose
The Okinawa Peace Tour project appears to be focused on peace tourism and education related to Okinawa's history and culture.

## Repository Status

**Current State:** Empty repository - no source files yet
**Active Branch:** `claude/claude-md-mi46ffnf2gesx54s-01XTm4JgLpRKqNFyun3KHoX8`

## Codebase Structure

*This section will be updated as the project structure is established.*

### Expected Project Structure
```
okinawa-peace-tour/
├── src/                 # Source code (to be determined)
├── docs/                # Documentation
├── tests/               # Test files
├── public/              # Public assets (if web-based)
├── config/              # Configuration files
├── CLAUDE.md            # This file
├── README.md            # Project documentation
└── package.json         # Dependencies (if Node.js based)
```

## Technology Stack

*To be determined based on project requirements*

Potential technologies:
- **Frontend:** TBD (React, Vue, Next.js, etc.)
- **Backend:** TBD (Node.js, Python, etc.)
- **Database:** TBD
- **Deployment:** TBD

## Development Workflows

### Branch Strategy

**Development Branch:** All AI assistant work should be done on branches with the pattern:
- `claude/claude-md-*` for Claude AI assistant work
- Current working branch: `claude/claude-md-mi46ffnf2gesx54s-01XTm4JgLpRKqNFyun3KHoX8`

**Important Branch Rules:**
1. Always develop on the designated `claude/*` branch
2. Never push directly to main/master without explicit permission
3. All branch names should start with 'claude/' and end with the session ID
4. Use descriptive commit messages

### Git Workflow

**Committing Changes:**
```bash
git add <files>
git commit -m "Clear, descriptive message"
git push -u origin <branch-name>
```

**Push Retry Policy:**
- Use `git push -u origin <branch-name>`
- If push fails due to network errors, retry up to 4 times with exponential backoff (2s, 4s, 8s, 16s)
- Branch must start with 'claude/' and end with matching session ID to avoid 403 errors

**Fetching Updates:**
```bash
git fetch origin <branch-name>
git pull origin <branch-name>
```

### Commit Message Conventions

Follow conventional commits format:
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` Code style changes (formatting, etc.)
- `refactor:` Code refactoring
- `test:` Adding or updating tests
- `chore:` Maintenance tasks

Example: `feat: add tour booking functionality`

## Key Conventions for AI Assistants

### Code Quality Standards

1. **Security First**
   - Always check for security vulnerabilities (XSS, SQL injection, command injection, OWASP Top 10)
   - Never commit secrets, API keys, or credentials
   - Validate and sanitize all user inputs
   - Use environment variables for sensitive configuration

2. **Code Style**
   - Follow the project's established coding style (to be defined)
   - Use consistent naming conventions
   - Write clear, self-documenting code
   - Add comments for complex logic

3. **Testing**
   - Write tests for new features
   - Ensure existing tests pass before committing
   - Aim for meaningful test coverage

4. **Documentation**
   - Update documentation when making changes
   - Use clear function/class documentation
   - Keep README.md current
   - Update this CLAUDE.md as project evolves

### Task Management

When working on tasks:

1. **Use TodoWrite Tool**
   - Create todos for multi-step tasks
   - Mark tasks as in_progress when starting
   - Mark completed immediately when done
   - Only have ONE task in_progress at a time

2. **Planning**
   - For complex tasks, create a plan before coding
   - Break down large features into smaller tasks
   - Research existing code patterns first

3. **Code References**
   - Use `file_path:line_number` format when referencing code
   - Example: "Error handling in src/utils/api.ts:42"

### Tool Usage Guidelines

**File Operations:**
- Use `Read` for reading files (not cat/head/tail)
- Use `Edit` for editing files (not sed/awk)
- Use `Write` for creating new files (not echo/heredoc)
- Use `Glob` for finding files by pattern
- Use `Grep` for searching file contents

**Exploration:**
- Use `Task` tool with `subagent_type=Explore` for codebase exploration
- Use specialized agents for complex multi-step tasks
- Run independent tasks in parallel when possible

**Communication:**
- Output text directly to communicate with users
- Never use bash echo or comments to communicate
- Be concise and clear
- Avoid emojis unless explicitly requested

## Project-Specific Guidelines

*This section will be updated as project-specific patterns emerge.*

### Naming Conventions
*To be established based on chosen technology stack*

### File Organization
*To be established as project structure develops*

### API Patterns
*To be documented when API is implemented*

### State Management
*To be documented if applicable*

### Testing Patterns
*To be established with test framework*

## Development Setup

*To be documented when development environment is established*

### Prerequisites
- Git
- (Additional tools TBD)

### Installation Steps
```bash
# Clone the repository
git clone <repository-url>
cd okinawa-peace-tour

# Install dependencies (TBD)
# npm install / pip install -r requirements.txt / etc.

# Setup environment
# cp .env.example .env

# Run development server (TBD)
# npm run dev / python manage.py runserver / etc.
```

### Environment Variables
*To be documented when configuration is established*

## Common Tasks

### Adding a New Feature
1. Create/checkout feature branch
2. Use TodoWrite to plan the feature
3. Implement with tests
4. Update documentation
5. Commit with clear message
6. Push to remote branch

### Fixing a Bug
1. Identify and reproduce the issue
2. Write a failing test (if applicable)
3. Fix the bug
4. Verify test passes
5. Commit with `fix:` prefix

### Updating Documentation
1. Make changes to relevant docs
2. Ensure accuracy and clarity
3. Update this CLAUDE.md if workflows change
4. Commit with `docs:` prefix

## Deployment

*To be documented when deployment process is established*

## Troubleshooting

### Common Issues

**Git Push Fails with 403:**
- Ensure branch name starts with 'claude/' and ends with session ID
- Check network connectivity
- Retry with exponential backoff

**Empty Repository:**
- This is a new project - structure will be established based on requirements
- Consult with user on technology choices and project setup

## Resources

### Documentation
- Project README: README.md (to be created)
- API Docs: (TBD)
- Architecture Docs: (TBD)

### External Resources
- Okinawa Peace Memorial Museum: https://www.peace-museum.pref.okinawa.jp/
- (Additional resources TBD)

## Updates and Maintenance

### Updating This Document

When making significant changes to the project:
1. Update relevant sections in CLAUDE.md
2. Add update date at the top
3. Document new patterns, conventions, or workflows
4. Remove outdated information

### Regular Reviews
- Review CLAUDE.md when project structure changes
- Update after major feature additions
- Keep technology stack section current
- Ensure examples reflect current codebase

## Notes for Future Development

**Initial Setup Considerations:**
- Determine primary technology stack and framework
- Establish code style and linting rules
- Set up CI/CD pipeline
- Configure testing framework
- Establish database schema (if applicable)
- Define API structure (if applicable)
- Create documentation structure
- Set up development environment
- Define deployment strategy

**Questions to Address:**
- What is the primary purpose of the tour? (Historical education, tourism booking, information portal, etc.)
- Who is the target audience?
- What features are essential for MVP?
- What languages should be supported? (Japanese, English, etc.)
- What platforms need to be supported? (Web, mobile, etc.)

---

**For AI Assistants:** This document should be your first reference when working on this project. Always check here for conventions, workflows, and project-specific guidelines. Update this document as you learn more about the project structure and patterns. When in doubt, ask the user for clarification rather than making assumptions.
