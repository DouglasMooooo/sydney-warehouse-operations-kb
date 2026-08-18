---
id: PB-FORENSICS-001
title: Historical Movement Forensics
type: playbook
evidence_level: SOP-CONFIRMED
status: active
updated: 2026-08-18
---

# Playbook

When outbound explanations are excluded or partial, trace the complete SKU + warehouse timeline, classify every movement, rebuild the running balance and investigate only residual unexplained quantity. Never double-count a unit already explained by a confirmed interface failure.

Treat the legacy-ledger closing balance, new-ledger opening balance and ERP balance as three separate checkpoints. A pre-opening physical movement can be absent from the new-ledger transaction log while already included in its opening balance. If known movements predict a larger difference than the observed snapshot, record the offsetting quantity and trace it backward; do not force the residual onto the latest document.

