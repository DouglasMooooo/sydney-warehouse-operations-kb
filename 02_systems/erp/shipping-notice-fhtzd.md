---
id: SYS-ERP-FHTZD-001
title: Shipping Notice FHTZD
type: system_reference
system: ERP
evidence_level: VERIFIED
status: active
updated: 2026-08-15
---

# FHTZD

FHTZD is the intermediate 发货通知单 between Sales Order and WMS. Read-only path: Sales Order → 关联查询 → 下查 → 发货通知单.

Inspect SH, SKU, quantity, warehouse, line closure, cumulative outbound and remaining outbound. Approved FHTZD with completed workflow does not alone prove inventory movement.

Do not submit, approve, unapprove, push, save, delete, close or warehouse-confirm.

