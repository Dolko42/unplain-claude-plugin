---
name: lead-magnet-report
description: Report how the user's Unplain lead magnets are doing and what to improve, based on their real numbers. Use when the user asks how a guide or lead magnet performs, which one works best, where visitors drop off, why signups are low, or wants a weekly or monthly lead magnet review.
---

# Lead magnet report

Base every statement on numbers the tools return. Never present a guess as data, and say plainly when there is too little data to judge.

## Gather

1. `list_lead_magnets` to see what exists and which are live.
2. `get_lead_magnet_performance` for the period the user means (7, 30 or 90 days, or all time). Add daily series, traffic sources, campaigns, read-through by page or clicked links only when the question needs them.
3. For one lead magnet in depth, `audit_lead_magnet`. Each finding carries its evidence; it stays silent where there is not enough data, and so should you.

## Read the numbers correctly

Every performance result includes `definitions`. Say the ones that change the meaning, for example that visitors are counted per day and are not unique people. Use the conversion rate the tool returns, as defined there, rather than computing your own.

## Write the report

Keep it short and in this order:

1. **The headline**: visitors, new leads and conversion for the period, per lead magnet and in total.
2. **What stands out**: the best and worst converting lead magnet or source, where visitors stop (before the form, in the form, or in the PDF), leads who never downloaded. Quote the evidence.
3. **Two or three next steps**, each tied to a finding. Examples: a missing description or cover image, a CTA button without a link, a PDF older than its ebook, a source that converts far below the rest. If a fix means editing a live page, offer it and use the `update-lead-magnet` skill, which asks before anything public changes.

Do not promise outcomes. "This should help" is fine; "this will double your leads" is not.

## Individual leads

`list_leads` and `get_lead` return personal data (emails, names) and only work when the user ticked lead access when connecting Unplain. Use them only when the user asks about specific people, never to pad a report, and do not copy lists of leads anywhere else unless the user asks. The performance numbers above never include who the leads are, so a normal report does not need them.
