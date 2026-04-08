---
name: typo3-frontend-patterns
description: "Reusable frontend patterns for TYPO3 sitepackages: sticky header, lazy loading, breadcrumb, language switcher, animations, scroll-to-anchor, skeleton loading, toast notifications, back-to-top. Use when implementing common UI components in TYPO3 v13+ projects with Fluid, TypeScript, and SCSS."
---

# TYPO3 Frontend Patterns

Reusable implementation patterns for TYPO3 v13+ sitepackage development. Each pattern provides a complete implementation with Fluid template, TypeScript plugin, SCSS partial, and accessibility considerations.

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

- `references/patterns-sticky-header.md`
- `references/patterns-lazy-loading.md`
- `references/patterns-animations.md`
- `references/patterns-breadcrumb.md`
- `references/patterns-language-switcher.md`
- `references/patterns-scroll-to-anchor.md`
- `references/patterns-skeleton-loading.md`
- `references/patterns-toast-notification.md`
- `references/patterns-back-to-top.md`
