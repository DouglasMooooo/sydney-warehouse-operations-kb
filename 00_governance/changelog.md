---
id: GOV-CHANGELOG
title: Changelog
type: governance
status: active
updated: 2026-08-15
---

# Changelog

## 2026-08-15

- Restructured the Google Doc into governance, rules, systems, playbooks, exceptions, cases, references and diagrams.
- Added simplified ERP outbound flow.
- Preserved FHTZD as an investigation reference.
- Added WRONG_WAREHOUSE_XSCKD.
- Encoded 2026-08-11 EOD ledger cutoff and evidence hierarchy.

# 2026-08-17

- Added the Sydney warehouse machine-only scope and required ERP default filter scheme.
- Added verified ERP inventory and transfer query navigation.
- Recorded that a suspected transfer is not classified as duplicated without complete ERP movement evidence.
- Verified direct-transfer details for 75-ZJDB2608000009 and 75-ZJDB2608000002; recorded the current SN-query limitation.

# 2026-08-18

- Recorded the SOP-confirmed `WMS SN entry → ERP writeback → ERP transfer document` flow for Repair → Repair_Good.
- Added Opening/Historical Migration Difference as the leading inferred cause of the current Sydney machine residuals.
- Corrected the audit-cycle ledger cutoff: current Google Ledger data is authoritative through 2026-08-17, while `Prepared` remains physical inventory.
- Added the 2026-08-17 three-SKU forensic case and explicit SN-level closure criteria.
- Verified the sales-order `默认方案 → 坏机SN → Enter → 等待结果返回` lookup workflow and documented the unchanged-full-page failure signal.
- Corrected the bad-SN query workflow: Enter starts the query; clicking Search immediately afterwards can create overlapping requests and stale, one-SN-behind results.
- Promoted query synchronisation to a global ERP rule: one trigger at a time, wait for the result grid to finish refreshing, and never use repeated Enter/Search actions.
- Added the explicitly authorised Sales Order → FHTZD creation and workflow-audit procedure.
- Recorded that typed display text must be committed by blur/selection before required-field validation can pass.
- Added verified case SH-2608-00172641 and generated FHTZD 75-FHTZD260806040.
- Refined safety boundaries so mutation authority is document- and stage-specific while investigation remains read-only by default.
