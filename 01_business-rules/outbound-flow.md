---
id: ERP-OUTBOUND-001
title: Current ERP Sales Outbound Flow
type: business_rule
system: ERP
domain: outbound
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-15
---

# Rule

A normal sales outbound flows from SH through WMS execution and ERP writeback before inventory validation.

## Business Logic

High-level: `SH → WMS outbound → WMS writeback → XSCKD → automatic audit → inventory validation`.

Detailed: `Sales Order → FHTZD → WMS outbound → WMS reverse-write ERP → XSCKD → ERP inventory effect`.

If inventory matches, XSCKD is approved and ERP deduction completes. If not, XSCKD is returned/reviewed and investigation covers inventory, warehouse, quantity or historical movement.

FHTZD remains an important intermediate investigation reference.

