# Sourcing Data Workspace

Internal data workspace for the Meridian Group procurement desk.

## Contents

- `data/vendor_registry.json` — scoped supplier master export for the current
  sourcing cycle (120 supplier records, each with certification records and its
  contract ledger).
- `docs/sourcing_policy.md` — definitions for contract statuses and
  certification records.
- `shortlist/` — review outputs produced by sourcing analysts.

The portal preview cache that analysts keep in their local workspace is
refreshed nightly and may lag behind this export. Use the registry export as the
authoritative source for any review or ranking.

## Conventions

- Currency: EUR
- Identifier formats: `VND-####` for suppliers, `CTR-YYYY-#####` for contracts.
