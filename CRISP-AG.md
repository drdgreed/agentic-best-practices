<!-- GENERATED — do not edit.
     Derived by tools/derive_public.py from the internal edition.
     Regenerate with: python3 tools/derive_public.py
-->

# CRISP-AG — Comprehensive Risk & Implementation Standard for Practical Agentic Governance

**Public edition of v3.0** · Author: David Reed, PhD · Generated 2026-09-18

> This is a brand-neutral edition, published as general best-practice guidance. It
> carries no organisation-specific implementation detail. Draft-review front matter has been removed: the draft banner, the reviewer preamble, the reviewer question list, and the pre-publication decision list.

---

# What changed in v3.0

Each row records a material change from v2.4.1, why it was made, and the external source that motivated it. Rows are ordered by section. Changes that are purely editorial (renumbering, cross-reference updates) are not listed.

| **Section** | **Change** | **Why** | **External anchor** |
|----|----|----|----|
| Abstract; Exec. Summary; §1.1 | Seven artifacts (was four). Contributions list adds AIR, AISIA, WWIR. | Identity, ethics, and adoption had no producible artifact — the paper's own thesis applied to its gaps. | CSA/Strata 2026 \[24\]; ISO/IEC 42005 \[25\]; McKinsey 2026 \[29\] |
| Exec. Summary | 48% statistic reworded to match the Vanta survey question; 65% "use outpaces understanding" figure added. | Original wording overstated what the survey asked. | Vanta State of Trust 2025 \[15\] |
| Exec. Summary graphic; Figure 7 | Both graphics re-rendered (Draft 2): the statistic tile now carries the survey's own wording and the 65% figure; Figure 7 carries the corrected McKinsey source, drops the illustrative dollar amounts, and adds the §9.4 workforce-transition line. | Images had contradicted the corrected text. | Vanta 2025 \[15\]; McKinsey Oct 2025 \[13\] |
| §1 | Reference \[22\] split into three sources; 21% real-time-registry figure added. | Three surveys had been conflated into one citation. | \[22\] CSA/Workday; \[23\] Entro; \[24\] CSA/Strata |
| §1.2 | Claim-boundary standards row adds ISO/IEC 42005 and the OWASP Agentic Top 10. | Currency. | — |
| §2 | EU AI Act paragraph rewritten for the post-Omnibus timeline; ISO/IEC 42005 positioning added; OWASP "Least Agency" named. | The August 2026 high-risk timeline is no longer correct. | Digital Omnibus on AI \[31\] |
| §2.1 | Positioning matrix: three rows added (agent identity; affected-person impact; workforce adoption). | New artifacts. | — |
| §3.1 | Evidence-maturity rows added for the three artifacts; §5.1.3 and §6.3 evidence type restated as design proposal with external convergence. | Unnamed production-system claims removed. | CSA ATF v0.9.1 \[19\] |
| §4 | Note added: class is determined by behavior, not provenance; vendor-supplied agents are classified identically. | Vendor-agent track (§5.8). | IMDA MGF v1.5 \[21\] |
| §5.1.1 | Responsible AI / Privacy review level added to the approval matrix. | No ethics or privacy seat existed in the DAS. | ISO/IEC 42001 \[5\]; 42005 \[25\]; Colorado SB 26-189 \[26\] |
| §5.1.3 | Production-system reference removed; convergence with CSA ATF promotion gates and demotion rule documented instead. | Conflict-of-interest-safe evidence posture. | CSA ATF \[19\] |
| §5.1.4 (new) | DAS ↔ ATF crosswalk. | Two independently derived earned-autonomy models agree; worth recording. | CSA ATF \[19\] |
| §5.3 | Output schema extended with range/enum checks; degradation policy rolled up to pipeline level. | ASI08 cascading failures. | OWASP ASI08 \[17\] |
| §5.4 | Consequential-decision flag (§5.4.3); Figure 5 replaced by the promised horizontal spectrum with the flag as a band. | Regulated decision domains needed a structural autonomy cap, not a judgment call. | Colorado SB 26-189 \[26\]; EU AI Act Annex III \[6\] |
| §5.5 (new) | Agent Identity & Registry Record (AIR). | Answers "which agent instance, holding which credential, under which sponsor"; closes the ASI03 "partial". | NIST NCCoE \[27\]; IMDA v1.5 \[21\]; CSA AIGF \[28\]; OWASP ASI03 \[17\] |
| §5.6 (new) | AI System Impact Assessment (AISIA) aligned to ISO/IEC 42005, including a disclosure rule for affected persons. | Fairness, bias, affected persons, and impact assessment did not appear in v2.4.1. | ISO/IEC 42005 \[25\]; EU AI Act Art. 4, 50 \[6\]; Colorado \[26\] |
| §5.7 (new) | Workflow & Workforce Impact Record (WWIR) with reviewer-capacity model and adoption scorecard. | Change management was the only phase with no producible artifact. | McKinsey 2026 \[29\]\[30\]; RAND 2024 \[14\]; Verizon DBIR 2026 via CSA \[33\] |
| §5.8 (new) | Governing vendor-supplied agents: which artifacts the deployer still owns. | Bought-not-built deployments were under-treated. | IMDA v1.5 provider/deployer split \[21\] |
| §6, §6.1, §6.2 | Phase outputs and gate evidence updated for the three artifacts; Gate 2 adds reviewer capacity, adoption baseline, and a signed role-impact table. | Every artifact needs a phase and a gate. | — |
| §6.3 | Production-system reference removed; standing governance invariants presented as a design proposal. | As §5.1.3. | — |
| §7 | Three OWASP incident anchors added; ASI crosswalk updated (ASI03, ASI08, ASI09 now covered). | Currency. | OWASP Agentic Top 10 \[17\] |
| §7.2, §7.3 | Mitigations drafted for ASI08 and ASI09; remaining uncovered threats moved to §7.3; OWASP MCP Top 10 named for tool poisoning. | v2.4.1 promised these for v3. | OWASP \[17\]\[32\]; IMDA v1.5 automation-bias guidance \[21\] |
| §8.1 (new) | Human-side metrics: active-user ratio, reviewer behavior, automation-bias index, shadow-tool signal, impact-assessment currency. | All prior metrics were system metrics. | IMDA v1.5 \[21\]; McKinsey adoption playbook \[30\] |
| §9 | Reference \[13\] corrected; §9.4 workforce-transition cost added as a fourth, non-summed line; §9.5 renumbered. | Citation error; change-management cost was hidden inside the loaded hourly rate. | McKinsey Oct 2025 \[13\] |
| §10–§13 | Roadmap exit evidence, validation studies, limitations, and conclusion updated for seven artifacts. | Consistency. | — |
| Appendix A | Three artifact rows added. | — | — |
| Appendix B | B.5 adds Article 4 and Article 50 rows with the post-Omnibus timeline; B.7 updated; B.8 rows updated (IMDA v1.5, ATF v0.9.1, NIST deliverables) and CSA AIGF, OWASP MCP Top 10 added; new B.9 U.S. state and sector note. | Currency. | \[21\]\[19\]\[20\]\[28\]\[32\]\[26\]\[34\]\[35\] |
| References | \[13\], \[19\], \[20\], \[21\] corrected or updated; \[22\] split into \[22\]–\[24\]; \[25\]–\[36\] added. | — | — |

**Contents**


[What changed in v3.0](#what-changed-in-v3.0)

[Abstract](#abstract)

[Executive Summary for Practitioners](#executive-summary-for-practitioners)

[1. Introduction](#introduction)

[1.1 Contributions](#contributions)

[1.2 Claim boundary](#claim-boundary)

[2. Related Work and Positioning](#related-work-and-positioning)

[2.1 Positioning matrix](#positioning-matrix)

[2.2 Literature gaps to strengthen in future research and protocol guidance](#literature-gaps-to-strengthen-in-future-research-and-protocol-guidance)

[3. Methodology and Evidence Status](#methodology-and-evidence-status)

[3.1 Evidence maturity table](#evidence-maturity-table)

[3.2 Threats to validity](#threats-to-validity)

[4. Agent Class Taxonomy](#agent-class-taxonomy)

[5. Seven Core CRISP-AG Artifacts](#seven-core-crisp-ag-artifacts)

[5.1 Delegation Authority Scoping](#delegation-authority-scoping)

[5.2 Contractor Access Governance](#contractor-access-governance)

[5.3 Orchestration Contract](#orchestration-contract)

[5.4 Capability Frontier Taxonomy](#capability-frontier-taxonomy)

[5.5 Agent Identity & Registry Record](#agent-identity-registry-record)

[5.6 AI System Impact Assessment](#ai-system-impact-assessment)

[5.7 Workflow & Workforce Impact Record](#workflow-workforce-impact-record)

[5.8 Governing vendor-supplied agents](#governing-vendor-supplied-agents)

[6. The CRISP-AG Nine-Phase Lifecycle](#the-crisp-ag-nine-phase-lifecycle)

[6.1 Phase gates](#phase-gates)

[6.2 Per-class compressed tracks](#per-class-compressed-tracks)

[6.3 Standing invariants](#standing-governance-invariants)

[7. Security Architecture](#security-architecture)

[7.1 Security requirements by class](#security-requirements-by-class)

[7.2 Threats addressed in this revision: cascading failures and trust exploitation](#threats-addressed-in-this-revision-cascading-failures-and-trust-exploitation)

[7.3 Threats still not covered in this framework](#threats-still-not-covered-in-this-framework)

[8. Evaluation and Metrics](#evaluation-and-metrics)

[8.1 Human-side metrics](#human-side-metrics)

[9. ROI and Business Case Guidance](#roi-and-business-case-guidance)

[9.1 Capacity value (the formula)](#capacity-value-the-formula)

[9.2 Quality value](#quality-value)

[9.3 Risk reduction (qualitative)](#risk-reduction-qualitative)

[9.4 Workforce-transition cost (new in v3.0)](#workforce-transition-cost-new-in-v3.0)

[9.5 Why different evidence standards](#why-different-evidence-standards)

[10. Implementation Roadmap](#implementation-roadmap)

[11. Validation Agenda](#validation-agenda)

[12. Limitations](#limitations)

[13. Conclusion](#conclusion)

[Appendix A. Minimal Artifact Checklist](#appendix-a.-minimal-artifact-checklist)

[Appendix B. Standards Mapping Matrix](#appendix-b.-standards-mapping-matrix)

[B.1 Delegation Authority Scoping (DAS)](#b.1-delegation-authority-scoping-das)

[B.2 Contractor Access Governance (CAG / CAP)](#b.2-contractor-access-governance-cag-cap)

[B.3 Orchestration Contract](#b.3-orchestration-contract)

[B.4 Capability Frontier Map](#b.4-capability-frontier-map)

[B.5 Cross-cutting (CRISP-AG lifecycle)](#b.5-cross-cutting-crisp-ag-lifecycle)

[B.6 Phase-to-RMF function alignment](#b.6-phase-to-rmf-function-alignment)

[B.7 Mapping limitations](#b.7-mapping-limitations)

[B.8 Emerging 2026 agentic-specific frameworks](#b.8-emerging-2026-agentic-specific-frameworks)

[B.9 U.S. state and sector note](#b.9-u.s.-state-and-sector-note)

[References](#references)

\[Feng\] Feng, K. J. K., McDonald, D. W., Zhang, A. X. "Levels of Autonomy for AI Agents." arXiv:2506.12469, June 2025. Cited in §5.1.4 for the task-type descriptors.

# Abstract

Enterprise adoption of agentic artificial intelligence systems — multi-step, tool-calling, and sometimes multi-agent architectures built on large language models — is outpacing the operational governance artifacts needed to deploy them safely. This paper proposes CRISP-AG, an artifact-centered implementation framework for governed agentic AI deployment. CRISP-AG extends the lifecycle logic of CRISP-DM by adding three agentic-specific phases: Operational Context Assembly, Trust/Governance/Risk Architecture, and Iterative Refinement and Scale. It formalizes seven implementation artifacts that are under-specified in common AI governance and MLOps practices: Delegation Authority Scoping, Contractor Access Governance, Orchestration Contracts, Capability Frontier Classification, the Agent Identity & Registry Record, an AI System Impact Assessment aligned to ISO/IEC 42005, and the Workflow & Workforce Impact Record.

CRISP-AG is positioned as the implementation layer beneath management-system standards such as ISO/IEC 42001, impact-assessment guidance such as ISO/IEC 42005, and risk-management frameworks such as NIST AI RMF — not as a replacement for them. The standards establish what governance must achieve; CRISP-AG specifies what the producible artifacts look like.

The evidence base for this version is practitioner experience, structured framework comparison, and alignment with standards and security references, not a controlled empirical validation. Claims are therefore framed as design propositions and implementation guidance rather than proven causal effects. The paper concludes with a validation agenda for testing whether the proposed artifacts reduce deployment risk, improve auditability, and improve production readiness across domains.

**Keywords:** agentic AI; AI governance; LLM agents; multi-agent systems; agent identity; prompt injection; human-in-the-loop; impact assessment; change management; RAG evaluation; AI lifecycle; CRISP-DM; auditability.

# Executive Summary for Practitioners

CRISP-AG should be read as an implementation framework, not as a replacement for risk-management standards or legal compliance regimes. It sits beneath ISO/IEC 42001, ISO/IEC 42005, and NIST AI RMF, specifying the artifacts those frameworks require organizations to produce.

The core contribution is artifact design: each governance concern is converted into a document, schema, decision gate, or reviewable control. Version 3.0 extends that discipline to three concerns that earlier versions left at the level of principle — who the agent is (identity and registry), whom it affects (impact assessment), and who has to change how they work (workforce impact and adoption).

The most ambitious claims have been narrowed: CRISP-AG is proposed and structured, not yet empirically proven.

The framework is strongest for Class 2 and Class 3 enterprise agents: ReAct-style agents and orchestrated multi-agent systems with tool access.

Class 4 code-executing agents require additional security engineering, sandboxing, and red-team validation beyond the base CRISP-AG lifecycle.

Two structural ceilings apply regardless of measured performance: irreversible high-consequence actions cannot be promoted past HITL-REQUIRED (§5.1.2), and tasks that materially influence a consequential decision about a person — employment, housing, credit, insurance, education, health, legal status, essential services — cannot be promoted past HITL-REQUIRED either (§5.4.3).

The framework also explicitly acknowledges its scope limits: it does not address liability allocation between vendors and deploying enterprises, vendor selection, red-team execution methodology, or single-number ROI quantification.

<img src="./media/image2.png" style="width:5.39583in;height:2.15625in" />

*Context snapshot. In Vanta's 2025 State of Trust survey, 48% of organizations reported having developed frameworks to limit or define agent autonomy, while 65% said their use of agentic AI is outpacing their understanding of it \[15\].*

# 1. Introduction

Agentic AI differs from conventional predictive or generative AI applications because it can select tools, call APIs, retrieve operational context, coordinate sub-agents, and execute multi-step workflows. In conventional predictive deployments, a model normally produces an output that a human interprets before acting. In agentic deployments, the system may produce an action sequence and execute it against enterprise systems. That inversion changes the governance problem.

The scale of the gap is now measurable in identity terms, which is a sharper framing for a security audience than general AI-project failure statistics. Survey work published by the Cloud Security Alliance in 2026 finds non-human identities outnumber human identities by roughly 45:1 enterprise-wide \[22\]; research on cloud-native environments cited by the same body puts the ratio near 144:1 there \[23\]. A separate CSA survey of 285 security leaders, published with Strata Identity in February 2026, finds that only about 28% of organizations can trace a given agent's action back to an accountable human sponsor across all environments, only 21% maintain a real-time registry of active agents, and 68% require human-in-the-loop review but lack an architectural approach for delivering it \[24\]. Every artifact in this paper is, in one sense, an answer to those figures: the DAS ties an action to a named approver, the Orchestration Contract ties a sub-agent's behavior to a written specification, the CAP ties an agent's effective access to an accountable authorization scope, and — new in this version — the Agent Identity & Registry Record ties a running agent instance to a named human sponsor and a revocable credential. The governance gap is not abstract; it is a traceability gap at enterprise scale, and it is widening faster than headcount-based governance models can track.

The central premise of CRISP-AG is that agentic governance fails when it remains at the level of principles. Statements such as "keep humans in the loop" or "apply least privilege" are directionally useful but insufficient unless translated into concrete artifacts that can be reviewed, approved, tested, audited, and revised. CRISP-AG therefore defines governance as a lifecycle of producible artifacts. Version 3.0 applies that test to the framework itself: three concerns that earlier versions addressed only as principles — identity, impact on affected people, and workforce adoption — are converted into artifacts with schemas, phases, gates, and standards mappings.

This white paper adopts a deliberate claim boundary. The framework is not yet validated as causing better outcomes. It is a structured proposal derived from practitioner deployment experience, standards comparison, and recurring governance gaps observed in enterprise agentic systems. The appropriate next step is empirical validation through multi-site case studies and controlled comparisons.

<img src="./media/image3.jpg" style="width:4.39583in;height:2.29167in" />

*Implementation urgency. Organizational failure modes often dominate technical failure modes in AI initiatives \[14\].*

## 1.1 Contributions

**Delegation Authority Scoping (DAS):** a formal classification of every action an agent may technically perform into one of five autonomy positions. Structurally similar to a role-based access control table; the contribution is the *process* of producing it upstream of architecture with named cross-functional approval, and of re-evaluating it against live evidence.

**Contractor Access Governance (CAG):** an explicit Contractor Access Profile for enforcing data-access constraints in mixed FTE/contractor/vendor workforces.

**Orchestration Contract:** a formal specification artifact for each sub-agent in a multi-agent system, connecting implementation, testing, and auditability.

**Capability Frontier Taxonomy:** a task classification approach that links reliability, consequence, reversibility, and review protocol, with a consequential-decision flag that caps autonomy structurally.

**Agent Identity & Registry Record (AIR)** *(new in v3.0)*: a per-agent identity, sponsorship, credential-scope, and lifecycle record that answers which agent instance, holding which credential, under which human sponsor, is running right now.

**AI System Impact Assessment (AISIA)** *(new in v3.0)*: an ISO/IEC 42005-aligned assessment of who is affected by the agent, how, and what will be done about it — produced before architecture and refreshed on defined triggers, with a disclosure rule for affected persons.

**Workflow & Workforce Impact Record (WWIR)** *(new in v3.0)*: an as-is/to-be workflow with the agent's autonomy positions marked on each step, a role-impact table, a reviewer-capacity model, and an adoption scorecard, so that adoption is measured rather than assumed.

**CRISP-AG lifecycle:** a nine-phase implementation sequence that extends CRISP-DM with agentic-specific operational, governance, and post-deployment monitoring phases, with per-class compressed tracks (see §6.2) calibrated to agent class.

## 1.2 Claim boundary

| **Claim type** | **What this paper claims** | **What this paper does not claim** |
|----|----|----|
| Framework proposal | CRISP-AG defines a coherent artifact-centered lifecycle for agentic AI implementation. | That CRISP-AG has been statistically proven to outperform alternatives. |
| Practitioner evidence | The artifacts reflect recurring problems from enterprise deployment contexts. | That the observed problems have quantified population prevalence. |
| Standards alignment | CRISP-AG is the implementation layer beneath NIST AI RMF, NIST AI 600-1, ISO/IEC 42001, ISO/IEC 42005, EU AI Act obligations, and OWASP LLM and Agentic guidance — specifying the artifacts those frameworks require. | That CRISP-AG itself is a recognized standard or certification scheme, or that producing its artifacts constitutes legal compliance in any jurisdiction. |
| Thresholds | Suggested thresholds are practitioner-anchored starting targets calibrated against adjacent benchmarks. | That the thresholds are universally valid predictors of production success. |
| Scope | The framework addresses agentic AI implementation governance, including the deployer's obligations when the agent is vendor-supplied. | That it allocates legal liability, prescribes vendor selection, or replaces formal application security review. |

**Where each artifact lives in a reference implementation (§10.4).** Section identifiers are those of the Agentic PRD Standard; other implementations substitute their own.

| **Artifact** | **Lives in** |
|----|----|
| Delegation Authority Scope | Hub H8, with the six mandatory action-boundary rows of H9 at PROHIBITED; machine-readable in M |
| Contractor Access Profile | S3.2 role-capability matrix |
| Agent Identity & Registry Record | S3.1 and the enterprise registry entry |
| AI System Impact Assessment | S4.4 |
| Workflow & Workforce Impact Record | Summary in hub H5; full record as S5.6 |
| System landscape map | S1.4 |
| Tool specification | S1.4 |
| Orchestration Contract | S1 (written in the specification form) |
| Pipeline policy | S5.2 |
| Capability Frontier Map | S2.10 (frontier and graduation evidence) |
| Security threat model | S3.4 |
| Regression suite | S2.2 |

# 2. Related Work and Positioning

CRISP-AG occupies the implementation layer between high-level AI governance frameworks and low-level agent implementation libraries. Governance frameworks such as NIST AI RMF, NIST AI 600-1, ISO/IEC 42001, ISO/IEC 42005, and the EU AI Act establish risk-management, management-system, impact-assessment, and compliance expectations. Agentic implementation frameworks such as ReAct, AutoGen, and LangGraph establish implementation patterns for reasoning, tool use, and orchestration. CRISP-AG proposes implementation artifacts for the middle layer: what must be produced, approved, tested, and audited before an agentic system should operate in an enterprise environment.

**Positioning relative to ISO/IEC 42001.** ISO/IEC 42001 is an AI management system standard. It establishes that an organization must have controls for AI risk management, lifecycle integrity, and stakeholder accountability. It does not specify *what those controls should look like* in implementation terms. CRISP-AG specifies the artifacts that satisfy ISO/IEC 42001 obligations for agentic systems specifically: the DAS satisfies management-system clauses on accountability and risk treatment for delegated decisions; the CAP and the AIR satisfy data-classification, information-handling, and access-control clauses; the Orchestration Contract satisfies operational-control clauses for multi-agent systems; the Capability Frontier Map satisfies performance-evaluation and continual-improvement clauses; the WWIR satisfies competence, awareness, and resource clauses. The relationship is implementation-to-standard: an organization aligned with ISO/IEC 42001 uses CRISP-AG to produce the operational artifacts the standard requires it to maintain.

**Positioning relative to ISO/IEC 42005.** ISO/IEC 42005:2025 provides guidance — not certifiable requirements — for assessing the impacts of an AI system on individuals, groups, and society across the lifecycle, and is designed to sit beneath ISO/IEC 42001 as the impact-assessment discipline the management system calls for. Earlier versions of CRISP-AG did not cite it and, as a consequence, had no artifact in which fairness, bias, affected persons, or transparency to affected persons appeared. The AI System Impact Assessment in §5.6 adopts ISO/IEC 42005 as its anchor rather than inventing a bespoke ethics instrument.

**Positioning relative to NIST AI RMF.** NIST AI RMF organizes governance into four functions: Govern, Map, Measure, and Manage. CRISP-AG artifacts and phases align with each. DAS is primarily a Govern artifact (accountability, risk policy). CAP, AIR, and the impact assessment are primarily Map artifacts (operational context, third-party risk, affected parties). Orchestration Contracts are Measure artifacts (test specifications) that also serve Manage (audit and incident response). The Capability Frontier Map is a Measure artifact tied to Manage (verification protocol calibrated to risk). The WWIR is a Manage artifact (workforce and adoption treatment). Appendix B contains a more granular crosswalk.

**Positioning relative to OWASP.** OWASP LLM 2025 identifies attack surfaces; CRISP-AG specifies governance artifacts that address those surfaces (least-privilege scoping for LLM06 Excessive Agency; output gating for LLM05 Improper Output Handling and LLM01 Prompt Injection; data-tier constraints for LLM02 Sensitive Information Disclosure). The OWASP Top 10 for Agentic Applications 2026 \[17\] extends that list to agent-specific risks (ASI01–ASI10) and names *Least Agency* as its organizing principle — the term OWASP uses for what the DAS enforces at the action level. §7 carries an item-by-item crosswalk.

**Positioning relative to the EU AI Act.** The EU AI Act establishes regulatory obligations for AI systems; CRISP-AG produces the documentation and evaluation evidence those obligations require but do not themselves specify in operational form. The timeline matters for how the artifacts are used. The Digital Omnibus on AI, adopted by the European Parliament on June 16, 2026 and by the Council on June 29, 2026, and in force from July 27, 2026, deferred the stand-alone Annex III high-risk obligations to December 2, 2027 and the Annex I embedded-system obligations to August 2, 2028 \[31\]. It did not move the Article 4 AI-literacy duty, in force since February 2, 2025, or the Article 50 transparency obligations, which applied on August 2, 2026 as originally scheduled (the Article 50(2) machine-readable marking obligation for systems already on the market carries a grace period to December 2, 2026, and a new Article 5 prohibition applies from the same date). For a deployer today, therefore, Article 4 and Article 50 are the obligations *in force*, and Articles 9–17 for Annex III systems are the obligations *coming*. Appendix B.5 records both. The AISIA in §5.6 is where Article 50 disclosure and Article 4 literacy planning are recorded; the DAS, Orchestration Contract, and Capability Frontier Map remain the evidence base for Articles 9–17 when those apply.

The NIST Generative AI Profile is particularly relevant because it provides a cross-sector companion to the AI RMF for identifying and managing risks specific to generative AI. ISO/IEC 42001 is relevant because it specifies requirements for establishing, implementing, maintaining, and improving an AI management system. OWASP's LLM and Agentic guidance is relevant because prompt injection, excessive agency, sensitive information disclosure, and related risks become more consequential when an LLM has tool access.

**Narrowed novelty claim.** CRISP-AG does not claim that no prior work discusses delegation, human oversight, access control, identity, impact assessment, evaluation, or auditability. The DAS, in particular, is structurally similar to a role-based access control table — a pattern with decades of IAM lineage — and the AIR is structurally similar to a service-account inventory. CRISP-AG's contribution is not the table formats. It is the discipline of producing the artifacts *before* architecture design begins, with named cross-functional approval, as a constraint on the architecture rather than a retrofit, and of re-evaluating them against live evidence afterward. This narrowed claim is more defensible and matches the framework's actual contribution.

## 2.1 Positioning matrix

| **Dimension** | **High-level governance standards** | **Agent frameworks** | **CRISP-AG contribution** |
|----|----|----|----|
| Delegation authority | Principles for human oversight and risk management | Usually left to application design | Action-by-action autonomy classification artifact, produced upstream of architecture and re-evaluated on evidence |
| Mixed workforce access | General access-control and privacy expectations | Not usually modeled as a first-class agent concern | Contractor Access Profile and output constraints, produced before architecture |
| Multi-agent coordination | Rarely specifies sub-agent contracts | Provides orchestration mechanics | Orchestration Contract for implementation, testing, and audit |
| Capability frontier | Measurement and risk management guidance | Task benchmarks vary by implementation | Task classification linked to verification protocol, with a consequential-decision cap |
| Agent identity | Emerging: NIST NCCoE concept paper, IMDA v1.5, CSA ATF and AIGF call for verifiable agent identity | Service accounts or API keys, often shared | Agent Identity & Registry Record: one verifiable identity per agent, one named sponsor, scoped and expiring credentials |
| Impact on affected persons | ISO/IEC 42005 guidance; EU AI Act Art. 50; U.S. state ADMT laws | Not modeled | AI System Impact Assessment with a consequential-decision screen and a disclosure rule |
| Workforce and adoption | Competence and awareness clauses; Art. 4 literacy duty | Not modeled | Workflow & Workforce Impact Record with reviewer-capacity model and adoption scorecard, gated at Gate 2 |
| Lifecycle | Cross-cutting governance functions | Build-time implementation workflows | Nine-phase implementation lifecycle, with per-class compressed tracks |

## 2.2 Literature gaps to strengthen in future research and protocol guidance

AI auditability, assurance cases, and evidence management for ML/LLM systems.

Identity and access management models for agent-mediated workflows, including RBAC, ABAC, delegated authorization, workload identity (SPIFFE/SPIRE-style attestation), and policy enforcement points.

Human oversight taxonomies, the practical limits of human-in-the-loop review, and the measurement of automation bias in operational settings.

Agent evaluation benchmarks beyond RAG, including tool-use reliability, planning robustness, and multi-agent coordination failure modes.

Security literature on indirect prompt injection, excessive agency, confused deputy problems, sandboxing for code-executing agents, and tool-poisoning / supply-chain attack surfaces specific to agentic systems.

Organizational research on workflow redesign, role change, and skill degradation when agents absorb entry-level tasks.

# 3. Methodology and Evidence Status

This white paper uses a practitioner framework-development methodology. The process consisted of: (1) identifying recurring governance needs in enterprise agentic deployment contexts; (2) comparing those needs against existing lifecycle and governance frameworks; (3) converting high-level governance needs into producible artifacts; (4) organizing the artifacts into a lifecycle sequence; and (5) reviewing the resulting lifecycle against standards, security guidance, and practical deployability constraints. Version 3.0 added a sixth step: (6) verifying every emerging-framework citation and motivating statistic against its live source, and re-applying step (3) to the framework's own remaining principle-level statements.

Because this white paper does not present a controlled study, the methodology should be treated as design research / practitioner experience rather than empirical validation. The evidence is appropriate for proposing artifacts and explaining why they are needed. It is not sufficient to prove that the artifacts reduce incidents, accelerate deployment, or improve ROI.

## 3.1 Evidence maturity table

| **Artifact / claim** | **Current evidence type** | **Maturity** | **Needed validation** |
|----|----|----|----|
| Delegation Authority Scoping | Standards alignment + practitioner reasoning | Moderate conceptual maturity | Case studies showing fewer unauthorized actions or clearer sign-off decisions |
| Earned autonomy (§5.1.3) and standing governance invariants (§6.3) | Design proposal + independent convergence with CSA ATF promotion/demotion gates | Conceptually corroborated, outcome-unvalidated | Field data on promotion/demotion decisions and invariant firings |
| Contractor Access Governance | Structural risk analysis + practitioner observation | Promising but under-validated | Incident analysis and policy-enforcement tests in mixed workforces |
| Orchestration Contract | Software specification analogy + multi-agent deployment need | Strong artifact logic, weak outcome evidence | Ablation study comparing multi-agent systems with and without contracts |
| Capability Frontier Taxonomy | Benchmark-anchored thresholds + expert judgment | Useful but threshold-sensitive | Longitudinal studies across model updates and task domains |
| Agent Identity & Registry Record | Survey evidence of the gap \[24\]\[28\] + convergence of NIST, IMDA, CSA guidance | Well-motivated, schema untested at scale | Measurement of sponsor traceability and credential hygiene before/after adoption |
| AI System Impact Assessment | Standards alignment (ISO/IEC 42005) + regulatory requirement analysis | Externally anchored, framework-specific fields untested | Comparison of assessment completeness and downstream design changes |
| Workflow & Workforce Impact Record | Industry survey evidence on adoption failure \[14\]\[29\]\[30\] + practitioner reasoning | Well-motivated, under-validated | Adoption and override-rate outcomes with vs. without a signed WWIR |
| Nine-phase lifecycle | Derived artifact dependency graph | Coherent framework proposal | Comparative deployment study against MLOps-only or ad hoc governance processes |
| ROI model | Consulting-style scenario modeling | Useful practitioner aid | Prospective measurement of cycle time, adoption, quality, and risk outcomes |

## 3.2 Threats to validity

**Selection bias:** the framework was derived from a limited set of enterprise contexts and may overfit procurement, learning, and operational workflow automation.

**Construct validity:** terms such as "capability frontier", "governance intensity", and "adoption" require stronger operational definitions before controlled study.

**External validity:** regulated healthcare, finance, legal, and public-sector deployments may require additional controls not captured here.

**Measurement validity:** proposed thresholds are starting points and should not be treated as universal production criteria.

**Evidence limitation:** without case data, the framework should not be treated as a validated empirical model. In particular, the earned-autonomy mechanism (§5.1.3) and standing governance invariants (§6.3) are presented in this version as design proposals whose shape is corroborated by an independently developed external framework, not as reports of measured operating results.

# 4. Agent Class Taxonomy

Agentic systems should not receive a uniform governance treatment. A single-step tool-calling assistant and an autonomous code-executing agent create very different risks. CRISP-AG therefore uses a four-class taxonomy organized by governance consequence rather than implementation elegance.

<img src="./media/image4.jpg" style="width:5.60417in;height:4.19792in" />

*Figure 1. Agent type taxonomy decision tree.*

| **Class** | **Agent type** | **Definition** | **Primary governance risk** | **Minimum CRISP-AG intensity** |
|----|----|----|----|----|
| 1 | Single-step tool-calling | The LLM may call one or more tools in a single invocation, but there is no autonomous loop and humans review outputs before action. | Output quality, hallucination, weak evidence citation. | Basic: DAS, output review, data handling, simple evaluation, impact screen. |
| 2 | ReAct-loop agent | The system performs iterative reasoning and tool use until a goal or step limit is reached. | Scope creep, loop divergence, unintended tool sequences. | Standard: DAS, AIR, CAP where relevant, step limits, HITL triggers, evaluation suite, impact assessment, WWIR. |
| 3 | Hierarchical multi-agent | An orchestrator delegates to specialized sub-agents across systems or tasks. | Emergent coordination failures, audit fragmentation, contract gaps, cascading failures. | Enhanced: Orchestration Contracts, per-agent identity and permissions, cross-agent audit trail, pipeline circuit breaker. |
| 4 | Autonomous code-executing | The agent generates or executes code, or can alter production state — a system of record, deployed configuration, or anything a human or downstream system acts on without further review. Writes confined to a sandbox or staging area under deny-by-default production-write restrictions and human promotion do not make an agent Class 4; such an agent is classified by the remaining tests but carries the Class 4 write controls (sandboxing, production-write restrictions, qualified red-team review of the write path). | Irreversible actions, privilege escalation, sandbox escape, data exfiltration. | Critical: all Class 3 controls plus sandboxing, red team review, production-write restrictions. |

**Decision logic:** If the agent does not execute multiple autonomous reasoning/action steps, classify as Class 1. If it can execute code or alter production state directly, classify as Class 4. If its writes are confined to staging under the Class 4 write controls, continue to the next test and record ‘Class 4 write controls carried’ in the AIR. If it coordinates two or more role-distinct agents, classify as Class 3. Otherwise, an extended autonomous loop with tool calls is Class 2.

**Provenance does not change class.** An agent embedded in a vendor product — a work-order triage assistant in a facilities platform, an invoice-exception agent in an accounts-payable suite, a research assistant in a productivity suite — is classified by what it does, not by who built it. A vendor agent that loops over tools is a Class 2 agent; one that writes to a production system of record is a Class 4 agent. §5.8 specifies which artifacts the deployer still owns in that case.

# 5. Seven Core CRISP-AG Artifacts

Versions through 2.4.1 specified four artifacts. Version 3.0 adds three. The test for adding an artifact is the paper's own thesis: a governance concern that is stated as a principle but has no schema, no phase, no gate entry, and no standards mapping is a concern the framework does not actually govern. Identity, impact on affected persons, and workforce adoption failed that test. Each new artifact below receives the same treatment as the DAS: a minimum schema, the phase in which it is produced, the gate at which it is checked, and the standards it maps to.

## 5.1 Delegation Authority Scoping

Delegation Authority Scoping converts autonomy into an approval artifact. Let A be the set of actions the agent can technically perform. DAS is a function mapping each action to one of five classes: PROHIBITED, HUMAN-ONLY, HITL-REQUIRED, AGENT-DIRECTED, and FULLY-AUTONOMOUS. A valid DAS is complete, approved by accountable stakeholders at appropriate levels, and technically enforceable.

The DAS structure resembles a role-based access control table. This is intentional. The contribution is not the table format but the discipline of producing it as a governance artifact upstream of architecture: cross-functional sign-off before implementation, used as an architectural constraint rather than retrofitted to a built system.

<img src="./media/image5.jpg" style="width:5in;height:2in" />

*Figure 2. Delegation Authority Spectrum for action-level scoping of human control and agent autonomy.*

| **DAS class** | **Meaning** | **Technical enforcement expectation** | **Example procurement action** |
|----|----|----|----|
| **PROHIBITED** | Agent may not perform or assist execution. | Remove tool/API path or block at policy enforcement layer. | Waive compliance requirement. |
| **HUMAN-ONLY** | Agent may research or draft; human decides and executes. | No execution tool exposed to agent. | Contract negotiation strategy. |
| **HITL-REQUIRED** | Agent may prepare action; qualified human must approve before execution. | Approval workflow required before tool call. | Vendor approval. |
| **AGENT-DIRECTED** | Agent may execute within bounds; human reviews output or sample. | Telemetry, SLA review, rollback path. | Qualification recommendation. |
| **FULLY-AUTONOMOUS** | Agent may execute without per-instance review. | Telemetry and automated monitoring; only reversible low-consequence actions. | Document fetch or validation. |

### 5.1.1 Required approval levels by autonomy class

A complete DAS specifies *which* Legal, Operations, Executive, and — new in this version — Responsible AI / Privacy approvers signed each action's classification, at what review level. Generic "Legal approved" attestations are insufficient for audit and provide no escalation discipline. The Responsible AI / Privacy column exists because an ISO/IEC 42001-aligned enterprise already has that seat, and because the consequential-decision flag (§5.4.3) and the impact assessment (§5.6) need an approver who is accountable for them. The recommended calibration: An implementation's delivery workflow must seat a Legal reviewer for the PROHIBITED and HUMAN-ONLY rows; where no Legal role exists in the workflow's RACI, the DAS is incomplete.

| **Autonomy class** | **Required Legal review level** | **Required Operations review level** | **Required Executive level** | **Required Responsible AI / Privacy review level** |
|----|----|----|----|----|
| PROHIBITED with regulatory waiver, statutory non-compliance, or material legal exposure | General Counsel or designated equivalent | Operations VP with compliance ownership | Executive Sponsor at officer level | Responsible-AI lead confirms the prohibition rationale at initial classification. |
| HUMAN-ONLY with contract decisions, negotiation positioning, or executory commitments | Contracting counsel or commercial Legal | Operations leader for the affected workflow | Executive Sponsor | Privacy Officer where the research or draft touches personal data; otherwise not required. |
| HITL-REQUIRED in regulated workflows (financial services, healthcare, government contracting) or with the consequential flag set | Compliance officer with domain expertise | HITL operations leader with SLA accountability | Executive Sponsor | Responsible-AI lead or Privacy Officer at initial approval and on any consequence-class change; mandatory where the consequential flag (§5.4.3) is set. |
| AGENT-DIRECTED in documented regulated workflows | Compliance officer review | Operations leader for the workflow | Executive Sponsor | Privacy Officer at initial approval where personal data is processed; impact-assessment currency (§8.1) checked at each evidence review. |
| FULLY-AUTONOMOUS reversible operations | Compliance officer review at initial DAS approval; subsequent review only on consequence change | Operations leader review at initial approval | Executive Sponsor | Impact-assessment screen confirms no affected-person consequence; no further review unless the screen result changes. |

The DAS template therefore includes per-action columns recording: action name, autonomy class, technical enforcement mechanism, Legal approver name and review level, Operations approver name and review level, Responsible AI / Privacy approver name and review level, Executive Sponsor name, consequential flag (§5.4.3), approval date, rationale, evidence-review cadence, and the accountable reviewer for promotion/demotion decisions (§5.1.3). Without these columns the DAS provides poor evidence in audit and creates ambiguity about who is accountable for which classification decisions.

### 5.1.2 The governing rule on reversibility and consequence

Irreversible actions require at minimum HITL-REQUIRED. High-consequence irreversible actions require HUMAN-ONLY. Performance is not the deciding factor; reversibility and consequence are. An agent performing well on an irreversible high-consequence action does not justify AGENT-DIRECTED classification — what matters is what happens when the agent gets the action wrong.

### 5.1.3 Earned, not just assigned

The DAS as specified above is a design-time artifact: autonomy positions are classified and approved before architecture begins, then enforced. That is necessary but not sufficient. A defensible DAS should also be *revisited against live evidence* on a defined cadence, rather than treated as permanent once signed.

The refinement: for each action, track a rolling evidence record — sample size, pass rate against defined success criteria, and incident history — and gate promotion or demotion between autonomy positions on that record rather than on the original design-time judgment alone. A HITL-REQUIRED action with a long, clean evidence history is a candidate for promotion review toward AGENT-DIRECTED; an AGENT-DIRECTED action whose pass rate drops below its threshold should be *automatically* demoted pending review, not left at its original classification until someone notices a problem.

This design is not unique to CRISP-AG. The Cloud Security Alliance's Agentic Trust Framework \[19\], developed independently and published as a v0.9.1 public-review draft in April 2026, arrives at the same shape: four autonomy levels (Intern, Junior, Senior, Principal); promotion gated on demonstrated accuracy over an evaluation period, a security audit, positive impact, a clean incident history, and explicit stakeholder approval; and a rule that a critical incident triggers immediate demotion to the lowest level. Two independently derived models converging on "earned, not assigned, and automatically revoked" is not evidence that the mechanism improves outcomes — that remains on the validation agenda in §11 — but it is a reason to treat the mechanism as the default rather than an option. §5.1.4 records the crosswalk.

The ceiling on autonomy remains capped by consequence class — no amount of evidence promotes an irreversible high-consequence action past HITL-REQUIRED, consistent with §5.1.2 — and, new in this version, by the consequential-decision flag in §5.4.3. The point is not that any specific tooling should be adopted; it is that DAS classifications age, and a framework that only specifies design-time assignment without a re-evaluation mechanism will drift out of sync with what the agent has actually demonstrated.

Practically: the DAS template carries two additional columns — evidence-review cadence (e.g., quarterly, or triggered by N executions) and the accountable reviewer for promotion/demotion decisions. Automatic demotion triggers should be technically enforced at the same policy-enforcement layer that enforces the classification itself, not left to a human noticing a dashboard. The promotion ledger (attempts, passes, and current position per action) is itself an audit artifact and should be retained under the same policy as the DAS.

### 5.1.4 Crosswalk: DAS positions and CSA ATF levels

The ATF assigns a level to an *agent*; the DAS assigns a position to an *action*. An agent may therefore hold different DAS positions for different actions while carrying a single ATF level. The Agent Identity & Registry Record (§5.5) records the ATF level; the DAS records the per-action positions. The mapping below is a mapping of intent, not a claim that the boundaries are defined identically.

| **ATF level** | **ATF meaning** | **Nearest DAS position** | **Note** |
|----|----|----|----|
| **Intern** | Observe and report; continuous human oversight | HUMAN-ONLY | Default at creation in both models. An agent's first AIR entry carries ATF level Intern. |
| **Junior** | Recommend and approve; humans approve all actions | HITL-REQUIRED | Ceiling for irreversible high-consequence actions (§5.1.2) and for consequential-decision tasks (§5.4.3). |
| **Senior** | Act and notify; post-action notification | AGENT-DIRECTED | Requires telemetry, SLA review, and a rollback path. |
| **Principal** | Autonomous; strategic oversight only | FULLY-AUTONOMOUS | Under the DAS, only reversible low-consequence actions ever reach this position. |
| **—** | No ATF equivalent | PROHIBITED | The DAS removes the tool path entirely; the ATF has no "never" level. This is the one place the two models differ in kind. |

**Task-type descriptors (Feng, McDonald & Zhang \[Feng\]).** A third vocabulary describes the human–agent interaction mode per task type — operator, collaborator, consultant, approver, observer. It maps onto the table above as follows: *operator* and *collaborator* → HUMAN-ONLY (Intern); *consultant* → HITL-REQUIRED (Junior); *approver* → AGENT-DIRECTED (Senior); *observer* → FULLY-AUTONOMOUS (Principal); PROHIBITED has no equivalent. These descriptors remain useful in the WWIR's role-impact table (§5.7); they are not an approval or enforcement vocabulary and should not be used as one. Note the temporal trap: Feng's *approver* denotes human approval *after* the agent acts, whereas HITL-REQUIRED denotes approval *before* execution.

## 5.2 Contractor Access Governance

Contractor Access Governance addresses a specific confused-deputy risk: an agent may possess access rights that exceed the rights of the contractor or vendor user invoking it. If the agent returns confidential outputs to a contractor because the agent can access the underlying system, the organization has created agent-mediated access escalation.

<img src="./media/image6.jpg" style="width:4.60417in;height:2.40625in" />

*Figure 3. The Contractor Access Gap: agent-mediated access can bypass individual authorization levels unless explicitly constrained.*

**Minimum Contractor Access Profile schema**

| **Field** | **Required content** | **Default** |
|----|----|----|
| **Contractor category** | Role, vendor, region, contract type, start/end dates. | No inherited access. |
| **Permitted systems** | Explicit list of systems/tools callable in contractor-invoked sessions. | None. |
| **Permitted data tiers** | Data tiers that may be read, reasoned over, and surfaced. | Tier 1 only. |
| **Output constraints** | Fields or categories forbidden in user-facing outputs. | Do not surface Tier 2/3 verbatim. |
| **Prompt visibility** | Whether contractor can inspect or export system prompt/policies. | Redacted. |
| **Offboarding** | Credential revocation and audit review process. | Immediate revocation at contract end. |

The architectural rule that closes the gap: the agent's effective access for any session is the *intersection* of the agent's technical access and the invoking user's authorization scope, not the union. The Agent Identity & Registry Record (§5.5) records the agent side of that intersection; the CAP records the invoking-user side. Contractor Access Profiles are produced before architecture design begins because the existence of contractors in scope changes what tools and data the agent can surface, and the architecture must be constrained by the CAP rather than retrofitted.

## 5.3 Orchestration Contract

The Orchestration Contract is the specification for a sub-agent. It is simultaneously an implementation artifact, a test artifact, and an audit artifact. It reduces ambiguity in Class 3 systems by specifying each sub-agent's role, input/output schemas, data-tier constraints, failure modes, HITL triggers, latency SLA, and logging obligations.

<img src="./media/image7.jpg" style="width:4.60417in;height:2.39583in" />

*Figure 4. The Orchestration Contract: a shared implementation, testing, and audit artifact for multi-agent systems.*

**v3.0 extension for cascading failures (OWASP ASI08).** Two fields are strengthened. The *output schema* now carries expected ranges and enumerations — not just types — so that each downstream hop can validate upstream output against its expected distribution and reject out-of-range results rather than treat them as valid input. The *failure modes* field now specifies a degradation policy per failure type (retry / degrade / abort), and the set of contracts in a pipeline rolls up to a pipeline-level policy with a blast-radius budget: the maximum number of downstream actions that may proceed on unvalidated upstream output before a mandatory human checkpoint. §7.2 specifies the halt-the-line rule that operates on these fields.

**Sample Orchestration Contract excerpt**

| **Element** | **Example: Sanctions Screening Sub-Agent** |
|----|----|
| **Role** | Check candidate vendors against approved sanctions-screening sources and return a structured risk status. |
| **Input schema** | vendor_name: string; country: ISO-3166 code; tax_id: optional string; source_context_id: string. |
| **Output schema** | status: enum {clear, possible_match, confirmed_match, error}; confidence: 0–1; evidence_refs: array; data_tier: Tier 1/Tier 2. |
| **Output validation (new)** | confidence must lie in \[0, 1\]; status must be a member of the enumeration; evidence_refs must be non-empty whenever status ≠ error. A downstream hop that receives a violating output rejects it and counts one unit against the pipeline blast-radius budget. |
| **HITL triggers** | status in {possible_match, confirmed_match}; confidence \< 0.85; source unavailable; conflicting records. |
| **Failure modes and degradation policy** | API timeout: retry twice, then escalate. Schema violation: abort this hop. Source unavailable: degrade to possible_match with human review. Pipeline-level: after three degraded hops in one run, halt the line (§7.2). |
| **Data constraints** | May read approved sanctions databases; may not surface raw Tier 3 identifiers in contractor sessions. |
| **Latency SLA** | P95 ≤ 30 seconds for API response plus evidence normalization. |
| **Audit log** | Record input hash, source version, tool call IDs, response status, escalation result, model version, and the agent identity (AIR ID, §5.5) under which the call ran. |

## 5.4 Capability Frontier Taxonomy

The Capability Frontier Taxonomy classifies tasks by specifiability, observed performance, error consequence, and reversibility. It is not intended to make broad claims about model intelligence. It is an operational classification that determines the review protocol for a task in a specific deployment context.

<img src="./media/image8.png" style="width:6.30208in;height:3.41667in" />

*Figure 5. Capability Frontier spectrum: the four positions ordered by suitability for delegation, with the default verification protocol beneath each and the consequential-decision flag drawn as a band because it applies regardless of position. Replaces the 2×2 quadrant used through v2.4.1.*

| **Position** | **Criteria** | **Default verification protocol** | **Re-evaluation trigger** |
|----|----|----|----|
| **Within Frontier** | Task is fully specifiable; performance is strong on domain-representative tests; errors are detectable and reversible. | 10–30% spot-check and automated monitoring. | Every model update or material corpus/tool change. |
| **Frontier Edge** | Task requires judgment, performance is variable, or errors carry legal/financial consequence. | 50–100% expert review; HITL mandatory. | Every model update plus any adverse incident. |
| **Outside Frontier** | Task cannot be sufficiently specified or performance is below acceptable threshold. | Human-authored final decision; agent may provide research only. | Explicit governance committee review. |
| **Unsuitable** | Task requires empathy, live social judgment, physical presence, or non-delegable legal authority. | Never delegate. | Normally permanent unless legal/organizational policy changes. |
| **Consequential flag (any position)** | Task materially influences a consequential decision about a person (§5.4.3). | Capped at HITL-REQUIRED; impact assessment mandatory; disclosure to affected persons; records retained. | Any frontier re-evaluation trigger, plus any change in the decision the task feeds. |

### 5.4.1 Threshold framing

Suggested benchmark-related cutoffs (such as 85% performance for Within Frontier classification, 60% for the boundary between Frontier Edge and Outside Frontier, and 10–30% spot-check rates for Within Frontier tasks) are *anchored* to RAG benchmarks such as CRAG (Yang et al., 2024) and FaithJudge (Bao et al., 2025). They are not *derived* from those benchmarks in a rigorous statistical sense. State-of-the-art RAG systems achieve approximately 63% hallucination-free response rates on general-domain questions, so an 85% threshold represents performance meaningfully above SOTA. This is the basis for the threshold; it is not equivalent to a validated production-readiness criterion.

These thresholds are practitioner-anchored starting points. Each deployment must calibrate them against task consequence, false positive/negative cost structure, and review capacity — and §5.7 now specifies how review capacity is measured. An 85% threshold may be too low if false-positive cost is severe. It may be too high if the domain is harder than the benchmarks measure. The thresholds should be argued *down* from based on local conditions, not defended as universal values.

### 5.4.2 Visualization note

The 2×2 quadrant used through v2.4.1 has been replaced by Figure 5, the horizontal spectrum promised in earlier revisions. The four positions are not orthogonal coordinates on specifiability and consequence axes; they are positions on a single suitability-for-delegation spectrum, with reliability and consequence as influencing factors. Figure 5 orders them left-to-right by suitability, stacks the verification protocol beneath each, and draws the consequential-decision flag as a band across the spectrum because the flag applies regardless of position. The classification logic in the table above is unchanged.

### 5.4.3 The consequential-decision flag

Some tasks are governed by what they feed rather than by how well the agent performs them. A task that *materially influences* a consequential decision about a person — a decision that affects access to or the terms of employment, housing, credit or lending, insurance, education, health care, legal status, or essential government services — carries a flag that is orthogonal to the four frontier positions. The domains listed are those named in Colorado SB 26-189 \[26\] and overlap substantially with EU AI Act Annex III \[6\]; deployers in other jurisdictions should extend the list to match local law.

The flag imposes four structural requirements. First, **an autonomy ceiling**: no action within a flagged task may be classified above HITL-REQUIRED, regardless of measured pass rate — the same ceiling logic §5.1.2 applies to irreversibility, applied here to consequence for the affected person. Second, **a mandatory impact assessment** (§5.6) with a fairness and bias testing plan proportional to the decision. Third, **a Responsible AI / Privacy approver** on the DAS (§5.1.1). Fourth, **disclosure and records**: affected persons receive notice under §5.6.2, and the decision record — inputs, agent output, human reviewer, outcome — is retained for at least the period local law requires (three years under Colorado SB 26-189).

"Materially influences" is read broadly on purpose. A recommendation, score, ranking, or shortlist that a human then adopts is within scope, because the failure mode the flag guards against is not the agent deciding but the human deferring — the automation-bias problem that §7.2 and §8.1 address. The flag is set during the impact-assessment screen in Phase 1, recorded on the DAS and the AIR, and re-evaluated on every frontier re-evaluation trigger and whenever the downstream decision changes.

## 5.5 Agent Identity & Registry Record

The Agent Identity & Registry Record (AIR) answers the question the other artifacts do not: *which agent instance, holding which credential, under which human sponsor, is running right now — and until when?* The DAS answers who approved an action class; the CAP answers what an invoking contractor may see; the Orchestration Contract answers what a sub-agent is specified to do. None of them identifies the running agent. That gap is why ASI03 (Agent Identity & Privilege Abuse) was marked "partial" in the v2.4.1 crosswalk, and it is the gap the market has converged on: only 21% of organizations maintain a real-time registry of active agents and 28% can trace agent actions to a human sponsor across all environments \[24\]; 78% have no documented policy for creating or removing agent identities \[28\]. NIST's NCCoE concept paper proposes applying OAuth 2.0, OpenID Connect, and SPIFFE/SPIRE-style workload identity to agents as distinct non-human identities \[27\]; IMDA v1.5 requires verifiable agent identity and an audit trail of which agent acted under whose authorization \[21\]; the CSA Agentic Trust Framework's first question of any agent is "Who are you?" \[19\].

**Minimum Agent Identity & Registry Record schema**

| **Field** | **Required content** | **Default** |
|----|----|----|
| **Agent ID** | Unique, cryptographically verifiable identity distinct from any human account and from any other agent (a workload identity per NIST NCCoE / SPIFFE-style attestation, or the platform's equivalent — for example one service principal per agent). | Required for Class 2+; recommended for Class 1. |
| **Human sponsor** | Named accountable individual — not a team mailbox or distribution list — who answers for the agent's actions. | Required, all classes. |
| **Class and DAS pointer** | Agent class (§4) and the DAS version, with approval date, the agent operates under; consequential flag if set. | Required. |
| **Class 4 write controls carried** | Whether the agent carries the Class 4 write controls — sandboxing, production-write restrictions, and qualified red-team review of the write path — without being Class 4 (§4 Draft 4 qualifier). | yes / no. Required wherever the agent writes to any sandbox or staging area. |
| **Credential scope** | Systems, tools, and data tiers the agent's credential can reach; the intersection rule with the invoking user (§5.2). | Least privilege; no shared or static credentials; secrets held in a managed vault, never in prompts or code. |
| **Provenance** | Built internally or vendor-supplied; vendor and product where applicable (§5.8); model provider and version. | Required. |
| **Lifecycle** | Provisioning approver and date; review cadence; retirement trigger; offboarding steps including credential revocation and log retention. | Auto-expire on sponsor change or departure, or after 90 days of inactivity; retirement is a logged decision (§6.3), never a silent deletion. |
| **ATF level (optional crosswalk)** | Intern / Junior / Senior / Principal per §5.1.4. | Intern at creation. |
| **Audit anchor** | Where the agent's action log lives, what it records (at minimum: AIR ID, invoking user, tool call IDs, DAS position invoked, HITL decision if any), and the retention period. | Per Orchestration Contract audit specification; retention at least the longest applicable regulatory period. |

**Rules the record enforces.** One identity per agent, never shared across agents or with a human. One named sponsor per agent; when the sponsor leaves or changes role, the credential expires until a new sponsor is recorded. Credentials are scoped and short-lived; a long-lived static API key in an agent's configuration is a registry violation, not a convenience. Inactivity suspends, and reactivation requires the sponsor's approval. Retirement is a logged governance decision with the same evidentiary weight as provisioning.

**The registry is also an inventory.** The set of AIR entries is the organization's enumeration of every agent in or near production, and its completeness is itself a governance metric: an agent discovered running without an AIR entry is a finding in the same sense as an unregistered service account. For an organization early in its agentic adoption, producing the registry — every inventoried agent assigned a named sponsor — is the single fastest way to move past the 28% traceability benchmark, and it can be done before any other artifact is complete.

**Phase and gate.** The AIR is created in Phase 2 (Operational Context Assembly) when the agent's scope is first defined, and activated — credential issued — at Gate 1. It is updated at every DAS re-evaluation, sponsor change, or credential-scope change, and closed at retirement. For Class 1 agents on the compressed track (§6.2), a reduced record (ID, sponsor, class, provenance, retirement trigger) is produced in Phase 1.

**Standards mapping**

| **Standard / framework** | **Section** | **Mapping** |
|----|----|----|
| NIST NCCoE concept paper \[27\] | Agent identity and authorization | Direct: the AIR is the record of the per-agent identity and delegated authorization the concept paper describes. |
| IMDA MGF for Agentic AI v1.5 \[21\] | Verifiable agent identity; audit trail of which agent acted under whose authorization | Direct. |
| CSA Agentic Trust Framework \[19\] | "Who are you?"; maturity level per agent | Direct: the ATF level field. |
| CSA Agent Identity Governance Framework \[28\] | Identity creation, ownership, and removal policy | Direct: sponsor, lifecycle, and offboarding fields. |
| OWASP Agentic Top 10 \[17\] | ASI03 Agent Identity & Privilege Abuse | Direct: closes the v2.4.1 "partial". |
| ISO/IEC 42001 \[5\] | Annex A controls (access control, asset inventory, third-party) | Direct: the AIR is the asset inventory and access-control record for agents. |
| NIST AI RMF 1.0 \[3\] | Govern 1.1; Map 1.1 | Direct: accountable owner and system context per agent. |
| EU AI Act \[6\] | Article 12 (record-keeping), Article 26 (deployer obligations) | Approximate: the audit-anchor field supports these obligations when they apply. |

## 5.6 AI System Impact Assessment

The AI System Impact Assessment (AISIA) answers: *who is affected by this agent, how, and what will we do about it — before architecture.* Earlier versions of CRISP-AG treated ethics implicitly — the Unsuitable position, the reversibility rule, and the claim-boundary discipline are all ethical commitments in operational clothing — but the words fairness, bias, discrimination, affected persons, and impact assessment did not appear. A framework positioned as the implementation layer beneath ISO/IEC 42001 cannot leave out ISO/IEC 42005:2025 \[25\], which is precisely the standard that operationalizes impact assessment at the system level. The AISIA adopts it rather than inventing a bespoke ethics instrument, and adds the agent-specific fields the standard's general guidance does not name.

### 5.6.1 Minimum contents

| **Element** | **Required content** | **Proportionality** |
|----|----|----|
| **System description and intended use** | What the agent does, for whom, in which workflow; agent class; DAS pointer; AIR pointer. | All classes. |
| **Affected parties** | Users; subjects of decisions or recommendations; workers whose roles change (cross-reference the WWIR, §5.7); third parties including contractors, vendors, and customers of customers. | All classes. |
| **Consequential-decision screen** | Does any task materially influence a decision in the domains listed in §5.4.3? If yes, the flag is set on the DAS and AIR, and the remaining elements are mandatory at full depth. | Screen for all classes; full depth when flagged. |
| **Foreseeable impacts** | Benefits and harms to each affected party, including erroneous output, unequal performance across groups, exclusion, loss of recourse, and over-reliance. ISO/IEC 42005 categories. | Depth scales with consequence. |
| **Fairness and bias testing plan** | Which outputs are tested, across which groups, with what metric and threshold, on what cadence; who reviews results. | Mandatory when flagged; recommended otherwise. |
| **Transparency and disclosure plan** | How affected persons learn an agent is involved (§5.6.2): EU AI Act Art. 50 disclosures; state-law pre-use notice; adverse-decision explanations. | Mandatory when flagged or when Art. 50 applies. |
| **AI-literacy plan** | What the people who operate, review, or are informed by the agent need to know (EU AI Act Art. 4 for EU staff); cross-reference the WWIR training plan. | All classes. |
| **Worker-impact statement** | Roles created, changed, and removed; reviewer-monitoring disclosure (§8.1); skill-degradation risk where the agent absorbs entry-level tasks. | All classes; detail from the WWIR. |
| **Environmental note** | Material compute or energy consequences of the deployment, where relevant. | Where material. |
| **Mitigations and owners** | For each significant impact: the control, the CRISP-AG artifact that carries it, and a named owner. | All classes. |
| **Re-assessment triggers** | The frontier re-evaluation triggers (§5.4) plus any change in affected parties, decision domain, or jurisdiction. | All classes. |
| **Approvals** | Responsible AI / Privacy approver (§5.1.1); Legal where flagged; Executive Sponsor. | All classes. |

### 5.6.2 Disclosure rule for affected persons

CRISP-AG through v2.4.1 had a prompt-visibility rule for contractors (§5.2) but no disclosure rule for the people an agent's output affects. The rule: **a person who interacts with an agent, or about whom an agent produces an output that materially influences a decision, is told so, in plain language, before or at the point of interaction, and — for flagged decisions — is told after an adverse outcome what role the agent played and how to request human review.** The wording, timing, and channel are recorded in the AISIA. This rule is drafted to satisfy EU AI Act Article 50 (in force since August 2, 2026) and the pre-use notice, adverse-decision explanation, and human-review provisions of Colorado SB 26-189 (effective January 1, 2027); deployers in other jurisdictions should confirm local requirements. The AISIA records what the organization decided to disclose; whether that disclosure is legally sufficient is a determination for Legal and Privacy, not for the framework.

### 5.6.3 Phase, gate, and refresh

The consequential-decision screen and the affected-parties list are produced in Phase 1 (Business and Stakeholder Understanding), because they change what the DAS may permit. The full assessment is completed in Phase 2 alongside the CAP and constraint log, checked at Gate 1, refreshed at Gate 2 with the frontier map and evaluation scorecard, and re-run on any re-assessment trigger. The impact-assessment currency metric in §8.1 tracks whether that refresh actually happens.

**Standards mapping**

| **Standard / framework** | **Section** | **Mapping** |
|----|----|----|
| ISO/IEC 42005:2025 \[25\] | AI system impact assessment process and documentation | Direct: the AISIA is a 42005-conformant assessment with agent-specific fields added. |
| ISO/IEC 42001 \[5\] | Clause 6.1.4 (AI system impact assessment); Annex A | Direct: the AISIA is the artifact the management system requires. |
| NIST AI RMF 1.0 \[3\] | Map 1 (context), Map 5 (impacts to individuals, groups, society) | Direct. |
| EU AI Act \[6\]\[31\] | Article 4 (AI literacy); Article 50 (transparency) — in force | Direct: the literacy and disclosure plans. |
| EU AI Act \[6\]\[31\] | Articles 9, 10, 13, 14, 27 (Annex III systems, from December 2, 2027) | Approximate: the AISIA provides the impact and oversight documentation these will require. |
| Colorado SB 26-189 \[26\] | ADMT in consequential decisions: notice, human review, records | Direct where the flag is set. |
| OWASP LLM 2025 \[7\] | LLM09 Misinformation | Approximate: over-reliance is an assessed impact. |

## 5.7 Workflow & Workforce Impact Record

The Workflow & Workforce Impact Record (WWIR) answers: *what work changes, for whom, and how will we know adoption is real?* Phase 8 (Workflow Integration and Change Management) has been part of the lifecycle since the first version, and the RAND finding that organizational causes dominate AI project failure \[14\] has motivated the paper since v2.3. But Phase 8 was the only phase with no producible artifact — a principle-level statement in a framework whose thesis is that principles fail. Three facts make the omission costly. The DAS creates new human jobs (HITL reviewers, promotion/demotion decision-makers, standing-invariant responders) and removes others, and the paper never asked who those people are. Frontier Edge tasks require 50–100% expert review, which at enterprise scale is a headcount question the threshold guidance deferred to "review capacity" without saying how to measure it. And the §9 capacity-value formula depends on active users — an adoption variable that nothing in §8 measured. Externally, McKinsey's 2026 State of AI survey finds that high performers redesign workflows around AI rather than inserting AI into existing ones \[29\], and Vanta finds 65% of organizations report their agentic use outpacing their understanding of it \[15\].

**Minimum Workflow & Workforce Impact Record contents**

| **Element** | **Required content** | **Produced** |
|----|----|----|
| **As-is / to-be workflow** | Step-level process maps with the agent's DAS position marked on each to-be step; hand-off points; what the human sees at each HITL gate. | Draft in Phase 1; final in Phase 8. |
| **Role-impact table** | For each affected role: tasks removed; tasks added (HITL review, promotion/demotion decisions, standing-invariant response, exception handling); capacity delta in hours per week; skill gap; whether the role is created, changed, or removed. | Phase 1 draft; signed by the affected function's leader and HR before Gate 2. |
| **Reviewer-capacity model** | See formula below; checked against actual staffed capacity, with the shortfall and its remedy stated. | Before Gate 2. |
| **Training and AI-literacy plan** | What each role must be able to *do* — for example, redesign a workflow step, recognize an out-of-scope agent action, or override with a recorded reason — measured by demonstrated capability, not module completion. Satisfies EU AI Act Art. 4 for EU staff. | Phase 8. |
| **Adoption scorecard** | Active users vs. eligible; override rate; workaround and shadow-tool signals; user satisfaction; baseline measured before rollout. | Baseline before Gate 2; ongoing in Phase 9. |
| **Communication plan and sponsor/champion map** | Who says what to whom, when; named champions in each affected team; the workforce-voice input gathered (frontline interviews or surveys) and what changed because of it. | Phase 8. |
| **Reviewer-monitoring disclosure** | What is measured about HITL reviewers (§8.1), why, who sees it, and the commitment that it is used for gate design rather than individual performance management unless HR has agreed otherwise. | Before Gate 2. |

**Reviewer-capacity model**

> **Required review FTE = (Expected task volume per period × Review rate from §5.4) × Minutes per review ÷ Available reviewer minutes per FTE per period**

The review rate is the verification protocol for the task's frontier position — 10–30% for Within Frontier, 50–100% for Frontier Edge — and the minutes per review should be measured in the pilot, not estimated. The result is compared with the reviewers actually staffed. If the gap is closed by lowering the review rate, that is a threshold decision that must be argued on §5.4.1 grounds and approved on the DAS, not absorbed silently. This is also the point at which the argument for workflow redesign upstream becomes concrete: if the to-be workflow requires more review than the organization can staff, Phase 5 architecture should be constrained by the to-be workflow, not the reverse.

**Phase and gate.** The WWIR is drafted in Phase 1, when the business problem and baseline are stated, and completed in Phase 8. Gate 2 (§6.1) now requires three WWIR conditions: reviewer capacity confirmed, adoption baseline measured, and the role-impact table signed by the affected function's leader and HR. The scorecard feeds the §9 capacity value — no ROI figure should be presented until the adoption baseline exists — and the human-side metrics in §8.1.

**Shadow AI as a change-management signal.** Employee use of unapproved AI tools roughly tripled in a year, reaching about 45% of the workforce in the 2026 Verizon Data Breach Investigations Report as cited by CSA \[33\]. For a large enterprise this is a change-management problem before it is a security problem: people route around tools that do not fit their work. The WWIR treats shadow-tool signals as a leading indicator of an unmet need and recommends an amnesty-style intake — "tell us what you are using; we will help you do it safely" — that feeds the registry (§5.5) rather than an enforcement action.

**Standards mapping**

| **Standard / framework** | **Section** | **Mapping** |
|----|----|----|
| ISO/IEC 42001 \[5\] | Clause 7.2 (competence), 7.3 (awareness), 7.1 (resources) | Direct: training plan, literacy plan, reviewer-capacity model. |
| NIST AI RMF 1.0 \[3\] | Govern 2 (accountability structures, training); Manage 4 (post-deployment monitoring) | Direct. |
| EU AI Act \[6\] | Article 4 (AI literacy); Article 14 (human oversight, when applicable) | Direct: the literacy plan; the reviewer design supports Article 14 oversight measures. |
| IMDA MGF v1.5 \[21\] | Human accountability; automation-bias safeguards; skill-degradation and operational continuity | Direct: reviewer design and worker-impact statement. |
| ISO/IEC 42005 \[25\] | Impacts on workers as an affected group | Direct: the worker-impact statement is shared with the AISIA. |

## 5.8 Governing vendor-supplied agents

CRISP-AG is silent on vendor *selection* (§12) and remains so. But governing a vendor's agent is not the same thing as selecting a vendor, and most enterprises early in agentic adoption meet their first agents inside products they already license. IMDA v1.5 distinguishes platform-provider, system-provider, and deployer responsibilities explicitly \[21\]; the framework should say which artifacts the deployer still produces when the agent is someone else's. The rule: **the deployer owns every artifact that records its own authority, its own people, its own data, and its own affected persons, regardless of who built the agent.** The vendor owns the artifacts that specify the agent's internals, and the deployer's obligation is to obtain enough of them to complete its own.

| **Artifact** | **Owner when the agent is vendor-supplied** | **What the deployer needs from the vendor** |
|----|----|----|
| **DAS (§5.1)** | Deployer, always. The vendor's configuration options are the action inventory. | The complete list of actions the agent can take against the deployer's systems, and the configuration mechanism that disables each. |
| **CAP (§5.2)** | Deployer. | Confirmation that the agent enforces the invoking user's authorization scope (intersection, not union), and how. |
| **Orchestration Contract (§5.3)** | Vendor, for sub-agents inside the product; deployer, for any orchestration it builds around the product. | Input/output schemas, HITL triggers, failure modes, and audit-log contents for each exposed capability — or contractual equivalents. |
| **Capability Frontier Map (§5.4)** | Deployer, on the deployer's tasks and data. | Vendor evaluation results as an input, never as a substitute. |
| **AIR (§5.5)** | Deployer. | A distinct, revocable identity per deployed agent instance; no shared vendor credential across customers or across the deployer's own agents. |
| **AISIA (§5.6)** | Deployer. | Model provenance, training-data and limitation disclosures (the developer-to-deployer disclosures Colorado SB 26-189 requires), and any fairness testing performed. |
| **WWIR (§5.7)** | Deployer. | Nothing beyond product documentation; the workforce is the deployer's. |
| **Regression suite; model-update approval record** | Vendor runs; deployer approves. Model updates inside a vendor product are frontier re-evaluation triggers (§5.4). | Advance notice of model or tool changes; release notes sufficient to re-run the deployer's own evaluation. |
| **Threat model (§7)** | Shared. Vendor covers the product; deployer covers the integration and the data. | Security attestations; results of the vendor's adversarial testing at the §7.1 coverage level for the agent's class. |

A vendor agent for which the deployer cannot obtain the action inventory, a distinct identity, and update notice cannot be classified above HITL-REQUIRED under this framework, because the deployer cannot produce a complete DAS or a valid AIR for it. That is a governance consequence, not a procurement recommendation.

# 6. The CRISP-AG Nine-Phase Lifecycle

CRISP-AG extends CRISP-DM by adding phases that address operational context, governance architecture, and post-deployment capability drift. The lifecycle is iterative. Phase boundaries are not intended as bureaucracy; they are intended to prevent architecture and deployment decisions from being made before authorization, data, workforce, security, and evaluation constraints are known. Version 3.0 moves workforce and affected-person constraints upstream: the impact screen and the WWIR draft are Phase 1 outputs, so that Phase 5 architecture is constrained by the to-be workflow and the consequential-decision flag rather than the reverse.

| **Phase** | **Name** | **Key output** | **Why it matters for agentic AI** |
|----|----|----|----|
| 1 | Business and Stakeholder Understanding | Problem statement, quantified baseline, DAS draft, RACI, consequential-decision screen and affected-parties list (§5.6), WWIR draft with role-impact table (§5.7). | Defines what the agent is for, who authorizes action, whom it affects, and whose work changes. |
| 2\* | Operational Context Assembly | Context specification, CAP, constraint log, system inventory, AIR created (§5.5), full impact assessment (§5.6). | Captures workforce, policy, identity, and operational constraints before architecture. |
| 3 | Data and System Landscape Discovery | API catalog, permission matrix, latency/dependency map, identity model for agents (service principals, secrets management). | Agents interact with live systems; system reliability becomes model reliability. |
| 4 | Data and Context Preparation | RAG corpus, tool specs, system prompt, data classifications. | Prepares runtime context and enforces data boundaries. |
| 5 | Agent Architecture Design | Architecture decision record, orchestration design, contracts, HITL spec — constrained by the to-be workflow and the consequential flag. | Replaces model selection with workflow, tool, memory, and agent topology design. |
| 6\* | Trust, Governance, and Risk Framework | Threat model, audit spec, compliance mapping, tier policy, pipeline circuit-breaker and halt-the-line rule (§7.2). | Creates reviewable controls for trust, security, and accountability. |
| 7 | Capability Frontier Evaluation | Frontier map, evaluation scorecard, regression suite, reviewer-capacity check. | Determines what the agent may do autonomously and what requires review — and whether the review can be staffed. |
| 8 | Workflow Integration and Change Management | As-is/to-be process, enablement plan, HITL operations, completed WWIR with adoption baseline and signed role-impact table. | Addresses adoption and human workflow redesign with a producible artifact. |
| 9\* | Iterative Refinement and Scale | Observability, model-update approval, prompt versioning, scaling gates, standing governance invariants (§6.3), human-side metrics (§8.1), AIR and AISIA refresh. | Agentic systems evolve after deployment; governance must remain active. |

*\* New phase with no direct CRISP-DM equivalent.*

## 6.1 Phase gates

| **Gate** | **Required before progression** | **Minimum evidence** |
|----|----|----|
| **Gate 1: Architecture Design Entry** | Before Phase 5 begins. | Data tiers assigned; tool specifications complete; system prompt reviewed; DAS approved at the levels required in §5.1.1 including the Responsible AI / Privacy level where required; CAP reviewed where contractors are in scope; AIR activated with a named sponsor and scoped credential; impact assessment complete, consequential flag recorded; adversarial prompt tests completed (see §7.1 for coverage requirements); latency feasibility checked. |
| **Gate 2: Production Deployment Entry** | Before Phase 8 workforce rollout. | Frontier map approved; evaluation scorecard meets deployment-specific targets; HITL triggers tested; zero unresolved Tier 2/3 data incidents; threat model and security testing complete; observability ready; reviewer capacity confirmed against the §5.7 model; adoption baseline measured; role-impact table signed by the affected function's leader and HR; impact assessment refreshed; disclosure to affected persons in place where required. |

## 6.2 Per-class compressed tracks

Not all agent classes require all nine phases. The lifecycle compresses based on the agent class established in §4. The compression is not a relaxation of governance; it is a calibration of phase work to the actual stakes. The three new artifacts compress with the track: a Class 1 agent needs an impact *screen* and a reduced registry entry, not a full assessment and a full WWIR.

| **Class** | **Required phases** | **Phase gates required** | **Notable additional requirements** | **Typical time-to-production** |
|----|----|----|----|----|
| **Class 1 — Single-Step Tool-Calling** | 1, 4, 5, 8 (skip 2, 3, 6, 7, 9) | None | Output review by humans replaces formal frontier evaluation. Model updates handled via standard application versioning. Impact screen and reduced AIR (ID, sponsor, class, provenance) in Phase 1; WWIR reduced to the role-impact table. | 2–4 weeks for a small team |
| **Class 2 — ReAct-Loop** | 1, 2, 3, 4, 5, 7, 8 (skip 6, optionally skip 9 if not at scale) | Gate 1 required | CAP required if any non-FTE category invokes the agent. Step limits and HITL triggers required. Full AIR; full impact assessment when flagged, otherwise screen plus affected-parties list; WWIR with reviewer-capacity model. | 6–10 weeks |
| **Class 3 — Hierarchical Multi-Agent** | All 9 phases | Gate 1 and Gate 2 required | Orchestration Contracts mandatory for every sub-agent, with output validation and degradation policy. Cross-agent audit trail mandatory. Phase 6 threat model must address inter-agent attack surfaces and specify the pipeline circuit breaker. One AIR per sub-agent. | 3–6 months |
| **Class 4 — Autonomous Code-Executing** | All 9 phases plus quarterly re-testing | Gate 1, Gate 2, plus quarterly Gate 2 re-validation | Sandboxing and qualified red-team review required at Phase 6. Regression suite reruns at Phase 7 after any model, tool, or RAG corpus change. Quarterly penetration testing at Phase 9. AIR credential scope reviewed at each re-validation. Sandboxing and production-write restrictions apply equally to an agent of any other class that carries the Class 4 write controls (§4). | 4–8 months. Maintenance is 20–30% of build effort, ongoing. |

The principle: phase work scales with what is at stake. A Class 1 FAQ assistant does not need a threat model that addresses sandbox escape. A Class 4 operations agent does. Compressed tracks make the framework usable for low-stakes deployments without compromising the rigor needed for high-stakes ones.

## 6.3 Standing governance invariants

Phase 9 as specified in §6 covers observability, model-update approval, prompt versioning, and scaling gates — a monitoring and re-approval cadence. What it does not by itself specify is what happens to governance work *after* it is approved and closed: a signed-off DAS entry, a closed threat-model gap, a passed regression suite, an activated AIR credential. The implicit assumption is that once approved, an artifact stays valid until the next scheduled review.

That assumption should be made explicit and stronger. The proposal: completed governance work should convert into a standing governance invariant — a continuously and automatically checked condition, not a one-time sign-off that is trusted until the next audit. A closed threat-model gap becomes a monitored condition that pages a human the moment its underlying assumption stops holding (e.g., a mitigation control is disabled, a scope boundary is widened, a dependency the mitigation relied on changes). An approved DAS entry becomes a monitored condition tied to the evidence-based re-evaluation mechanism in §5.1.3. An AIR entry becomes a monitored condition on its sponsor, credential scope, and activity (§5.5).

Two properties distinguish a standing governance invariant from a conventional monitoring alert. First, it never silently self-repairs — automated remediation that fixes and forgets a governance violation produces exactly the audit gap DAS and CAP were designed to close. A standing governance invariant that fires routes to a human; it does not close itself. Second, retirement of a standing governance invariant is itself a logged, approved governance decision — indistinguishable in evidentiary weight from the original approval that created it — never a silent deletion when it becomes inconvenient or noisy.

**Terminology.** A *standing governance invariant* is distinct from a system's *governing invariant* or *protocol invariant* — a property of the system's own behavior that its design holds and enforces (the implementing specification form defines that term). The former watches governance work after approval; the latter is what the system is built never to violate.

This is presented as a design proposal. Its shape is consistent with the "continuous verification" posture of the CSA Agentic Trust Framework \[19\] and with the standing-control expectations of ISO/IEC 42001 clause 9, and it is on the validation agenda in §11. Phase 9 in its current form (regression suites, model-update approval, frontier drift) covers the *model and task* side of post-deployment drift well. It does not yet cover the *governance-artifact* side — the risk that an approved control quietly stops being true. Standing invariants close that gap.

# 7. Security Architecture

Agentic AI security requires treating the model's context and tool-use path as part of the attack surface. Prompt injection becomes more consequential when a model can call tools or influence downstream systems. Indirect prompt injection is especially relevant to RAG and document-processing workflows because malicious instructions can enter the context through content that appears to be ordinary business material.

The risks are no longer hypothetical. The OWASP Top 10 for Agentic Applications 2026 \[17\] anchors its entries to documented incidents: a zero-click prompt-injection exfiltration path in a widely deployed enterprise assistant (CVE-2025-32711, "EchoLeak") for ASI01 goal hijack; a tool-connection exploit against a source-control MCP integration for ASI04 supply-chain compromise; and an agent that deleted a production database during a code freeze for ASI10 rogue agents. OWASP's organizing principle for the list is *Least Agency* — grant an agent the minimum autonomy the task requires — which is the DAS stated as a security principle. The complementary framing from the CSA and RSAC 2026 discussions of the Agentic Trust Framework — move from *access* control to *action* control — is a one-line summary of what output gating does.

<img src="./media/image9.jpg" style="width:5.60417in;height:3.95833in" />

*Figure 6. Agentic system threat model showing principal attack surfaces and aligned mitigations.*

| **Attack surface** | **Risk** | **CRISP-AG mitigation** | **Residual risk** |
|----|----|----|----|
| **User input surface** | Direct prompt injection. | Adversarial testing, structured refusal rules, DAS-enforced action boundaries. | Cannot fully separate instructions from data in all cases. |
| **Retrieved content surface** | Indirect injection through documents, emails, web pages, or database text. | Document provenance, content scanning, context sanitization, tool permission limits, output gating (see below). | Malicious content may still influence reasoning; blast radius must be limited. |
| **Tool-call surface** | Excessive agency: too much functionality, permission, or autonomy. | Least-privilege tools, scoped per-agent credentials (AIR), HITL gates, audit logging. | Mis-scoped tools can still create unauthorized side effects. |
| **Output / action surface** | Agent action plan diverges from user request scope. | Output gating: action plans for HITL-REQUIRED+ actions verified against an independently-derived expectation of the original user request scope; divergent plans flagged regardless of input cleanliness. | Output gating depends on accurate request-scope inference. |
| **Inter-agent surface** | Cross-agent instruction propagation, delegated scope leakage, cascading failures. | Orchestration Contracts with output validation, per-agent identity and permission boundaries, inter-agent message validation, pipeline circuit breaker (§7.2). | Emergent behavior may not be fully captured by unit tests. |
| **Code-execution surface** | Sandbox escape, privilege escalation, file/database modification. | Sandboxing, deny-by-default production writes, red team review, separate secrets boundary. | Class 4 systems remain high-risk and require separate security acceptance. |
| **Persistent memory surface (OWASP ASI06)** | Standing-policy poisoning: an entry written once into retrieved memory, a lessons store, or a precedent collection reloads on every subsequent invocation, carrying the authority the system grants its own knowledge base. Unlike a one-shot injection, the effect survives the context window. | Provenance on every write (originating run, evidence, approving identity); writes gated on an independent verifier rather than the producing agent; mechanical scan before load; periodic re-testing of sampled entries against ground truth; retirement by logged decision, never silent deletion. | An entry authored by a legitimately authorized human remains indistinguishable from a correct one at write time. Detection depends on the re-testing cadence, not on the write path. |
| **Human-review surface (OWASP ASI09)** | Reviewer rubber-stamps agent output; the HITL gate stops holding. | Reviewer-behavior metrics, known-bad injections, latency floors, reviewer rotation, evidence-first UI (§7.2); reviewer capacity staffed (§5.7). | Measurement itself can change behavior; requires disclosure and ground-truth sampling. |

Output gating deserves particular emphasis as a defense category. For HITL-REQUIRED and higher actions, the agent's planned action is verified against an independently-derived expectation of what the original user request entailed. Action plans diverging from expected scope are flagged regardless of input cleanliness. This is the most effective single defense against indirect prompt injection because it does not depend on perfect input sanitization — it operates on the planned action, where the consequence of a successful injection would manifest.

### Related frameworks

This threat model was developed independently and is organized by attack surface rather than by a published agentic-specific taxonomy. Two frameworks cover closely related ground and are worth naming explicitly rather than leaving the overlap unacknowledged.

The Cloud Security Alliance's MAESTRO framework (Multi-Agent Environment, Security, Threat, Risk, and Outcome; introduced February 2025) \[18\] is a threat-modeling methodology purpose-built for autonomous multi-agent systems. It extends STRIDE-style analysis across seven architectural layers — foundation model, data, deployment, observability, security, compliance, and agent ecosystem — which is a different decomposition from the attack-surface organization used here. Its coverage overlaps most with this section's inter-agent and orchestration surfaces; its observability and compliance layers have no direct counterpart in this table and are handled in §6 and §8 instead.

The OWASP Top 10 for Agentic Applications 2026 (published 9 December 2025; ASI-prefixed, distinct from and additive to the OWASP LLM Top 10 already cited in §2) is a flat ten-item risk list, not a thematic taxonomy. The crosswalk against this section's surfaces, updated for v3.0:

| **OWASP ASI item** | **Covered by this framework?** |
|----|----|
| ASI01 Agent Goal Hijack | Yes — user-input and output/action surfaces. |
| ASI02 Tool Misuse & Exploitation | Yes — tool-call surface. |
| ASI03 Agent Identity & Privilege Abuse | Yes (v3.0) — Agent Identity & Registry Record (§5.5) plus CAP (§5.2). Was "partial" in v2.4.1. |
| ASI04 Agentic Supply Chain Compromise | No — named as uncovered in §7.3; OWASP MCP Top 10 \[32\] recommended as the pointer. |
| ASI05 Unexpected Code Execution | Yes — code-execution surface. |
| ASI06 Memory & Context Poisoning | Yes — persistent memory surface. |
| ASI07 Insecure Inter-Agent Communication | Yes — inter-agent surface. |
| ASI08 Cascading Agent Failures | Yes (v3.0) — mitigations drafted in §7.2; contract fields in §5.3. |
| ASI09 Human-Agent Trust Exploitation | Yes (v3.0) — mitigations drafted in §7.2; metrics in §8.1; capacity in §5.7. |
| ASI10 Rogue Agents | Partial — bounded by DAS (§5.1) and detected by standing governance invariants (§6.3) and AIR inactivity rules (§5.5), rather than by behavioral detection. |

One of ten remains uncovered and one is partial. Adopters using both frameworks should not assume that satisfying this threat model implies satisfying the OWASP list. Conversely, the surface model treats output gating and human-review integrity as first-class defense categories, which the ASI list does not call out separately.

## 7.1 Security requirements by class

Adversarial test count is not a meaningful security metric. *Coverage* is. Test coverage must include direct injection variants (instruction override, context confusion, role manipulation), indirect injection vectors (RAG corpus poisoning, tool response poisoning, multi-document instruction smuggling), and excessive-agency tests (out-of-scope tool calls, permission escalation attempts). Minimum: at least three tests per documented vector.

| **Class** | **Minimum security expectations** |
|----|----|
| **Class 1** | Direct injection coverage (instruction override, context confusion, role manipulation); schema validation; access-controlled prompt storage; basic logging. |
| **Class 2** | Class 1 coverage plus indirect injection coverage (RAG corpus poisoning, tool response poisoning, multi-document smuggling); step limits; scoped tools under a per-agent identity; HITL triggers; output gating for HITL-REQUIRED+ actions; model/corpus version logging. |
| **Class 3** | Class 2 coverage plus cross-agent injection tests, per-sub-agent identity and permissions, Orchestration Contracts with output validation, cross-agent audit trail, pipeline circuit-breaker test, and excessive-agency coverage on the orchestrator. |
| **Class 4** | Class 3 coverage plus sandbox isolation, production-write restrictions, qualified red-team review, code-execution-specific scenarios, and re-testing after every material model/tool update. |

## 7.2 Threats addressed in this revision: cascading failures and trust exploitation

v2.4.1 named OWASP ASI08 and ASI09 as uncovered and promised mitigations for v3. Both are drafted here. They are design proposals, calibrated against OWASP's guidance and IMDA v1.5's automation-bias safeguards \[21\], and are on the validation agenda in §11.

### 7.2.1 Cascading agent failures (ASI08)

A fault, bad output, or degraded dependency in one agent propagates through an orchestrated pipeline, with each downstream agent treating the corrupted upstream result as valid input. The Orchestration Contract's failure-modes field bounds a single sub-agent's behavior; the pipeline needs its own controls.

- **Per-hop output validation.** Every downstream hop validates upstream output against the expected ranges and enumerations in the upstream contract's output schema (§5.3), not merely its types. Out-of-range output is rejected at the hop, not passed on.

- **Blast-radius budget.** Each pipeline declares the maximum number of downstream actions that may proceed on degraded or unvalidated upstream output before a mandatory human checkpoint. The budget is a Phase 6 artifact, approved with the threat model, and enforced at the orchestrator.

- **Halt-the-line rule.** Any sub-agent, the orchestrator, or a monitoring invariant may halt the pipeline when the blast-radius budget is exhausted, when the same failure mode recurs across hops, or when a HITL-REQUIRED action is reached with degraded inputs. Who may halt, who may resume, and what evidence resumption requires are recorded in the pipeline policy. Halting is never penalized in the metrics that govern the pipeline.

- **Degradation policy at pipeline level.** Each contract's retry / degrade / abort policy rolls up into a pipeline-level policy that states what the pipeline delivers when a segment is aborted — a partial result with an explicit degraded-status flag, or nothing — so that a downstream consumer never receives a silently degraded output as if it were complete.

- **Regression coverage.** The Class 3 regression suite includes at least one injected upstream failure per contract to confirm that validation, budget, and halt behave as specified.

### 7.2.2 Human-agent trust exploitation (ASI09)

An agent's fluency, confidence, or accumulated reliability induces a human reviewer to approve what they have not actually verified — the failure mode that turns a HITL gate into a rubber stamp. This is a direct threat to CRISP-AG's own control model, because the DAS and the Capability Frontier both discharge risk into human review and assume that review is real. IMDA v1.5 addresses the same risk as automation bias and recommends monitoring override rates and response times \[21\]. The mitigations treat the reviewer as a designed role rather than an assumed one:

- **Reviewer-behavior metrics.** Approval latency, override rate, and spot-check accuracy per HITL gate (§8.1), reported at gate level. A latency distribution collapsing toward zero or an override rate near zero on a Frontier Edge task is a signal that the gate has stopped holding.

- **Known-bad injections.** Randomized, labeled-after-the-fact insertion of outputs known to be wrong into the review queue, at a rate the WWIR states, to measure spot-check accuracy directly rather than infer it.

- **Approval-latency floors.** For high-consequence and consequential-flagged actions, the interface does not accept an approval before a minimum review time has elapsed and the evidence has been displayed.

- **Reviewer rotation and capacity.** Rotation across reviewers on high-volume gates; reviewer load kept within the §5.7 capacity model, because an overloaded reviewer is a rubber stamp by necessity.

- **Evidence-first interface rules.** The review surface shows the agent's evidence and confidence before its recommendation; never a one-click approve for HITL-REQUIRED actions; override requires a recorded reason, and the reasons are reviewed as a corpus.

- **Disclosure and use limits.** Reviewers are told what is measured and why (§5.7). The metrics are used for gate design and staffing, not for individual performance management, unless HR has agreed to that use and the reviewers have been informed. Measurement of reviewers that is undisclosed or used punitively converts a security control into a workforce harm, and the impact assessment (§5.6) records the decision.

## 7.3 Threats still not covered in this framework

CRISP-AG's threat model is OWASP-aligned, which means it is conservative. The following threat categories are emerging in 2025–2026 and are *not* fully addressed by the framework as currently published. Until they are, defense is a deployer responsibility outside CRISP-AG.

**Tool poisoning and agentic supply chain (ASI04).** A tool's output schema or behavior is silently changed (for example, by a compromised dependency, upstream service, or tool-description manipulation in a connector). The agent receives plausible-looking but adversarial responses. Mitigation requires response-schema validation, tool-integrity verification, and connector allow-listing; the output-validation field added to the Orchestration Contract in v3.0 covers the first of these but not the second or third. OWASP now maintains a separate MCP Top 10 for the tool-connection layer \[32\], and deployers using connector protocols should apply it alongside this section.

**Supply-chain attacks on model providers and inference layers.** A compromised model checkpoint, an injection in the inference layer's system-prompt prepending, or an adversarial finetune-via-API attack can affect agent behavior in ways the deployer cannot detect at integration time. Mitigation requires model-provenance verification and inference-layer integrity attestations; commercial offerings for this are nascent.

**Side-channel inference.** Adversaries infer information about agent state, system prompt, retrieved content, or other agents' actions through timing variations, partial response patterns, or error message content. Mitigation requires output normalization and timing controls; not currently specified.

**Model-extraction attacks against deployed agents.** Adversaries reconstruct system prompt, tool definitions, or proprietary data through repeated probing of a deployed agent. Mitigation requires query rate limiting and probe-pattern detection; not currently specified.

These categories are not exhaustive. Deployers should consult contemporary AI red-teaming literature for emerging threats; the field is moving faster than this document is revised.

# 8. Evaluation and Metrics

The evaluation strategy should be deployment-specific. CRISP-AG proposes a minimum set of metric categories rather than a universal scorecard. Each target should be justified against the task class, data tier, consequence level, and review capacity. Version 3.0 adds a second table: every metric in the first is a *system* metric, and none of them measures whether the humans around the agent use it, trust it, override it, or route around it.

| **Metric** | **Definition** | **Use** | **Caution** |
|----|----|----|----|
| **Task completion rate** | Percent of initiated tasks completed without abort or inappropriate escalation. | Operational readiness. | High completion can be bad if HITL gates are bypassed. |
| **RAG faithfulness** | Percent of grounded outputs without unsupported factual claims. | Retrieval and output reliability. | LLM-as-judge results require human spot-checking. |
| **HITL trigger accuracy** | Correct routing to human review versus autonomous completion. | Governance alignment. | False negatives matter more for high-consequence tasks. |
| **Tool success rate** | Percent of tool calls completing within SLA and without error. | Runtime reliability. | System SLAs compound across multi-step workflows. |
| **Data-tier incident rate** | Number of Tier 2/3 boundary violations. | Security and privacy control effectiveness. | Any severe incident should trigger scope review. |
| **Output-gating divergence rate** | Frequency of action plans flagged as outside expected request scope. | Indirect injection and excessive agency monitoring. | Persistent divergence indicates either an injection-active environment or mis-calibrated scope inference. |
| **Frontier drift** | Change in task classification or metric performance after model/tool/corpus update. | Phase 9 monitoring. | Requires version-locked regression suites. |
| **Registry completeness** | Agents observed running (from identity-provider and gateway logs) that have a current AIR entry, as a share of all agents observed. | Traceability; ASI03 and ASI10 monitoring. | Depends on the observability of the identity layer; an unobservable agent is the finding. |

## 8.1 Human-side metrics

| **Metric** | **Definition** | **Use** | **Caution** |
|----|----|----|----|
| **Active-user ratio** | Eligible users who used the agent in the period, as a share of all eligible users; baseline measured before rollout (§5.7). | Adoption; the §9 capacity-value input. | A high ratio with a high override rate is tolerance, not trust. |
| **Reviewer behavior (ASI09)** | Approval latency, override rate, and spot-check accuracy for each HITL gate; latency-distribution shape. | Detects rubber-stamping; informs gate design and staffing. | Disclose to reviewers; use for gate design, not individual performance management, unless HR agrees and reviewers are informed. |
| **Automation-bias index** | Rate at which reviewers accept agent output later found wrong, compared with the rate at which they accept output later found right. | Direct measure of ASI09 exposure; IMDA v1.5 anchor. | Requires ground-truth sampling or known-bad injections (§7.2.2); small samples are noisy. |
| **Shadow-tool signal** | Unapproved AI tool usage in the workflow's population, from survey and data-loss-prevention telemetry. | Change-management leading indicator; registry intake. | Handle as an enablement and wellbeing signal, not an enforcement trigger; the intake is an amnesty. |
| **Capability-based literacy** | Share of affected staff who can demonstrate the WWIR training outcomes (e.g., redesign a step, recognize an out-of-scope action), assessed rather than self-reported. | Art. 4 evidence; adoption readiness. | Module completion is not this metric. |
| **Impact-assessment currency** | Days since the last AISIA refresh, against the re-assessment triggers that have occurred. | Ethics governance; Responsible AI approver's review input. | A triggered-but-unrefreshed assessment is a gate finding. |

# 9. ROI and Business Case Guidance

ROI for agentic AI is a decision-support model, not proof of framework effectiveness. The most defensible model separates capacity value, quality value, and risk-reduction value, and uses different evidence standards for each. Critically, CRISP-AG does not recommend summing across the three buckets — doing so forces speculation into the risk bucket and contaminates the credibility of the legitimately quantified buckets. Version 3.0 adds a fourth line, workforce-transition cost, which is likewise not summed into the value buckets: it is presented alongside them so the change-management work that §5.7 requires is financially visible rather than hidden inside a loaded hourly rate.

<img src="./media/image10.png" style="width:6in;height:3.94792in" />

*Figure 7. Three-bucket ROI framework separating capacity, quality, and risk-reduction value, with the workforce-transition cost line added in v3.0 (§9.4) shown alongside rather than summed.*

## 9.1 Capacity value (the formula)

Capacity value uses an explicit formula rather than illustrative dollar amounts:

> **Capacity Value = Active users × Hours saved per week × Working weeks per year × Loaded hourly rate**

The "hours saved per week" parameter should be calibrated to a documented industry range. For procurement-domain agentic deployments, McKinsey's October 2025 analysis estimates that agentic AI could increase procurement efficiency by 25–40% \[13\]; its February 2026 follow-up reports case results of 20–30% staff-efficiency gains from autonomous sourcing and up to 90% reductions in negotiation analysis time \[36\]. The range, not the upper case, is the calibration. For non-procurement domains, comparable industry productivity studies should be used; if no domain-specific study exists, the calibration should be made explicit and bounded conservatively. The "active users" parameter is the adoption scorecard's active-user ratio (§8.1) applied to the eligible population, and no capacity figure should be presented until the WWIR adoption baseline exists.

| **Scenario** | **Hours saved per week parameter** | **Active user count** |
|----|----|----|
| **Conservative** | Lower bound (e.g., 25% of current cycle time for procurement) | Conservative active-user count (only currently-engaged users, from the adoption baseline) |
| **Base case** | Midpoint (e.g., 32–33%) | Realistic active-user count (existing users plus likely adopters in year one) |
| **Optimistic** | Upper bound (e.g., 40%) | Stretch active-user count (full target population) |

The output is three dollar ranges, not a single number. This is intentional. Providing a single number obscures the modeling uncertainty and invites scrutiny of inputs that cannot be defended at single-point precision.

## 9.2 Quality value

Quality value is calibrated from organizational history, not projected from speculation. The categories include:

- Reduction in compliance incidents (use historical incident rate as baseline)

- Reduction in vendor data quality issues (baseline from data quality audits)

- Reduction in external consultant spend (baseline from spend records)

- Reduction in rework cycles (baseline from process metrics)

- Duplicate-record reduction (baseline from master-data audits)

Each category should be presented with the historical baseline, the projected post-deployment value, and the source of the projection (analogous deployment history, vendor benchmarks, or pilot data). Categories without historical baselines should be presented qualitatively rather than projected speculatively.

## 9.3 Risk reduction (qualitative)

Risk reduction is named and framed, not assigned a speculative dollar amount. The categories include:

- Regulatory data violation exposure

- Contractor access incident exposure

- Model update disruption exposure

- Excessive agency / unauthorized action exposure

- Prompt injection / indirect injection exposure

- Untraceable-agent exposure (an agent acting without a registered sponsor)

- Consequential-decision exposure (notice, human-review, or record-keeping failure)

For each category, the business case should reference the specific risk register entry, the qualitative likelihood and severity assessment, and the CRISP-AG artifact that addresses it. Risk reduction *should not* be summed with capacity or quality value to produce a unified ROI figure. The CFO performs the integration with their own risk weighting.

## 9.4 Workforce-transition cost (new in v3.0)

The change-management work that §5.7 requires has a cost, and in earlier versions it was invisible — absorbed into the loaded hourly rate or omitted. It is presented here as an explicit line with three components, drawn directly from the WWIR: **training and literacy** (hours per affected role × roles × loaded rate, plus content development); **reviewer capacity** (the FTE result of the §5.7 model, whether newly hired, reassigned, or contracted — and, if reassigned, the work no longer done); and **role redesign** (the one-time cost of the to-be workflow: process documentation, tooling changes, and any severance or redeployment). The line is not netted against capacity value in the framework's presentation, for the same reason the three buckets are not summed: it has a different evidence standard (it is an estimate of committed spend, not a projection of benefit), and netting it invites the reader to treat the capacity range as a certainty. Presenting it separately also makes the change-management artifact financially visible to the executive who funds it.

## 9.5 Why different evidence standards

The buckets use different evidence standards because they are different kinds of claims. Capacity is a forward projection grounded in a formula calibrated to industry data. Quality is a measured improvement grounded in organizational baselines. Risk is a probability-weighted exposure that cannot be rigorously quantified for low-frequency high-severity events without inviting unsupportable precision. Workforce-transition cost is a committed-spend estimate.

Mixing these standards into a single number is the most common mistake in AI investment cases. The result is a number that the CFO can attack on its weakest input (typically the speculative risk-reduction figure), which then contaminates the credibility of the capacity and quality figures that were defensible. Keeping the buckets separate, with their respective evidence standards intact, is what consistently lands in real CFO conversations.

# 10. Implementation Roadmap

<img src="./media/image11.jpg" style="width:5.19792in;height:2.07292in" />

*Figure 8. Ongoing governance timeline emphasizing frontier monitoring, review cadence, and post-deployment telemetry.*

| **Stage** | **Timeframe** | **Focus** | **Exit evidence** |
|----|----|----|----|
| **Foundation and pilot** | Months 1–6 | Inventory every agent in or near production and register it (AIR); produce DAS/CAP; impact screen; discover systems; prepare context; pass Gate 1; pilot limited workflow. | Registry with a named sponsor for every agent; pilot artifact package; initial evaluation results; adoption baseline; zero unresolved severe incidents. |
| **Governance and scale** | Months 7–12 | Complete trust/governance architecture; Gate 2; reviewer role designed and staffed; role enablement; department rollout. | Security acceptance; HITL and reviewer-behavior metrics; adoption data; signed role-impact table; updated CAP, AISIA, and frontier map. |
| **Institutionalize and evolve** | Months 13–18 | Operational monitoring; regression suite; model-update approval; standing governance invariants; enterprise governance cadence; vendor-agent track applied to the most consequential licensed tools. | Phase 9 dashboard including human-side metrics; version-control process; scaling gate results; measured ROI report in three buckets plus workforce-transition cost. |

The roadmap above describes the typical Class 3 case. Class 1 deployments compress to a 2–4 week timeline using only Phases 1, 4, 5, 8 (see §6.2). Class 4 deployments extend to 4–8 months and add ongoing quarterly Gate 2 re-validation indefinitely. Regardless of class, the registry can be produced first: it depends on nothing else in the lifecycle, and for an organization early in agentic adoption it is the fastest reportable governance result.

## 10.4 Reference implementation

An enterprise implementation of CRISP-AG consists of four instruments: a *document standard* that defines the content of the artifacts in §5 and Appendix A; a *specification form* in which contracts, invariants, and governance clauses are written; a *runtime control specification* that defines the mechanisms enforcing DAS positions and the standing governance invariants of §6.3; and a *delivery workflow* that sequences the phases of §6 as gated stages with named approvers.

The author's employer implements CRISP-AG with the *Agentic PRD Standard* (v3), *Specification-Driven Design for Agentic Systems* (v1.0.1), the *Enterprise Agentic AI Harness Specification* (v1.0), and the *Agentic Delivery Workflow* (v1.1). Those documents are internal and are cited here by title only. Where an implementation and this framework differ, the implementation's own precedence rule records the resolution: this framework governs the definition of the governance artifacts; implementations govern their content, form, controls, and sequence.

# 11. Validation Agenda

The most important next step is not adding more framework detail. It is validating whether the framework changes outcomes. The following studies would strengthen future protocol guidance and support more rigorous research validation.

| **Study** | **Research question** | **Design sketch** |
|----|----|----|
| **Multi-site case study** | Do organizations produce more complete governance evidence when using CRISP-AG? | Apply artifact completeness rubric across deployments and compare with baseline governance practices. |
| **Controlled deployment comparison** | Does CRISP-AG reduce production incidents or rework compared with MLOps-only governance? | Matched teams or workflows using CRISP-AG versus existing process, with pre-registered metrics. |
| **CAP incident study** | How often does agent-mediated access exceed contractor/user authorization? | Audit simulated and real contractor-invoked workflows across access levels. |
| **Frontier drift study** | How often do task classifications change after model or tool updates? | Run fixed regression suites across model versions and measure classification movement. |
| **Orchestration Contract ablation** | Do formal sub-agent contracts reduce coordination failures? | Compare multi-agent systems with and without contracts on controlled task suites. |
| **Earned-autonomy study** | Do evidence-gated promotion and automatic demotion change incident rates relative to fixed design-time assignment? | Compare action-level incident rates before and after the §5.1.3 mechanism, or across matched deployments. |
| **Registry traceability study** | Does the AIR raise sponsor-traceability and credential hygiene, and by how much? | Measure share of observed agents with a current sponsor and scoped credential before and after registry adoption; compare with the 28% / 21% benchmarks \[24\]. |
| **Impact-assessment study** | Does the AISIA change designs? | Count and characterize architecture or DAS changes attributable to the assessment across deployments; compare completeness with generic 42005 assessments. |
| **Adoption study** | Do a signed WWIR and a staffed reviewer-capacity model change active-user ratio and override rate? | Compare adoption scorecards for deployments with and without a completed WWIR at Gate 2. |
| **Reviewer-integrity study** | Do known-bad injections, latency floors, and evidence-first interfaces improve spot-check accuracy? | Within-gate A/B on interface rules; automation-bias index as the outcome. |

# 12. Limitations

The framework is under-validated empirically. It should not yet be described as a proven standard or best practice.

The practitioner contexts that motivated the framework may not generalize to all regulated domains.

Thresholds require local calibration and should not be treated as universal acceptance criteria.

Industry reports are useful for motivating urgency but should not be used as the primary evidence for scholarly claims.

Security recommendations are a baseline for governance design, not a substitute for formal application security review, red teaming, or compliance assessment.

The framework currently emphasizes text-centric LLM agents and may need extension for multimodal agents, robotics, and real-time autonomous control systems.

**The impact assessment is guidance-anchored, not a legal determination.** ISO/IEC 42005 is guidance, not a certifiable standard, and the AISIA records what an organization assessed and decided. Whether a given disclosure, fairness test, or record-retention practice satisfies a particular law is a determination for Legal and Privacy in the relevant jurisdiction. The consequential-decision domains in §5.4.3 are drawn from specific statutes and will need extension as other jurisdictions legislate.

**The workforce artifact measures adoption; it does not guarantee it.** The WWIR makes adoption visible and gates deployment on capacity and sign-off. It does not resolve disagreements about role change, and it should not be read as a substitute for the organization's own employment, consultation, and labor-relations obligations, which vary by jurisdiction.

**Liability allocation is outside scope.** When an agent classified as AGENT-DIRECTED takes an action that causes harm, the question of who bears legal liability — model vendor, deploying enterprise, individual approvers, executive sponsor — is a legal and contractual question that varies by jurisdiction and depends on contract terms between enterprise and vendor. CRISP-AG produces the *evidence trail* that enables liability allocation after an incident; it does not allocate liability itself. Adopters should engage General Counsel separately on contractual liability allocation between deploying enterprise and model/tool vendors. Internal governance documentation is not a substitute for contractual liability terms.

**Vendor and platform selection are outside scope.** CRISP-AG is silent on which model providers, orchestration platforms, or vendor stacks to use. The framework constrains how an organization deploys whatever it selects; it does not constrain selection itself. §5.8 describes what a deployer must obtain from a vendor to govern a vendor-supplied agent; it does not say which vendor to choose.

**Red-team execution methodology is outside scope.** Phase 6 and §7 call for adversarial testing and qualified red-team review, but the framework does not specify *how* to conduct that testing. AI red-teaming methodology is a separate discipline with its own evolving literature; deployers should adopt established methodology rather than expect CRISP-AG to provide it.

**Single-number ROI is outside scope by design.** §9 explicitly does not produce a unified ROI figure. The three-bucket framework and the workforce-transition cost line provide structured evidence for the CFO conversation; integration into a single decision figure is the CFO's responsibility, not the framework's.

# 13. Conclusion

CRISP-AG proposes an artifact-centered implementation framework for enterprise agentic AI governance. Its practical value lies in converting abstract governance principles into concrete artifacts: action authority maps, contractor access profiles, sub-agent contracts, capability frontier maps, agent identity records, impact assessments, workforce impact records, phase gates, and post-deployment monitoring processes. Its academic limitation is equally clear: the framework is not yet empirically validated. The appropriate interpretation is as a structured practitioner framework and validation agenda, not as a completed theory or proven standard.

Version 3.0 applied the framework's own test to itself. Three concerns that earlier versions handled as principles — who the agent is, whom it affects, and who has to change how they work — now have schemas, phases, gates, and standards mappings. That change also brings the framework into alignment with where external guidance has converged in 2026: on verifiable agent identity and a named human sponsor, on impact assessment as the operational form of ethics, and on the human reviewer as a designed role rather than an assumed one.

The narrowed contribution is still useful. Enterprises adopting agentic AI need a bridge between high-level risk-management standards (NIST AI RMF, ISO/IEC 42001, ISO/IEC 42005, EU AI Act) and low-level agent implementation libraries (ReAct, AutoGen, LangGraph). CRISP-AG offers one such bridge, occupying the implementation layer beneath the standards rather than competing with them. The next phase of work should test whether the proposed artifacts measurably improve deployment readiness, auditability, security posture, adoption, and operational outcomes across multiple domains.

# Appendix A. Minimal Artifact Checklist

| **Artifact** | **Required by class** | **Minimum contents** |
|----|----|----|
| **Delegation Authority Scope** | All classes | Action inventory, autonomy class, approvers including Responsible AI / Privacy level, consequential flag, technical enforcement mapping, review date, evidence-review cadence, promotion/demotion reviewer (§5.1). |
| **Contractor Access Profile** | Class 2+ where mixed workforce exists | Contractor category, systems, data tiers, output constraints, prompt visibility, offboarding. |
| **Agent Identity & Registry Record** | All classes (reduced record for Class 1) | Agent ID, human sponsor, class and DAS pointer, credential scope, provenance, lifecycle and retirement trigger, ATF level (optional), audit anchor (§5.5). |
| **AI System Impact Assessment** | Screen for all classes; full assessment for Class 2+ or when the consequential flag is set | Affected parties, consequential-decision screen, foreseeable impacts, fairness/bias testing plan, disclosure plan, AI-literacy plan, worker-impact statement, mitigations and owners, re-assessment triggers, approvals (§5.6). |
| **Workflow & Workforce Impact Record** | All classes (role-impact table only for Class 1) | As-is/to-be workflow with DAS positions, role-impact table, reviewer-capacity model, training plan with capability measures, adoption scorecard and baseline, communication plan, reviewer-monitoring disclosure (§5.7). |
| **System landscape map** | All classes | Systems, APIs, permissions, latency, reliability, owners, data tiers, identity model for agents. |
| **Tool specification** | Class 1+ | Name, purpose, input/output schema, permissions, errors, SLA, logging. |
| **Orchestration Contract** | Class 3+ | Role, schemas with output validation, HITL triggers, failure modes and degradation policy, data constraints, SLA, audit log (§5.3). |
| **Pipeline policy** | Class 3+ | Blast-radius budget, halt-the-line authority and resumption evidence, pipeline-level degradation policy (§7.2). |
| **Capability Frontier Map** | All classes | Task classification, consequential flag, evidence, review protocol, re-evaluation triggers. |
| **Security threat model** | All classes; intensity by class | Assets, adversaries, attack surfaces, controls including output gating and reviewer integrity, residual risk, threats not currently covered (§7.3). |
| **Regression suite** | Class 2+ | Representative test set with vector coverage per §7.1, injected upstream failures for Class 3, expected outputs, model/corpus/tool version, pass/fail criteria. |
| **Model update approval record** | Class 2+ | Version change, regression results, frontier changes, impact-assessment refresh decision, approver, rollback plan. |

# Appendix B. Standards Mapping Matrix

This appendix provides a partial crosswalk between CRISP-AG artifacts and major governance standards. It is *partial by design* — some mappings are exact, others are approximate, and a few are gaps where CRISP-AG addresses concerns the standards do not specify or vice versa. Gaps are explicitly marked as such; precision is favored over coverage. The standards mappings for the three artifacts added in v3.0 appear with the artifacts themselves (§5.5, §5.6, §5.7) and are not repeated here.

## B.1 Delegation Authority Scoping (DAS)

| **Standard** | **Section / Article** | **Mapping** |
|----|----|----|
| NIST AI RMF 1.0 | Govern 1.1 (Roles and accountability) | Direct: DAS specifies action-level accountability and approval. |
| NIST AI RMF 1.0 | Govern 1.4 (Risk management policies) | Direct: DAS is the agent-specific risk-management policy artifact. |
| NIST AI RMF 1.0 | Manage 1.1 (Risks based on impact) | Direct: DAS classification by reversibility and consequence is the risk-impact treatment. |
| NIST AI 600-1 | Human-AI Configuration sub-category | Direct: autonomy classes correspond to documented human-AI configuration variants. |
| ISO/IEC 42001 | Clause 6.1 (Actions to address risks and opportunities) | Direct: DAS is the operational artifact for delegated-action risk treatment. |
| ISO/IEC 42001 | Clause 9.3 (Management review) | Approximate: DAS approval, evidence review, and re-approval are part of the management-review cadence. |
| EU AI Act | Article 14 (Human oversight) | Direct: DAS specifies the form and degree of human oversight per action. |
| EU AI Act | Article 16 (Obligations of providers of high-risk AI systems) | Approximate: DAS contributes to the documentation supporting Article 16 obligations. |
| OWASP LLM 2025 | LLM06 Excessive Agency | Direct: DAS bounds agency at the action level. |
| OWASP Agentic 2026 | Least Agency principle; ASI10 Rogue Agents | Direct: the DAS is the action-level expression of Least Agency. |
| CSA ATF | Maturity levels and promotion gates | Direct (mapping of intent): see §5.1.4. |

## B.2 Contractor Access Governance (CAG / CAP)

| **Standard** | **Section / Article** | **Mapping** |
|----|----|----|
| NIST AI RMF 1.0 | Map 4.1 (Approaches to map risk) | Approximate: CAP is a workforce-context risk-mapping artifact. |
| NIST AI RMF 1.0 | Manage 1.2 (Risk treatment selection) | Direct: CAP is the treatment for agent-mediated access escalation risk. |
| NIST AI 600-1 | Data privacy / third-party risk sub-categories | Direct: CAP enforces data-handling constraints for non-FTE invocation. |
| ISO/IEC 42001 | Clause 7 (Support — resources and information) | Direct: CAP is the information-classification artifact for agent-mediated access. |
| ISO/IEC 42001 | Annex A controls (information classification, third-party access) | Direct: CAP operationalizes Annex A controls for agentic systems. |
| EU AI Act | Article 10 (Data and data governance) | Approximate: CAP enforces data-governance constraints in agent-mediated workflows. |
| EU AI Act | Article 22 (Authorised representatives) | Gap: CAP does not address authorized representative obligations specifically. |
| OWASP LLM 2025 | LLM02 Sensitive Information Disclosure | Direct: CAP output constraints prevent unauthorized data surfacing. |
| OWASP LLM 2025 | LLM06 Excessive Agency | Direct: CAP bounds agent-mediated access scope. |

## B.3 Orchestration Contract

| **Standard** | **Section / Article** | **Mapping** |
|----|----|----|
| NIST AI RMF 1.0 | Map 1.1 (System context established) | Direct: contracts specify per-sub-agent system context. |
| NIST AI RMF 1.0 | Measure 2.1 (Test cases for performance) | Direct: contracts are the test-case substrate for sub-agent verification. |
| NIST AI 600-1 | AI lifecycle integration sub-category | Direct: contracts integrate sub-agent build, test, and audit phases. |
| ISO/IEC 42001 | Clause 8 (Operation) | Direct: contracts are the operational-control specification for multi-agent systems. |
| ISO/IEC 42001 | Annex A controls (operational management) | Direct: contracts operationalize multi-agent operational controls. |
| EU AI Act | Article 9 (Risk management system) | Approximate: contracts contribute to the per-component risk management documentation. |
| EU AI Act | Article 13 (Transparency and provision of information) | Approximate: contracts contribute to system-design transparency documentation. |
| OWASP LLM 2025 | LLM05 Improper Output Handling | Direct: contracts specify output schemas, validation ranges, and tier classifications. |
| OWASP LLM 2025 | LLM07 System Prompt Leakage | Approximate: contract-level prompt isolation reduces leakage surface. |
| OWASP Agentic 2026 | ASI07 Insecure Inter-Agent Communication; ASI08 Cascading Agent Failures | Direct: contract output validation and the pipeline policy (§7.2). |

## B.4 Capability Frontier Map

| **Standard** | **Section / Article** | **Mapping** |
|----|----|----|
| NIST AI RMF 1.0 | Measure 2 (Verification, performance) | Direct: frontier classification determines verification protocol. |
| NIST AI RMF 1.0 | Measure 3 (Performance metrics tracking) | Direct: frontier drift is a Measure-3 monitoring artifact. |
| NIST AI RMF 1.0 | Manage 2.3 (Mechanisms identified) | Direct: per-frontier-position verification mechanisms are the Manage-2.3 outputs. |
| NIST AI 600-1 | Performance evaluation / harm assessment | Direct: frontier classification is a harm-calibrated performance assessment. |
| ISO/IEC 42001 | Clause 9 (Performance evaluation) | Direct: frontier evaluation is the operational performance-evaluation artifact. |
| ISO/IEC 42001 | Clause 10 (Improvement) | Direct: frontier re-evaluation triggers continual improvement. |
| EU AI Act | Article 15 (Accuracy, robustness, cybersecurity) | Direct: frontier thresholds are the per-task accuracy/robustness criteria. |
| EU AI Act | Article 17 (Quality management system) | Approximate: frontier maintenance is part of the quality management system. |
| OWASP LLM 2025 | LLM09 Misinformation | Direct: frontier classification governs verification stringency to prevent unsupported outputs. |
| Colorado SB 26-189 | ADMT in consequential decisions | Direct: the consequential flag (§5.4.3) caps autonomy for in-scope tasks. |

## B.5 Cross-cutting (CRISP-AG lifecycle)

**Timeline note (September 2026).** The Digital Omnibus on AI \[31\] entered into force on July 27, 2026. Rows below are marked *in force* or *applies from* accordingly. Deployers should re-check the timeline at each management review; it has changed once and may change again.

| **Standard** | **Section / Article** | **Mapping** |
|----|----|----|
| NIST AI RMF 1.0 | All four functions (Govern, Map, Measure, Manage) | Direct: lifecycle phases align with all four RMF functions; see per-phase mapping below. |
| ISO/IEC 42001 | Clauses 4–10 (full management system) | Direct: lifecycle is the implementation-level realization of the management system. |
| ISO/IEC 42005 | AI system impact assessment | Direct: the AISIA (§5.6) is the lifecycle's impact-assessment artifact. |
| EU AI Act | Article 4 (AI literacy) — *in force since February 2, 2025* | Direct: the WWIR training and literacy plan (§5.7) and the AISIA literacy element (§5.6). |
| EU AI Act | Article 50 (Transparency obligations) — *in force since August 2, 2026; Art. 50(2) marking for existing systems from December 2, 2026* | Direct: the disclosure rule for affected persons (§5.6.2). |
| EU AI Act | Articles 9–17 (Annex III high-risk requirements) — *apply from December 2, 2027*; Annex I embedded systems from August 2, 2028 | Approximate: lifecycle phases produce the documentation supporting these obligations. |
| EU AI Act | Article 26 (Deployer obligations) and Article 27 (Fundamental rights impact assessment) — *apply with the high-risk timeline* | Approximate: the AISIA and AIR provide the deployer-side records; Article 27 applies only to specified deployers. |

## B.6 Phase-to-RMF function alignment

| **Phase** | **Primary RMF function** | **Secondary RMF function** |
|----|----|----|
| Phase 1 — Stakeholder Understanding | Govern | Map |
| Phase 2 — Operational Context | Map | Govern |
| Phase 3 — System Discovery | Map | — |
| Phase 4 — Data and Context Prep | Map | Measure |
| Phase 5 — Architecture Design | Manage | Measure |
| Phase 6 — Trust/Governance/Risk | Manage | Govern |
| Phase 7 — Frontier Evaluation | Measure | Manage |
| Phase 8 — Workflow Integration | Manage | Govern |
| Phase 9 — Iterative Refinement | Measure | Manage |

## B.7 Mapping limitations

The following are explicit gaps in this matrix that future revisions should address:

- The mapping to NIST AI 600-1 sub-categories is approximate; the Generative AI Profile uses sub-category identifiers that are not fully crosswalked above.

- ISO/IEC 42001 Annex A includes 38 controls; the matrix above maps the categories most relevant to CRISP-AG artifacts but does not crosswalk every control.

- ISO/IEC 42005 is mapped at the level of the assessment as a whole; its individual guidance clauses are not crosswalked to AISIA fields.

- The EU AI Act mapping is at the article level; sub-paragraph-level mapping for high-risk-system obligations (Annex III) is not yet performed, and the Annex III obligations themselves do not apply until December 2, 2027.

- OWASP LLM 2025 entries LLM03 (Supply Chain), LLM04 (Data and Model Poisoning), LLM08 (Vector and Embedding Weaknesses), and LLM10 (Unbounded Consumption), and OWASP Agentic entry ASI04, are partially or not addressed by current CRISP-AG artifacts; these align with the threats identified in §7.3 as not yet covered.

- This matrix does not include sector-specific standards (HIPAA, SOX, GLBA, GDPR, PCI-DSS, FedRAMP) — those crosswalks are deployment-specific and should be produced per implementation. B.9 is a note on U.S. state law, not a crosswalk.

- The frameworks listed in B.8 are named and, where noted, crosswalked to individual artifacts, but not at B.1–B.6 granularity throughout — treat B.8 as a currency note, not a completed mapping.

The mapping in B.1 through B.6 is sufficient to demonstrate that CRISP-AG sits in the implementation layer beneath the standards rather than competing with them. It is not sufficient to claim full standards coverage. Adopters using CRISP-AG to support specific compliance attestations should verify the mappings against their auditor's interpretation of the relevant clauses.

## B.8 Emerging 2026 agentic-specific frameworks

The frameworks below were published or substantially updated since this paper's v2.3 revision (May 2026). They are named here so a reader evaluating CRISP-AG against the current landscape does not have to wonder whether the author is aware of them. Versions and dates were verified against live sources on September 2, 2026.

| **Framework** | **Publisher / date** | **Relationship to CRISP-AG** |
|----|----|----|
| **OWASP Top 10 for Agentic Applications 2026 (ASI-prefixed)** | OWASP GenAI Security Project, 9 Dec 2025 | Extends, does not replace, the OWASP LLM Top 10. A flat ten-item list, ASI01–ASI10, anchored to documented incidents; organizing principle "Least Agency." §7 carries the item-by-item crosswalk: one item (ASI04) uncovered, one (ASI10) partial after v3.0. |
| **OWASP MCP Top 10** | OWASP GenAI Security Project, 2026 | Tool-connection-layer risk list. Named as the pointer for ASI04 tool poisoning and supply chain (§7.3); not crosswalked. |
| **Cloud Security Alliance MAESTRO** | Cloud Security Alliance, Feb 2025 | A named threat-modeling methodology specific to multi-agent systems, decomposing across seven architectural layers rather than by attack surface; overlaps most with §7's inter-agent and orchestration surfaces. Not yet clause-crosswalked against Orchestration Contracts. |
| **Cloud Security Alliance Agentic Trust Framework (ATF)** | CSA blog Feb 2, 2026; open specification v0.9.1 public-review draft, April 2026, approaching v1.0 | Zero-trust governance for agents: four maturity levels (Intern, Junior, Senior, Principal), five promotion gates, and immediate demotion on a critical incident. Independently convergent with §5.1.3; crosswalked to DAS positions in §5.1.4; the ATF level is an optional AIR field (§5.5). |
| **Cloud Security Alliance Agent Identity Governance Framework (AIGF)** | CSA, May 2026 | Governance of agent identity creation, ownership, and removal; motivated by the finding that 78% of organizations have no documented policy for creating or removing agent identities. Anchors the AIR lifecycle and offboarding fields (§5.5). |
| **NIST AI Agent Standards Initiative** | NIST, via CAISI; launched Feb 17, 2026; page updated Aug 14, 2026 | Three pillars (industry-led standards, open-source protocols, security and identity research). Deliverables to date: an RFI on agent security (closed March 9, 2026), an NCCoE concept paper on agent identity and authorization (comments closed April 2, 2026) proposing OAuth 2.0, OIDC, and SPIFFE/SPIRE for agents, and sector listening sessions from April 2026. No final guidance yet. The concept paper anchors the AIR (§5.5). |
| **Singapore IMDA Model AI Governance Framework for Agentic AI** | Infocomm Media Development Authority; v1.0 Jan 22, 2026; v1.5 May 20, 2026 (updated June 5, 2026) | Four dimensions: assess and bound risk; human accountability; technical controls; end-user responsibility. v1.5 added multi-agent guidance, third-party agent guidance, platform-provider vs. system-provider responsibilities, automation-bias safeguards (override-rate and response-time monitoring), and skill-degradation guidance. Requires verifiable agent identity and an audit trail of which agent acted under whose authorization. Anchors the AIR (§5.5), the vendor-agent track (§5.8), and the ASI09 mitigations (§7.2). |

## B.9 U.S. state and sector note

U.S. state law on automated decision-making moved in 2025–2026 in ways that bear directly on the consequential-decision flag (§5.4.3) and the AISIA (§5.6). This note is a pointer, not a crosswalk; deployers should confirm applicability with counsel, and the "sector crosswalks are deployment-specific" caveat in B.7 applies.

| **Instrument** | **Status** | **What it requires that CRISP-AG artifacts record** |
|----|----|----|
| **Colorado SB 26-189 \[26\]** | Signed May 14, 2026; repeals and replaces the 2024 Colorado AI Act; effective January 1, 2027; Attorney General enforcement only, with a cure period through 2030 | Regulates automated decision-making technology that materially influences consequential decisions (employment, education, housing, lending, insurance, health care, essential government services). Pre-use notice; post-adverse-decision explanation within 30 days and a route to human review; three-year record retention; developer-to-deployer disclosures. Mapped to §5.4.3 (flag and autonomy cap), §5.6.2 (disclosure), §5.5 audit anchor (retention), §5.8 (developer disclosures). |
| **California Civil Rights Council regulations on automated-decision systems in employment \[34\]** | Effective October 1, 2025 | Anti-discrimination obligations for ADS used in employment decisions, including record-keeping. Mapped to the AISIA fairness-testing plan (§5.6.1) and the consequential flag. |
| **Illinois amendments to the Human Rights Act on AI in employment (HB 3773) \[35\]** | Effective January 1, 2026 | Prohibits discriminatory use of AI in employment decisions and requires notice to employees when AI is used for such decisions. Mapped to §5.6.2 and the consequential flag. |
| **Other jurisdictions** | Ongoing | Several states and the EU (Annex III, from December 2, 2027) regulate the same decision domains. The §5.4.3 list should be extended per deployment footprint. |

# References

\[1\] P. Chapman et al., "CRISP-DM 1.0: Step-by-step Data Mining Guide," SPSS Inc., 2000.

\[2\] S. Yao et al., "ReAct: Synergizing Reasoning and Acting in Language Models," ICLR, 2023.

\[3\] National Institute of Standards and Technology, "Artificial Intelligence Risk Management Framework (AI RMF 1.0)," NIST AI 100-1, 2023.

\[4\] National Institute of Standards and Technology, "Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile," NIST AI 600-1, 2024.

\[5\] ISO/IEC 42001:2023, "Information technology — Artificial intelligence — Management system," 2023.

\[6\] European Parliament and Council, "Regulation (EU) 2024/1689 laying down harmonised rules on artificial intelligence," Official Journal of the European Union, 2024.

\[7\] OWASP Foundation, "OWASP Top 10 for LLM Applications and Generative AI 2025," 2024.

\[8\] National Vulnerability Database, "CVE-2024-5184: Prompt injection vulnerability in EmailGPT," NIST NVD, 2024.

\[9\] Q. Wu et al., "AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation," 2023.

\[10\] LangChain / LangGraph documentation and related implementation references.

\[11\] X. Yang et al., "CRAG: Comprehensive RAG Benchmark," arXiv:2406.04744, 2024.

\[12\] M. S. Tamber et al., "Benchmarking LLM Faithfulness in RAG with Evolving Leaderboards," arXiv:2505.04847, EMNLP 2025 Industry Track. (Introduces the FaithJudge evaluation framework.)

\[13\] J. Schmidt, R. Samuels, S. Khushalani, et al., "Transforming procurement for an AI-driven world," McKinsey & Company, October 27, 2025. (Source of the 25–40% procurement-efficiency estimate; corrected in v3.0 — v2.4.1 attributed the figure to \[36\].)

\[14\] J. Ryseff, B. F. De Bruhl, and S. J. Newberry, "The Root Causes of Failure for Artificial Intelligence Projects and How They Can Succeed: Avoiding the Anti-Patterns of AI," RAND Corporation, RR-A2680-1, August 2024.

\[15\] Vanta, "State of Trust Report 2025," Vanta Inc., October 2025. (Survey of approximately 3,500 business and IT leaders fielded July 2025: 48% have developed frameworks to limit or define agent autonomy; 65% say agentic AI use is outpacing their understanding of it.)

\[16\] McHugh, Šekrst, and Cefalu, "Hybrid Prompt Injection Threats Combining XSS/CSRF with LLM Manipulation," arXiv:2507.13169, 2025.

\[17\] OWASP GenAI Security Project, "OWASP Top 10 for Agentic Applications 2026," December 9, 2025.

\[18\] Cloud Security Alliance, "MAESTRO: Multi-Agent Environment, Security, Threat, Risk, and Outcome," February 2025.

\[19\] J. Woodruff (MassiveScale.AI) with the Cloud Security Alliance Zero Trust and AI Safety Working Groups, "Agentic Trust Framework (ATF)," CSA blog, February 2, 2026; open specification v0.9.1, public review draft, April 2026 (github.com/massivescale-ai/agentic-trust-framework).

\[20\] National Institute of Standards and Technology, via the Center for AI Standards and Innovation (CAISI), "AI Agent Standards Initiative," launched February 17, 2026; initiative page updated August 14, 2026.

\[21\] Infocomm Media Development Authority (IMDA), Singapore, "Model AI Governance Framework for Agentic AI," version 1.0, January 22, 2026; version 1.5, May 20, 2026 (updated June 5, 2026).

\[22\] Cloud Security Alliance (with Workday), "State of Non-Human Identity and AI Security" survey, 2026. (Source of the approximately 45:1 non-human-to-human identity ratio.)

\[23\] Entro Security, research on non-human identity ratios in cloud-native environments (approximately 144:1), 2025–2026, as cited by the Cloud Security Alliance.

\[24\] Cloud Security Alliance and Strata Identity, "Securing Autonomous AI Agents" survey, February 5, 2026. (285 respondents: 28% can trace agent actions to a human sponsor across all environments; 21% maintain a real-time registry of active agents; 68% require human-in-the-loop but lack an architectural approach for it.)

\[25\] ISO/IEC 42005:2025, "Information technology — Artificial intelligence (AI) — AI system impact assessment," May 2025.

\[26\] State of Colorado, Senate Bill 26-189, "Automated Decision-Making Technology," signed May 14, 2026; effective January 1, 2027.

\[27\] National Institute of Standards and Technology, National Cybersecurity Center of Excellence, concept paper on software and AI agent identity and authorization, February 2026 (public comment period closed April 2, 2026).

\[28\] Cloud Security Alliance, "Agent Identity Governance Framework," May 2026; and CSA research with Oasis Security reporting that 78% of organizations have no documented policy for creating or removing agent identities, 2026.

\[29\] McKinsey & Company, "The State of AI: Global Survey 2026," August 2026.

\[30\] McKinsey & Company, "Agentic AI change management: closing the adoption gap," 2026.

\[31\] European Parliament and Council, Regulation amending Regulation (EU) 2024/1689 as regards the timeline of certain obligations ("Digital Omnibus on AI"); adopted by the European Parliament June 16, 2026 and by the Council June 29, 2026; signed July 8, 2026; published in the Official Journal and in force July 27, 2026.

\[32\] OWASP GenAI Security Project, "OWASP MCP Top 10" (Model Context Protocol security risks), 2026.

\[33\] Verizon, "2026 Data Breach Investigations Report," 2026, as cited by the Cloud Security Alliance (unapproved AI tool use reaching approximately 45% of the workforce).

\[34\] California Civil Rights Council, regulations on automated-decision systems under the Fair Employment and Housing Act, effective October 1, 2025.

\[35\] State of Illinois, HB 3773 (Public Act 103-0804), amending the Illinois Human Rights Act regarding the use of artificial intelligence in employment, effective January 1, 2026.

\[36\] A. Mittal, R. Belotserkovskiy, and T. Liakopoulou, "Redefining procurement performance in the era of agentic AI," McKinsey & Company, February 5, 2026. (Reports 20–30% procurement-staff efficiency gains from autonomous sourcing and up to 90% reduction in negotiation analysis time in case examples. Cited in v2.4.1 under incorrect authors as the source of the 25–40% range; see \[13\].)
