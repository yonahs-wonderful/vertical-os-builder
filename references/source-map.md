# Design baseline and source map

Retail Work and Tower connector source were inspected against active Retail OS 1.0.77 on 2026-10-26. Earlier local source locators were recorded on 2026-10-21. The Banking URL below was supplied by the user; its deployed revision has not been compared with the local checkout. Resolve source and revision again before a new build. Source apps remain read-only during a fork.

## Locate the originals

The originating project root on Yonah's machine is:

`/Users/yonah.s/.wonderful-code/userdata/one-off-chats/c1ebe9409603697b`

| Reference | Location within that root | Purpose |
| --- | --- | --- |
| Earlier inspected Retail OS | `retail-os/` | Historical local implementation; package version 1.0.11 at that inspection. Retrieve the selected current hosted source for newer Work/navigation/connector refinements. |
| Banking OS — NAB demo / Trusted Workforce Console | `research/nab/agentic-bank-demo/apps/trusted-workforce-console/` (frontend in `app/`) | Authoritative Banking implementation reference; verify checkout revision against the selected hosted copy |
| Atlas Banking copy | `wonderful-os-atlas/src/banking/` | Historical derivative of NAB; not the authoritative Banking OS source |
| Earlier retail fork | `aeo-retail-atlas/` | Historical context; prefer the newer `retail-os/` implementation |
| AEO Command Center source | `research/aeo-command-center/` | Example of a customer architecture imported into a common journey format |

### Hosted app references

**Banking OS — user-supplied copy of the NAB demo's Trusted Workforce Console:**
`https://usa.app.demo.wonderful.ai/workspace/179893f9-710b-4355-bcb5-9b9eeef1afb3/apps/trusted-workforce-console`

Use this copy when locating or inspecting Banking OS. Environment: USA demo (CLI profile `usa`); source workspace locator: `179893f9-710b-4355-bcb5-9b9eeef1afb3`; app slug: `trusted-workforce-console`. Resolve the current app identity through supported tools. The local NAB checkout above is an implementation reference, not a claim that it matches the currently deployed copy byte for byte. Compare or retrieve the relevant source before selecting a revision for cloning.

**Retail OS:**
`https://usa.app.demo.wonderful.ai/workspace/97cbe143-ad11-4e14-9532-9d40a116e2dd/apps/retail-os`

On 2026-10-26, the active version was `1.0.77` (`7ec0839c-7ca4-49b7-852a-d86a5196eba4`). Its source-inclusive bundle supplied the actual company-wide Work overview and Tower connector styles used for the Automotive OS refinements. This records inspected provenance, not a permanent pin: resolve the current version and retrieve its source before a new build. Keep the complete CSS cascade and verify relevant imports.

These URLs locate source apps, not the deployment destination for a new vertical. Resolve the new app's target environment and workspace separately from the launch inputs. Do not reuse the source apps' customer or resource IDs automatically.

If these local paths are unavailable, discover the relevant source checkout or app through supported project/app tools and current app guidance. Search by app name rather than guessing resource IDs. If the source cannot be retrieved, continue research and reuse mapping while resolving retrieval. A token/screenshot mockup may be explicitly provisional, but does not satisfy the copied-OS deliverable. The token snapshot is not a substitute for source recovery or a complete runnable app template.

## Inspect these files for a fork

| Concern | Retail files relative to `retail-os/` |
| --- | --- |
| App entry and console shell | `src/App.tsx`, `src/retail/RetailTower.tsx`, `src/retail/RetailWorkspace.tsx` |
| Theme and appearance | `src/retail/ab/theme.css`, `src/retail/console.css`, `src/retail/retail.css`, `src/useAtlasAppearance.ts` |
| Workforce ring and filters | `src/retail/screens/TowerAgents.tsx`, `TowerAgentsFilter.tsx` |
| Tower connection appearance | Full `src/retail/screens/tower.css` cascade plus imported console wrapper styles; see `design-and-motion.md` for the inspected stroke/glow/dot values |
| Journey renderer and layout | `src/retail/screens/Tower.tsx`, `tower.css` |
| Compact/docked journey details | `src/retail/JourneyOverview.tsx` and the detail-mode state in `screens/Tower.tsx` |
| Org and role-based scope | `src/retail/screens/TowerOrg.tsx`, `org.ts`, `todayScope.ts`, `ViewerMenu.tsx` |
| Passports | `src/retail/RetailPassport.tsx` and canonical architecture data |
| Domain model | `src/retail/getRetailArchitecture.ts`, `retailExpansion.ts`, `retailFunctions.ts` |
| Existing execution infrastructure (optional reuse; no new demo required) | `src/retail/data/retailDemo.ts`, `retailCaseContext.ts`, `RetailCaseExecution.tsx` |
| Company-wide Work overview | `src/retail/RetailWorkOverview.tsx`, `src/retail/screens/work-overview.css`; see `work-overview.md` |
| Main-view navigation and persistence | `src/retail/useRetailNavigation.ts`, `src/App.tsx` |
| Work execution, controls, audit (separate from the overview) | `src/retail/RetailWork.tsx`, `RetailControls.tsx`, `RetailAudit.tsx` |
| Case map, zoom, controls | `src/retail/CaseMap.tsx`, `screens/panzoom.ts`, `CanvasControls.tsx` |
| Shared agent assets | `src/retail/ab/orbs/`, including spheres and the orb video |
| Customer architecture normalization | `src/retail/aeoCommandCenter/getAeoJourneyMap.ts`, `getAeoCareJourney.ts` |

In the grouped file rows, unprefixed sibling filenames are in the same folder as the first file. Verify actual imports before copying; the source may evolve.

For Banking inspect the NAB console, relative to `research/nab/agentic-bank-demo/apps/trusted-workforce-console/`:

| Concern | NAB Banking source |
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

The Atlas `src/banking/` files use different wrapper names and local replay behavior. Do not mistake that derivative for the NAB implementation or use its synthetic execution behavior as evidence of what the hosted NAB copy runs.

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
