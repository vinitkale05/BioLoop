# 🤝 Contributing to BioLoop

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to this project.

---

## 📋 Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [How to Contribute](#how-to-contribute)
3. [Development Setup](#development-setup)
4. [Commit Guidelines](#commit-guidelines)
5. [Pull Request Process](#pull-request-process)
6. [Coding Standards](#coding-standards)
7. [Testing](#testing)

---

## 📜 Code of Conduct

- Be respectful and inclusive
- Welcome diverse perspectives
- Report issues constructively
- Focus on the code, not the person

---

## 🎯 How to Contribute

### Types of Contributions

✅ **Bug Reports**: Found a bug? Report it with details
✅ **Feature Requests**: Have an idea? Suggest it
✅ **Code Improvements**: Optimize, refactor, improve
✅ **Documentation**: Improve README, add examples, fix typos
✅ **Tests**: Increase test coverage
✅ **Performance**: Optimize code and reduce bundle size

---

## 🛠️ Development Setup

### Prerequisites
- Node.js v18+
- npm or yarn
- Git

### Local Setup

```bash
# 1. Fork and clone the repo
git clone https://github.com/vinitkale05/BioLoop.git
cd BioLoop

# 2. Add upstream remote
git remote add upstream https://github.com/karand07/BioLoop.git

# 3. Create feature branch
git checkout develop
git checkout -b feature/your-feature-name

# 4. Install dependencies
npm install

# 5. Start development
npm run dev
```

---

## 📝 Commit Guidelines

### Format
```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Code style (formatting, semicolons, etc.)
- `refactor`: Code refactoring
- `perf`: Performance improvement
- `test`: Adding/updating tests
- `chore`: Build, dependencies, tooling

### Examples

```
feat(auth): Add JWT token refresh mechanism
fix(marketplace): Resolve filter dropdown lag
docs(setup): Update installation instructions
refactor(api): Optimize database query performance
test(payment): Add Razorpay integration tests
```

### Commit Message Best Practices

✅ Use imperative mood ("add feature" not "added feature")
✅ Don't capitalize first letter
✅ No period at the end
✅ Limit subject to 50 characters
✅ Keep body to 72 characters per line
✅ Reference issues: "Fixes #123"

---

## 🔄 Pull Request Process

### Before Creating a PR

1. Update your branch with latest changes:
   ```bash
   git fetch upstream
   git merge upstream/main
   ```

2. Ensure code quality:
   ```bash
   npm run lint
   npm run format
   npm test
   ```

3. Update documentation if needed

### Creating a PR

1. Push your feature branch
   ```bash
   git push origin feature/your-feature-name
   ```

2. Create PR with:
   - Clear title describing changes
   - Detailed description of what and why
   - Screenshots for UI changes
   - Link to related issues: "Closes #123"
   - Checklist completed

### PR Description Template

```markdown
## Description
Brief explanation of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Related Issues
Closes #(issue number)

## Screenshots (if applicable)
Add screenshots for UI changes

## Testing
Describe testing performed

## Checklist
- [ ] My code follows style guidelines
- [ ] I have performed self-review
- [ ] I have commented complex logic
- [ ] I have updated documentation
- [ ] My changes have no new warnings
- [ ] I have added tests
```

### PR Review Process

- At least one approval required
- All checks must pass
- No conflicts with base branch
- Discussions resolved constructively

---

## 💻 Coding Standards

### TypeScript
- Use strict mode: `"strict": true`
- Define proper types, avoid `any`
- Use interfaces for objects
- Document complex functions

### React
- Use functional components
- Meaningful component names
- Props destructuring
- Proper hook dependencies

### Naming Conventions
- `PascalCase`: Components, Classes, Interfaces
- `camelCase`: Variables, functions, methods
- `UPPER_SNAKE_CASE`: Constants
- `kebab-case`: File/folder names (except components)

### Code Style
```typescript
// Good
const getUserById = async (id: string): Promise<User> => {
  return await db.users.findById(id);
};

// Bad
const getuserbyid = async (id) => {
  return db.users.findById(id);
};
```

### File Structure
```
src/
├── components/        # Reusable UI components
├── hooks/            # Custom React hooks
├── pages/            # Page components
├── services/         # API services
├── types/            # TypeScript types
├── utils/            # Utility functions
└── constants/        # Constants
```

---

## 🧪 Testing

### Running Tests
```bash
npm test
npm test -- --coverage
```

### Writing Tests
- Test behavior, not implementation
- Use descriptive test names
- Aim for >80% coverage
- Group related tests

### Example Test
```typescript
describe('UserService', () => {
  it('should fetch user by ID', async () => {
    const user = await getUserById('123');
    expect(user.id).toBe('123');
  });
});
```

---

## ✅ Checklist Before Submitting PR

- [ ] Branch created from `develop`
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex logic
- [ ] Documentation updated
- [ ] No console.log or debug code
- [ ] Tests pass locally
- [ ] No merge conflicts
- [ ] Commit messages follow guidelines
- [ ] PR description is clear

---

## 📚 Resources

- [Git Workflow Guide](https://git-scm.com/book/en/v2)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [React Documentation](https://react.dev/)
- [Conventional Commits](https://www.conventionalcommits.org/)

---

## ❓ Questions?

- Check existing issues/discussions
- Open a new discussion for questions
- Ask in PR comments for clarification

---

**Thank you for contributing to BioLoop! 🌱**

