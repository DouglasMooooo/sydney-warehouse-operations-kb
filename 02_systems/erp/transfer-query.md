# ERP Transfer Query

## Verified navigation

The ERP inventory menu exposes both `调拨申请单列表` and `直接调拨单列表` under:

`主控台菜单 → 供应链 → 库存管理`

## Investigation rule

Select **默认方案** before applying 快捷过滤. Query both transfer lists by material code and use the widest available date range. A transfer number mentioned in feedback is only a lead until the ERP detail establishes source warehouse, destination warehouse, quantity, status, and posting time.

Do not label a transfer as duplicated merely because a ledger or audit note says it may be duplicated. Duplicate Transfer requires two distinct posted ERP movements or another independently verified duplicate effect.

## Verified live-query findings (2026-08-17)

- The account can query direct transfers by material and see bill number, date, status, quantity, source warehouse, and destination warehouse.
- `75-ZJDB2608000009` is an approved 2026-08-14 direct transfer of 2 units of `97-141-00062-B0` from 悉尼物料仓 to 悉尼维修仓.
- `75-ZJDB2608000002` is an approved 2026-08-04 direct transfer of 4 units of `97-223-00088-00` from 悉尼维修仓 to 悉尼良品仓.

Under the Sydney Repair → Repair_Good SOP, an ERP transfer document may be generated from WMS SN writeback. The presence of the document does not by itself prove direct manual ERP entry or an erroneous ERP quantity.

The list contains `业务查询 → 序列号`, but it remained hidden/disabled for the selected row. This proves the ERP build has an SN-query feature but does not yet prove that the user has SN-detail permission or that the selected material/document is serial-managed.
