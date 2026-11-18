# FINORA — Personal Finance

FINORA adalah aplikasi keuangan pribadi berbasis HTML/CSS/JavaScript murni, dengan penyimpanan lokal (`localStorage`), dapat diterbitkan sebagai GitHub Pages dan dibungkus menjadi APK Android menggunakan WebView bawaan Android.

## Fitur awal
- Dashboard saldo, pemasukan, pengeluaran, ringkasan bulanan
- Transaksi pemasukan/pengeluaran: tambah, edit, hapus
- Dompet tunai dan digital
- Anggaran bulanan
- Target tabungan
- Utang dan piutang
- Tagihan rutin
- Laporan sederhana
- Tema gelap/terang
- Backup dan restore JSON
- Profil lokal sederhana

## Jalankan di GitHub
1. Buat repository bernama `FINORA`.
2. Unggah seluruh isi folder proyek ini ke root repository.
3. Buka **Settings → Pages**, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Website akan tersedia melalui alamat GitHub Pages repository.

## Build APK
Workflow `.github/workflows/build-apk.yml` akan membangun APK ketika ada push ke `main` atau dijalankan manual.
Buka **Actions → Build FINORA Android APK → Run workflow**. APK tersedia pada bagian Artifacts dari hasil workflow.

## Penyimpanan dan batasan
- Data disimpan pada perangkat/browser yang digunakan. Data website GitHub Pages dan APK Android memiliki penyimpanan terpisah.
- Hapus data aplikasi/browser atau uninstall dapat menghapus data lokal. Lakukan backup JSON secara berkala.
- Backup/restore manual tersedia di menu Pengaturan.
- Versi awal ini tidak menggunakan sinkronisasi cloud atau database online.
- APK menggunakan Android WebView bawaan; tidak ada library JavaScript tambahan.

## Struktur
- `index.html`, `assets/`: aplikasi web untuk GitHub Pages
- `app/`: proyek Android WebView untuk APK
- `.github/workflows/`: workflow build APK


## Logo FINORA
Logo FINORA sudah dipasang sebagai favicon website dan ikon launcher Android.
Aset utama: `assets/finora-logo.png`.
Ikon Android tersedia pada folder `app/src/main/res/mipmap-*`.
