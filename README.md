#  Web Performance Optimization Demo

An interactive, single-page presentation dashboard designed to demonstrate critical web performance optimization concepts. The page includes real-time simulations comparing resource loading speeds, rendering timelines, Lighthouse audit scores, and Core Web Vitals statistics before and after optimization techniques are applied.

---

##  File Directory

- [INDEX.html](./INDEX.html): Complete dashboard implementation detailing inline styles, SVG visualizers, simulation buttons, and script logic.

---

##  Interactive Features & Optimization Demos

The dashboard is structured around four primary performance areas:

1. **Google Lighthouse Audit Simulator**:
   - Features animated circular SVG progress rings showing score meters for **Performance**, **Accessibility**, **Best Practices**, and **SEO**.
   - Toggles dynamically between *Before Optimization* (Performance at `42`) and *After Optimization* (Performance at `97`).
2. **Technique 1: Lazy Loading + WebP/AVIF Format**:
   - Demonstrates a grid of color-mapped images loading asynchronously as they approach the viewport using the `IntersectionObserver` API.
   - Images are preloaded 150px before entering the screen, swapping the real source, hiding loading spinners, and fading in.
3. **Technique 2: Advanced Caching Policies**:
   - Interactive table detailing caching strategies (Immutable, Long Cache, SWR 60s, No Cache) and max-age settings for different file extensions.
   - Includes a **Simulate Reload** button to visualize browser cache reads vs fresh network fetches.
4. **Technique 3: Eliminating Render-Blocking Resources**:
   - Visualized execution timeline comparing standard parser-blocking script loops vs non-blocking scripts (using `async` and `defer` attributes) and CSS asynchronous media rules (`media="print" onload="this.media='all'"`).
5. **Core Web Vitals Metric Gauges**:
   - Detailed comparison matrix logging exact numbers for First Contentful Paint (FCP), Largest Contentful Paint (LCP), Time to Interactive (TTI), Total Blocking Time (TBT), and Cumulative Layout Shift (CLS).

---

##  Technology Stack

- **Visualizations**: CSS3 keyframe sweeps, vector-based SVG score indicators, CSS grids
- **Optimization APIs**: HTML5 IntersectionObserver, async font loading, preconnect links
- **Logic**: Deferred Vanilla JavaScript ES6

---

##  How to Run

Open [INDEX.html](./INDEX.html) directly in your browser.

If running a local server:
```bash
npx serve .
```
Then visit: `http://localhost:3000/LEVEL_3/TASK_2/INDEX.html`
