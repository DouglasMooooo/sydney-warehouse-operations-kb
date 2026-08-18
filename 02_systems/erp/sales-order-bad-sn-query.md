---
id: SYS-ERP-SO-BAD-SN-001
title: Sales Order Bad-SN Query
type: system_reference
system: ERP
evidence_level: VERIFIED
status: active
updated: 2026-08-18
---

# Sales Order Bad-SN Query

Use this read-only workflow to map a bad-machine serial number to its sales-order number:

`销售订单列表 → 默认方案 → 快捷过滤 → 坏机SN → 输入 SN → Enter → 等待结果返回`

## Required controls

1. Click **默认方案** and verify that it is selected before applying the filter.
2. Select the exact quick-filter field **坏机SN**. Do not substitute **故障序列号**.
3. Enter one SN at a time.
4. Press **Enter** after entering the SN. Enter both synchronises the multiline filter value and starts the query.
5. Wait for the returned grid to finish refreshing, then read **单据编号**. Verify that the input still equals the current SN and that the grid is not showing the preceding query's result.
6. Do **not** click the search icon after pressing Enter. Doing both can create overlapping requests and cause the grid to lag one SN behind.
7. If the result is empty, record `无匹配` and continue to the next SN.
8. Treat an unchanged full page (for example, 200 rows) as a failed filter application, not as a match. Re-enter the SN and press Enter once.

Do not click 保存, 提交, 审核, 下推, 删除 or any other mutation control.
