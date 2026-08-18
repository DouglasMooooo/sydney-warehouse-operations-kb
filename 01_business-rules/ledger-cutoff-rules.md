---
id: LEDGER-CUTOFF-001
title: Ledger Cutoff Rules
type: business_rule
system: Google-Ledger
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-18
---

# Rule

For the 2026-08-17 Sydney machine audit, current Google Ledger data is authoritative through **2026-08-17**. Rows with status `Prepared` have zero outbound effect and remain physical inventory; `Prepared ≠ Outbound`.

New ledger takes priority. Old ledger fills historical movement before the new ledger existed. Do not double-count the same SKU + warehouse + SH.

Absence of a pre-opening SH from the new-ledger transaction log is not evidence that physical outbound did not occur. Check the legacy ledger and determine whether the movement is already absorbed into the new-ledger opening balance.

