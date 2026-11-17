# Text Behind Person Hero Implementation Plan

> **For agentic workers:** Execute this plan task by task in the current session.

**Goal:** Revise the existing hero to show two animated text rows behind the centered grayscale portrait.

**Architecture:** Keep the plain HTML structure in `index.html`; implement the layout and animation in `style.css`. Preserve existing button markup and styles, the `antonio.png` asset, and all non-hero sections.

**Tech Stack:** Plain HTML and CSS.

**Spec:** User-provided “Hero Section – Text Behind Person Layout” spec in the conversation.

## Global Constraints

- The hero is white and full width; the portrait stays grayscale.
- Marquees loop in opposite directions, with duplicated text, hidden overflow, and no selection.
- Respect reduced motion and responsive sizing; do not change navigation, other sections, or button styles.

## Review Focus

- Narrow screens: no horizontal overflow at 375px.
- Reduced motion: marquee animation is stopped or slowed.
- Layering: portrait covers both text rows; buttons remain above portrait where overlapping.
- Existing grayscale treatment and controls remain intact.

---

### Task 1: Implement hero layers and styling

**Files:**
- Modify: `index.html` hero section only.
- Modify: `style.css` hero rules and related keyframes only.

**Interfaces:** Keep the existing hero ID, title ID, portrait asset, button links, and accessibility labels.

- [ ] Add two duplicated marquee rows behind the portrait, using the specified heading and subtitle copy.
- [ ] Style the hero as full width, white, and at least viewport height; position and clip the portrait at the bottom while preserving grayscale.
- [ ] Add opposite-direction CSS marquee loops, mobile sizing, `user-select: none`, and reduced-motion handling.
- [ ] Verify the listed acceptance criteria at 375px, 768px, and 1440px; check stacking and that non-hero sections and controls retain their existing styles.
