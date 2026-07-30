# Thred: Data Model & Examples

**Purpose:** Concrete examples of the core data structures referenced
throughout the Thred documentation.

---

## 1. Tracks (Target Schemas)

A **Track** defines a target state for a student — a career direction
with a specific set of required skills and proficiency levels.

### Example: "Full Stack Developer"

- **Track ID:** `track_fullstack`
- **Description:** Builds end-to-end web applications; frontend and
  backend competence.
- **Target Skills (subset):**
  - Python — Level 3 (Applied)
  - React — Level 3 (Applied)
  - SQL — Level 2 (Academic) — most heavy lifting handled by ORMs
  - REST APIs — Level 4 (Professional) — critical for integration work
  - System Design — Level 2 (Academic)

### Example: "Data Engineer"

- **Track ID:** `track_dataeng`
- **Target Skills (subset):**
  - Python — Level 4 (Professional) — optimization matters here
  - SQL — Level 5 (Mastery) — complex joins, window functions
  - Cloud Infrastructure (AWS) — Level 3 (Applied)

## 2. The Resource Registry

Maps **Gaps** to **Resources** — including both internal resources and
anything offered by a **component program**.

`Skill Gap → [Resources, sorted by relevance/effectiveness]`

### Example: Gap = React, Level 0 → 3

| Priority | Resource | Type | Time Cost | Source |
| :--- | :--- | :--- | :--- | :--- |
| 1 | UX Engineering course | Class | 1 semester | Internal |
| 2 | "Build a Clone" project challenge | Project | 3 weekends | Internal |
| 3 | Frontend-focused alumni workshop | Event | 1 evening | Component program |
| 4 | Dev club weekly meetings | Club | 1 hr/week | Component program |
| 5 | Official framework tutorial | Self-study | 10 hours | Internal |

## 3. Gap Analysis (Example)

**Student:** Example student, Sophomore
**Track:** Full Stack Developer

| Skill | Target | Current | Gap | Status |
| :--- | :--- | :--- | :--- | :--- |
| Python | 3 | 2 | −1 | To Do |
| React | 3 | 0 | −3 | To Do (critical) |
| Git | 4 | 4 | 0 | Acquired |
| SQL | 2 | 1 | −1 | To Do |

## 4. Semester Plan (Example)

**Context:** a single term, capacity of 4 major commitments.

1. **[Class]** Advanced Programming — closes Python gap
2. **[Project]** Personal React + backend project — closes React gap
   (flagged as high-cost given the size of the gap)
3. **[Component Program]** Data Science club — networking / soft-skill
   evidence
4. **[Self-study]** Targeted SQL exercises — closes SQL gap

## 5. Artifact (Example)

- **Skill:** React
- **Type:** GitHub repository + live demo link
- **Submitted by:** student
- **Reviewed by:** advisor or automated quality check
- **Outcome:** Level updated from 0 → 2; Market GPA recalculated;
  resume-ready summary generated
