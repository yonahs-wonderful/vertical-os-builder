# In-depth industry research and adaptation

Use this process to establish how the target industry actually operates, then adapt the existing Banking/Retail implementation to it. Keep the source UI, sphere behavior and suitable flow structures. The research output is an evidence-backed operating model and journey architecture, not implemented demo scenarios.

Use [the research workbook](../assets/industry-research-workbook.md) as the output structure. Keep source notes and locators alongside it when they would otherwise make the brief unwieldy. Scale investigation to industry complexity and material gaps; a fixed source count does not establish completeness.

## 1. Define the industry precisely

Record the segment/subsector, geography and jurisdiction, business model, customer/partner types, channels, organization size/operating footprint, audience and scope. A hospital network and an outpatient clinic, or a life insurer and a property insurer, need different operating models even within the same broad vertical.

Distinguish a generic industry OS from a named-customer OS. For a named customer, record its verified segments, channels, operating footprint, structure, strategic priorities and available existing discovery material. Label industry-common practices separately from confirmed customer practices. Do not infer a customer's systems or policy from a competitor's implementation.

Inspect Banking/Retail to understand the available implementation and catalog. Establish the target's business model in its own language before assigning source flow analogues. Preserve the UI foundation while avoiding an operating model biased by the source industry's vocabulary.

Output: a scoped research brief with assumptions and the few unanswered questions that could materially change the model. Continue independent work while optional information remains unknown.

## 2. Build an evidence plan and read the sources

Create a coverage matrix listing the questions to answer, source types, current findings, evidence strength and gaps. Cover all of these lenses:

| Lens | Questions | Useful evidence |
| --- | --- | --- |
| Business and value chain | Who is served, who pays, how is value delivered, and where are the major handoffs? | Official service descriptions, annual reports, operating-segment disclosures, industry process references |
| Departments and ownership | Which functions perform and own the work? What is central, local, outsourced or partner-operated? | Company operating descriptions, organizational material, role descriptions, practitioner/association material |
| Work and pain points | What starts work, what creates delay or rework, and how is it resolved? | Supplied SOPs, service policies, official guidance, industry studies, dated company statements |
| Systems and records | Which records move through which systems, and which system owns the final state? | Customer documents, official product/process documentation, verified implementation references |
| Decisions and constraints | Who has authority, what evidence is needed, and which rules apply in this jurisdiction? | Current official regulatory/government sources, supplied policy, professional standards |
| Outcomes and economics | What do operators optimize and how are results measured? | Reported business priorities, operational metric definitions, credible industry studies |
| Industry/customer differences | Which practices are common, segment-specific, local, or unique to the named customer? | Representative operators in the relevant segment and region, customer-specific sources |

Start with supplied and authorized internal material when relevant. Use current primary sources for stated strategy, actual services, rules and policies. Use industry bodies and reputable practitioners for workflow detail and independent corroboration. Examine representative operators to identify common practice and important variation rather than copying one company's org chart as the entire industry.

Read underlying pages/documents and retain supporting passages or precise page/section locators. Search results and AI-generated summaries are discovery aids, not the evidence. Search using the industry's actual process and role terms, including exceptions, appeals, escalations and operational deadlines. Broaden or change the query when results are only vendor AI marketing.

For named customers, existing discovery can contribute stated pain points, transformation history and technology signals. This industry-architecture task does not require researching meeting attendees or calendars. Review/complaint/forum material can reveal possible pain themes but does not establish policy, prevalence or a customer's system architecture.

Prefer current operating evidence and record dates. Verify that a rule is effective and applies to the right region/entity rather than relying on the latest search ranking. Older durable process references may still be useful; identify their age and check material changes.

## 3. Map the value chain, operating pressures and boundaries

Describe the path from demand or request through service/product delivery, settlement/payment, ongoing support, exception handling and relevant closure/renewal. Adapt the lifecycle to the industry rather than imposing a retail purchase model.

For each major stage identify the external/internal actor, accountable business owner, work performed, key record, upstream/downstream dependency and intended result. Include suppliers, partners, field/local operations and outsourced functions where relevant. A cross-company or cross-department handoff should be visible.

Record the main operating pressures: time sensitivity, capacity, service levels, unit economics, quality, loss/rework and relevant regulatory exposure. Link these to stated evidence. Use metric definitions where measured values are unavailable; do not invent volumes, staffing ratios, savings or projected returns.

Output: an end-to-end value-chain map and a short account of the most consequential bottlenecks and industry differences. This determines what the OS needs to represent beyond customer service.

## 4. Establish departments, teams and real ownership

Map core industry operations, customer/partner-facing functions and corporate support functions. Explicitly consider Finance and Legal, plus relevant People/HR, IT, Procurement, Risk/Compliance, Security and Data. Show shared services as shared services; local and central teams may have different responsibilities.

For every department record its mission, owner role, teams, core activities, critical records/systems, upstream/downstream dependencies and relevant journeys. Explain meaningful omissions and uncertain ownership. Separate documented organizational facts from a proposed presentation hierarchy.

Translate work into proposed agent roles only after understanding it. Map business activities to agent capabilities, parent-agent skills, shared specialists and human decision boundaries. Do not create one AI worker for every employee title. Justify proposed role counts by process breadth and specialist needs rather than presenting them as actual headcount.

### Allocate the workforce by business importance

Size the workforce from the industry's value chain before filling department slots. A full industry OS should visibly concentrate specialist coverage where the business creates and delivers its product or service. Giving every department four agents, or another repeated quota, hides those priorities and is not an acceptable default.

1. Classify departments as **core business**, **enabling**, or **corporate support**, and identify the primary core departments. Explain each classification from its mission, customer/service or revenue impact, operational criticality, process breadth, exceptions and specialist decision boundaries. Use volumes only when evidenced; do not fabricate traffic or employee counts to justify importance.
2. Research core journeys first, then identify distinct workers needed across their stages and exceptions. Allocate substantially more specialist roles to the primary core departments. Reuse the same specialist across journeys; a skill, human gate or repeated journey appearance is not another worker.
3. Keep enabling and corporate support departments proportionate and compact. Group closely related capabilities into parent-agent skills and use shared specialists where responsibilities fit. The obligation to include HR, Finance or Legal does not mean they deserve the same number of workers as the main business.
4. Check the proposed distribution using unique workers: core business collectively holds more than half of the workforce; each primary core department has at least twice as many agents as any individual non-core department by default; and HR has strictly fewer agents than every core business department. The 2:1 rule is a design sanity check for substantial differentiation, not a claim about actual staffing or an automatic generator of roles. A near-even split such as five core agents versus four support agents does not meet that default.
5. If the distribution fails, revisit missing core workflow coverage, duplicate support roles, overly narrow worker definitions and mistaken classifications. Do not pad departments, relabel a support function as core, or invent specialists merely to pass the count checks. Record unresolved gaps as provisional rather than claiming the allocation is complete. An explicitly narrower user-requested scope takes precedence; a full-vertical launch does not imply such an exception.

For a telecom operator, network planning/buildout, network operations and assurance, service provisioning/activation, product/revenue operations and customer service journeys are candidates for core coverage, depending on the segment. Internal employee IT, HR and general procurement are supporting functions. Network operations must not be reduced to a small generic IT department while HR receives the same or more workers. These are classification examples, not a fixed department list or count template; a carrier, MVNO, infrastructure operator and equipment supplier need different models.

Record department classification, primary-core designation, importance rationale, distinct covered work, proposed count and share, consolidated skills, and sources/assumptions in a workforce allocation table. Report core versus non-core totals, the smallest primary core department versus the largest non-core department, and HR versus every core department. Use those counts in Agents, Org and filters, and feed them into the inherited proportional-sector geometry. Do not equalize ring sectors or add decorative workers to obtain symmetry.

Output: a department/team/ownership matrix and workforce allocation table with evidence and sizing rationale, plus the distribution check results. Feed them into the source OS's existing proportional-sector and positioning logic.

## 5. Research journeys stage by stage

Discover journeys across the value chain, not just conversational support. Consider service intake/onboarding, core delivery/operations, changes and exceptions, partner/supplier work, finance/settlement, legal/compliance, and internal employee/IT work where relevant.

Select journeys for importance to the industry and the audience. Use evidence of business impact, frequency where known, cross-team complexity, time sensitivity, unmet need and source strength. A source OS flow's convenience is not evidence that the journey matters. Avoid a fixed catalog count or invented precision in prioritization.

For each proposed catalog journey, create an architecture-level research card:

- Industry name, business purpose, customer/internal actor, trigger, preconditions and accountable team/role.
- The current process as understood from sources: each meaningful stage's task, performing role, input/evidence, system/record, output and next handoff.
- Cross-team/partner handoffs, why they occur, and the information that moves with them.
- Relevant decisions and their authority: what is checked automatically, where a person decides, and which evidence is needed.
- Important exceptions, missing information, escalation/rework loops and relevant timing dependencies. Label proposed or inferred exceptions when sources are silent.
- Intended outcome and useful KPI definitions, such as cycle time or first-pass completion, without unsupported numeric targets.
- Proposed agent/skill allocation and autonomy limits, clearly separated from evidence about current human work.
- Supporting sources, confidence, unresolved questions and candidate Banking/Retail source flow.

Investigate representative core journeys in each major function deeply enough to expose real stages, records and exceptions before expanding the catalog. Every displayed journey still needs an intelligible supported architecture; do not pad the list with name-only entries.

When sources do not reveal the internal process, mark the proposed sequence as a design assumption. Do not describe invented detail as a customer's SOP. Journey cards research what could be represented; they do not require synthetic cases, scripts, replay, execution branches or audit-history implementation.

## 6. Identify systems, data and decision boundaries

Map the systems of record and important entities to journey stages: what arrives, what is read, what could be updated and which system owns the resulting state. Capture meaningful lifecycle/status changes and relevant data availability or sensitivity constraints at architecture level.

Use separate labels for a confirmed customer system, an industry-common system category, an inferred technology signal, and a proposed integration. A job advertisement or vendor case study has a specific scope/date; do not overstate it. Naming a CRM category does not prove access or an available connector.

Research relevant legal, professional and policy boundaries for the actual segment and geography. Identify the specific action or decision affected, the source of authority, the responsible role and the architectural consequence. Do not add generic human gates for visual symmetry or treat a regulatory obligation as a blanket requirement for human review unless supported.

Differentiate law/regulation, professional guidance, company policy and an illustrative design threshold. A consequential rule needs primary-source support or a clearly recorded unresolved gap. Reading a public rule does not establish that a particular customer has configured the proposed control.

Output: a systems/records map and decision-boundary table linked to the relevant journey cards. This is design research, not integration configuration or legal sign-off.

## 7. Triangulate findings and expose uncertainty

Maintain a source register: source ID, title/publisher, exact URL/document locator, published/updated/effective date where available, access date, relevant segment/geography, supporting passage/locator and claims supported. Connect claim IDs or source IDs to departments, journeys and material adaptation decisions.

Label each important statement as **fact**, **inference**, **assumption** or **proposal**. Assign evidence confidence based on directness, authority, recency, applicability and independent corroboration, not on how many sites repeat the claim.

Cross-check material operating claims where possible. For consequential rules, use the authoritative primary source; seek corroboration where it meaningfully reduces ambiguity rather than imposing a two-source quota. Use independent operator/practitioner evidence to distinguish industry practice from a single supplier's marketing.

Record contradictions and resolve them by scope, jurisdiction, date and source authority. Do not silently merge different companies' procedures or incompatible rules. Where public evidence is thin, name the exact uncertainty and what customer document, role or answer would resolve it. Continue verified areas while affected entries remain provisional.

## 8. Map source reuse and test industry fit

Create this adaptation map for each target department/journey:

| Field | Meaning |
| --- | --- |
| Target | Industry department, team or journey |
| Source | Banking/Retail OS and specific file, catalog entry or flow |
| Treatment | Reuse unchanged; rename/reconfigure; adapt; or new |
| Retained structure | Components, stage order, branches, role pattern, node positions and routing |
| Required changes | Actors, tasks, records, systems, labels, owner, decision authority or meaningful new branches |
| Evidence/rationale | Supported reason the source process fits and why changes are needed |
| Status/gaps | Planned architecture or checked existing Active capability, with remaining uncertainty |

Reuse full topology and layout wherever the semantics fit. Finance, legal review, document collection, service requests, approvals and exceptions can share graphs across industries. Similar graphs are legitimate when the underlying decision structure matches.

For each important reuse decision, review:

1. Does the trigger represent a real need for this segment and actor?
2. Do the stage tasks, order and handoffs make operational sense?
3. Are records, system responsibilities and required information plausible and evidenced?
4. Do decision authority, escalation and exception loops fit the industry?
5. Can the team/owner reasonably perform or oversee the proposed work?
6. Does the outcome close the original business need, and is it measurable?
7. Can a domain owner recognize the process from its terms, records and constraints?

If only the labels changed, confirm why that is sufficient. Shared diagrams are welcome; unsupported domain claims are not. Change only the meaningful process gaps and preserve sphere geometry, component behavior and applicable source flow layout.

## 9. Review coverage and know when research is complete

Walk the architecture from the perspective of a front-line operator, function owner, Finance/Legal and an IT/system owner, using the evidence. This is an analytical review, not a claim that real subject-matter experts approved it. Check missing handoffs, invented departments, duplicate specialists, unsupported autonomy and important functions absent from the catalog.

Complete research when:

- The segment/business model and value chain are explicit, with core operations and relevant corporate functions covered.
- Departments have credible missions, ownership and importance-based role-sizing rationale. Core operations dominate the proposed workforce; primary core departments are substantially larger than individual support functions, HR is smaller than every core department, and allocation checks are recorded.
- Proposed journeys have stage-level substance, records, decisions, exceptions, outcomes and traceable support.
- Industry-common practices and named-customer facts remain separate.
- Important systems and consequential boundaries have credible support or visible provisional gaps.
- Material contradictions are resolved or recorded; critical unanswered questions are prioritized by their effect on the architecture.
- Every journey maps to a justified source-flow reuse/adaptation or a genuine new requirement.

Use targeted follow-up searches to close gaps. Do not stop after a broad company overview, one annual report or a list of AI use cases. Do not continue collecting repetitive pages after coverage is sufficient. Unresolved critical gaps prevent claiming the affected design is verified, not completing independent work or delivering a provisional draft.

## Output and model handover

Deliver one readable research workbook containing scope, industry/value-chain brief, evidence coverage, department/team matrix, journey cards, systems/decision maps, source register, reuse map and open questions. Keep detailed evidence notes separate only when useful. The result should explain why this OS fits the industry and exactly what the source OS supplied.

Adapt the existing canonical data model rather than adding a new framework. Resolve stable IDs across departments/teams, agents, parent-agent skills, journeys, gates and systems. Derive views, passports, ownership filters and counts from those records. Reuse specialist identity across journeys; keep proposed roles distinct from verified customer staffing.

New researched journey architectures remain Planned. Preserve Active only for existing implemented capability that remains valid and has been checked in context. Actual cases, conversations, integrations, replay/decision engines and audit history belong to each journey's separate demo-preparation task and are not research-completion requirements.
