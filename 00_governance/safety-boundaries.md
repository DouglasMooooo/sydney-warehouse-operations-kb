---
id: GOV-SAFETY-001
title: Read-only Investigation Safety
type: governance
status: active
updated: 2026-08-18
evidence_level: SOP-CONFIRMED
---

# Safety Boundaries

Investigation is read-only. Allowed: search, view, inspect, 上查, 下查, workflow/node/approval-route viewing, refresh and narrowly authorised export.

提交, 审核, 下推, 保存, warehouse/SN/quantity/status changes, reverse-write and other data mutations require explicit user authorisation for the named document and stage. Authorisation to prepare a draft does not authorise submit or audit; authorisation to submit does not implicitly authorise unrelated follow-on actions.

Never execute 反审核, 删除, 关闭, 仓储确认, stock adjustment, transfer/posting or any other destructive/stock-affecting action unless the user explicitly names and authorises that exact action.

For authorised mutations, trigger each action once and wait for the page's explicit result before continuing. A click, typed display value or still-loading status is not proof of completion.

A visible button does not grant authority. Last processor ≠ next-step owner ≠ root-cause owner; use 流程Owner待确认 unless direct evidence names an owner.

