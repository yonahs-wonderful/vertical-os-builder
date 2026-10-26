# Company-wide Work overview

Work is part of the default vertical OS foundation alongside Tower. It lets a viewer scan company activity without opening a particular journey. Preserve Retail's actual overview rather than replacing it with a new dashboard or requiring individual workflow implementations first.

## Reuse the actual Retail implementation

In the inspected Retail OS 1.0.77 source, start with:

- `src/retail/RetailWorkOverview.tsx`: team pulse cards, metrics, filters, work rows and empty state.
- `src/retail/screens/work-overview.css`: the complete original stylesheet, including its final responsive rules.
- `src/retail/useRetailNavigation.ts` and `src/App.tsx`: main-view selection, sidebar entry and navigation persistence.
- `src/retail/screens/todayScope.ts`: viewer scope; adapt it to the target's canonical ownership and journey model.
- Existing sphere assets, shared UI controls and semantic theme tokens.

Verify these paths against the selected source revision. Use a small target adapter for work items and ownership rather than copying retail customer records, execution services or business rules. If the base is Banking, reuse the Retail overview components and adapt their inputs. Record this reuse and the source revision in the reuse map.

## Activity and model

Retain department/team pulse cards, summary metrics and a company-wide work list. Cards filter the list. Rows show the work name/reference, department, accountable owner, current activity/stage, status, responsible people and participating agents with their canonical colored spheres. Distinguish work with agents, awaiting people, needing attention and completed items; preserve meaningful text labels rather than relying on color.

Use one collection for rows, pulse cards, totals, status counts and viewer scope. Apply department, search and status filters together; show the result count and provide an empty state with a clear-filter action. Scope items through existing ownership/journey relationships. A restricted viewer sees the relevant work and counts; changing scope must not leave an invalid department selection or reveal restricted details.

Resolve department names, agents, owners, stage records, handoffs and human decision boundaries to the target's canonical architecture. Do not hardcode Automotive's twelve departments, forty-two examples or status totals into another vertical. Model participation and example status are different facts.

When real activity is unavailable, create lightweight illustrative overview items derived from the researched journey stages. Keep a persistent **Demo snapshot** label and a visible explanation that these items are illustrative and no live company systems are connected. Do not label a static snapshot as live or imply actual customer operations. Replace that wording only when verified feeds support the claim; label mixed demo/live sources clearly when applicable.

Keep illustrative activity separate from implementation readiness and architecture preview status. A demo item marked Completed or With agents never makes its journey implemented, changes the saved Active preview selection, or increases verified working-journey counts. These overview records do not require realistic full cases, conversations, audit histories or an execution engine. Leave row drill-downs and flow execution out until separately requested; department cards and filters remain interactive.

## Navigation, motion and appearance

Expose Work alongside Tower in the inherited side rail. Switching views preserves Work filters and the Tower's selected tab, agent/journeys, filters and camera. Reuse mounted-view state or an equivalent source pattern; merely remounting both pages on every navigation loses this context.

Persist the selected main view across reloads with an app-specific namespace, including tenant, workspace, app and user when available. Validate stored values and fall back to a valid view; navigation remains usable if storage is unavailable. Use the real hosted SDK context for hosted identity and a static dev context only for local preview.

Pause pulse/connector animations and remove unnecessary animation loops in hidden views. Honor the app's explicit reduce-motion control and the OS preference. Apply the app's Light/Dark tokens to cards, labels, metrics, inputs/placeholders, selected controls and empty states. Use accessible shared controls, including an exposed selected state and keyboard support. Wrap controls and long department names at narrow widths without horizontal page overflow.

## Verify the overview

- Compare the original Retail overview and adapted view at matching viewport sizes. Inspect Light/Dark at desktop, shared-screen and mobile widths, including 1440px, 720px and 390px where practical.
- Check all department cards, totals and each status count against the actual item collection; combine department, search and status filters, then recover from an empty result.
- Change viewer scope and confirm items, department choices and counts agree. Switch Tower → Work → Tower and back to verify preserved context; reload to check main-view persistence and validate storage fallback.
- Inspect long department names, sphere assets, selected/keyboard control states and text contrast. Confirm the overview works without opening any individual flow.
- Verify explicit/OS reduced motion and hidden-view suspension. Confirm illustrative labels remain visible and examples do not alter canonical readiness or preview status.

Record checks actually performed. The Automotive OS implementation was validated with twelve departments and forty-two illustrative items; those counts describe that app, not a requirement for future verticals. Adding the overview or these instructions does not authorize new integrations or publication outside the user's requested destination.
