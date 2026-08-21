VACS V5.8 — ACCESS_LOG NOW 1x24H

IMPORTANT CHANGE REQUESTED BY OPERATOR
ACCESS_LOG itself is now the 1x24h operational grouped view:
- One person/owner + one calendar date = ONE ROW.
- All IN/OUT cycles are stored in the same Riwayat IN/OUT cell.
- Example: IN 10:35 | OUT 11:39 | IN 13:17 | OUT 17:00.
- Multiple vehicles used by the same person that day are combined in the same row.

RAW HISTORY
- ACCESS_HISTORY is the immutable/raw transaction ledger.
- Every IN/OUT remains preserved there as one transaction per row.
- This prevents loss of audit history while ACCESS_LOG remains the operator-friendly 1x24h view.

MIGRATION
- On first load, if ACCESS_LOG contains the old raw schema, its existing rows are copied to ACCESS_HISTORY.
- ACCESS_LOG content is then replaced by the grouped 1x24h view.
- Formatting, column widths, colors, borders, freeze settings are preserved because only cell contents are cleared.

MASTER
- OWNERS = owner profile.
- VEHICLES = vehicle profile.
- No Polisi is the only mandatory vehicle master field.
- All other profile fields are optional and can be completed later.

REAL TIME
- IN/OUT writes to ACCESS_HISTORY.
- ACCESS_LOG is rebuilt immediately.
- REPORT_24H is also rebuilt.
- Multi-device uses the same central Spreadsheet and Apps Script.
- ScriptLock protects concurrent writes.

DEPLOY
Replace Code.gs + index.html together in the EXISTING project.
Apps Script: Save -> Manage deployments -> Edit -> New version -> Deploy.
GitHub: replace index.html and commit.
Keep the SAME Spreadsheet and SAME /exec URL.
Do not mix with older versions.
