---
id: EXC-OPENING-MIGRATION-DIFFERENCE
title: Opening or Historical Migration Difference
type: exception_pattern
evidence_level: INFERRED
status: active
updated: 2026-08-18
---

# Pattern

ERP and the authoritative physical ledger retain a residual quantity after verified post-opening movements are applied, and the first comparable snapshot already contains the difference or an offsetting discrepancy.

# Classification rule

Use `OPENING_OR_HISTORICAL_MIGRATION_DIFFERENCE` only when:

- current physical-ledger rules and warehouse scope are fixed;
- pre-opening movements have been checked in the legacy ledger;
- verified post-opening ERP/WMS movements do not create the residual; and
- the remaining quantity logically predates the first comparable snapshot.

Evidence remains **INFERRED** until a dated ERP opening record, migration file or SN-set comparison proves the first divergence.

# Common false attribution

Do not blame the most recent transfer merely because the residual becomes visible after it posts. A late ERP posting can expose an older offsetting difference without being the original cause.
