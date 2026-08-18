---
id: PB-INVENTORY-GAP-001
title: Investigate Inventory Gap
type: playbook
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-18
---

# Playbook

Freeze scope/cutoff; separate explained from unexplained quantity; exclude known outbound explanations; trace full SKU + warehouse history from opening to current; classify Opening, Inbound, Transfer, Adjustment, Repair → Repair_Good, Return/Recovery, Historical Migration and Material Code Conversion; rebuild running balance; find first unexplained divergence.

When Repair → Repair_Good is WMS-SN-driven, do not compare only document quantities. Extract ERP and physical/WMS SN sets, calculate the one-sided difference, and trace the unmatched SN. If post-opening movements reconcile but the same residual exists at the first comparable snapshot, classify `OPENING_OR_HISTORICAL_MIGRATION_DIFFERENCE` at **INFERRED** level pending opening-source evidence.

