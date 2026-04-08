# TYPO3 Frontend Patterns Skill

Reusable frontend implementation patterns for TYPO3 v13+ sitepackage development. Each pattern provides a complete implementation with Fluid template, TypeScript plugin, SCSS partial, and accessibility considerations.

## Installation

### Claude Code Marketplace

```bash
claude install netresearch/typo3-frontend-patterns-skill
```

### Composer

```bash
composer require netresearch/typo3-frontend-patterns-skill
```

## Available Patterns

| Pattern | Description |
|---------|-------------|
| Sticky Header | Scroll-triggered fixed header with `requestAnimationFrame` optimization |
| Lazy Loading | Deferred component initialization using `IntersectionObserver` |
| Breadcrumb | Breadcrumb navigation with JSON-LD structured data and Schema.org markup |
| Language Switcher | Multi-language navigation using `b13/menus` LanguageMenu DataProcessor |
| Animations | Scroll-triggered animations with `prefers-reduced-motion` support |
| Scroll to Anchor | Smooth scroll to anchor links with sticky header offset compensation |
| Skeleton Loading | CSS-only shimmer placeholder animations for async content |
| Toast Notification | Lightweight notification system with auto-dismiss and ARIA live regions |
| Back to Top | Scroll-to-top button with visibility threshold and smooth scroll |

## License

MIT
