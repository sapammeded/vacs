VACS V6.0 FINAL — VEHICLE LOGBOOK

Exact operational columns:
Nama | Nomor Kendaraan | Bagian/Divisi | Jenis Kendaraan | Model | Warna Kendaraan | Jam Masuk | Jam Keluar | Hari/Tanggal | Keterangan

Logic:
- 1 owner/person + 1 day = one visual group.
- Every IN→OUT cycle = one separate row.
- Name is vertically merged and centered across all rows for that person/day.
- Other columns remain row-by-row.
- Open IN remains with blank Jam Keluar and MASIH DI DALAM.
- OUT without an IN is retained as OUT tanpa IN.
- One owner can have unlimited registered vehicles; no hard-coded per-owner limit.
- Partial plate lookup and central multi-device database retained.
- Raw transaction history remains in ACCESS_HISTORY.
- ACCESS_LOG is the final human-readable operational logbook.
- Spreadsheet layout is preserved: content only is cleared/written; no auto-resize/reformat.

Deploy Code.gs + index.html together in the existing Apps Script/GitHub project, keeping the same Spreadsheet and /exec URL.
