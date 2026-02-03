# CLAUDE.md - AI Assistant Guidelines

This document provides comprehensive guidelines for AI assistants working on this repository.

## Project Overview

**Repository:** claude-code-test-app
**Type:** Test Application
**Status:** New project (initial setup)

## Repository Structure

```
claude-code-test-app/
├── CLAUDE.md           # AI assistant guidelines (this file)
├── src/                # Source code (to be created)
├── tests/              # Test files (to be created)
├── docs/               # Documentation (to be created)
└── package.json        # Project configuration (to be created)
```

## Development Conventions

### Git Workflow

1. **Branch Naming:**
   - Feature branches: `feature/<description>`
   - Bug fixes: `fix/<description>`
   - AI session branches: `claude/<session-id>`

2. **Commit Messages:**
   - Use clear, descriptive messages
   - Start with a verb (Add, Fix, Update, Remove, Refactor)
   - Keep the first line under 72 characters
   - Reference issue numbers when applicable

3. **Git Operations:**
   - Always use `git push -u origin <branch-name>` for pushing
   - Fetch specific branches when possible: `git fetch origin <branch-name>`
   - Retry failed network operations with exponential backoff (2s, 4s, 8s, 16s)

### Code Style

1. **General Principles:**
   - Write clean, readable code
   - Follow the DRY (Don't Repeat Yourself) principle
   - Keep functions focused and small
   - Use meaningful variable and function names

2. **TypeScript/JavaScript:**
   - Use TypeScript for type safety when applicable
   - Prefer `const` over `let`, avoid `var`
   - Use async/await over raw promises
   - Include proper error handling

3. **Documentation:**
   - Add JSDoc comments to exported functions
   - Keep README.md updated with setup instructions
   - Document API endpoints and interfaces

### Testing

1. **Test Coverage:**
   - Write unit tests for business logic
   - Include integration tests for API endpoints
   - Aim for meaningful coverage, not just metrics

2. **Test Organization:**
   - Place tests in `tests/` or `__tests__/` directories
   - Name test files with `.test.ts` or `.spec.ts` suffix
   - Group related tests using `describe` blocks

### File Organization

1. **Source Code:**
   - Keep related files together
   - Use index files for clean exports
   - Separate concerns (routes, controllers, services, models)

2. **Configuration:**
   - Store environment-specific config in `.env` files
   - Never commit sensitive data (use `.env.example`)
   - Keep configuration centralized

## AI Assistant Guidelines

### Before Making Changes

1. **Read First:** Always read relevant files before modifying them
2. **Understand Context:** Review related files and dependencies
3. **Check Tests:** Ensure existing tests pass before changes
4. **Plan Approach:** Use TodoWrite for complex multi-step tasks

### When Making Changes

1. **Minimal Changes:** Only modify what's necessary for the task
2. **Avoid Over-Engineering:** Keep solutions simple and focused
3. **Security First:** Never introduce vulnerabilities (XSS, SQL injection, etc.)
4. **Preserve Functionality:** Don't break existing features

### After Making Changes

1. **Run Tests:** Verify all tests pass
2. **Verify Build:** Ensure the project builds successfully
3. **Commit Properly:** Use descriptive commit messages
4. **Update Docs:** Keep documentation in sync with code

## Common Commands

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Run tests
npm test

# Build for production
npm run build

# Lint code
npm run lint
```

## Security Guidelines

1. **Input Validation:** Always validate user input
2. **Authentication:** Use secure authentication methods
3. **Secrets:** Never commit secrets, use environment variables
4. **Dependencies:** Keep dependencies updated

## Troubleshooting

### Common Issues

1. **Build Failures:**
   - Check Node.js version compatibility
   - Clear `node_modules` and reinstall
   - Verify TypeScript configuration

2. **Test Failures:**
   - Check for missing environment variables
   - Ensure test database is configured
   - Review recent changes for regressions

3. **Git Issues:**
   - For push failures, retry with exponential backoff
   - Ensure branch name follows conventions
   - Check remote repository accessibility

## Contact and Resources

- **Repository Issues:** Use GitHub Issues for bug reports
- **Documentation:** Check `/docs` directory for detailed guides

---

*Last Updated: 2026-02-03*
*This file should be updated as the project evolves.*
