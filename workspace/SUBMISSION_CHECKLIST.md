# Course Assignment Submission Checklist & Summary
**Student Name:** Nguyen Tung Lam  
**Student ID:** V202603373  
**Group:** Group 10  
**Course:** Advanced Software Engineering (AY 26–27) · VinUniversity  
**Topic:** Requirements Engineering and Specification (Chapter 2 – SoopiFood)  

---

## 1. Submission Structure (Slide 77 Compliance)

All deliverables required by Slide 77 ("Lab Submission") are completely fulfilled and organized in [`workspace/`](file:///Users/tunglambg131003/SE_LEC2/workspace):

| # | Item Required (Slide 77) | Deliverable File in `workspace/` | Status |
|---|---|---|---|
| **1** | Interview guide for restaurant manager (Lab 1) | [`01_interview_guide.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/01_interview_guide.md) & [`02_interview_guide_iterate.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/02_interview_guide_iterate.md) | ✅ Complete |
| **2** | 2–3 personas of restaurant managers (Lab 2) | [`03_personas.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/03_personas.md) (Mateo, Sarah, David) | ✅ Complete |
| **3** | Functional requirements for restaurant app (Lab 3) | [`04_functional_requirements.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/04_functional_requirements.md) (14 atomic FRs) | ✅ Complete |
| **4** | NFR table for restaurant app (Lab 4) | [`05_non_functional_requirements.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/05_non_functional_requirements.md) (8 measurable NFRs) | ✅ Complete |
| **5** | Epics, features, and stories backlog for 5 devs (Lab 5) | [`06_epics_stories.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/06_epics_stories.md) (3 Epics, 10 Stories + Criteria) | ✅ Complete |
| **6** | Outputs of Labs 6–9: | | |
| | • MoSCoW Round 1 (Backlog only) | [`moscow_round1.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/moscow_round1.md) | ✅ Complete |
| | • MoSCoW Round 2 (Stakeholder notes) | [`moscow.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/moscow.md) | ✅ Complete |
| | • Scope change decisions & trade-offs | [`scope_changes.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/scope_changes.md) | ✅ Complete |
| | • Gherkin acceptance criteria (Writer v1) | [`discount.feature`](file:///Users/tunglambg131003/SE_LEC2/workspace/discount.feature) | ✅ Complete |
| | • Acceptance criteria review against rules | [`review.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/review.md) | ✅ Complete |
| | • Gherkin criteria rewrite on boundaries (v2) | [`discount_v2.feature`](file:///Users/tunglambg131003/SE_LEC2/workspace/discount_v2.feature) | ✅ Complete |
| | • Definition of Done PR audit | [`dod_audit.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/dod_audit.md) | ✅ Complete |
| **7** | Prompt log with rationale for every change | [`prompt_log.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/prompt_log.md) | ✅ Complete |
| **★** | **OPTIONAL 1:** Prototype wireframe & assumptions | [`optional_prototype_assumptions.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/optional_prototype_assumptions.md) | 🌟 Bonus |
| **★** | **OPTIONAL 2:** End-to-end traceability chain | [`optional_traceability_chain.md`](file:///Users/tunglambg131003/SE_LEC2/workspace/optional_traceability_chain.md) | 🌟 Bonus |

---

## 2. Git Commit Instructions

To commit and push your work to your GitHub repository:

```bash
# 1. Stage all workspace files, tutorial documentation, and starter materials
git add README.md TUTORIAL.md starter/ solutions/ workspace/

# 2. Commit with a clear, professional message
git commit -m "Complete Chapter 2 Requirements Engineering tutorial deliverables (Labs 1-9) - Nguyen Tung Lam (V202603373)"

# 3. Push to your GitHub repository
git push origin main
```

---

## 3. Creating the Submission Zip File

Per Slide 77, the zip archive must be named `V202603373_chap2.zip`:

```bash
zip -r V202603373_chap2.zip workspace/
```
