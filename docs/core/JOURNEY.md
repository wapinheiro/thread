# Thred: The Journey

**Core metaphor:** a student holding a thread through a labyrinth. Each
stage below is described by its **function**, not by a persona or
character — whether a stage is powered by software, an advisor, a rule
engine, or (optionally, later) an AI feature is an implementation
decision, not a branding one. See [Theme](THEME.md).

---

## 1. Getting Started (Anchor)

Establish the student's starting point and constraints — most critically,
time. The system calculates how many semesters/terms remain and sets
realistic limits on how much a student can take on at once.

**Example:** A student indicates an expected graduation date. The system
calculates remaining terms and caps the number of major commitments it
will suggest per term.

## 2. Choose a Path (Track Selection)

The student selects a target direction. This loads a **Target Schema** —
the specific set of skills and proficiency levels associated with that
Track.

**Example:** A student selects "Full Stack Developer" and the system
loads its required skills (Python, a frontend framework, REST APIs,
database design, version control) with target levels for each.

## 3. Calibrate

Before self-rating, the student sees clear rubric definitions for each
proficiency level. This exists specifically to counter the tendency
students have to over- or under-rate themselves before they understand
the standard.

## 4. Gap Analysis

The student rates current proficiency against the Track's targets.

`Gap = Target Level − Current Level`

- Gap ≤ 0 → **Acquired**
- Gap > 0 → **To Do**

## 5. Get Connected (Plan Generation)

*This is the plug-in point for the whole ecosystem.* Thred consults the
**Resource Registry** — internal resources (classes, project ideas) and
every onboarded **component program** — to propose ways to close each
gap.

**Example:** To close a React gap, Thred might surface a relevant class,
a personal project idea, an upcoming alumni-tech-society event on
frontend engineering, and a milestone-sticker challenge — all as options
a student can add to their plan.

See [Partner Registry](../ecosystem/PARTNER_REGISTRY.md) for how a
component program registers itself here.

## 6. Advisor Review

A human reviews the draft plan for nuance that a system can't fully
capture — course load balance, burnout risk, scheduling conflicts. Plans
move from `PENDING_REVIEW` to `APPROVED`.

## 7. Do the Work (Execution & Evidence)

The student executes the plan and submits an **Artifact** as proof of
completion — not a checkbox. Submitted evidence is verified (by a person,
a rubric, or a quality-check function) before a gap is marked closed.

## 8. Payoff & Loop

Once verified, the system updates the student's **Market GPA** and can
generate a resume-ready summary of the completed work. The journey loops
back to Gap Analysis for the next target.

---

## Design Note: This Journey Is a Backbone, Not a Fixed Sequence

Component programs don't need to reproduce all eight stages internally.
A program only needs to define how it plugs into **Stage 5** (as a
resource) and **Stage 7** (as a source of verifiable evidence). See the
[Partner Template](../partners/TEMPLATE.md).
