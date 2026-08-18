---
id: REC-SYD-SCOPE-001
title: Sydney Warehouse Machine Reconciliation Scope
type: business_rule
domain: inventory-reconciliation
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-17
---

# Rule

Sydney warehouse inventory reconciliation covers machines only in the following ERP warehouses:

- 悉尼维修仓
- 悉尼良品仓（业务口径“销售仓”）
- 悉尼物料仓

Exclude AUSFAIR/AUSFAIR-悉尼仓、悉尼售后仓、墨尔本各仓 and all parts/accessories from the Sydney machine inventory-gap result.

# Source

User-confirmed business scope on 2026-08-17.

# ERP query convention

For ERP list investigations, select the **默认方案** before applying 快捷过滤. Do not rely on a shared or personal scheme because retained conditions or hidden columns can change the observed result.
