---
id: SYS-ERP-001
title: ERP Overview
type: system_reference
system: ERP
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-18
---

# ERP

ERP is the investigation object. Core objects: Sales Order/SH, Shipping Notice/FHTZD, Sales Outbound/XSCKD and Instant Inventory. Direct navigation and some field semantics remain UNKNOWN where the source did not verify them.

## Query synchronisation rule

This rule applies to every ERP list and quick-filter investigation:

1. Trigger only one query at a time.
2. After pressing Enter or clicking Search, wait until the current query has returned and the result grid has finished refreshing before reading values or entering the next condition.
3. Never press Enter repeatedly, click Search repeatedly, or press Enter and then immediately click Search. Overlapping requests can leave the result grid one condition behind and produce an incorrect bill number or other stale value.
4. Before recording evidence, verify that the filter input still equals the intended condition and that the result population is not the preceding query's population.
5. An unchanged full page after a narrow filter is a failed filter application, not evidence of a match. Re-enter the condition and trigger one query only.

