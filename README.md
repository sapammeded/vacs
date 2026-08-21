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
