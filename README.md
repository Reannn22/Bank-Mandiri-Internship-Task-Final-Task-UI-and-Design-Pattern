# Virtual Internship Mandiri

Panduan untuk menjalankan proyek ini.

## Persyaratan
- Flutter SDK versi terbaru
- Android Studio / VS Code
- Dart SDK
- Android Emulator / Perangkat Android fisik

## Instalasi Flutter
1. Download Flutter SDK:
   - Kunjungi https://docs.flutter.dev/get-started/install/windows
   - Download Flutter SDK untuk Windows
   - Extract file zip ke C:\flutter
   - Hindari lokasi yang memerlukan privilege tinggi (seperti C:\Program Files)

2. Install Android Studio:
   - Download dari https://developer.android.com/studio
   - Install Android Studio
   - Jalankan Android Studio dan selesaikan setup wizard
   - Install plugin Flutter dan Dart:
     - Buka Android Studio
     - Buka Settings/Preferences
     - Pilih Plugins
     - Cari dan install plugin Flutter
     - Restart Android Studio

3. Setup Android Emulator:
   - Di Android Studio, buka Tools > Device Manager
   - Klik Create Device
   - Pilih dan download sistem Android yang diinginkan
   - Buat dan jalankan emulator

## Setup Flutter PATH
Sebelum menjalankan proyek, pastikan Flutter sudah terdaftar di PATH sistem:

1. Temukan lokasi Flutter SDK:
   - Buka Command Prompt
   - Jalankan perintah berikut untuk menemukan lokasi Flutter:
   ```bash
   where flutter
   ```
   - Atau pada PowerShell:
   ```bash
   Get-Command flutter
   ```
   - Path yang muncul akan menunjukkan lokasi flutter.bat (contoh: C:\flutter\bin\flutter.bat)
   - Lokasi Flutter SDK adalah folder parent dari 'bin' 

2. Tambahkan Flutter ke System PATH:
   - Buka "Edit System Environment Variables" (ketik "environment" di Start menu)
   - Klik "Environment Variables"
   - Pada "System Variables", cari variable "Path"
   - Klik "Edit" dan tambahkan path ke folder bin Flutter SDK 
     (C:\flutter\bin)
   - Klik "OK" untuk menyimpan

3. Penting: Tutup dan buka kembali Command Prompt/PowerShell setelah mengubah PATH
   - PATH baru tidak akan terbaca pada jendela terminal yang sudah terbuka
   - Buka terminal baru untuk menggunakan perubahan PATH

4. Verifikasi instalasi dengan:
```bash
flutter --version
```

## Troubleshooting PATH
Jika perintah 'flutter' tidak dikenali:

1. Verifikasi lokasi Flutter:
   - Buka File Explorer
   - Pastikan Flutter terinstall di C:\flutter
   - Pastikan ada folder 'bin' di dalamnya
   - Copy full path ke folder bin tersebut

2. Periksa PATH di Command Prompt:
```bash
echo %PATH%
```
   - Pastikan path ke C:\flutter\bin muncul dalam output

3. Alternatif sementara:
   - Gunakan full path ke flutter.bat:
   ```bash
   C:\flutter\bin\flutter --version
   ```
   - Atau pindah ke direktori bin Flutter:
   ```bash
   cd C:\flutter\bin
   .\flutter --version
   ```

## Troubleshooting PowerShell
Jika Flutter berfungsi di Git Bash tetapi tidak di PowerShell:

1. Periksa Path di PowerShell:
```powershell
$env:Path -split ';'
```
   - Pastikan C:\flutter\bin muncul dalam daftar

2. Solusi Cepat:
   - Buka PowerShell sebagai Administrator
   - Jalankan perintah berikut untuk menambahkan Flutter ke Path untuk sesi ini:
   ```powershell
   $env:Path += ";C:\flutter\bin"
   ```

3. Solusi Permanen:
   - Buka PowerShell sebagai Administrator
   - Jalankan perintah berikut:
   ```powershell
   [Environment]::SetEnvironmentVariable(
       "Path",
       [Environment]::GetEnvironmentVariable("Path", "Machine") + ";C:\flutter\bin",
       "Machine"
   )
   ```
   - Tutup dan buka kembali PowerShell

4. Verifikasi:
   ```powershell
   flutter --version
   ```

Catatan: Jika masih mengalami masalah, gunakan Git Bash sebagai alternatif untuk menjalankan perintah Flutter.

`