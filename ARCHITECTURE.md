# AI Summarizer - Architecture Documentation

## Overview

AI Summarizer is a WordPress Gutenberg block plugin that provides AI-powered summarize button groups with flexible layouts and advanced styling capabilities. Built following WordPress Core Contributor guidelines and modern block development standards, the plugin offers seamless integration with the WordPress block editor.

## Table of Contents

2. [Plugin Structure](#plugin-structure)
3. [Contributing](#contributing)
4. [Resources](#resources)


---

## Plugin Structure

### Directory Layout

```
ai-summarizer/
├── ai-summarizer.php           # Main plugin file (entry point)
├── package.json                # NPM dependencies and scripts
├── webpack.config.js           # Custom webpack configuration
├── LICENSE                     # GPL-2.0-or-later license
├── README.md                   # User-facing documentation
├── ARCHITECTURE.md             # This file
│
├── src/                        # Source files (uncompiled)
│   ├── admin/                  # Admin settings (future)
│   │   └── index.js
│   └── blocks/                 # Block source files
│       ├── tests/              # Unit and integration tests
│       │   └── index.js
│       └── summarize-button/   # Summarize Button block
│           ├── block.json      # Block metadata (schema)
│           ├── index.js        # Block registration
│           ├── edit.js         # Editor component (React)
│           ├── save.js         # Frontend save function
│           ├── view.js         # Frontend interactivity (JS)
│           ├── transforms.js   # Block transformations
│           ├── deprecated.js   # Deprecated versions
│           ├── style.scss      # Frontend & editor styles
│           └── editor.scss     # Editor-only styles
```

### File Responsibilities

| File | Purpose |
|------|---------|
| `ai-summarizer.php` | Plugin initialization, block registration via manifest |
| `block.json` | Block metadata, attributes, supports configuration |
| `index.js` | Block type registration with React components |
| `edit.js` | Editor UI component (what users see in Block Editor) |
| `save.js` | Frontend markup generation (saved to post_content) |
| `view.js` | Frontend JavaScript for interactivity (loaded on frontend) |
| `transforms.js` | Block-to-block transformation rules |
| `deprecated.js` | Legacy block versions for backward compatibility |

---

## Contributing

### Development Workflow

1. Fork repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Make changes and test thoroughly
4. Run linters: `npm run lint:js && npm run lint:css`
5. Format code: `npm run format`
6. Commit changes: `git commit -m 'Add amazing feature'`
7. Push to branch: `git push origin feature/amazing-feature`
8. Open Pull Request

### Coding Standards

- **JavaScript**: [WordPress JavaScript Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/javascript/)
- **CSS**: [WordPress CSS Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/css/)
- **PHP**: [WordPress PHP Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/php/)

### Code Review Checklist

- [ ] Follows WordPress coding standards
- [ ] No console errors or warnings
- [ ] Accessibility compliant (WCAG 2.1 AA)
- [ ] Backward compatible (no breaking changes)
- [ ] Documentation updated
- [ ] Tests added/updated (when applicable)

---

## Resources

### Official Documentation

- [Block Editor Handbook](https://developer.wordpress.org/block-editor/)
- [Block API Reference](https://developer.wordpress.org/block-editor/reference-guides/block-api/)
- [@wordpress/scripts Documentation](https://developer.wordpress.org/block-editor/reference-guides/packages/packages-scripts/)

### Learning Resources

- [Block Development Examples](https://github.com/WordPress/block-development-examples)
- [Gutenberg GitHub Repository](https://github.com/WordPress/gutenberg)
- [Create Block Tutorial](https://developer.wordpress.org/block-editor/getting-started/create-block/)

---

## License

This plugin is licensed under GPL-2.0-or-later. See [LICENSE](LICENSE) file for details.

---

**Last Updated**: December 21, 2025  
**Plugin Version**: 0.4.0  
**WordPress Compatibility**: 6.1+  
**PHP Compatibility**: 7.4+
