---
id: DIA-ERP-XSCKD-001
title: ERP XSCKD Logic
type: diagram
status: active
updated: 2026-08-15
---

# ERP XSCKD Logic

```mermaid
flowchart TD
    A[SH order] --> B[WMS outbound]
    B --> C[WMS writeback ERP]
    C --> D[Generate XSCKD]
    D --> E{Inventory validation}
    E -->|Match| F[XSCKD approved; ERP deduction complete]
    E -->|Mismatch| G[Return for review / exception]
    G --> H[Investigate inventory, warehouse, quantity or historical movement]
```

FHTZD remains the intermediate investigation reference.

