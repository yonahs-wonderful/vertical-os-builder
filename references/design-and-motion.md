# Copy the OS behavior, then refine its presentation

## Copy the actual components

Banking and Retail are the implementation, not merely mood boards. Fork the existing app and preserve its sphere assets/component code, shared styles, geometry and interactions. A newly written ring that looks broadly similar is not an equivalent result.

Preserve the following unless the requested adaptation requires a specific change:

- Sphere image/video assets, rendering treatment, sizes, orbital/ring positions, sector padding, relative spacing, label placement, and alignment to neighboring spheres.
- The data-driven angle/radius calculations and proportional department sectors. A changed workforce may change the displayed positions through the existing algorithm; do not replace the algorithm.
- Sphere hover/selection/focus states, relationship highlighting, path activation, transitions, camera framing and pan/zoom behavior.
- Shared console shell, Agents/Journeys/Org views, filters, passports, card shapes, connectors/routing, human gates, popups and appearance controls.
- Existing journey graphs, stage alignment, branches and node positions wherever the flow remains appropriate for the target industry.

Reuse the canonical tokens and assets, including Inter, the neutral light stage, white cards, subtle borders/shadows, glossy colored spheres, colored connections, and warm human-gate treatment. Use the source appearance styles and semantic tokens for the corresponding dark surfaces. Scope app styles to the app root for host shadow-root compatibility.

Compare source and fork at matching viewport, zoom and selection state. Check the ring before and after industry-data adaptation. Explain unavoidable differences caused by agent counts; fix drift caused by rewritten layout or interaction code.

## Light/Dark option in the top right

Place an explicit Light/Dark control in the top-right app header, available from every app page. Reuse the source or shared UI control, expose its selected state and an accessible name, and support keyboard operation and visible focus. At narrow widths, wrap the header so both options remain reachable without horizontal page overflow.

Default to Light when no valid preference exists. Remember an explicit choice across navigation and reloads using an app-specific key such as `<app-slug>:appearance`; continue working when storage is unavailable. Apply the choice on the app root with its own theme attribute and color scheme. Do not change the host document's theme or another app's preference.

Map both the inherited and shared UI semantic tokens to the selected mode. Check canvas, shell, cards, tabs, toggle indicators, borders, text, labels, icons, inputs, menus, popups and passports, including Agents, Journeys, Org and other inherited pages. Shared components may use aliases such as `--surface-100`; map these to the themed card surface so dark mode does not leave white panels or unreadable text. Keep agent spheres fully colorful in either theme, retain readable status and human-gate treatments, and preserve the complete-name and interaction-only connection requirements.

Verify both modes at desktop, shared-screen and mobile widths. Change the theme, navigate through the views, open details/menus, and reload to confirm each choice persists. Confirm app-scoped styling and graceful behavior without storage. Check that switching themes neither resets selection nor reveals idle connections or starts motion.

## Complete names, without clipped letters

Render every intended department, team and agent label completely. Missing leading/trailing letters, overlapping names and fragments such as `OURCIN` for `SOURCING` are unacceptable. Tooltips or correct DOM text do not compensate for clipped visible text. An intentional, meaningful short department name may be used consistently; do not silently abbreviate a name to hide a layout defect or shrink it until unreadable.

For a curved department label, size its invisible text guide independently of the colored sector arc. Small departments still need enough guide length for the full name. A centered semicircle at the inherited label radius and reading direction is one proven fix: preserve the sector midpoint, colored arc, sphere angles and positions. Check neighboring label extents and canvas bounds after extending guides; keep labels attached to their original departments.

Verify the actual rendered first and last letters of every label at desktop, shared-screen and mobile sizes, with fonts loaded and at the normal fit view. Inspect screenshots and SVG character extents where available (`getNumberOfChars`, `getExtentOfChar`, `getComputedTextLength`, and path `getTotalLength`). Flag zero-size non-space glyphs, text longer than its guide, collisions and clipped bounds. Check names in Org and journey cards as well as the ring; provide enough space for complete names.

## Colorful agents in every state

Keep every worker logo/sphere bright, fully opaque and colorful, including proposed roles with no implemented capability. Remove inherited grayscale, desaturation and opacity reductions from the sphere and its ancestors in Agents, Journeys, Org, popups and passports. Replace gray/silver worker asset assignments with the inherited colored assets. Derive the sphere choice from the canonical agent identity so the same worker retains its color across views.

Check idle, hover, selection, journey/department filters and viewer-scope changes. Keep all workers colorful during these interactions; convey focus through outlines, size, glow and stronger connected paths. Retain existing role-scope detail restrictions and status wording. Proposed roles and Planned journeys remain labeled honestly; colorful presentation does not establish implementation, authority or live activity.

## Preserve the Retail navigation fixes

Default to the inherited Tower experience with Agents, Journeys and Org. Do not include standalone Brief or Controls tabs/pages unless explicitly requested. Remove inherited links to omitted pages and handle stale saved navigation by returning to a valid main view. Keep research/source documentation in the handoff; retain relevant policy, ownership and human-decision information in existing details. Appearance, filters, zoom, motion and detail controls remain available.

Selected journeys pack together sequentially with gaps based on actual content height; removing a middle journey closes the gap. Fit frames the visible selection rather than hidden catalog space. Reuse this implementation.

Journey details start compact and support expand, collapse, open beside map, dock, close, Escape and sensible focus restoration. Preserve an independently usable scrolling list. At narrow widths use the inherited responsive layout rather than squeezing the side pane into unreadable text.

Every imported journey uses the shared card, connector, zoom and popup renderer. Skill and Human gate labels remain explicit. Preserve the Active/Planned distinction and compute working-journey counts from valid implemented capability.

## Motion refinements within this skill

First copy and inspect the existing motion unchanged. Then refine the shared components in place, with a focused comparison against the baseline. Keep the Agents page free of connection lines and traveling dots on initial load and whenever no agent is hovered or selected. Reveal only the hovered or clicked/keyboard-selected agent's modeled handoffs. End the preview on pointer exit unless a selection is pinned; clearing the selection restores the calm view. Filters alone do not reveal lines or animate dots. Keep this behavior bounded to the visible view and honor motion preferences. Do not add synthetic relationships to make the diagram busier. Further refinements can come from:

| Area | Reuse first | Possible incremental refinement |
| --- | --- | --- |
| Spheres | Existing assets, alignment, hover/selection and animation | More deliberate illumination or selected-sphere depth |
| Connections | Existing paths, dashed flow and relationship highlights | Clearer directional signals along the same paths |
| Focus | Existing zoom, fit, framing and selection | Smoother transitions and stronger focus hierarchy |
| Panels | Existing compact details and popups | More responsive transitions and restrained elevation |
| Stage | Existing neutral canvas and layers | Subtle depth that preserves legibility and spatial stability |

Prototype a refinement on one existing architecture view, inspect it in motion, and apply the shared change consistently. Do not rotate or reorganize the whole ring, detach labels from their spheres, or replace familiar interactions with a new visual system.

Hovered/selected-path animation illustrates the architecture without building case execution. Keep signals slow and restrained: target roughly one quarter of the original traversal speed, with a minimum four-second duration even on short paths. Animate only the focused agent's existing links while keeping every worker sphere colorful. Filters may organize/highlight workers without starting connection motion. Retain meaningful labels and avoid showing invented traffic, queue counts, approvals, revenue or completed cases. It is presentation motion, not proof that the journey runs.

Do not build a case storyboard, scenario/event engine, conversations, replay controls, decision outcomes or audit synchronization to satisfy this motion pass. Those belong to a separately scoped journey demo task. Existing reusable execution infrastructure may stay in the clone without creating new scenarios.

## Accessibility and performance

Preserve keyboard selection, focus-visible controls and readable status labels. Respect reduced-motion preferences for CSS, JavaScript, SVG/video and camera transitions. Preserve or add a pause/reduce control for persistent decorative motion without requiring a journey replay feature.

Prefer bounded visible signals and transform/opacity changes. Suspend unnecessary loops in hidden views and release timers/listeners. Check interaction responsiveness with several architecture previews selected, a normal desktop viewport, shared-screen width and mobile.

A still screenshot checks alignment and style; a short recording or timed frames can verify inherited sphere/connector motion and refinements. Report only the checks actually performed.
