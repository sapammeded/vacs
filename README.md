VACS V6.3 — FINAL TWO-SHEET EDITION

ONLY TWO GOOGLE SHEETS ARE REQUIRED:

1) VEHICLES
Exactly 6 columns:
Nama
Nomor Kendaraan
Bagian/Divisi
Jenis Kendaraan
Model
Warna Kendaraan

2) ACCESS_LOG
Exactly 10 columns:
Nama
Nomor Kendaraan
Bagian/Divisi
Jenis Kendaraan
Model
Warna Kendaraan
Jam Masuk
Jam Keluar
Hari/Tanggal
Keterangan

All old helper sheets are NOT required.
You may manually delete all other sheets.

WEB APP:
- DAFTAR KENDARAAN writes directly to VEHICLES.
- Partial/full plate search reads VEHICLES.
- Vehicle IN/OUT writes the operational log to ACCESS_LOG.
- One IN -> OUT cycle = one row.
- Same person's name is merged vertically and centered for all rows in the same day.
- Multiple vehicles per person are supported without a hard-coded limit.
- Unregistered plates are rejected.
- Existing plate updates its VEHICLES row instead of creating a duplicate.
- PDF/Excel report is generated from ACCESS_LOG.

IMPORTANT:
Delete all other Google Sheets tabs manually if desired.
Keep only VEHICLES and ACCESS_LOG.
Do not mix Code.gs with older versions.
Deploy Code.gs + index.html together in the same Apps Script/GitHub project and keep the same Spreadsheet ID and /exec URL.
