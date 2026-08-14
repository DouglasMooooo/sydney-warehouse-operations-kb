---
id: EXC-WRONG-WH-XSCKD
title: Wrong Warehouse XSCKD
type: exception_pattern
evidence_level: VERIFIED
classification: WRONG_WAREHOUSE_XSCKD
status: active
updated: 2026-08-15
---

# Pattern

If Ledger actual outbound is SKU + SH + Warehouse A, but approved ERP XSCKD has the same SKU + SH/quantity under Warehouse B, the outbound may have completed while ERP deducted the wrong warehouse. This is not MISSING_XSCKD.

Verified case: [SH-2605-00144355](../05_verified-cases/sh-2605-00144355.md).

