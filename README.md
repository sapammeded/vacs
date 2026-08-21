VACS V7.0 — P0 + P1 PRO UPGRADE
CREATED BY: Mbah Pri

CENTRAL SPREADSHEET:
- VEHICLES: exactly 6 columns
  Nama
  Nomor Kendaraan
  Bagian/Divisi
  Jenis Kendaraan
  Model
  Warna Kendaraan

- ACCESS_LOG: exactly 10 columns
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

P0:
1. Vehicle unique key — Nomor Kendaraan.
2. IN/OUT state validation — duplicate IN and OUT-without-IN rejected.
3. Auto-fill master — gate search pulls profile from VEHICLES.
4. 1x24h reporting — every IN->OUT cycle is a separate row.
5. Server timestamp — Asia/Jakarta server time.
6. Multi-device consistency — central Spreadsheet + ScriptLock.

P1:
7. Audit — server-side audit events, with CREATED BY: Mbah Pri.
8. Currently Inside.
9. Backup — creates timestamped central Spreadsheet copy.
10. Excel template — six exact VEHICLES headers.
11. Excel/CSV master import — upsert by Nomor Kendaraan.

CREATED BY is fixed to:
Mbah Pri

Deployment:
Replace Code.gs + index.html together.
Apps Script: Deploy > Manage deployments > Edit > New version > Deploy.
Keep the same /exec URL.
