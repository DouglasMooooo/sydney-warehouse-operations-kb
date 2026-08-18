---
id: SYS-ERP-FHTZD-001
title: Shipping Notice FHTZD
type: system_reference
system: ERP
evidence_level: VERIFIED
status: active
updated: 2026-08-18
---

# FHTZD

FHTZD is the intermediate 发货通知单 between Sales Order and WMS. Read-only path: Sales Order → 关联查询 → 下查 → 发货通知单.

Inspect SH, SKU, quantity, warehouse, line closure, cumulative outbound and remaining outbound. Approved FHTZD with completed workflow does not alone prove inventory movement.

## Authorised creation workflow

Default to read-only investigation. Execute the following mutation workflow only when the user explicitly authorises the target SH and the requested stages:

1. Open **销售订单列表**, select **默认方案**, and set the quick-filter field to **单据编号**.
2. Enter the exact SH number and click Search once. Wait until loading has finished and the returned grid contains the intended SH; do not use repeated Enter/Search actions.
3. Select only result lines whose **销售数量 is greater than zero**. Negative reversal lines must not be pushed.
4. Click **下推**, select **发货通知单**, and confirm only after checking the selected lines and target document type.
5. In the new FHTZD, set **起运港** and every detail line's **出货仓库** from the authorised operational source/ledger.
6. Text-entry success is not field-commit success. For text fields such as 起运港, trigger blur/Tab and then verify the visible value before submitting. For basic-data fields such as 出货仓库, select the actual lookup record, close the lookup, and verify every row.
7. Click **提交** once and wait for an explicit success message containing the generated FHTZD number. Do not click 审核 while required-field validation or saving is still pending.
8. If audit is authorised, click **审核** once, wait for the workflow task panel, select **审核通过**, click the workflow **提交** once, and wait until the workflow panel closes or the status/result changes. Do not repeat the action while status is **审核中**.

## Verification gates

- Query input equals the intended SH and the refreshed grid contains that SH.
- Only positive-quantity source lines are selected.
- 起运港 survives blur and required-field validation.
- Every detail line shows the intended 出货仓库 after the lookup closes.
- Submission returns a generated FHTZD number.
- Audit workflow is handled separately from document submission and is not treated as complete merely because the Audit button was clicked.

Never unapprove, delete, close, warehouse-confirm, alter inventory, or perform any other mutation outside the user's explicit authorisation.

