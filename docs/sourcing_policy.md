# Sourcing Data Policy (extract)

## Contract ledger

Every supplier record carries its contract history. The `status` field is one of:

- `Active` — contract currently in force; its value counts toward committed
  (active) spend.
- `Completed` — fulfilled in the past; excluded from active spend.
- `Terminated` — cancelled before completion; excluded from active spend.

## Certification records

Every certification entry has `scheme`, `status` and `valid_until`.

- `Active` — certificate issued and currently in force.
- `Expired`, `Suspended`, `In Progress` — not usable for procurement qualification.

A certificate counts as current only when its status is `Active` **and** the
listed `valid_until` date is on or after the review date. Records occasionally
lag behind renewals, so always check the date, not just the status label.

## Review outputs

Approved vendor lists are stored under `shortlist/` as JSON documents with a
`review_date` field and an ordered `shortlist` array.
