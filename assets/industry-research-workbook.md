# Industry OS research workbook

Use this document for a specific vertical adaptation. Replace the guidance rows with researched findings and cite source IDs. Mark unverified sections provisional. Keep claims about current operations separate from proposed agents and architecture.

## Scope and target

| Field | Finding |
| --- | --- |
| Research date and researcher | |
| Industry and precise segment | |
| Geography/jurisdiction | |
| Business model, actors and channels | |
| Generic vertical or named customer | |
| Audience and intended OS scope | |
| Source OS and revision | |
| Requested target environment/profile or tenant | |
| Destination workspace and verified identity | |
| New app name/slug and local destination | |
| Delivery intent and authorized hosted actions | |
| Important assumptions/exclusions | |

## Operating model and priorities

Describe how value is created/delivered, who pays, the major operating pressures and the relevant differences from the source industry. Identify evidence-backed priorities and explain why these journeys matter.

## Value chain

| Stage | Actor | Accountable owner | Work/record | Upstream/downstream handoff | Outcome | Sources |
| --- | --- | --- | --- | --- | --- | --- |

## Evidence coverage

Use substantiated, partial or unresolved to describe each area. Identify what would close a material gap.

| Research area | Key finding | Evidence/claim IDs | Confidence and reason | Gap and architectural impact | Next evidence needed |
| --- | --- | --- | --- | --- | --- |
| Segment/business model | | | | | |
| Core value chain/operations | | | | | |
| Customers/partners/channels | | | | | |
| Departments/teams and ownership | | | | | |
| Finance and Legal | | | | | |
| Other relevant corporate functions | | | | | |
| Systems and records | | | | | |
| Decisions/rules and exceptions | | | | | |
| Outcomes and economics | | | | | |
| Named-customer differences, if applicable | | | | | |

## Departments, teams and proposed workforce

| Department/team | Mission and owner | Core activities | Dependencies/journeys | Records/systems | Proposed agents/skills and sizing rationale | Facts vs proposals; sources |
| --- | --- | --- | --- | --- | --- | --- |

Explicitly account for Finance and Legal and explain relevant shared services or omissions. Role counts describe proposed agent coverage, not employee staffing.

## Workforce allocation by business importance

Classify and prioritize departments before assigning counts. Core operations should dominate the workforce; do not distribute an equal quota across departments. Explain importance through the value chain, business/service impact, criticality and distinct workflow coverage. Separate proposed design choices from known operational facts.

| Department | Core / enabling / corporate support | Primary core? | Importance and distinct work requiring specialists | Unique proposed agent count | Share of total | Capabilities consolidated into skills/shared roles | Evidence or explicit assumption |
| --- | --- | --- | --- | --- | --- | --- | --- |

Count each canonical worker once, excluding skills, human gates and repeated appearances in journeys. Record these checks for a full industry OS:

| Distribution check | Counts/calculation and result | Coverage revision or unresolved gap |
| --- | --- | --- |
| Core business collectively has a clear majority | Core count / total; greater than 50% | |
| Each primary core department substantially exceeds each individual non-core department | Smallest primary core count / largest enabling or corporate support count; at least 2:1 by default | |
| HR is smaller than every core business department | HR count versus each core department; strictly fewer in every comparison | |
| No equal-per-department quota or symmetry padding | Explain meaningful size differences and merged/removed duplicate roles | |
| Canonical counts agree with the visible architecture | Agents, Org, filters and proportional ring sectors reflect the allocation | |

Treat the 2:1 comparison as a proposed design check, not a staffing fact or permission to invent roles. Research missing core work and consolidate overlapping support roles when checks fail; keep unresolved allocations provisional. For telco, distinguish core network/service operations from internal employee IT and corporate support. Record an explicitly narrower user-requested scope if it changes which business is being modeled.

## Journey catalog and priority

| Journey | Actor/trigger | Owner | Business relevance and priority rationale | Intended outcome/KPI definition | Source flow | Evidence/confidence | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |

## Journey research card — repeat per catalog journey

Record the industry name, purpose, scope, actor/trigger, preconditions and accountable owner. Identify what is sourced current work and what is the proposed AI allocation.

| Stage | Current task and performing role | Input/evidence | System/record | Output and next handoff | Supporting evidence or assumption |
| --- | --- | --- | --- | --- | --- |

Document cross-team/partner dependencies, important exceptions/rework loops, missing information and relevant timing constraints. Identify proposed agents, parent-agent skills and human decision boundaries. Define the intended outcome and useful metrics without inventing achieved results. List confidence, material gaps and the source OS flow being reused/adapted.

## Systems and records

| System/category | Confirmed customer / industry category / inferred / proposed | Relevant entity and lifecycle | Journey stages and read/write purpose | Access/availability assumptions | Sources |
| --- | --- | --- | --- | --- | --- |

## Decision and constraint map

| Action/decision | Relevant segment/jurisdiction | Law, guidance, company policy or design assumption | Responsible role and required evidence | Architecture implication | Source and effective date | Gap |
| --- | --- | --- | --- | --- | --- | --- |

## Reuse/adaptation map

| Target entry | Source OS/file/flow | Reuse unchanged / rename / adapt / new | Retained graph/layout/components | Meaningful changes and fit rationale | Sources | Remaining gap |
| --- | --- | --- | --- | --- | --- | --- |

## Source and claim register

| Source ID | Title/publisher and exact URL/document locator | Published/updated/effective date; access date | Segment/geography | Supporting passage or page/section | Claims supported |
| --- | --- | --- | --- | --- | --- |

| Material claim | Fact / inference / assumption / proposal | Source IDs | Confidence and reason | Conflicting evidence and resolution |
| --- | --- | --- | --- | --- |

## Open questions and fit review

| Question/gap | Affected department/journey | Why it changes the design | Provisional treatment | Evidence/person/document needed |
| --- | --- | --- | --- | --- |

Review whether a domain operator, department owner and systems owner could recognize and follow the architecture. Record actual analytical checks and unresolved gaps without implying external approval.

## Handover

Summarize the researched operating model, the copied source foundation, important adaptations, credible reuse and remaining uncertainty. Identify separate future journey demo preparation at a high level. This workbook does not require implementing cases, scripts, replay, decision engines, integrations or audit history.
