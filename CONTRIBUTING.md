# Contributing to Demo

Thank you for your interest in contributing to the Demo project! We welcome contributions from everyone. This document provides guidelines and instructions for contributing.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Making Changes](#making-changes)
- [Committing Your Changes](#committing-your-changes)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Code Style Guidelines](#code-style-guidelines)
- [Testing](#testing)
- [Documentation](#documentation)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inspiring community for all. Please read and adhere to our code of conduct:

- **Be Respectful**: Treat all contributors with respect and kindness
- **Be Inclusive**: Welcome people of all backgrounds and experiences
- **Be Professional**: Keep discussions constructive and focused on the project
- **Be Collaborative**: Work together to solve problems and improve the project

### Unacceptable Behavior

- Harassment, bullying, or discrimination
- Offensive language or personal attacks
- Spam or self-promotion
- Sharing private information without consent

## Getting Started

### Prerequisites

- Git installed and configured
- Node.js v14+ or Python 3.8+
- Basic command-line knowledge
- A GitHub account

### Fork and Clone

1. **Fork the repository** by clicking the "Fork" button on GitHub
2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/demo.git
   cd demo
   ```

3. **Add upstream remote**
   ```bash
   git remote add upstream https://github.com/Mr-mtweve/demo.git
   ```

## Development Workflow

### Create a Feature Branch

```bash
# Update your local repository
git fetch upstream
git checkout upstream/main

# Create a new branch
git checkout -b feature/your-feature-name
# or for bug fixes
git checkout -b bugfix/issue-description
```

### Branch Naming Convention

- `feature/feature-name` - For new features
- `bugfix/issue-description` - For bug fixes
- `docs/description` - For documentation updates
- `test/test-description` - For test additions

## Making Changes

### 1. Code Structure

Keep your changes:
- Small and focused on a single issue
- Well-organized and easy to understand
- Free of unnecessary comments (code should be self-documenting)

### 2. Write Clear Code

```javascript
// ✅ Good: Clear variable names and logic
function calculateTotalPrice(items) {
  return items.reduce((total, item) => total + item.price, 0);
}

// ❌ Bad: Unclear variable names
function calc(x) {
  return x.reduce((a, b) => a + b.p, 0);
}
```

## Committing Your Changes

### Commit Message Format

We follow the Conventional Commits specification:

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- `feat` - A new feature
- `fix` - A bug fix
- `docs` - Documentation changes
- `style` - Code style changes (formatting, semicolons, etc.)
- `refactor` - Code refactoring without adding features or fixing bugs
- `test` - Adding or updating tests
- `chore` - Maintenance tasks, dependency updates

### Examples

```bash
git commit -m "feat(auth): add user login functionality"
git commit -m "fix(ui): resolve button alignment issue"
git commit -m "docs: update installation instructions"
git commit -m "test: add unit tests for auth module"
```

## Submitting a Pull Request

### Before Submitting

1. **Update your branch with latest upstream changes**
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

2. **Run tests locally**
   ```bash
   npm test
   # or
   python -m pytest
   ```

3. **Ensure code follows style guidelines**

### Creating a Pull Request

1. **Push your branch to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

2. **Open a Pull Request** on GitHub with:
   - Clear title describing the change
   - Detailed description of what was changed and why
   - Reference to any related issues (e.g., "Fixes #123")
   - Screenshots for UI changes (if applicable)

### Pull Request Template

```markdown
## Description
Brief description of the changes

## Type of Change
- [ ] New feature
- [ ] Bug fix
- [ ] Documentation update
- [ ] Other

## Related Issues
Fixes #123

## How to Test
Steps to verify the changes

## Screenshots (if applicable)
Add screenshots here

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex logic
- [ ] Documentation updated
- [ ] Tests added/updated
- [ ] All tests passing
```

## Code Style Guidelines

### General Rules

- Use consistent indentation (2 or 4 spaces)
- Keep lines under 100 characters
- Use meaningful variable and function names
- Add comments for complex logic
- Remove console.log and debug code before submitting

### Example

```javascript
// ✅ Good style
function validateEmail(email) {
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return emailRegex.test(email);
}

// ❌ Bad style
function vE(e){return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(e);}
```

## Testing

### Writing Tests

- Write tests for new features
- Update tests when changing existing code
- Aim for >80% code coverage
- Use clear, descriptive test names

### Running Tests

```bash
# Run all tests
npm test

# Run tests in watch mode
npm test -- --watch

# Run tests with coverage
npm test -- --coverage
```

## Documentation

### Updating Documentation

- Update README.md for major changes
- Add inline comments for complex code
- Document new features and APIs
- Include examples where applicable

### Documentation Format

```markdown
### Feature Name

Brief description of the feature.

**Usage:**
```
code example
```

**Parameters:**
- `param1` - Description

**Returns:**
Description of return value
```

## Reporting Bugs

### Before Reporting

- Check if the bug has already been reported
- Try to reproduce it consistently
- Gather relevant information

### Bug Report Template

**Title:** Brief description of the bug

**Environment:**
- OS: [e.g., Windows 10, macOS]
- Browser: [e.g., Chrome, Firefox]
- Version: [e.g., 1.0.0]

**Description:**
Clear description of what went wrong

**Steps to Reproduce:**
1. Step 1
2. Step 2
3. Step 3

**Expected Behavior:**
What should happen

**Actual Behavior:**
What actually happened

**Screenshots:**
Add screenshots if helpful

## Suggesting Enhancements

### Enhancement Proposal Template

**Title:** Brief description of the enhancement

**Problem:**
What problem does this solve?

**Proposed Solution:**
How should this be implemented?

**Alternatives:**
Other solutions you've considered

**Additional Context:**
Any additional information

## Getting Help

- 💬 Open a discussion for questions
- 📧 Email: contact@example.com
- 📖 Check the documentation
- 🔍 Search existing issues and discussions

## Review Process

1. Automated tests must pass
2. Code review by maintainers
3. Address feedback and make changes
4. Final approval and merge

## Recognition

Contributors will be recognized in:
- README.md contributors section
- Release notes
- GitHub contributors page

---

**Thank you for contributing to Demo!** 🎉

If you have questions, feel free to open an issue or reach out to the maintainers.
