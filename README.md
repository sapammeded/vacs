VACS V5.5 FINAL — 1x24H OWNER REPORT

WHAT IS FIXED
- Generate Report button has explicit loading/error handling.
- Report groups by OWNER/PERSON + CALENDAR DATE (1x24h operational window).
- All IN/OUT events for that person during that day appear in ONE ROW.
- Multiple vehicles used by the same person are combined into the same row.
- Timeline example:
  IN 10:35 [B1234XX] | OUT 11:39 [B1234XX] | IN 13:17 [B5678YY] | OUT 17:00 [B5678YY]
- Status is based on complete day's events, not the selected display filter.
- REPORT_24H is generated without resizing, recoloring, refreezing, or reformatting the sheet.
- Existing Spreadsheet layout remains administrator-owned.
- Excel export and Print/PDF use the grouped 1x24h report.
- All devices continue to use the same central Spreadsheet and Apps Script endpoint.

DEPLOY
1. Replace Code.gs and index.html together.
2. Apps Script: Save -> Deploy -> Manage deployments -> Edit -> New version -> Deploy.
3. Keep the same /exec URL and same Spreadsheet.
4. GitHub Pages: replace index.html.
5. Refresh/reopen VACS.

IMPORTANT
Do not mix this pair with older V5.x files.
