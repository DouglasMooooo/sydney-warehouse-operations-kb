---
id: PB-OUTBOUND-GAP-001
title: Investigate Sales Outbound Gap
type: playbook
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-15
---

# Playbook

1. Establish Ledger actual outbound and approved XSCKD quantities.
2. Match SKU + warehouse + SH; use SN for unit tracing.
3. Confirm final current instruction and cancellation/change state.
4. Trace SH → FHTZD → WMS outbound → writeback → XSCKD.
5. If outbound exists but XSCKD is missing, classify probable writeback failure; do not upgrade without retry/log evidence.
6. Check duplicate/draft XSCKD before any authorised recovery.

