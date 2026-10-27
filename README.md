# DevTools Responsive & Accessibility Testing Note

I tested the Internship Dashboard using browser DevTools.

**1. Theme Testing (Light & Dark Mode):**
- **Automatic Mode:** I used DevTools to toggle the system preference for Dark Mode (`prefers-color-scheme: dark`). The CSS variables automatically update the colors because no hard-coded `data-theme="light"` attribute blocks it.
- **Manual Override:** *(If a toggle were added via JS, setting `data-theme="light"` on the HTML would force light mode).*

**2. Advanced CSS Feature Verification:**
- **Container Queries:** Resized the `.container-card` using DevTools to verify the `.task-item` switches from a row to a column at 400px width.
- **@supports:** Verified that `backdrop-filter` applies a blur to the header.
- **Animations:** Confirmed `@keyframes fillProgress` animates from 0 to 65%.
- **Logical Properties:** Verified that `margin-block-end` correctly applies spacing regardless of text direction.
- **min(), max(), minmax():** Verified the grid layout uses `minmax(min(100%, 300px), 1fr)` to automatically adjust card sizes without media queries.

**3. Accessibility Testing:**
- Tabbed through the page: The `:focus-visible` outlines appear on all interactive elements.
- **Reduced Motion:** Toggled "Emulate CSS prefers-reduced-motion: reduce" in DevTools. Verified that the progress bar animation is disabled and jumps immediately to 65%.
- Confirmed the Mobile Navigation uses `<details>` and `<summary>`, making it accessible without JavaScript.
- Confirmed the table has a `<caption>` and the notification button has an `aria-label` describing the unread count.