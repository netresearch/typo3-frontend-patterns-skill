---
name: typo3-frontend-patterns
description: "Reusable frontend patterns for TYPO3 sitepackages: sticky header, lazy loading, breadcrumb, language switcher, animations, scroll-to-anchor, skeleton loading, toast notifications, back-to-top. Use when implementing common UI components in TYPO3 v13+ projects with Fluid, TypeScript, and SCSS."
---

# TYPO3 Frontend Patterns

Reusable implementation patterns for TYPO3 v13+ sitepackage development. Each pattern provides a complete implementation with Fluid template, TypeScript plugin, SCSS partial, and accessibility considerations.

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
