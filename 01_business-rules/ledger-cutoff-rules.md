---
id: LEDGER-CUTOFF-001
title: Ledger Cutoff Rules
type: business_rule
system: Google-Ledger
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-15
---

# Rule

Google Ledger truth for this cycle ends at **2026-08-11 EOD**.

Rows dated 2026-08-12 or later are operational registrations only and do not automatically establish the ERP baseline. Prepared remains physical inventory; Prepared ≠ Outbound.

New ledger takes priority. Old ledger fills historical movement before the new ledger existed. Do not double-count the same SKU + warehouse + SH.

