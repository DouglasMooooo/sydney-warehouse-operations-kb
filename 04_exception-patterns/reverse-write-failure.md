---
id: EXC-WRITEBACK-001
title: WMS Reverse-write Failure
type: exception_pattern
evidence_level: VERIFIED
status: active
updated: 2026-08-15
---

# Pattern

WMS physical outbound + FHTZD exists + XSCKD missing. Use exact SH + SKU + warehouse, final instruction, duplicate check and verified exports. Do not retry in read-only mode.

Verified example: [SH-2607-00168887](../05_verified-cases/sh-2607-00168887.md).

