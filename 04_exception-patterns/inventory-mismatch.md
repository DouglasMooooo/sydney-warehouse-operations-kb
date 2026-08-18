---
id: EXC-INVENTORY-MISMATCH
title: Inventory Mismatch
type: exception_pattern
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-18
---

# Pattern

Ledger and ERP quantities disagree after applying cutoff and primary keys. Use the inventory-gap and historical-forensics playbooks to classify outbound, warehouse, quantity or movement causes.

If current movements reconcile and the residual appears to predate the comparable ledger window, use `OPENING_OR_HISTORICAL_MIGRATION_DIFFERENCE`. This is a leading hypothesis, not a verified root cause, until opening records or SN history prove the first divergence.

