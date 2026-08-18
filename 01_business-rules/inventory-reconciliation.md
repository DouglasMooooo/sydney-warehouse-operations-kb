---
id: REC-001
title: Inventory Reconciliation
type: business_rule
domain: reconciliation
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-18
---

# Rule

Compare Ledger Actual Outbound Qty with ERP Approved XSCKD Qty using **SKU + Warehouse + SH**. Batch is auxiliary only.

If equal, exclude sales outbound first, then investigate Opening, Inbound, Transfer, Adjustment, Repair → Repair_Good, Return/Recovery, Historical Migration and Material Code Conversion.

If Ledger Outbound > approved XSCKD, investigate MISSING_XSCKD, XSCKD_PENDING, XSCKD_REAPPROVAL and WMS_WRITEBACK_FAILURE. If XSCKD exists under another warehouse, classify WRONG_WAREHOUSE_XSCKD.

## Repair → Repair_Good rule

Sydney operators normally do not create Repair → Repair_Good inventory movements directly in ERP. The operator records the machine SN in WMS; WMS writes the event back and ERP then generates the corresponding document.

Therefore, when ERP good-warehouse quantity exceeds physical good-warehouse quantity, do **not** assume an operator manually entered a larger ERP quantity. Investigate in this order:

1. opening balance or historical migration mismatch;
2. a later physical return to repair/isolation without a successful reverse writeback;
3. WMS retry, duplicate writeback, reversal or material/SN mapping anomaly;
4. only then, exceptional manual ERP activity if audit logs prove it.

An opening difference may be the leading hypothesis, but remains **INFERRED** until a dated opening snapshot or SN-set comparison establishes the first divergence.

