# Requirements Engineering Prompt Log & Iteration History
**Student Name:** Nguyen Tung Lam  
**Student ID:** V202603373  
**Group:** Group 10  
**Course:** Advanced Software Engineering (AY 26–27) · VinUniversity  
**Lab Assignment:** Chapter 2 – Requirements Engineering with AI Agents (SoopiFood)  
**Session Principle:** *Round 1 (Generate) → Review (Critique) → Iterate with Context (Refine)*  
*Core Lesson: "What did the agent not know? The fix is more domain context, not a longer prompt."*

---

## Summary of Labs & Prompt Iterations

| Lab # | Part | Step / Prompt | Goal / Action | Review Finding & Rationale for Iteration |
|---|---|---|---|---|
| **Lab 1** | **Part A** | `01_interview_guide.md` | Draft 45–60 min semi-structured interview guide for restaurant manager (discovery stage). | **Initial Prompt:** Created 9 questions across 6 sections with probes.<br>**Review Finding:** Q1 assumed overwhelm ("juggle") and Q4 led the manager to complain ("most frustrating challenges"). |
| **Lab 1** | **Part A** | `02_interview_guide_iterate.md` | Neutralize questions in the same session. | **One-line rationale:** *Neutralized leading and biased questions into objective phrasing so the manager can freely describe positive, neutral, or negative operational realities.* |
| **Lab 2** | **Part B** | `03_personas.md` | Synthesise interview notes (I1–I8) and observations (O1–O2) into 2–3 manager personas. | **Initial Prompt:** Produced Mateo, Sarah, and David.<br>**Review Finding & Rationale:** *Grounded all persona goals in operational end-states (not immediate UI tasks) and verified that every single behavior and pain point strictly cites source evidence [e.g., I1, O2] with no demographic hallucinations.* |
| **Lab 3** | **Part C** | `04_functional_requirements.md` | Specify functional requirements for the restaurant tablet. | **Initial Prompt:** Drafted FRs across 5 functional areas.<br>**Review Finding & Rationale:** *Enforced atomic 'The system shall...' syntax with exactly one observable behavior per requirement (eliminating compound 'and' statements) and replaced guessed timers with explicit [TBC] markers.* |
| **Lab 4** | **Part D** | `05_non_functional_requirements.md` | Formulate NFRs across FURPS+ / ISO categories with test methods. | **Initial Prompt:** Created NFRs for tablet and order service.<br>**Review Finding & Rationale:** *Replaced vague quality desires with measurable metrics, defined operational conditions (peak 6–9pm, Wi-Fi drops), and listed explicit stakeholder clarification questions for unresolved [TBC] thresholds.* |
| **Lab 5** | **Part E** | `06_epics_stories.md` | Decompose into Epics → Features → Stories for 5 devs in 2-week sprints. | **Initial Prompt:** Decomposed requirements into backlog items.<br>**Review Finding & Rationale:** *Structured stories as end-to-end demonstrable vertical slices with Given/When/Then criteria, withheld story points as instructed, and separated architectural NFRs into an explicit uncovered guardrails list.* |
| **Lab 6** | **Part F** | `07_moscow_round1.md` | MoSCoW prioritization of 15 stories using `backlog.yaml` only (50 pt budget). | **Round 1:** Prioritized based on core ordering flow (Must: 29 pts, Should: 10 pts, Could: 11 pts, Won't: 8 pts).<br>**Review Finding:** Placed promo codes (SF-06) in Should and reviews (SF-10) in Could because business launch strategy was unknown. |
| **Lab 6** | **Part F** | `08_moscow_round2.md` | Re-prioritize with `stakeholder_notes.md`. | **One-line rationale:** *Incorporated Founder, Operations, and Marketing stakeholder context to promote SF-06 to Must and SF-10 to Should while preserving the 50-point capacity budget.* |
| **Lab 7** | **Part G** | `09_change_requests.md` | Evaluate CR-01 (Allergens, 2 pts) and CR-02 (Split bill, 8 pts) against fixed 50 pt capacity. | **Review Finding & Rationale:** *Accepted non-negotiable legal regulation (CR-01) by explicitly funding it through demoting SF-09 to Won't, while rejecting marketing request CR-02 to prevent scope creep without trade-offs.* |
| **Lab 8** | **Part H** | `10_criteria_writer.md` | Write Gherkin acceptance criteria for SF-06 without business rules. | **Round 1:** Writer guessed promo values, assumed flat 10%, ignored delivery fees, and wrote invalid error strings. |
| **Lab 8** | **Part H** | `11_criteria_review_rewrite.md` | Review against `business_rules.md` (R1–R3) and rewrite scenarios on boundaries. | **One-line rationale:** *Audited initial criteria in review.md to expose missed caps, invalid fee math, and untested boundaries, then rewrote discount_v2.feature with exact boundary tests for rules R1, R2, and R3.* |
| **Lab 9** | **Part I** | `12_dod_audit.md` | Audit PR #42 (`pr_sf06.md`) against `DEFINITION_OF_DONE.md`. | **Review Finding & Rationale:** *Disregarded the author's subjective PR claims in favor of objective CI logs and diff inspection, exposing 5 failed DoD items (failing acceptance test, float division, skipped mypy, unreviewed, unverified staging) to issue an evidence-backed 'Not Done' verdict.* |

---

## Key Methodological Insights
1. **The Cost of Late Discovery:** Slide 5 shows the 100x–1,000x cost explosion when requirement defects reach production. Catching ambiguities in Lab 1 (interview phrasing) and Lab 8 (business rule gaps) prevents building the wrong system.
2. **Context Over Prompt Length:** In Lab 6 and Lab 8, the agent produced flawed outputs not because of flawed prompts, but because it lacked critical business and stakeholder context. Once supplied with `stakeholder_notes.md` and `business_rules.md`, output quality reached production standard immediately.
3. **Scope Discipline:** In Lab 7, respecting the "No new scope without a named trade-off" rule prevented budget overrun when external legal regulations emerged.
4. **Trust But Verify:** In Lab 9, developer self-certification ("All tests pass ✅") was proven false by CI run #318 (`1 failed`). Rigorous engineering requires verifiable evidence over verbal claims.
