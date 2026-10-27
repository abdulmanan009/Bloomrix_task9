# DevTools Responsive & Accessibility Testing Note

I tested the Internship Dashboard using browser DevTools.

**1. Viewport Testing:**
- **Mobile (375px):** Dashboard grid is a single column. The Container Query on the `.container-card` triggers `max-width: 399px`, stacking the task items vertically for readability.
- **Desktop (1440px):** The grid expands to 2 columns. The multi-column text section automatically splits into 2 columns using CSS `columns`.
- **Theme Testing:** I used DevTools to toggle the system preference for Dark Mode. The CSS variables automatically update via `@media (prefers-color-scheme: dark)`.

**2. Advanced CSS Feature Verification:**
- **Container Queries:** Resized the `.container-card` using the DevTools element panel to verify the `.task-item` switches from row to column at 400px width.
- **@supports:** Verified that `backdrop-filter` applies a blur to the header on supported browsers.
- **Animations:** Confirmed the `@keyframes fillProgress` animates the progress bar from 0 to 65% on page load.
- **Logical Properties:** Verified that `margin-block-end` applies correct spacing regardless of text direction.


**3. Accessibility Testing:**
- Tabbed through the page: The `:focus-visible` outlines appear on all interactive elements.
- **Reduced Motion:** Toggled "Emulate CSS prefers-reduced-motion: reduce" in DevTools Rendering tab. Verified that the progress bar animation is disabled and jumps immediately to 65%.
- Confirmed the Skip Link is the first element to receive focus.