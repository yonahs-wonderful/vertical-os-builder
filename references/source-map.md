# Design baseline and source map

## Supply the source for this installation

This skill adapts an existing Banking OS or Retail OS; it does not bundle those apps or grant access to them. Before building, obtain an authorized source checkout or source app locator from the person providing the OS foundation. Keep source apps read-only while creating the new vertical.

Record these inputs in the research workbook:

| Source input | What to provide |
| --- | --- |
| Source OS | Retail OS or the original Banking Trusted Workforce Console |
| Source app | Its actual hosted app URL, or its environment/workspace and app name |
| Source checkout | An accessible local directory or Git repository containing the app source and sphere assets |
| Source revision | The checked-out commit and, where available, the matching deployed version |
| Destination | The separate environment/workspace and new app identity requested by the user |

Use the original Banking console as the Banking reference; an Atlas-derived view is not the authoritative source. Prefer the current Retail source when its navigation and shared components fit the requested vertical. Retrieve or compare the actual source with the selected hosted app before claiming revision fidelity. A local checkout is not proof that it matches the currently deployed version.

Resolve supplied names through supported project/app tools and the current Wonderful Apps guidance. Do not guess tenant/workspace IDs or use a source app as the new app's destination. If source access is missing, continue research and reuse mapping while obtaining it. A token/screenshot mockup may be explicitly provisional, but does not satisfy the copied-OS deliverable.

The paths below are implementation landmarks from the source family. Some checkouts place the frontend under `app/`; inspect actual imports and repository instructions to resolve the current layout.

## Inspect these files for a fork

| Concern | Retail files relative to `retail-os/` |
| --- | --- |
| App entry and console shell | `src/App.tsx`, `src/retail/RetailTower.tsx`, `src/retail/RetailWorkspace.tsx` |
| Theme and appearance | `src/retail/ab/theme.css`, `src/retail/retail.css`, `src/useAtlasAppearance.ts` |
| Workforce ring and filters | `src/retail/screens/TowerAgents.tsx`, `TowerAgentsFilter.tsx` |
| Journey renderer and layout | `src/retail/screens/Tower.tsx`, `tower.css` |
| Compact/docked journey details | `src/retail/JourneyOverview.tsx` and the detail-mode state in `screens/Tower.tsx` |
| Org and role-based scope | `src/retail/screens/TowerOrg.tsx`, `org.ts`, `todayScope.ts`, `ViewerMenu.tsx` |
| Passports | `src/retail/RetailPassport.tsx` and canonical architecture data |
| Domain model | `src/retail/getRetailArchitecture.ts`, `retailExpansion.ts`, `retailFunctions.ts` |
| Existing execution infrastructure (optional reuse; no new demo required) | `src/retail/data/retailDemo.ts`, `retailCaseContext.ts`, `RetailCaseExecution.tsx` |
| Work, controls, audit | `src/retail/RetailWork.tsx`, `RetailControls.tsx`, `RetailAudit.tsx` |
| Case map, zoom, controls | `src/retail/CaseMap.tsx`, `screens/panzoom.ts`, `CanvasControls.tsx` |
| Shared agent assets | `src/retail/ab/orbs/`, including spheres and the orb video |
| Customer architecture normalization | The source app's customer-architecture adapters |

In the grouped file rows, unprefixed sibling filenames are in the same folder as the first file. Verify actual imports before copying; the source may evolve.

For Banking inspect the original Trusted Workforce Console, relative to its repository root:

| Concern | Banking source |
| --- | --- |
| App identity and frontend package | `wonderful.json`, `app/package.json` |
| App shell and Tower entry | `app/src/App.tsx`, `app/src/screens/TowerScreen.tsx` |
| Workforce ring and filters | `app/src/screens/TowerAgents.tsx`, `app/src/screens/TowerAgentsFilter.tsx` |
| Journey renderer and layout | `app/src/screens/Tower.tsx`, `app/src/screens/tower.css` |
| Org and ownership | `app/src/screens/TowerOrg.tsx`, `app/src/screens/org.ts` |
| Passports | `app/src/screens/Passport.tsx` |
| Sphere assets and theme | `app/src/ab/orbs/`, `app/src/ab/theme.css` |
| Pan/zoom | `app/src/screens/panzoom.ts` |
| Model and console data | `app/src/data/types.ts`, `app/src/data/useConsoleData.ts`, `shared/console/demo-seed.ts` |
| Existing case infrastructure (optional reuse) | `app/src/screens/CaseScreen.tsx` |

The Atlas `src/banking/` files use different wrapper names and local replay behavior. Do not mistake that derivative for the original Banking implementation or use its synthetic execution behavior as evidence of what the selected hosted Banking copy runs.

## Reuse and adaptation rules

- Read the chosen repository's `AGENTS.md` and current app skill before implementation. Follow actual component and bundle contracts instead of stale deployment recipes.
- Fork or copy into a new app destination. Inspect source status first and preserve user changes.
- Clone the app first and verify the unchanged copy builds. Preserve actual sphere rendering, relative alignment/spacing, ring-position calculations, highlight/motion behavior, shared components and useful complete flow graphs. Adapt industry data/configuration behind them; do not rebuild from a screenshot.
- Keep a reuse/adaptation map linking each target entry to the source flow/file and classifying it as reuse unchanged, rename/reconfigure, adapt, or new. Reuse the same flow topology and layout wherever it fits.
- Rename product/namespace and visible customer content deliberately. Existing execution infrastructure may remain in the clone, but real journey implementation is separate demo-preparation work.
- Reuse recent Retail fixes rather than recreating the earlier blank journey rows, cramped details, or separate imported-diagram skin.
- Inspect inherited data types: Retail still contains bank-shaped compatibility types. Define clean target-specific records where necessary; do not expose accounts/payees in an unrelated industry just because the types exist.
- Keep source-backed branding and licenses with copied assets. Do not export credentials or tenant-specific runtime configuration as a starter.
- Preserve runtime SDK boundaries and package versions according to the chosen app's current manifest. No platform keys or controller URLs belong in browser code.

`assets/design-tokens.css` contains a portable light-theme token snapshot extracted from the actual Retail theme. It supports token comparison or an explicitly provisional mockup; actual source code is the foundation for a completed adaptation. Load the source appearance styles for supported dark variants rather than guessing their colors.
