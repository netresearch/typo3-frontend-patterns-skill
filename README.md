# TYPO3 Frontend Patterns Skill

> **Deprecated — merged into [`typo3-a11y-skill`](https://github.com/netresearch/typo3-a11y-skill).** This repository is archived and read-only.
>
> All nine frontend patterns were absorbed into the `typo3-a11y` skill, which fires at the same trigger moment (implementing a frontend component in a TYPO3 v13/v14 sitepackage). Two skills competing for the same activation were consolidated into one.
>
> - The patterns now live at [`typo3-a11y-skill/skills/typo3-a11y/references/`](https://github.com/netresearch/typo3-a11y-skill/tree/main/skills/typo3-a11y/references) and were **improved** during the move (added `prefers-reduced-motion`, `aria-hidden` on decorative icons, JSON-encoded JSON-LD values, `f:image` instead of raw `EXT:` paths) — see [typo3-a11y-skill#12](https://github.com/netresearch/typo3-a11y-skill/pull/12), released as [v1.3.0](https://github.com/netresearch/typo3-a11y-skill/releases/tag/v1.3.0).
> - The marketplace entry moved accordingly in [claude-code-marketplace#79](https://github.com/netresearch/claude-code-marketplace/pull/79).
>
> **Install [`netresearch/typo3-a11y-skill`](https://github.com/netresearch/typo3-a11y-skill) instead.** The content below is kept for historical reference only and is no longer maintained here.

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

This project uses split licensing:

- Code (`scripts/**`, `.github/workflows/**`, config files) is licensed under the [MIT License](LICENSE-MIT).
- Documentation and skill content (`skills/**`, `references/**`, `README.md`) is licensed under [CC-BY-SA-4.0](LICENSE-CC-BY-SA-4.0).

SPDX expression: `(MIT AND CC-BY-SA-4.0)`.

## Maintainer

Maintained by [Netresearch DTT GmbH](https://www.netresearch.de).
