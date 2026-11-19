---
name: update-lead-magnet
description: Change a lead magnet or guide that already exists in Unplain, including live ones. Use when the user wants to edit, fix, extend, restyle or refresh a guide, change its landing page text or form, swap its PDF, pause or take it down, or edit their public Library.
---

# Update a lead magnet in Unplain

A lead magnet is the published form of an ebook: a PDF snapshot of the saved ebook plus a landing page with an email form. Editing the ebook does NOT change the public PDF. The PDF changes only when it is refreshed. Keep this straight for the user, because it is the most common surprise.

## Find it

- By name: `list_lead_magnets` (lead magnets, their status, public URL, lead counts and whether the PDF is stale), or `list_ebooks` with `search` for the ebook behind it.
- Never ask the user for an id before trying these.

## Change the content

1. `get_ebook` to read the block ids and the `version`.
2. `update_ebook` with `operations` for precise edits (replace text, insert after a block, set a table, convert a block). Pass the `version` so a change made in the web app meanwhile is not overwritten. Prefer operations over replacing the whole `content` when the ebook has images, tables or buttons: replacing the body rebuilds every block and drops stored images.
3. `preview_ebook` to check the pages that changed, and tell the user what you see.
4. If the user writes new sections with you, follow the writing rules in the `create-lead-magnet` skill: true facts only, nothing invented.

## Push it to the public PDF

1. `get_lead_magnet` shows whether the PDF is older than the ebook (stale) and the readiness report.
2. `update_lead_magnet` with `refreshPdf: true`. On a LIVE lead magnet the first call applies nothing and returns the exact change. Show it to the user and repeat the same call with `confirmLiveChange: true` only after they agree. The address, leads and numbers stay the same.

## Landing page, form and placement

`update_lead_magnet` with only the fields that change. Drafts and paused ones change at once; live ones go through the same show-then-confirm step.

## A lead magnet made from a PDF

`create_lead_magnet_from_pdf` with `magnetId` and a public link to the new PDF replaces the file at the same address. On a live one it returns the change to confirm first.

## Take it down or put it back

- `unpublish_lead_magnet`: `pause` (default) keeps the page up saying it is unavailable; `draft` makes it private again. Nothing is deleted: the ebook, PDF, leads and numbers are kept.
- `publish_lead_magnet` puts it back at the same address. Only when the user asks.

## The Library

`update_library` changes the public Library: heading, website and privacy links, header links, the sender name and subject of the email new leads receive, whether the user is emailed about each new lead, and the order of guides. The first call returns the changes; apply with `confirmLiveChange: true` after the user agrees. Changing the Library address itself uses `claim_library` with `confirmChange: true`, and every published link moves, so make sure the user understands that.
