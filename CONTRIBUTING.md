# Contributing to GitScope

Thank you for your interest in contributing to GitScope! This document provides guidelines and instructions for contributing.

## Code of Conduct

By participating in this project, you agree to maintain a respectful and inclusive environment for everyone.

## How to Contribute

### Reporting Bugs

1. Check if the bug has already been reported in [Issues](https://github.com/Elomami1976/GitScope/issues)
2. If not, create a new issue with:
   - A clear, descriptive title
   - Steps to reproduce the bug
   - Expected vs actual behavior
   - Browser and OS information
   - Screenshots if applicable

### Suggesting Features

1. Check existing issues and discussions for similar suggestions
2. Create a new issue with the `enhancement` label
3. Describe the feature and its use case
4. Explain why it would be valuable

### Pull Requests

1. **Fork** the repository
2. **Clone** your fork locally
3. **Create a branch** for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. **Make your changes** to `index.html` (remember: single-file app!)
5. **Test locally** by opening `index.html` in a browser
6. **Commit** with a clear message:
   ```bash
   git commit -m "Add: description of your changes"
   ```
7. **Push** to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
8. **Open a Pull Request** against the `main` branch

## Development Guidelines

### Project Structure

```
GitScope/
├── index.html          # The entire app (HTML + CSS + JS)
├── manifest.json       # PWA manifest
├── sw.js              # Service worker for offline support
├── README.md          # Documentation
├── LICENSE            # MIT License
├── CONTRIBUTING.md    # This file
└── *.png              # Favicon files
```

### Code Style

- **JavaScript**: Use vanilla JS only (no frameworks)
- **CSS**: Keep styles in the `<style>` tag within `index.html`
- **HTML**: Semantic markup, accessible elements
- **Comments**: Add comments for complex logic
- **Formatting**: Use consistent 4-space indentation

### Design Guidelines

- Follow the existing dark theme aesthetic
- Accent color: `#e8ff47` (electric yellow-green)
- Background: `#0a0a0f`
- Fonts: Syne (headings) + Space Mono (code/data)
- Maintain responsive design (down to 768px)

### Testing

Before submitting a PR, test:
- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (if available)
- [ ] Mobile responsive view
- [ ] Dark and light theme modes
- [ ] Keyboard navigation
- [ ] Different repository sizes (small, medium, large)

### Commit Message Format

Use clear, descriptive commit messages:
- `Add: new feature description`
- `Fix: bug description`
- `Update: what was updated`
- `Remove: what was removed`
- `Refactor: what was refactored`

## Areas for Contribution

Here are some areas where contributions are welcome:

### Features
- [ ] Additional visualization types
- [ ] More export formats
- [ ] Repository comparison
- [ ] Commit timeline view
- [ ] File content preview
- [ ] GitLab/Bitbucket support

### Improvements
- [ ] Performance optimizations
- [ ] Accessibility enhancements
- [ ] Mobile experience
- [ ] Internationalization (i18n)
- [ ] Better error messages

### Documentation
- [ ] Code comments
- [ ] Usage examples
- [ ] Video tutorials
- [ ] Translations

## Questions?

Feel free to open an issue for any questions about contributing.

Thank you for helping make GitScope better! 🎉
