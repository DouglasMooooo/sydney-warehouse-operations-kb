---
id: SYS-WMS-ERP-001
title: WMS to ERP Writeback
type: system_reference
system: WMS
evidence_level: VERIFIED
status: active
updated: 2026-08-18
---

# WMS → ERP Writeback

WMS outbound may complete while reverse-write fails to create XSCKD. A retry may recover it, but retry is a business-state operation and requires explicit authorisation.

Before proof: “疑似WMS反写ERP失败 / ERP销售出库单未形成”. After authorised retry recovery: “WMS反写ERP失败，重试后恢复”.

## Repair → Repair_Good

SOP-confirmed Sydney flow:

`WMS records machine SN as Repair_Good → WMS writes back to ERP → ERP creates the inventory/transfer document`

Direct manual ERP entry is not the normal operating path. A document quantity in ERP normally reflects SN events received from WMS. If ERP good inventory is one unit higher than the physical good area, test opening/migration and later reverse movement before alleging that ERP transferred one extra unit manually.

For closure, compare the complete ERP SN set with the current physical/WMS SN set. The single ERP-only SN identifies the history that needs investigation.

