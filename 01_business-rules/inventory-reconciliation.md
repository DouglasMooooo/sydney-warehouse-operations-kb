---
id: REC-001
title: Inventory Reconciliation
type: business_rule
domain: reconciliation
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-15
---

# Rule

Compare Ledger Actual Outbound Qty with ERP Approved XSCKD Qty using **SKU + Warehouse + SH**. Batch is auxiliary only.

If equal, exclude sales outbound first, then investigate Opening, Inbound, Transfer, Adjustment, Repair → Repair_Good, Return/Recovery, Historical Migration and Material Code Conversion.

If Ledger Outbound > approved XSCKD, investigate MISSING_XSCKD, XSCKD_PENDING, XSCKD_REAPPROVAL and WMS_WRITEBACK_FAILURE. If XSCKD exists under another warehouse, classify WRONG_WAREHOUSE_XSCKD.

