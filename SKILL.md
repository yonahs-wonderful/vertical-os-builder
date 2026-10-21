---
name: vertical-os-builder
description: Clone and adapt the existing Banking OS or Retail OS into another industry OS, preserving their sphere behavior, ring alignment, shared components, and reusable journey flows. Research and adapt departments, teams, agents, and journey architecture. Build each real demo journey as a separate task. Use for requests such as Healthcare OS, Insurance OS, or another vertical OS, not an unrelated dashboard or operating-system installation.
metadata:
  version: "0.4.8"
  status: "draft"
---

# Vertical OS builder

Clone an existing Banking OS or Retail OS and adapt it to a new vertical. The source app is the implementation foundation: copy its actual components, sphere assets, ring geometry, alignment logic, interaction behavior, and useful journey flows. Change the industry model and content around that foundation. A similar-looking app rebuilt from scratch does not satisfy this skill.

The deliverable is the vertical OS foundation: a researched workforce, clickable architecture and journey catalog, and the inherited OS experience. Building each real journey into a complete demo is a separate, explicitly scoped demo-preparation task. Do not make realistic cases, conversations, execution/replay controls, decision engines, or audit-history implementation a prerequisite here.

## Expected inputs

Read these from the launch prompt and existing conversation. Use [assets/launch-brief.md](assets/launch-brief.md) as a compact handoff template.

| Input | Requirement and handling |
| --- | --- |
| `vertical` | Required: the industry to create, such as Insurance. |
| `target_environment` | Required for a hosted deliverable: environment/profile or tenant name plus destination workspace name; alternatively, explicitly request local-only work. Resolve names through supported tools rather than asking for opaque IDs. |
| `industry_scope` | Strongly recommended: segment, geography/jurisdiction, business model and audience, such as US property & casualty insurance. Research and state assumptions when omitted; clarify if competing interpretations materially change the operating model. |
| `app_name` / `app_slug` | Optional: default to a distinct new industry app, such as Insurance OS / insurance-os. An existing matching app is not permission to overwrite it. |
| `source_os` | Optional: Banking, Retail, or auto. Auto chooses the closest existing source and reuses useful parts of the other. Supply an accessible source checkout or app locator as described in the source map. |
| `delivery` | State plan/research only, local build/preview, or create/publish/activate in the named destination. Follow explicit task authorization; absent a publication request, complete research/build work without publishing. |
| `customer` / `constraints` | Optional: named customer, supplied material, branding, priority journeys and required exclusions. Default to a generic industry model with documented assumptions. |

Record the resolved inputs in the research workbook. Environment/profile/tenant selects the platform destination; workspace selects a sub-scope inside that tenant; a local project folder is the filesystem destination. Do not treat these as interchangeable.

Before any hosted creation or publication, resolve and verify the supplied destination with available governed environment/app-target tools and current app guidance. Use returned identities. Do not infer the destination from the source app, current working directory, previous artifact publication, or an unrelated active profile. If the target is missing or ambiguous, continue useful research/local work and obtain the missing destination before the affected hosted action. Do not add a confirmation when the user has already clearly specified and authorized it.

## Availability and handoff

This is a global Wonderful Code skill. New chats using the same profile can invoke `$vertical-os-builder`; the editable copy is under the active Wonderful Code home's `skills/vertical-os-builder/` directory. Transfer the entire skill folder, including references and assets, when using a different profile or machine. The skill folder contains source-discovery guidance rather than the Banking/Retail app source itself; verify that the receiving environment can access the actual source checkout or retrieve it through supported app tools.

## 1. Choose and clone the existing OS

Extract the target vertical, customer, geography, audience, destination, and scope from the conversation and available files. State useful assumptions and continue. A request to revise this skill or produce a plan does not authorize a new app build.

Read [references/source-map.md](references/source-map.md) and resolve the authorized hosted app or source checkout supplied for this installation. Banking OS means the original Trusted Workforce Console; the Atlas Banking view is a derivative, not the authoritative Banking source. Locate the actual source, verify its relationship to the selected hosted reference, record its revision, and choose the closest existing OS as the base. Prefer current Retail for its navigation refinements; use Banking when its flows and structure fit better. Reuse selected components or flows from the other OS where useful.

Copy/fork the source app into its own destination and confirm the unchanged copy builds before adapting it. Keep source apps and tenant resources read-only. Preserve dependencies, shared renderers, styles, sphere assets/animation, layout calculations, filtering, zoom, and navigation. Avoid creating a new shell, sphere component, ring layout engine, or journey renderer when the source already provides one.

For a packaged app load the available `wonderful-apps` skill and current repository instructions. Preserve current bundle/SDK contracts. Give the new app its own identity and state namespace; remove inherited customer-specific names, links, records, and business rules from its visible experience as needed. Preserve canonical entity IDs where the identity is retained; remap deliberately where it changes.

If source retrieval fails, continue research and reuse mapping while resolving it. Do not silently substitute a fresh implementation from a palette or screenshot. A token-only mockup is a provisional fallback, not the completed clone.

## 2. Research what the new industry changes

Read [references/research-and-model.md](references/research-and-model.md) and use [assets/industry-research-workbook.md](assets/industry-research-workbook.md) for the research output. This is a substantive discovery stage, not a naming exercise. Inspect the source OS as the implementation baseline, then establish the target industry's operating model in its own business terms before deciding which source flows fit.

Research in depth: the precise segment/geography and business model; value chain and economics; departments, teams and ownership; real workflow steps, handoffs and exceptions; systems and records; relevant decision/regulatory boundaries; and customer-specific differences when a customer is named. Read underlying sources and record claim-level evidence, not just search snippets or AI opportunity lists.

Build an evidence coverage matrix, source register, department/team map, architecture-level journey cards, and reuse/adaptation map. Every journey needs a concrete trigger, owner, meaningful stages, relevant records/systems, proposed gates, exceptions and intended outcome. These are research and architecture outputs, not executable scenarios or demo scripts.

Keep facts, inferences, assumptions and proposed AI roles distinct. Separate industry-common practices from verified customer facts. Triangulate important claims and resolve or record conflicting evidence. Do not claim industry fit when a critical process, system or decision boundary remains unverified; deliver the affected area as provisional and continue independent work.

Explicitly consider Finance and Legal, plus relevant People/HR, IT, Risk/Compliance, Procurement, Security and Data. Reuse existing support-function flows when the work fits. Allocate agents by business importance, supported process breadth and specialist needs; do not assign an equal quota such as four agents per department or invent employee counts.

For a full industry OS, identify the core value-producing departments before sizing teams. Give core operations a clear majority of unique agents and make primary core departments substantially larger than individual enabling or corporate support departments. Use at least a 2:1 primary-core-to-support count as the default design check. HR must have fewer agents than every core business department. Keep support coverage compact by putting related capabilities into skills or genuinely shared specialists. In telco, network operations and service delivery are core business, not generic internal IT; classify functions from the business model rather than their names. Record classifications, counts, shares and work-based reasons in the workbook. Reject uniform or support-heavy allocations and revise the coverage without padding the core with invented roles. Preserve the existing variable-sector ring algorithm so real differences in workforce size remain visible. See the research reference for allocation checks.

Apply the research completion criteria and industry-fit tests in the reference before marking the architecture researched. The goal is evidence coverage and credible process detail, not a fixed number of web pages or journeys.

## 3. Map reuse before creating anything new

Create a short reuse/adaptation map: target department or journey → source OS/file or flow → retained structure → required changes. Classify each as **reuse unchanged**, **rename/reconfigure**, **adapt**, or **new**. Describe new components only where research or an explicit user request reveals a gap.

Reuse complete flow structures when they fit: intake → checks → specialist handoff → human decision → system/record, for example. Finance, legal review, document collection, service requests, exceptions, and approvals may use the same topology across industries. There is no requirement to invent a different graph for every vertical. Preserve stage order, branching, positions, and connector routing wherever they remain appropriate; adapt the actor names, systems, labels, decision descriptions, and ownership.

Keep source application data shapes and generators where sound. Derive Agents, Journeys, Org, passports, filters, and counts from one canonical model. Reuse a specialist's identity across journeys rather than duplicating workers.

Keep **Agent**, **Skill**, **Human gate**, **System**, and **Policy check** distinct. A Skill belongs to an agent and does not inflate worker counts. Label **Skill** and **Human gate** explicitly on cards and popups. Describe the human decision boundary in the architecture; implementing its runtime behavior belongs to that journey's separate demo task.

Each architecture entry needs a trigger/business actor, owner, relevant stages and agents, skills/systems, proposed decision points, and intended outcome. This is a researched map and brief, not a scripted execution scenario. Mark new entries **Planned** until their real journey has been built and checked separately. Preserve an existing **Active** journey only when the reused capability genuinely remains valid in the new context; copying its diagram alone does not make it active.

When bringing in an existing customer architecture, preserve its meaningful agents, skills, branches, systems, and gates, and render it through the inherited common journey components.

## 4. Preserve the exact sphere and layout behavior

Read [references/design-and-motion.md](references/design-and-motion.md). Reuse the actual sphere assets and component code, sizes, relative positioning, rings, sector spacing, label placement, connected highlights, hover/selection behavior, and animations. Preserve the calculation of sphere positions and their alignment to one another. Let the original data-driven geometry accommodate a changed department/agent count.

Complete names are a release requirement. No department, team or agent name may lose letters through SVG text-path clipping, masks, container bounds or overlap. A fragment such as `OURCIN` in place of `SOURCING` is unacceptable. Fit the complete intended label while retaining sphere positions and sector alignment; verify first and last letters at desktop, shared-screen and mobile widths. See the design reference for text-guide fixes and checks.

All agent logos/spheres stay bright, colorful and fully opaque across Agents, Journeys, Org and details. Planned/proposed status, lack of implementation, selection, filters and viewer scope must not gray out or desaturate workers. Use the inherited colored assets, replace gray/silver worker assignments, and keep each agent's color identity consistent across views. Preserve truthful status text and scope/access behavior; visual brightness does not make a journey Active.

Include an explicit Light/Dark control in the top-right app header. Default to Light, remember the user's choice across reloads with an app-specific storage key, and keep the appearance scoped to this app. Apply both themes consistently to the shell, Agents/Journeys/Org, passports, menus, details and other app pages using inherited semantic tokens. Keep complete names readable and every worker colorful in both modes. Make the control keyboard accessible and reachable at mobile widths. See the design reference for theme coverage and persistence checks.

Keep the default app navigation focused on Agents, Journeys and Org within the inherited Tower experience. Omit the standalone Brief and Controls tabs/pages unless the user explicitly requests them. When adapting or cleaning up an existing app, remove their navigation entries, imports, route/render branches and unused page components; hiding the tabs alone is insufficient. Keep the research workbook and source brief in the handoff, and show relevant ownership, policy and human-decision information in existing agent/journey details. This navigation simplification preserves working filters, appearance, zoom, motion and detail controls.

Reuse the console shell, Inter typography, theme tokens, cards, connectors, gates, popups, pan/zoom, filters, Agents/Journeys/Org views, and passports. Compare the fork with the source at matching viewport and zoom to catch visual or behavioral drift. Preserve inherited case/work infrastructure if useful, without requiring new working journeys or surfacing irrelevant source-customer cases.

Keep the Retail refinements: sequentially packed selected journeys with no empty catalog gaps; compact details by default; clear expand/collapse, side-panel, dock, close and Escape controls; stable list scrolling and page position; and one consistent imported-journey format.

Use **Active** and **working journeys** where existing implemented capability warrants them, with computed counts. New architecture previews stay **Planned**. Do not label copied architecture or presentation animation as a functioning demo or live integration.

## 5. Refine the inherited motion

First reproduce how the Banking/Retail spheres and connectors already move and respond. Then spend a focused pass enhancing shared presentation: sphere illumination, directional connector flow, selection depth, smooth focus/framing, and panel transitions. Apply small shared changes to the copied components rather than replacing their behavior or arrangement.

Keep the Agents page calm at rest: connection lines and traveling dots appear only for the agent the user hovers over or clicks/selects, including keyboard selection. A department/journey filter alone must not reveal every connection or start motion. Show only that agent's existing modeled handoffs, and hide them when hover ends unless selection is pinned. Use slow, restrained traveling signals (about one quarter of the original speed, with at least four seconds per traversal) while every worker remains colorful. Do not invent links, traffic or execution to create this effect. Respect reduced-motion preferences, the pause/reduce control and hidden-view suspension.

Keep the ring and labels spatially stable and the family recognizable. Inspect one inherited architecture view before applying refinements across the OS. Architecture animation can show connectivity and a selected path without inventing cases, conversations, queue activity, or execution outcomes. Retain reduced-motion support, a pause/reduce control for persistent motion, and responsive interaction.

Scenario-driven motion tied to real case execution belongs to the separately scoped journey demo work. It is not needed to complete the OS foundation.

## 6. Verify and hand over the adapted OS

Use [references/acceptance.md](references/acceptance.md). Check the copied foundation, industry data, reuse map, sphere alignment and interactions, connected views, planned architecture previews, compact multi-selection, detail controls, and relevant build/package contracts. Compare source/fork at desktop, shared-screen width, mobile, keyboard and reduced motion. Check both Light and Dark, persisted choice after reload, and calm connection behavior in each theme. Record which checks actually ran.

Deliver the adapted OS when requested, a concise research/source brief, the reuse/adaptation map, and its journey catalog with honest status. Note which journeys can become separate demo-preparation tasks and what remains to prepare for each at a high level. Do not create or execute those tasks unless asked.

Completion here means the reused OS works as an industry architecture explorer and foundation. It does not depend on implementing any new end-to-end demo journey. Publish only within the user's existing task authorization and destination.
