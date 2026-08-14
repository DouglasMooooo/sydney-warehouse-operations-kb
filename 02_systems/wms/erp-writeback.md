---
id: SYS-WMS-ERP-001
title: WMS to ERP Writeback
type: system_reference
system: WMS
evidence_level: VERIFIED
status: active
updated: 2026-08-15
---

# WMS → ERP Writeback

WMS outbound may complete while reverse-write fails to create XSCKD. A retry may recover it, but retry is a business-state operation and requires explicit authorisation.

Before proof: “疑似WMS反写ERP失败 / ERP销售出库单未形成”. After authorised retry recovery: “WMS反写ERP失败，重试后恢复”.

