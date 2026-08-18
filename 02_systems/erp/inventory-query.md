# ERP Inventory Query

## Verified navigation

In Kingdee Cloud, the observed path is:

`主控台菜单 → 供应链 → 库存管理`

The inventory menu contains at least the following relevant objects:

- 即时库存
- 即时库存明细
- 物料收发汇总表
- 物料收发明细表
- 历史库存查询
- 调拨申请单列表
- 直接调拨单列表

## Required filter discipline

Before applying 快捷过滤, select **默认方案**. Do not rely on a shared or personal scheme because hidden preset conditions may change the evidence population.

For the Sydney machine audit, restrict results to machines/products and the following warehouses only:

- 悉尼维修仓
- 悉尼良品仓
- 悉尼物料仓

Explicitly exclude parts/accessories, AUSFAIR/AUSFAIR-悉尼仓, 悉尼售后仓, and all Melbourne warehouses.

## Export workflow

Observed read-only workflow:

`库存管理 → 即时库存 → 过滤 → 默认方案 → 设置条件 → 确定 → 引出`

Save every export as immutable raw evidence with an extraction timestamp. Do not edit or overwrite the raw file.

Evidence status: SOP-CONFIRMED for scope and default-scheme discipline; VERIFIED for the observed navigation and export controls.
