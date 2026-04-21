---
name: typo3-frontend-patterns
description: "Reusable frontend patterns for TYPO3 sitepackages (v13/v14 LTS; v14 removes core asset concat/compression #108055 so external build tool required — see [typo3-vite-skill](https://github.com/netresearch/typo3-vite-skill)): sticky header, lazy loading, breadcrumb, language switcher, animations, scroll-to-anchor, skeleton loading, toast notifications, back-to-top. Use when implementing common UI components in TYPO3 v13+/v14 projects with Fluid 4/5, TypeScript, and SCSS. Triggers: Fluid 5 strict-typed VHs, Camino theme, native dialog modal."
---

# TYPO3 Frontend Patterns

Reusable implementation patterns for TYPO3 v13 and **v14.3 LTS** sitepackage development. Each pattern provides a complete implementation with Fluid template, TypeScript plugin, SCSS partial, and accessibility considerations.

> **v14 heads-up**: the core no longer concatenates or compresses frontend CSS/JS (Breaking [#108055](https://docs.typo3.org/c/typo3/cms-core/main/en-us/Changelog/14.0/Breaking-108055-RemovedFrontendAssetConcatenationAndCompression.html)). Pair these patterns with an external build tool — see [typo3-vite-skill](https://github.com/netresearch/typo3-vite-skill). **Fluid 5** (v14) enforces strict ViewHelper typing ([#108148](https://docs.typo3.org/c/typo3/cms-core/main/en-us/Changelog/14.0/Breaking-108148-Fluid50.html)): all VHs in pattern templates must have typed arguments + `render(): string`. **Camino** (v14.1+, [#108539](https://docs.typo3.org/c/typo3/cms-core/main/en-us/Changelog/14.1/Feature-108539-Default-Theme-Camino.html)) is the v14 core's default theme alternative to bootstrap-package — patterns stay theme-agnostic.

These patterns solve common frontend problems that every TYPO3 sitepackage encounters. Instead of building from scratch, use these proven implementations that handle edge cases (scroll performance, reduced-motion, keyboard navigation, ARIA live regions) correctly from the start.

## Available Patterns

| Pattern | Description | Key Features |
|---------|-------------|-------------|
| Sticky Header | Scroll-triggered fixed header | IntersectionObserver, CSS transitions |
| Lazy Loading | Deferred component initialization | IntersectionObserver, placeholder content |
| Breadcrumb | Breadcrumb navigation | JSON-LD structured data, Schema.org |
| Language Switcher | Multi-language navigation | b13/menus LanguageMenu, flag icons |
| Animations | Scroll-triggered animations | `prefers-reduced-motion` support |
| Scroll to Anchor | Smooth scroll with offset | Header height compensation |
| Skeleton Loading | CSS placeholder animations | Content layout stability |
| Toast Notification | Notification messages | Auto-dismiss, ARIA live region |
| Back to Top | Scroll-to-top button | Visibility threshold, smooth scroll |

## Implementation Convention

Each pattern follows the same structure:
1. **Fluid template** -- Markup with semantic HTML and ARIA attributes
2. **TypeScript plugin** -- Behavior with `DOMContentLoaded` initialization
3. **SCSS partial** -- Styling with Bootstrap integration
4. **Vite entrypoint** -- Code splitting via `*.entry.ts`

## References

- `references/patterns-sticky-header.md` -- Scroll-triggered fixed header with IntersectionObserver
- `references/patterns-lazy-loading.md` -- Deferred component initialization with placeholder content
- `references/patterns-animations.md` -- Scroll animations with prefers-reduced-motion support
- `references/patterns-breadcrumb.md` -- Breadcrumb navigation with JSON-LD structured data
- `references/patterns-language-switcher.md` -- Multi-language navigation with b13/menus LanguageMenu
- `references/patterns-scroll-to-anchor.md` -- Smooth scroll with sticky header offset compensation
- `references/patterns-skeleton-loading.md` -- CSS placeholder animations for content loading
- `references/patterns-toast-notification.md` -- Auto-dismiss notifications with ARIA live region
- `references/patterns-back-to-top.md` -- Scroll-to-top button with visibility threshold
