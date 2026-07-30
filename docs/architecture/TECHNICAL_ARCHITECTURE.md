# Thred: Technical Architecture

*Placeholder — to be defined once [Data Model](../core/DATA_MODEL.md) and
[Tech Stack](TECH_STACK.md) are finalized.*

## Known Requirements (from the core docs)

- A **Track** model: skills + target proficiency levels.
- A **Skill** model, shared across Tracks.
- A **Gap** calculation: derived (Target − Current), not stored directly.
- An **Artifact** model: type, submitter, status (pending / verified /
  rejected), quality multiplier, linked skill, linked Track.
- A **Market GPA** calculation service: aggregates verified Artifacts +
  milestone bonuses per student.
- A **Resource Registry**: internal resources + component-program
  resources, queryable by skill/Gap.
- A **Component Program** model: metadata (owner, description, brand
  assets) + its registered resources + its Artifact type definitions.
- An **Advisor Review** workflow: plan state machine
  (`DRAFT → PENDING_REVIEW → APPROVED`).
- Reporting views for: early-warning/at-risk cohorts, Steering Committee
  quarterly reports, per-component-program engagement stats.
