VACS V7.1 — FINAL P1 UI + BUGFIX
CREATED BY: Mbah Pri

VISIBLE MENUS:
1. MASTER
   - Input Manual / Update
   - Import Excel / CSV
   - Download Template Excel
2. CURRENTLY INSIDE
3. AUDIT EVENT
4. BACKUP DATABASE
5. REPORT 1x24H
6. GATE

P0 retained:
- Vehicle unique key by Nomor Kendaraan.
- IN/OUT state validation.
- Auto-fill master.
- 1x24h report.
- Server timestamp Asia/Jakarta.
- Multi-device central Spreadsheet + ScriptLock.

P1 now visible:
- Audit Event menu and table.
- Currently Inside menu and refresh.
- Backup Database button.
- Official Excel template button.
- Excel/CSV import with upsert by Nomor Kendaraan.
- Manual input/update.

BUGFIX:
- All buttons are explicitly bound after the DOM is loaded.
- Template button directly generates VACS_VEHICLES_TEMPLATE.xlsx using SheetJS.
- Import reads xlsx/xls/csv and maps common headers.
- Backend has exact two-sheet contract.
- Legacy sheets are automatically removed.
- Vehicle master has exactly six columns.
- Access log has exactly ten columns.
- Duplicate IN is rejected.
- OUT without an open IN is rejected.
- Server time is used.
- Same-day Name rows are vertically merged and centered.

IMPORTANT:
Replace BOTH Code.gs and index.html.
Deploy a NEW web-app version:
Apps Script > Deploy > Manage deployments > Edit > New version > Deploy.
Keep the same /exec URL.


V7.1.1 HOTFIX:
- Fix Date object formatting from Google Sheets: Jam IN/OUT = HH:mm:ss, Tanggal = dd/MM/yyyy.
- Fix stale Gate error message remaining after a new search.
- Currently Inside now shows Nama + Nomor Kendaraan + Divisi + Jam IN + Tanggal.


V7.2 ADMIN DELETE + BUGFIX:
- Admin-only Delete from VEHICLES using PIN.
- ACCESS_LOG is never deleted when a vehicle is deleted from MASTER.
- Delete action is written to server audit log.
- Backend PIN is stored in Apps Script Script Properties (default PIN: 2580; change it before production).
- Existing V7.1.1 date/time hotfix retained.
- Existing stale-message search fix retained.
- No extra spreadsheet sheets are created.
- VEHICLES remains exactly 6 columns.
- ACCESS_LOG remains exactly 10 columns.
