# Vertical OS builder

A Wonderful Code skill for adapting an existing Banking OS or Retail OS into another industry OS, such as Insurance OS or Healthcare OS.

It preserves the original sphere assets, ring geometry, alignment, Retail-style Tower connections, company-wide Work overview, shared interactions and reusable journey components. It guides industry research, department/team/agent modeling, and a clickable catalog of proposed journeys. Implementing each real demo journey is a separate task.

## Install in Wonderful Code

Ask Wonderful Code to install this skill from this repository, or clone the complete repository into your Wonderful Code skills directory:

```sh
mkdir -p ~/.wonderful-code/skills
git clone https://github.com/yonahs-wonderful/vertical-os-builder.git ~/.wonderful-code/skills/vertical-os-builder
```

If you configured a different Wonderful Code home, use its `skills/vertical-os-builder` directory instead. Start a new chat after installation. Keep the entire repository: `SKILL.md` uses the included references and assets.

## Use

Give the assistant an authorized source checkout or source app location, then use this brief:

```text
Use $vertical-os-builder to create Insurance OS.
Industry scope: US property & casualty insurance.
Source OS: Retail OS.
Source app or checkout: <authorized app URL, repository, or local source directory>.
Target environment/tenant: <destination name>.
Target workspace: <destination workspace>.
App: Insurance OS / insurance-os (new).
Delivery: create, publish and activate.

Clone the existing source and preserve sphere behavior, alignment and shared
interactions. Complete the research workbook and adapt the departments,
agents and journey architectures. Keep real demo journeys as separate tasks.
```

For research or local work, replace Delivery with `research only` or `local build/preview`.

## Included requirements

- Short, distinct department names, distributed around the ring with uniform close letter-to-arc spacing and no clipped letters.
- Bright, colorful agent spheres across views, filters and Planned status.
- Retail's thin accent-colored Tower connections, subtle glow and matching moving dots, copied through the original CSS cascade. Calm agent maps reveal connections only on hover/selection, with slow signals and reduced-motion support.
- Retail's company-wide Work overview: department pulse cards, work list, search/status/department filters, viewer scope and preserved navigation context. Illustrative activity is clearly labeled as demo data and kept separate from journey readiness; flow drill-downs are separate work.
- A top-right Light/Dark choice that remembers the preference and themes the whole app.
- Tower (Agents/Journeys/Org) and Work navigation; standalone Brief and Controls pages are omitted unless requested.
- Eight fixed randomly selected Active demo journeys, consistent badges/filters/counts, and separate implementation readiness.
- Workforce sizing follows business importance: core operations receive the majority of agents, primary core departments are at least twice individual support departments by default, and HR stays smaller than every core department. Equal quotas per department are rejected.
- A substantive industry research workbook, evidence coverage, and a source-to-target reuse map.

## Contents

| Path | Purpose |
| --- | --- |
| [SKILL.md](SKILL.md) | Main workflow and requirements |
| [references/source-map.md](references/source-map.md) | Portable source setup and implementation landmarks |
| [references/research-and-model.md](references/research-and-model.md) | Research and industry-fit guidance |
| [references/design-and-motion.md](references/design-and-motion.md) | Layout, color, themes and interaction rules |
| [references/work-overview.md](references/work-overview.md) | Company-wide Work reuse, filters, scope, demo labeling and navigation |
| [references/acceptance.md](references/acceptance.md) | Completion checks and review prompts |
| [assets/launch-brief.md](assets/launch-brief.md) | Reusable launch prompt |
| [assets/industry-research-workbook.md](assets/industry-research-workbook.md) | Research workbook template |
| [assets/design-tokens.css](assets/design-tokens.css) | Light-theme comparison tokens |
| [agents/openai.yaml](agents/openai.yaml) | Skill display metadata and default prompt |

## Source access

This repository contains the skill, references and templates. The recipient also needs access to the actual Banking/Retail app source and sphere assets, plus the appropriate Wonderful environment for hosted delivery. Those apps, tenant credentials and machine-specific source locations are not bundled here. The skill directs the assistant to retrieve authorized source rather than rebuild a lookalike from screenshots.

Portable release: **0.5.0**.
