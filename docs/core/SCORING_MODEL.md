# Thred: Scoring Model — Market GPA

**Objective:** To quantify a student's market readiness into a single,
continuous metric: **Market GPA**.

This document carries forward the mechanics of RedThread's original
scoring model, with gaming-specific language (ranks, "Hz" units, combo
names) removed. See [Glossary](GLOSSARY.md) for what changed and why.

---

## 1. The Core Formula

Market GPA is not a simple sum of completed skills — it's weighted by
**level** and **verified quality**.

```
Market GPA = Σ (Base Value × Quality Multiplier) + Milestone Bonuses
```

### A. Base Values (by Proficiency Level)

The curve is intentionally non-linear. The jump from "academic knowledge"
to "applied, built-and-shipped work" is the hardest step for a student to
take — and the one with the highest real-world payoff — so it's weighted
accordingly.

| Level | Designation | Base Value | Logic |
| :--- | :--- | :--- | :--- |
| 1 | Exposed | 1 pt | Token credit; capped contribution. |
| 2 | Academic | 3 pts | Solid foundation, limited market value alone. |
| 3 | **Applied** | 10 pts | **The hiring baseline.** Rewards building something real. |
| 4 | Professional | 20 pts | Deployed / production-grade work. |
| 5 | Mastery | 40 pts | Rare; often sufficient on its own to secure an interview. |

### B. Quality Multiplier (Verification)

Level 3+ Artifacts are reviewed for quality, not just completion. This
can be done by an advisor, a rubric-based check, or an automated
quality-check function — the mechanism is an implementation choice (see
[Theme](THEME.md), Section 2).

| Multiplier | Judgment | Example Feedback |
| :--- | :--- | :--- |
| 0.0x | Not accepted | "This closely matches an existing tutorial with no independent work." |
| 1.0x | Standard | "Functional. Meets the minimum requirements." |
| 1.2x | Polished | "Good error handling, clear documentation, clean structure." |
| 1.5x | Exceptional | "Novel approach, production-quality practices — ready to show an employer." |

*Example:* A standard Level 3 project = 10 pts. An exceptional Level 3
project = 15 pts.

## 2. Milestone Bonuses

Completing a meaningful *set* of related skills yields a bonus, on top of
individual skill values. (Naming here should stay descriptive, not
game-flavored — see [Glossary](GLOSSARY.md).)

| Milestone | Requirement | Bonus |
| :--- | :--- | :--- |
| Foundation Complete | All Level 1 skills in a Track finished. | +5 pts |
| Core Skills Complete | Level 3 reached in a Track's core skills. | +25 pts |
| Professional Readiness | Resume + professional profile + mock interview, all at Level 3. | +15 pts |

### Sample Calculation

1. **Skills**
   - Python (Level 3, Polished): 10 × 1.2 = 12
   - React (Level 3, Standard): 10 × 1.0 = 10
   - SQL (Level 3, Standard): 10 × 1.0 = 10
   - Git (Level 2): 3
   - Subtotal: 35 pts
2. **Bonuses**
   - Core Skills Complete: +25 pts
   - Subtotal: 60 pts
3. **Professional Readiness**
   - Resume/profile/interview (Level 3): +15 pts
   - Level 3 evidence for soft skills: 3 × 3 pts = 9 pts
   - **Total: 84 pts**

## 3. Review Cooldown (Anti-Spam)

If a Level 3+ Artifact is not accepted on review, that skill enters a
short cooldown period before resubmission — this encourages meaningful
revision rather than rapid low-effort resubmission. No narrative framing
is attached to this mechanic; it's communicated plainly (e.g., "You can
resubmit this in 24 hours — consider revising based on the feedback
above").

## 4. Readiness Bands

Bands are descriptive, not ranks to "level up" through — they exist to
give advisors and recruiters a shared, plain-language read on where a
student stands.

| Score Range | Band | What It Signals |
| :--- | :--- | :--- |
| 0–30 | Getting Started | Early-stage; foundational work underway. |
| 31–60 | Building | Actively producing verified work. |
| 61–79 | Strong | Solid, verifiable readiness across a Track. |
| 80–99 | Market Ready | Fundamentals solid; ready for advanced job-search support. |
| 100+ | Exceptional | Well beyond baseline readiness; candidate for mentoring others. |
