# Cara membuat APK Kasir Warkop Waras

Proyek ini sudah lengkap. Aplikasi kasir (file `app/src/main/assets/index.html`)
dibungkus dalam aplikasi Android. Pilih salah satu cara di bawah.

## Cara A: lewat GitHub (tanpa instal apa pun, gratis)

1. Buat akun di github.com, lalu buat repository baru (boleh Private).
2. Unggah SEMUA isi folder ini ke repository (termasuk folder `.github`).
   Di halaman repository: Add file > Upload files, seret semua isi folder.
   Pastikan folder tersembunyi `.github` ikut terunggah.
3. Buka tab **Actions**. Jika diminta, aktifkan Actions.
4. Pilih workflow **Build APK**, klik **Run workflow**.
5. Tunggu sekitar 3-6 menit sampai ada tanda centang hijau.
6. Buka run tersebut, bagian **Artifacts**, unduh `kasir-warkop-waras-apk`.
   Ekstrak zip-nya, di dalamnya ada `app-debug.apk`.
7. Kirim `app-debug.apk` ke HP Android, buka, lalu izinkan
   "Instal dari sumber tidak dikenal" jika diminta.

## Cara B: lewat Android Studio

1. Instal Android Studio (developer.android.com/studio).
2. File > Open, pilih folder proyek ini, tunggu Gradle sync selesai.
3. Menu Build > Build Bundle(s) / APK(s) > Build APK(s).
4. APK ada di `app/build/outputs/apk/debug/app-debug.apk`.

## Catatan

- Android minimal 10 (API 29).
- Aplikasi butuh internet untuk sinkron Firebase. Data yang belum terkirim
  disimpan di perangkat dan dikirim saat online lagi.
- Cetak struk memakai layanan cetak Android (pilih printer atau "Simpan sebagai PDF").
- Tombol "Unduh Excel" menyimpan file ke folder Download.
- APK ini bertanda tangan debug, cukup untuk dipakai sendiri. Untuk Google Play
  perlu keystore rilis dan format AAB.
- Memperbarui aplikasi: ganti `app/src/main/assets/index.html`, naikkan
  `versionCode` di `app/build.gradle`, lalu build ulang.
