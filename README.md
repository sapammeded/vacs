VACS V6.5 — VEHICLES HEADER FIX

This version fixes the exact problem where VEHICLES appears blank.

On EVERY web-app request:
- The spreadsheet is normalized.
- All tabs except VEHICLES and ACCESS_LOG are deleted automatically.
- VEHICLES row 1 is forcibly written as:
  Nama | Nomor Kendaraan | Bagian/Divisi | Jenis Kendaraan | Model | Warna Kendaraan
- ACCESS_LOG row 1 is forcibly written as:
  Nama | Nomor Kendaraan | Bagian/Divisi | Jenis Kendaraan | Model | Warna Kendaraan | Jam Masuk | Jam Keluar | Hari/Tanggal | Keterangan

There is also setupVACS() for one-time verification if desired, but the web app does not depend on it.

IMPORTANT DEPLOYMENT:
Use this Code.gs in the same Apps Script project, save it, then create a NEW deployment/version of the Web App.
The old /exec deployment will continue serving the old code until a new version is deployed.
