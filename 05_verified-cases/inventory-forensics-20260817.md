---
id: CASE-SYD-INVENTORY-FORENSICS-20260817
title: Sydney Machine Inventory Forensics 2026-08-17
type: investigation_case
domain: inventory-reconciliation
evidence_level: INFERRED
status: open
updated: 2026-08-18
---

# Scope

Machines only in 悉尼维修仓、悉尼良品仓 and 悉尼物料仓. Current Google Ledger is authoritative; legacy Excel supplies pre-opening history. `Prepared` remains physical inventory.

# Leading conclusion

Opening or historical migration difference is the leading cause of the remaining inventory residuals. This is not yet verified at SN level.

## 97-141-00062-B0 / 悉尼物料仓

Current ERP 7 vs physical 8. Two verified wrong-warehouse SH records explain +2 ERP material stock. Legacy ledger verifies `SH-2607-00166403` physically left on 2026-07-08 with SN `60HD153064KM140`; ERP posted the sales outbound on 2026-08-14. The 2026-08-13 snapshot was ERP 10 vs physical 8, although the known effects predict +3. A separate offsetting -1 already existed. `75-ZJDB2608000009` exposed, but does not by itself create, the residual.

## 97-223-00088-00 / 悉尼良品仓

Current ERP 6 vs physical 5. `75-ZJDB2608000002` transferred 4 units Repair → Good on 2026-08-04. Sydney normally records the machine SN in WMS and lets WMS write back the ERP document, so “physical 5 but ERP operator entered 6” is not the leading explanation. Prioritise opening balance, later reverse movement without writeback, then interface retry/duplicate or SN mapping anomaly.

## 97-229-00012-00 / 悉尼良品仓

Current ERP 3 vs physical good area 2. WMS/ledger shows Repair_Good SN `60CQ00FR62CABBM` physically at `REPAIR-01`. This may be a status-to-warehouse mapping or physical-location timing difference. Substantial pre-opening transfer history prevents closure by quantity alone.

# Closure evidence

- dated ERP opening balances by the three Sydney warehouses;
- ERP/WMS/physical SN set differences for each target SKU;
- full lifecycle of `60HD153064KM140` and `60CQ00FR62CABBM`;
- the specific historical document referenced by feedback that a prior transfer may already have occurred.
