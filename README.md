# VACS V5.6 — FINAL ALL FEATURES READY DEPLOY

This is the coordinated Code.gs + index.html pair for the existing VACS central system.

## LOCKED REQUIREMENTS
- One central Google Spreadsheet for ALL devices.
- Existing Apps Script /exec endpoint remains the same.
- No Polisi is the only mandatory vehicle master field.
- Name, Employee ID, Divisi, Jabatan, Jenis, Merk, Model, Tahun, Warna are optional.
- Manual entry is supported from the VACS UI.
- Profile can be completed later without changing existing IN/OUT history.
- Existing No Polisi is recognized; same-owner import updates, not duplicates.
- Different-owner duplicate is treated as an ownership conflict and is not silently overwritten.
- Unregistered No Polisi is denied and logged to DENIED_LOG.
- Partial search works (e.g. 98, FUX, B9856).
- IN/OUT is written to the central ACCESS_LOG with server timestamp.
- Multi-device writes are protected with Apps Script LockService.
- Current Inside is based on the latest central IN/OUT state.
- Import supports Excel .xlsx/.xls and CSV.
- Report is grouped as ONE ROW PER PERSON PER DAY (1x24h operational report).
- Multiple IN/OUT cycles in the same day are combined in one row.
- Multiple vehicles used by the same person in that day are combined in the same row.
- REPORT_24H is a generated data view.
- Report can export Excel and Print/Save as PDF.
- Spreadsheet layout remains administrator-owned: no automatic column resizing, formatting reset, freeze reset, or redesign.

## GOOGLE SHEET MASTER ENTRY
- OWNERS = owner profile: Nama, Employee ID, Divisi, Jabatan, etc.
- VEHICLES = vehicle profile: No Polisi, Owner ID, Merk, Model, Jenis, etc.
- ACCESS_LOG = transaction history only.
- DENIED_LOG = denied/unregistered attempts only.
- USERS / SETTINGS = system support.
- REPORT_24H = generated 1x24h report view.

For direct sheet entry, do not type transactions into ACCESS_LOG manually. The safest workflow is VACS > Input Manual, because the system generates Owner ID / Vehicle ID automatically.

## DEPLOY
1. Replace Code.gs in the EXISTING Apps Script project.
2. Save.
3. Deploy > Manage deployments > Edit > New version > Deploy.
4. Keep the SAME /exec URL and SAME Spreadsheet.
5. Replace index.html in the existing GitHub Pages repository.
6. Commit.
7. Reopen/refresh VACS.
8. The status should become ONLINE. If it cannot reach the endpoint after retries, it shows OFFLINE with a visible error instead of hanging on CONNECTING.

Do not mix these files with older V5.x versions.
