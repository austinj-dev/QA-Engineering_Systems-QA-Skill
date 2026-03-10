# Accessibility Testing — QA Engineering (WCAG 2.2 AA)

## Keyboard Navigation
- [ ] Tab navigates through all interactive elements
- [ ] Shift+Tab navigates backward
- [ ] Enter/Space activates buttons and links
- [ ] Escape closes modals, dropdowns, popovers
- [ ] Arrow keys navigate within menus, tabs, lists
- [ ] Focus order matches visual order
- [ ] No keyboard traps (can always Tab out)

## Focus Management
- [ ] Focus indicator visible on all interactive elements
- [ ] Focus moves to modal when opened
- [ ] Focus returns when modal closed
- [ ] Focus moves to new content on navigation
- [ ] Skip-to-content link available

## Screen Reader
- [ ] All images have alt text (or aria-hidden if decorative)
- [ ] Form fields have associated labels
- [ ] Error messages programmatically associated with fields
- [ ] Tables have proper headers (th, scope)
- [ ] Landmarks used (main, nav, header, footer)
- [ ] Headings in proper hierarchy (h1 → h2 → h3)
- [ ] Dynamic content changes announced (aria-live)

## Color & Contrast
- [ ] Text contrast ratio ≥ 4.5:1 (normal text)
- [ ] Text contrast ratio ≥ 3:1 (large text)
- [ ] UI component contrast ≥ 3:1
- [ ] Information not conveyed by color alone
- [ ] Focus indicators meet contrast requirements

## Forms
- [ ] All fields have visible labels
- [ ] Required fields indicated (not just by color)
- [ ] Error messages descriptive and specific
- [ ] Autocomplete attributes on appropriate fields
- [ ] Form instructions provided before the form

## Content
- [ ] Text resizable to 200% without loss
- [ ] No horizontal scrolling at 320px width
- [ ] Touch targets ≥ 44x44px on mobile
- [ ] Animation can be paused/stopped (prefers-reduced-motion)
- [ ] No content flashes more than 3 times/second
