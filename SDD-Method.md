<!-- GENERATED — do not edit.
     Derived by tools/derive_public.py from the internal edition.
     Regenerate with: python3 tools/derive_public.py
-->

# Specification-Driven Design for Agentic Systems — The Method

**Public edition** · Author: David Reed, PhD · Generated 2026-09-18

> This is a brand-neutral edition, published as general best-practice guidance. It
> carries no organisation-specific implementation detail. This is the method, with every illustration set in a neutral worked example: a system that extracts contractual obligations from commercial agreements. The internal edition's organisation-specific worked example and platform playbook are not included — they describe an operating model rather than a method, and renaming would not have made them brand-neutral. Each requirement is stated inline rather than cited by an identifier, so this document stands on its own.

---

**Method**

Part A is for everyone who will write, review, or sign off a specification for an agentic system. It sets out why the conventional approach is insufficient, the one distinction that organizes everything else, the four layers a specification needs, ten principles with worked examples, the lifecycle that connects specification to enforcement, how to treat the regulatory frame as an input, and the evaluation science the method depends on.

**A1. Why agentic systems need a different kind of specification**

A conventional specification — IEEE 830 and its successors — describes what a deterministic system shall do. Agentic systems break three of its assumptions. The component that does the work is probabilistic: the same input can produce different outputs, and vendors now say so explicitly \[36\]. The component drifts: model versions change behind a stable identifier, prompts accrete, retrieved context shifts, and the distribution of outputs moves without any code change \[7\]. And components compose in ways that produce failures no single-agent test reveals: an orchestrator that trusts an upstream agent's confidence inherits that agent's miscalibration \[2, 4\].

The consequence is that an agentic specification must say four things a conventional one does not. What the system shall *not* do — the prohibitions and the absorbing safety invariants that no downstream computation can reverse. What must hold *across* agent interactions — compositional properties, message contracts, and scope boundaries. How the system *governs its own evolution* — who can change a prompt, a model, a rule, and what evidence they need first. And which properties the system is *able* to promise, given that its substrate is controlled by a vendor. That last point is not theoretical. In 2026 Anthropic deprecated the temperature parameter for models released after Claude Opus 4.6; a specification written a year earlier that required temperature = 0.0 for determinism became unimplementable, and it had never actually delivered determinism — the vendor's own documentation says results at 0.0 "will not be fully deterministic," and independent measurement found 80 distinct completions from 1,000 identical temperature-0 requests under production load \[36\]. A contract bound to a vendor knob rather than to an observable property is not a contract.

The evidence on AI-assisted delivery says the same thing from the other direction. DORA's 2024 survey associated a 25% increase in AI adoption with a 7.2% decrease in delivery stability; its 2025 report, with five thousand respondents, still finds AI positively linked to throughput but negatively to stability, and frames AI as an amplifier of whatever practices already exist \[29\]. Veracode's 2025 and 2026 benchmarks found roughly 45% of unguided AI-generated code insecure, flat across model generations \[30\]. The one controlled trial with experienced developers on real tasks found them 19% slower with AI while believing they were 20% faster \[31\]. None of this argues against agentic systems. It argues that the practices an organization brings to them are decisive, and specification is the first of those practices.

> **What "specification-driven" means here.** Piskala \[1\] distinguishes three rigor tiers: *spec-first* (the spec guides development and drifts from the code over time), *spec-anchored* (the spec continuously validates and gates the code), and *spec-as-source* (the spec generates the code). This document's method targets the spec-anchored tier: the specification is written before the build, and it is connected to gates — schema validation, deterministic checks, tests, permission rules, blocking hooks, CI evaluation — that refuse non-conforming behavior. Spec-as-source is not recommended for governed systems today; the 2026 empirical record on it is thin and mixed \[15, 29\].

**A2. The organizing distinction: what enforces and what guides**

A mechanism *enforces* a requirement when it can refuse: a Pydantic model that rejects a malformed message, a pre-flight function that routes a case to a human before any model is called, a Unity Catalog grant that denies a write, a test that fails a pipeline, a hook that blocks a tool call. A mechanism *guides* when it can only influence: a system prompt, a CLAUDE.md file, a constitution, a style guide, a code comment. Guiding mechanisms are valuable — they are how you get useful behavior most of the time — but they are not controls, and treating them as controls is the most common design error in agentic systems.

The tool vendors say this themselves. Anthropic's Claude Code documentation describes CLAUDE.md as "context, not enforced configuration" and adds: "To block an action regardless of what Claude decides, use a PreToolUse hook instead" \[10\]. Cursor's documentation warns that "AI guidance should not be your only security control" \[13\]. GitHub Spec-Kit's constitution file declares its principles "NON-NEGOTIABLE" and its templates describe "Phase -1 gates" — but nothing in Spec-Kit intercepts a tool call; the gates are template text \[9\]. Across Claude Code, GitHub Copilot, Cursor, OpenAI Codex, and AWS Kiro, the enforcing mechanism has converged on the same shape: a pre-tool hook that returns *deny* (or exits with code 2), plus permission rules, sandboxes, and tests \[10–12\]. Kiro is the instructive exception — it generates property-based tests from EARS-syntax requirements, converting a guiding artifact into an enforcing one \[12, 42\].

The empirical record now supports the distinction. Two 2026 studies found that instruction files alone "do not generally improve task success rates" and add more than 20% to token cost, while spec-first phases with executable checks show measurable gains \[14, 15\]. Thoughtworks' Technology Radar Vol. 34 (April 2026) moved "context engineering" and "curated shared instructions" to Adopt and put "agent instruction bloat" in Caution — and dropped spec-driven development as a technique blip after one volume in Assess, keeping Spec-Kit and OpenSpec as tools to evaluate \[13\]. Read together: curate the guidance, keep it short, and put the weight on enforcement.

**The mechanism table**

Every requirement in a specification written to this method names its enforcing mechanism from the table below. A requirement whose only mechanism is in the last row is flagged *prompt-only* in the traceability matrix and must be paired with an enforcing backstop or accepted as a known weakness by a named owner.

| **Mechanism class** | **Examples** | **Can it refuse?** | **Where it lives** |
|----|----|----|----|
| **Deterministic gate** | Pre-flight functions; injection-pattern screens; OCR quality thresholds; language checks | Yes — before any model call | Orchestrator code |
| **Type and schema** | Pydantic models at every boundary; structured-output JSON schema at generation; enum constraints (e.g., who may set a status) | Yes — malformed or unauthorized values cannot be constructed | Message layer; model API call |
| **Permission and scope** | Unity Catalog grants; service principal per agent; tool allow-lists; Claude Code permissions.deny; PreToolUse hooks | Yes — the action is denied | Platform; agent runtime; coding agent |
| **Protocol rule** | State machine transitions the orchestrator will not make; absorbing terminal states; human-only transitions | Yes — the transition does not exist | Orchestrator |
| **Test and CI gate** | Golden-set evaluation with thresholds; hallucination zero-tolerance; consistency tests; Stop hooks that fail while tests fail | Yes — deployment is blocked | CI pipeline; coding agent |
| **Monitoring and switch** | Drift metrics with alerts; autonomy switch; rate and budget caps | After the fact — stops future actions | Platform; admin API |
| **Prompt-only (guidance)** | System prompt instructions; CLAUDE.md; constitution text; rubrics | No | Prompts and instruction files |

**A3. Four layers of an agentic specification, plus traceability**

The method synthesizes four traditions, each used where it adds the most clarity, and adds a traceability layer that binds them to code and tests.

| **Layer** | **Drawn from** | **Answers** | **Written for** | **Typical artifacts** |
|----|----|----|----|----|
| **1. Intent and stakeholders** | GitHub Spec-Kit's specify/plan/tasks flow \[9\]; SPARC; user-journey practice | Why the system exists, who touches it, what success is, what must never happen | Non-engineers first | Problem statement with sourced figures; scope; stakeholder table; journeys; success criteria; hard and soft constraints; assumptions; threat model; regulatory frame |
| **2. Agent behavioral contracts** | Design by Contract \[3\]; Agent Behavioral Contracts \[2\] | What each agent requires, guarantees, never does, may consume, and how reproducible it is | Engineers and reviewers | PRE / POST / INVARIANT / PROHIBIT / RESOURCE / CONSISTENCY / ESCALATION clauses per agent; drift definitions |
| **3. Orchestration protocol invariants** | Multi-agent architecture research \[4, 5\]; protocol-invariant thinking | How agents compose without emergent failure | Engineers | Message schemas; role-capability scope matrix; state machine; pre-flight invariants; routing invariants; termination; compositionality |
| **4. Compliance and governance** | AGENTSAFE, POLARIS \[5, 6\]; the binding regulatory and professional frame | How the system is audited, secured, evaluated, changed, and stopped | Risk, compliance, audit, platform | Audit controls; access; governed evolution; evaluation and drift; runtime controls; data protection; professional-standards deny-list; change control |
| **Traceability** | IEEE 830 conventions, mechanized | Which requirement is enforced by what, verified how, and where the gaps are | Everyone | Machine-readable requirements table; generated matrix; computed coverage; gap register |

The layers are not phases. Intent is written first and revisited last; contracts and protocol invariants are written together because a contract's escalation triggers are the protocol's routing rules; governance is written alongside both because the regulatory frame produces hard constraints in layer 1 and controls in layer 4. Traceability is generated, never hand-maintained.

**Notation**

Requirements use shall (mandatory), shall not (prohibited), should (recommended; deviation requires a documented reason), and may (permitted). Behavioral clauses use the GIVEN / WHEN / THEN form — a precondition, an activation condition, and a required outcome — which is equivalent to a pre/post-condition pair without temporal-logic notation. Every requirement carries a stable identifier (PRE-EXT-01, PROTO-INV-03, GOV-04) that appears in code comments, test names, and the traceability table.

> AGENT CONTRACT: \<AgentName\>
>
> PRECONDITIONS — what must be true before the agent is invoked
>
> POSTCONDITIONS — what must be true after the agent returns
>
> INVARIANTS — properties that hold throughout execution
>
> PROHIBITIONS — what the agent must never do (hard negative constraints)
>
> RESOURCE BOUNDS — maximum resources per invocation
>
> CONSISTENCY — observable reproducibility properties
>
> ESCALATION TRIGGERS — conditions under which the agent must recommend escalation
>
> Behavioral clause:
>
> GIVEN \[context condition\]
>
> WHEN \[triggering event\]
>
> THEN \[required outcome\] — and the mechanism that enforces it

**A4. Ten principles**

Each principle is stated, justified, shown in a worked example — a system that extracts contractual obligations from commercial agreements — and paired with the anti-pattern it exists to prevent.

**Principle 1 Bind contracts to observable properties, not vendor controls**

> A contract clause shall reference an output, a distribution, a count, or a bound the system can measure — never a parameter whose availability or semantics the system does not own.

**Why.** Vendors change parameters, retire model identifiers, and alter defaults. A clause such as temperature = 0.0 promised determinism it could not deliver and then became a 400 error \[36\]. Decision-level consistency across repeated runs is measurable regardless of the API.

**In the worked example.** A consistency requirement: five independent extraction runs on the golden set must agree on each Tier A field value in at least 98% of cases, measured per model identifier and re-run on any change. No sampling parameter appears anywhere in the specification.

**Anti-pattern.** Specifying seed, temperature, or top_p values as the reproducibility control, and treating a passing test at one model version as evidence for the next.

**Principle 2 Put determinism before probability**

> Every request shall pass through deterministic pre-flight checks before any model is called, and a pre-flight decision to escalate shall be absorbing: no downstream agent output can reverse it.

**Why.** The cheapest, most auditable, and most reliable controls are the ones that never invoke a model. Pre-flight checks cost nothing in tokens, are fully testable, and give the system a place to put every rule a regulator or a professional body imposes as a bright line.

**In the worked example.** Seven pre-flight invariants route to a human, without a model call, any document that fails OCR quality thresholds, is in a language without a certified translation path, contains natural-person screening content, matches injection patterns, has missing or out-of-order pages, or names a counterparty on a sanctions watch-list. A composition rule makes those decisions absorbing: once a document is routed to a human, no downstream step can route it back.

**Anti-pattern.** Asking the model to decide whether a document is safe to process, then trusting its answer.

**Principle 3 Type every boundary and enforce the schema at generation**

> All inter-component messages shall be typed models validated at the boundary, and model outputs shall be produced under structured-output schema enforcement; a schema violation is a termination condition, not a retry.

**Why.** Types are the enforcing mechanism that costs nothing at runtime and catches an entire class of failures — including unauthorized values — before they propagate. Structured outputs at generation time are now generally available on the Anthropic API and on Databricks model serving \[36, 38\]; Pydantic validators can make an unauthorized state literally unconstructible.

**In the worked example.** The ExtractedField type requires a source citation (document, page, clause) for every value; the ReleaseDecision type's validator rejects any release without a human reviewer identifier. An agent cannot construct a released record.

**Anti-pattern.** Free-text agent outputs parsed with regular expressions, and retrying on parse failure until something parses.

**Principle 4 Confidence is a measured quantity, not a self-report**

> Any confidence score used to route work shall come from an estimator with a current calibration record, and routing thresholds shall be inoperative in its absence.

**Why.** Verbalized confidence from language models is systematically overconfident \[33\]. In document extraction, a model's own self-critique reached 12.9% specificity — it almost never said it was wrong when it was — while a lightweight classifier over the model's final-token embeddings achieved 99.9% precision at a 5% base error rate \[28\]. Routing on the former is routing on noise.

**In the worked example.** A calibration requirement: an external calibrated estimator — or cross-model agreement plus citation verification — with expected calibration error ≤ 0.05 on Tier A fields for the pinned model identifier. A routing invariant sends everything to human verification whenever no current calibration record exists.

**Anti-pattern.** Reading "confidence": 0.97 out of the model's JSON and comparing it to 0.95.

**Principle 5 The regulatory frame is a specification input that produces invariants**

> Each binding legal, regulatory, or professional instrument shall be listed with its status, and each shall produce at least one hard constraint or governance control that carries the instrument as its source.

**Why.** Regulation and professional standards are where the bright lines come from — the things a system must never do regardless of documentation quality. Treating them as a compliance appendix loses the invariants; treating them as inputs generates them. For a global firm the frame is also the map of where the same agent set is legal to run.

**In the worked example.** Professional licensing statutes yield the deny-list (no negotiating, no advising on terms, no signature, no holding out as licensed) \[23\]; EU AI Act Article 6(3) and California's 'substantially replaces human decision-making' test both reward the same design — agents propose, a named human decides \[16, 18\]; the financial-reporting standard governing the extracted fields defines which of them are Tier A \[20\]; where a statute or professional standard requires a licensed professional's judgment, that professional is the terminal state \[23\].

**Anti-pattern.** A compliance section that lists statutes and produces no requirement.

**Principle 6 Some decisions are human by design, not by threshold**

> Where law, professional standards, or the safety property require a human decision, the human-only path shall be enforced at three independent layers — agent contract, type, and protocol — so that no composition of agent outputs can reach the outcome.

**Why.** A threshold can be tuned; a structural boundary cannot. Enforcing the same property in three places means that a prompt regression, a schema change, and an orchestrator bug would all have to coincide.

**In the worked example.** Releasing a record to a client system, exercising or waiving a contractual option, notifying a counterparty, and communicating a professional opinion are human-only. Per-agent prohibition clauses, the ReleaseDecision validator, and a protocol invariant — RELEASED is reachable only from HUMAN_VERIFY, by a reviewer action — enforce it in three places; a composition rule states the pipeline-wide property.

**Anti-pattern.** One if confidence \> 0.95: auto_release() line as the only control on an irreversible action.

**Principle 7 Audit is the system of record, and platform logs are not**

> Every decision-relevant action shall write an immutable audit record — before processing begins, at each agent start and completion, at each state transition, and at each human action — carrying a correlation identifier, the actor, the model identifier, and the prompt version.

**Why.** Platform logs are best-effort and platform-owned; Databricks' own inference tables do not guarantee rows for 401/403/429/500 responses and drop payloads over 10 MiB \[38\]. An auditor under the FY2026 PCAOB amendments needs evidence over information 'processed using technology-based tools' \[22\]; a SOC 1 service auditor needs the control to be describable and testable \[21\]. Neither can rely on a log you do not control.

**In the worked example.** Seven audit requirements specify an append-only table with INSERT-only grants, CHECK constraints, correlation identifiers, start/complete pairs, actor accountability, and per-record model and prompt provenance; a 'pre-write before processing' rule proves a request was received even if the pipeline crashes.

**Anti-pattern.** Pointing the auditor at the model-serving inference table.

**Principle 8 Coverage is computed, not asserted**

> The traceability matrix shall be generated from a machine-readable requirements table, and coverage shall be reported by enforcement mechanism class with every unverified requirement listed as a gap.

**Why.** Hand-maintained matrices drift and flatter. In one agentic specification reviewed while developing this method, the matrix stated that every requirement lacking a test was flagged as a gap, and flagged none — 47% of its identifiers had no row at all. A generated matrix cannot hide that, and a generated matrix is the artifact a build team, a reviewer, and an auditor can all act on.

**In the worked example.** The coverage matrix is generated from the requirements table, never written by hand. It reports, per layer, how many requirements are enforced by a deterministic gate, a type, a permission, a protocol rule, a test, a monitor, or prompt text only — and lists the prompt-only ones by name.

**Anti-pattern.** A traceability table with a 'Verification' column that is filled in by hand and never re-derived.

**Principle 9 Model and prompt change is a drift event that re-opens the gate**

> The model identifier and prompt version shall be pinned in configuration and recorded on every decision; any change to either, or to a judge model or a rule set, shall require the golden set, the calibration record, and the judge validation to be re-run and approved by a named person before autonomous operation resumes.

**Why.** Vendors retire and update identifiers on their own schedule — Databricks retires databricks-claude-sonnet-4 on 9 October 2026, for instance \[38\] — and a system that pins nothing is drifting whether or not anyone is watching. FDA's predetermined-change-control thinking \[see Part A6\] and the professional-standards requirement for written reliability assessments of high-impact outputs both describe the same control.

**In the worked example.** Four change requirements: exact identifiers only; provenance on every record; a change gate with five evidence items and a named approver; immutable prompt versions once referenced by any persisted decision. A drift definition makes an observed identifier mismatch a drift event.

**Anti-pattern.** Using a floating alias such as latest, and discovering the model changed when reviewer overturn rates move.

**Principle 10 Threat-model the corpus, not just the wire**

> The specification shall include a threat model that treats every ingested document as untrusted input, denies write-capable tools to any agent that reads such input, and pairs prompt-borne defenses with deterministic screens.

**Why.** Indirect prompt injection is the canonical failure mode for systems that place third-party documents in a model's context \[37\]. Platform guardrails inspect prompts and responses on the wire; they do not see instructions embedded in a retrieved contract clause. A commercial agreement is authored by a counterparty's lawyer; it is not a trusted input.

**In the worked example.** The threat model produces four named threats and a pre-flight invariant for injection patterns; no extraction agent has a tool that can write to any store or send any message; the injection test suite includes agreements with embedded instructions.

**Anti-pattern.** Relying on the model-serving PII and jailbreak guardrails as the injection control.

**A5. The operational lifecycle and its gates**

The method is a sequence of artifacts, each gated by a review that checks a short list of properties before the next artifact is written. The gates are the operational guideline; the checklists that accompany them are the working form.

| **Stage** | **Artifact produced** | **Gate: what must be true to proceed** | **Owner** |
|----|----|----|----|
| **1. Constitution** | A one-page statement of the safety property, the human-only decisions, the enforce/guide rule, and the regulatory frame | Every human-only decision is stated as a structural property, not a threshold; the frame lists instruments with status | Service-line owner + risk |
| **2. Intent specification** | Problem statement with sourced figures; scope; stakeholders; journeys; success criteria; constraints; threat model | Every figure has a primary source; every hard constraint carries an instrument or the safety property as its source; the threat model names assets, vectors, and controls | Product owner |
| **3. Contracts and invariants** | Per-agent contracts; message schemas; scope matrix; state machine; pre-flight, routing, termination, and compositional invariants | Every clause names an observable property and an enforcing mechanism; every escalation trigger appears as a routing rule; the state machine has no agent transition into a human-only state | Tech lead + reviewer |
| **4. Governance specification** | Audit, access, governed evolution, evaluation and drift, runtime controls, data protection, professional-standards deny-list, change control | Each control names its evidence artifact; the audit store is a system of record you own; the change gate has a named approver | Platform + compliance |
| **5. Requirements table and generated matrix** | requirements.csv; matrix; coverage by mechanism class; gap register; prompt-only list | Coverage is computed; every prompt-only requirement has an enforcing backstop or a named risk owner | Tech lead |
| **6. Build with enforcement** | Code; tests named by REQ-ID; CLAUDE.md constitution; hooks; permissions; CI gate | Tests exist for every 'Test' mechanism; hooks block the denied actions; CI fails on threshold or hallucination | Engineers |
| **7. Evaluation baseline** | Golden set (versioned, stratified, sized); judge validation record; calibration record; consistency record | Golden set ≥ minimum size with power stated; judge κ ≥ threshold against human labels; ECE ≤ threshold; consistency ≥ threshold | Eval owner + domain experts |
| **8. Controlled operation** | Autonomy switch; drift monitors; weekly production sample; subgroup and per-field error reports | Switch tested; alerts wired; sample size stated; reviewer overturn rate tracked as a KPI | Operations |
| **9. Change control** | Change requests for model, prompt, judge, rule, inventory; re-run evidence; approval record | All five evidence items present; previous configuration retained for rollback | Change board |

Two properties of the lifecycle matter more than its sequence. First, stages 2 through 5 are cheap relative to stage 6 — they are documents and a table — and they are where the irreversible decisions get made. Second, stages 7 through 9 are permanent: the evaluation baseline is re-established at every change, and controlled operation never graduates into unmonitored operation. A system that passes its gate once and is then left alone is a system whose gate has been removed.

**A6. The regulatory frame as a specification input**

The method treats the regulatory and professional-standards frame as a worksheet completed early, not a review performed late. For each instrument: what it is, whether it binds this system in this jurisdiction, what it requires, and which requirement identifier carries it. Instruments that do not bind but embody good practice are adopted *by analogy* and labelled so.

**The worksheet, completed for a global commercial real estate firm**

The table below is the frame for the worked example, as of September 2026. It is what Principle 5 looks like when done. Every row produced at least one requirement.

| **Instrument** | **Status (Sept 2026)** | **What bites on document-extraction agents** | **Produces** |
|----|----|----|----|
| EU AI Act (Reg. 2024/1689) as amended by the Digital Omnibus (Reg. (EU) 2026/1744, in force 27 Jul 2026) \[16\] | Art. 50 transparency applies from 2 Aug 2026; Annex III high-risk obligations deferred to 2 Dec 2027 | Document-extraction workflows of this kind are not Annex III. Natural-person creditworthiness scoring is Annex III 5(b). The Art. 6(3) 'preparatory task' exemption is lost when a system issues a specific recommendation or evaluation that plays a decisive role (Commission draft guidelines, 19 May 2026). People interacting with an AI assistant must be told. | A hard constraint barring natural-person scoring; a human of record on every released output; an Art. 50 disclosure requirement; a per-agent Art. 6(3) rationale in the agent registry |
| GDPR / UK GDPR; CJEU *SCHUFA* C-634/21; UK DUAA 2025 Arts. 22A–22D (commenced 5 Feb 2026); EDPB Opinions 22/2024 and 28/2024 \[17\] | In force | Commercial agreements contain personal data (guarantors, signatories, sole traders). Art. 22 bites on solely automated significant decisions about natural persons — screening, not extraction. DPIA required for AI processing at scale. Deployers must do due diligence on model providers' training lawfulness and know the sub-processor chain. | A DPIA per pipeline; minimization and redaction before model calls; a vendor due-diligence record; the bar on natural-person scoring |
| US state privacy and AI laws: California CPPA ADMT regulations (effective 1 Jan 2026; ADMT duties from 1 Jan 2027); Colorado SB 26-189 (effective 1 Jan 2027); Texas TRAIGA (1 Jan 2026) \[18, 19\] | In force / phasing in | ADMT is technology that 'replaces or substantially replaces' human decision-making on significant decisions (housing, finance, employment). TRAIGA offers a safe harbour for substantial compliance with NIST AI RMF. | A human of record on every released output; NIST AI RMF as the documented governance spine; an agent-registry gate: 'does this agent make or substantially make a consequential decision about a natural person?' |
| The financial-reporting standards governing the extracted fields; SOX 404; SOC 1 (SSAE 18 / AT-C 320) and ISAE 3402; PCAOB AS 2601 / AICPA AU-C 402 \[20, 21\] | In force | Extracted fields that drive the balance sheet — commencement, non-cancellable term, options reasonably certain to be exercised, fixed and index-linked payments, incentives, discount-rate inputs, modifications — are Tier A. Where extracted data feeds a client's ICFR, agent controls sit inside the SOC 1 description and the client operates complementary user-entity controls. | The Tier A field list; provenance, reviewer of record, sampled error rates, and reconciliation from the extracted record through the system of record to the client's general ledger |
| PCAOB amendments to AS 1105 and AS 2301 on technology-assisted analysis, effective FY2026 audits \[22\] | In force | Auditors must evaluate the reliability of information 'obtained or processed using technology-based tools' and investigate items identified by such procedures. | Model and prompt provenance per record; documented per-field error rates |
| Professional-practice standards in the applicable domain \[23\] | In force | Where a professional standard governs the output, the professional must evaluate the tool and the data, perform independent analysis, and assess credibility; high-impact outputs need a written reliability assessment and approval by a named qualified individual. A machine-generated professional opinion issued by a licensee is that licensee's work product. | A human terminal state for any output a professional standard governs; a deny-list item barring the agent from rendering the professional opinion itself |
| Professional licensing statutes in the applicable jurisdiction \[23\] | In force | Only licensees may negotiate, advise clients on terms, or render the opinions the licence covers; a work product that resembles a licensed opinion must carry the appropriate disclaimer. | Hard constraints barring negotiation, counterparty communication, professional opinions and signature; a scope-matrix column 'may communicate externally' |
| FCRA; sector screening guidance (some withdrawn 2025; statutory duties remain) \[19\] | Statute in force | Natural-person screening — guarantors, individual counterparties — is where FCRA, GDPR Art. 22, EU Annex III 5(b), and CA/CO ADMT converge. | The bar on natural-person scoring; a pre-flight invariant routing screening content to a human with no model call |
| OFAC sanctions (strict liability) \[19\] | In force | Counterparty screening remains a compliance-officer decision; agents assemble evidence and flag. | A pre-flight watch-list check routing to compliance; no autonomous 'clear' |

Two observations from completing the worksheet. The instruments that bite hardest on this system are financial-reporting and professional standards, not AI law: the auditor's need for reliable evidence and the surveyor's duty of independent analysis set the human terminal states. And AI law, where it does apply, rewards the same design — a human of record, disclosure of AI interaction, documented rationale — so the controls that satisfy SOC 1 and the applicable professional standard are the controls that keep the system out of the high-risk and ADMT categories. That convergence is not a coincidence; it is the reason the regulatory frame belongs at the front of the specification.

**A7. Evaluation science: golden sets, calibration, judges, drift**

Four quantities the method depends on are routinely assumed rather than measured. Each has a body of evidence and a simple discipline.

**Golden-set size and statistical power**

An evaluation set is a sample, and a pass rate on it has a confidence interval. Twenty cases behind an 80% gate has a 95% interval of roughly ±18 points — it cannot distinguish a system at 80% from one at 62% \[34\]. The discipline: state the minimum size from the interval you can tolerate, stratify across the scenario groups the routing logic distinguishes (including hard cases such as amendments and handwritten riders), version the dataset by content hash, and report the interval alongside the pass rate. The worked example requires at least 200 agreements with expert-annotated Tier A fields, stratified by document quality, jurisdiction, and amendment count, and reports a Wilson interval on every run.

**Calibration of any confidence used for routing**

Calibration is the property that a confidence of 0.9 is right about 90% of the time. It is measured with expected calibration error (binned), the Brier score, and a reliability diagram; it is specific to a model identifier and a dataset version, and it decays when either changes \[33\]. Verbalized confidence from generative models is systematically overconfident; consistency-based aggregation and external classifiers do better \[28, 33\]. The discipline: no routing threshold is operative without a current calibration record, and the record is re-established at every change gate.

**Validity of the judge**

An LLM used as a judge is itself a model with biases — position, verbosity, and self-preference among them \[35\]. Strong judges can reach agreement with humans comparable to human-human agreement, but only the largest models align reasonably, percent agreement alone is misleading, and leniency bias is common \[35\]. The discipline: before any judge gates a pipeline, measure its agreement with at least two independent human experts on a labelled subset using a chance-corrected statistic (Cohen's κ), record the judge's model identifier and prompt version, and treat a judge change as a change-gate event.

**Drift, and the difference between monitoring and detecting**

Drift is a change in the distribution of outputs not explained by a change in the distribution of inputs \[7\]. It is detected by defined metrics with baselines and windows — approval or straight-through rates, reviewer overturn rates, per-field error rates, subgroup divergences — and by a change in the model identifier behind a pinned name. A weekly production sample must be large enough that the threshold is distinguishable from zero: a 5% hallucination threshold cannot be checked on 20 cases, where one event is 5%. The discipline: define the metric, the baseline, the window, and the sample size together, and make an identifier change a drift event by definition rather than a discovery.

> **A note on evidence quality throughout.** Rath's Agent Stability Index is cited for its structure, not its magnitudes — its validation is simulation-based \[7\]. The 2026 spec-driven-development studies are small, high-variance, and in some cases pre-registered without results yet \[15, 29\]. The independent contract-extraction benchmarks are the strongest evidence in this document and they are not specific to any one document type \[24–27\]. The method is designed so that the organization replaces these priors with its own measurements within the first two quarters of operation.

**References**

*Sources cited above. Numbering follows the full edition, so a reader comparing the two documents sees the same numbers.*

1. A lease administrator uploads a 78-page executed office lease for Client K. document_received is written to the audit store before anything else runs.

2. Pre-flight passes: OCR quality above threshold, English, all pages present and ordered, no screening content, no injection patterns, no watch-list hit.

3. IntakeAgent classifies the document as a base lease and opens a new lease family. ExtractionAgent produces 94 fields, each with a citation or a NOT_FOUND status; 31 are Tier A.

4. CriticalDateAgent derives expiration, three option windows, and a CAM audit deadline, each with a derivation trace to the clauses it used.

5. The calibrated estimator scores every field. 52 Tier B and C fields exceed their thresholds and are marked straight-through; 11 Tier B fields fall below and join the review queue with all 31 Tier A fields.

6. A senior lease analyst verifies the 31 Tier A fields (confirming 29, correcting 2 — a rent step date off by one month because the model read a table row boundary wrong — with the corrections recorded as reviewer feedback), reviews the 11 routed fields, and RELEASES the abstract. The release record carries her identifier, the model identifier, and the prompt version.

7. Rath, A. "Agent Drift: Quantifying Behavioral Degradation in Multi-Agent LLM Systems Over Extended Interactions." arXiv:2601.04170, January 2026. Agent Stability Index (12 metrics, 4 categories); validation is simulation-based — cited for structure, not magnitudes.

9. Delimarsky, D. "Spec-driven development with AI: Get started with a new open source toolkit." GitHub Blog, 2 September 2025. GitHub Spec-Kit v1.0.3, 1 September 2026; README disclaimer on community extensions (github.com/github/spec-kit).

10. Anthropic. Claude Code documentation (code.claude.com): *Memory* ("CLAUDE.md is context, not enforced configuration… To block an action regardless of what Claude decides, use a PreToolUse hook instead"); *Hooks* (event list, exit-code semantics, permissionDecision, Stop-hook eight-block ceiling); *Permissions* and *Permission modes*; *Headless* (claude -p, --json-schema, dontAsk); *Skills*; *Best practices*. Accessed 4 September 2026.

11. Agentic AI Foundation (Linux Foundation). *AGENTS.md* specification, donated by OpenAI 9 December 2025; OpenAI Codex documentation on hooks and AGENTS.md (32 KiB cap). Accessed September 2026.

12. Amazon Web Services. *Kiro documentation*: specs (requirements.md in EARS notation, design.md, tasks.md), steering, agent hooks, property-based tests generated from EARS requirements. GA 17 November 2025. Accessed September 2026.

13. Thoughtworks. *Technology Radar* Vol. 33 (November 2025; spec-driven development, Assess) and Vol. 34 (April 2026; GitHub Spec Kit and OpenSpec, Assess; context engineering and curated shared instructions, Adopt; agent instruction bloat, Caution; AI-accelerated shadow IT and complacency with AI-generated code, Caution). Cursor documentation: "AI guidance should not be your only security control."

14. Gloaguen, T., et al. "Do AI Agents Need Context Files?" arXiv:2602.11988, February 2026 (context files do not generally improve task success; \>20% cost increase). Khatri, S. arXiv:2607.27250, July 2026. Both preprints.

15. Feng, Chen, Meyer, Mussbacher. "Structured Spec-Driven Engineering." arXiv:2605.02455, May 2026 (pilot; any structured spec improved test pass rate; high variance). Rosa, et al. "Spec-Driven Code Generation with LLMs: Empirical Study Design." SANER 2026 registered report (no results yet). Alenezi, arXiv:2607.16680 (position paper; enterprise case claims unverified).

16. Regulation (EU) 2024/1689 (Artificial Intelligence Act) as amended by Regulation (EU) 2026/1744 (Digital Omnibus on AI), OJ L 24 July 2026, in force 27 July 2026: Article 50 applicable 2 August 2026; Annex III obligations deferred to 2 December 2027. European Commission, draft guidelines on high-risk classification, 19 May 2026 (Art. 6(3) exemption lost where a system issues a specific recommendation or evaluation). Annex III point 5(b) (creditworthiness of natural persons).

17. Regulation (EU) 2016/679 (GDPR) Arts. 22, 28, 35; CJEU, *SCHUFA Holding*, C-634/21, 7 December 2023; UK Data (Use and Access) Act 2025, UK GDPR Arts. 22A–22D, commenced 5 February 2026 (SI 2026/82); EDPB Opinion 22/2024 (processors and sub-processors) and Opinion 28/2024 (AI models), 2024.

18. California Privacy Protection Agency, regulations on automated decisionmaking technology, risk assessments, and cybersecurity audits, approved 23 September 2025, effective 1 January 2026 (ADMT notice and opt-out duties from 1 January 2027; first-compliance date reported variously as 1 January or 1 April 2027 — verify). Colorado SB 26-189 (2026), effective 1 January 2027, replacing SB 24-205.

19. Fair Credit Reporting Act, 15 U.S.C. §1681 et seq. (HUD 2 May 2024 AI tenant-screening guidance and CFPB January 2024 advisory opinions withdrawn in 2025; statutory duties remain). Texas Responsible Artificial Intelligence Governance Act (HB 149), effective 1 January 2026, safe harbour for substantial compliance with NIST AI RMF. OFAC sanctions programs (strict liability); FinCEN CRE AML ANPRM (December 2021; no proposed rule as of September 2026).

20. The financial-reporting standards governing the extracted fields — the recognition, measurement, option and modification requirements that determine which fields are Tier A.

21. AICPA SSAE 18 / AT-C 320 (SOC 1); IAASB ISAE 3402; PCAOB AS 2601 and AICPA AU-C 402 (service organizations and complementary user-entity controls).

22. PCAOB. Amendments to AS 1105 *Audit Evidence* and AS 2301 *The Auditor's Responses to the Risks of Material Misstatement* relating to technology-assisted analysis, effective for audits of fiscal years beginning on or after 15 December 2025 (FY2026). PCAOB Staff Spotlight on generative AI, 22 July 2024. AICPA SAS 142.

23. Professional-practice standards and licensing statutes in the applicable domain — the requirements that a qualified professional evaluate the tool and the data, perform independent analysis, and remain the terminal decision-maker for outputs the standard governs.

24. Hendrycks, D., et al. "CUAD: An Expert-Annotated NLP Dataset for Legal Contract Review." NeurIPS 2021 Datasets and Benchmarks (arXiv:2103.06268): 510 contracts, 13,101 clauses, 41 categories; best 2021 baseline AUPR 47.8%.

25. "The Hidden Structure: Input Format and LLM Performance on Contract Review." arXiv:2505.12837, 2025 (CUAD subset; GPT-4.1 exact match 48% → 79% with structure-aware input; authors judge insufficient for autonomous decisions).

26. "ContractEval: Benchmarking LLMs for Clause-Level Legal Risk Identification." arXiv:2508.03080, 2025 (19 models; performance comparable to junior legal assistants; over-abstention in open models).

27. "ContractScrub." arXiv:2608.20204, 20 August 2026 (nine frontier models; best macro recall 0.75, F1 \< 0.65; contextual inference recall 0.427; degradation when related text is \> 10,000 characters apart).

28. ApplyBoard. "Embedding Confidence to Enhance Trust in AI Document Entity Extraction." IEEE ICPRS 2025 (final-token-embedding classifier: F1 97.5%, precision 99.9%, recall 95.2% at 5% base error; LLM self-critique specificity 12.9%). "Know Your Limits: A Survey of Abstention in Large Language Models." TACL 2024.

29. DORA (Google Cloud). *Accelerate State of DevOps 2024* (25% AI adoption increase associated with −7.2% delivery stability); *State of AI-assisted Software Development 2025*, 23 September 2025 (~5,000 respondents; AI as amplifier; DORA AI Capabilities Model); *ROI of AI-assisted Software Development*, May 2026.

30. Veracode. *2025 GenAI Code Security Report*, 30 July 2025 (~45% of AI-generated code insecure across 100+ models); *Spring 2026 GenAI Code Security Update*, 24 March 2026 (45–55% pass rates, flat).

31. METR. "Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity." 10 July 2025 (RCT; developers 19% slower while believing 20% faster). Cui, Z., et al. "The Effects of Generative AI on High-Skilled Work: Evidence from Three Field Experiments." *Management Science*, 2025 (+26% completed tasks; 4,867 developers).

33. Xiong, M., et al. "Can LLMs Express Their Uncertainty? An Empirical Evaluation of Confidence Elicitation in LLMs." ICLR 2024 (arXiv:2306.13063). Tian, K., et al. "Just Ask for Calibration." EMNLP 2023 (arXiv:2305.14975).

34. Miller, E. "Adding Error Bars to Evals: A Statistical Approach to Language Model Evaluations." arXiv:2411.00640, November 2024.

35. Zheng, L., et al. "Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena." NeurIPS 2023 (arXiv:2306.05685). Thakur, A. S., et al. "Judging the Judges: Evaluating Alignment and Vulnerabilities in LLMs-as-Judges." arXiv:2406.12624 (2024; published 2025).

36. Anthropic. Claude Developer Platform, Messages API reference, temperature: "Deprecated. Models released after Claude Opus 4.6 do not support setting temperature. A value of 1.0 will be accepted for backwards compatibility, all other values will be rejected with a 400 error… Note that even with temperature of 0.0, the results will not be fully deterministic." Accessed 4 September 2026. He, H. (Thinking Machines Lab). "Defeating Nondeterminism in LLM Inference." September 2025 (80 distinct completions from 1,000 identical temperature-0 requests).

37. OWASP. *Top 10 for LLM Applications 2025* (March 2025: LLM01 Prompt Injection, LLM03 Supply Chain, LLM06 Excessive Agency, LLM08 Vector and Embedding Weaknesses); *Top 10 for Agentic Applications 2026* (9 December 2025); *Agentic AI — Threats and Mitigations* (February 2025).

38. Databricks documentation (docs.databricks.com), accessed 4 September 2026: *AI governance with Unity Gateway* (GA 4 August 2026; guardrails and service policies Beta); *Foundation Model APIs — supported models* (Claude endpoints; databricks-claude-sonnet-4 retirement 9 October 2026; Claude Sonnet 5 without sampling parameters); *Structured outputs* (Claude limitations); *Databricks Geos* and *Foundation Model APIs compliance*; *Inference tables* (best-effort delivery; 10 MiB payload limit); *Build agents on Databricks* (Databricks Apps as recommended runtime); *MLflow 3 GenAI evaluation, datasets, judges, production monitoring, tracing to Unity Catalog, Prompt Registry (Beta)*; *Data quality monitoring / data profiling*; *Declarative Automation Bundles*; *Unity Catalog privileges (fine-grained INSERT/UPDATE/DELETE, Beta), table properties (\`delta.appendOnly\`), constraints, multi-statement transactions*; *Databricks Apps authorization*; *Databricks AI Search*; *Agent skills in Unity Catalog (Beta)*; *Coding-agent integration via model provider services*.

42. Mavin, A., Wilkinson, P., Harwood, A., Novak, M. "Easy Approach to Requirements Syntax (EARS)." IEEE RE 2009.

