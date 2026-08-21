VACS V6.1 — FINAL MASTER VEHICLES CONTRACT

THIS IS THE LOCKED VEHICLES SHEET FORMAT.
It MUST contain exactly these six columns, in this order:

1. Nama
2. Nomor Kendaraan
3. Bagian/Divisi
4. Jenis Kendaraan
5. Model
6. Warna Kendaraan

No Owner ID.
No Vehicle ID.
No Employee ID.
No technical master columns.

VEHICLE LOOKUP:
- Nomor Kendaraan is the lookup key.
- A person can have unlimited vehicles; there is no hard-coded per-person vehicle limit.
- Partial search remains supported by the web app.
- The profile returned from a plate comes directly from the six VEHICLES fields.
- Missing profile fields are allowed and can be completed later.

OPERATIONAL LOG:
The final visible log uses exactly:
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

Every IN -> OUT cycle is one row.
The same person's Nama is vertically merged and centered for all their rows within the same day.
ACCESS_HISTORY remains the raw audit history.

Do not mix this Code.gs with older versions.
Replace Code.gs and index.html together in the existing Apps Script/GitHub project.
Keep the same Spreadsheet and /exec URL.
