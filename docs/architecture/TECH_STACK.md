# Thred: Tech Stack

*Placeholder — to be defined. RedThread's original proposal used Django,
PostgreSQL, HTMX/Alpine/Tailwind, and Celery/Redis; carry forward,
revisit, or replace as appropriate once Thred's own technical
requirements (multi-tenant component-program integrations, a partner API
for the Resource Registry, etc.) are scoped.*

## Open Questions

- Does the Partner Registry need a real API/webhook system for component
  programs to register resources and report Artifacts, or is a simpler
  admin-managed registry sufficient for v1?
- Multi-tenancy: do component programs need any degree of self-service
  access to manage their own entries?
- Reporting: what does the Steering Committee's quarterly reporting need
  to pull from, and does that shape the data layer?
