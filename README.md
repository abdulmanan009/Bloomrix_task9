# DevTools Responsive & Accessibility Testing Note

I tested the Internship Dashboard using browser DevTools.

**1. Theme Testing (Light & Dark Mode):**
- **Automatic Mode:** I used DevTools to toggle the system preference for Dark Mode (`prefers-color-scheme: dark`). The CSS variables automatically update the colors. 
- **Manual Override:** The HTML has no hard-coded `data-theme` attribute, meaning it respects the user's OS. *(If a toggle were added via JS, setting `data-theme="light"` would force light mode).*

**2. Advanced CSS Feature Verification:**
- **Container Queries:** Resized the `.container-card` using the DevTools element panel to verify the `.task-item` switches from a row to a column at 400px width.
- **@supports:** Verified that `backdrop-filter` applies a blur to the header.
- **Animations:** Confirmed `@keyframes fillProgress` animates using `calc()`.
- **Logical Properties:** Verified that `margin-block-end` correctly applies spacing.

**3. Accessibility Testing:**
- Tabbed through the page: The `:focus-visible` outlines appear on all interactive elements (including the notification button and form inputs).
- **Reduced Motion:** Toggled "Emulate CSS prefers-reduced-motion: reduce" in DevTools. Verified that the progress bar animation is disabled and jumps immediately to 65%.
- Confirmed the Mobile Navigation uses `<details>` and `<summary>`, making it accessible without JavaScript.