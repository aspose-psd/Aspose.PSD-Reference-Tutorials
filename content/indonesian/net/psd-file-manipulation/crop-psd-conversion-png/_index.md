---
title: Memotong File PSD saat Mengonversi ke PNG di Aspose.PSD untuk .NET
linktitle: Memotong File PSD saat Mengonversi ke PNG
second_title: Asumsikan.PSD .NET API
description: Pelajari cara memotong file PSD dengan mudah menggunakan Aspose.PSD untuk .NET. Ikuti panduan langkah demi langkah kami untuk konversi ke PNG tanpa hambatan.
type: docs
weight: 18
url: /id/net/psd-file-manipulation/crop-psd-conversion-png/
---
## Perkenalan
Dalam bidang pengembangan .NET, memanipulasi dan mengonversi gambar adalah tugas yang umum. Aspose.PSD untuk .NET menyediakan seperangkat alat canggih untuk menyederhanakan proses ini. Salah satu persyaratan yang sering dilakukan adalah memotong file PSD sebelum mengonversinya ke PNG. Dalam tutorial langkah demi langkah ini, kita akan mempelajari proses menggunakan Aspose.PSD untuk .NET.
## Prasyarat
Sebelum kita memulai perjalanan ini, pastikan Anda memiliki hal-hal berikut:
-  Aspose.PSD untuk .NET Library: Unduh dan instal perpustakaan dari[Aspose.PSD untuk Dokumentasi .NET](https://reference.aspose.com/psd/net/).
- Contoh File PSD: Siapkan file PSD untuk eksperimen. Jika Anda tidak memilikinya, Anda dapat menggunakan contoh yang disediakan dalam tutorial.
- Lingkungan .NET: Pastikan Anda telah menyiapkan lingkungan pengembangan .NET yang berfungsi.
- Direktori Dokumen: Tentukan jalur ke direktori dokumen Anda dalam kode.
## Impor Namespace
Dalam proyek .NET Anda, sertakan namespace yang diperlukan untuk Aspose.PSD untuk .NET:
```csharp
using Aspose.PSD.ImageOptions;
```
## Langkah 1: Muat Gambar PSD
```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// Muat gambar PSD yang ada
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // Kode Anda untuk langkah selanjutnya akan ditempatkan di sini
}
```
## Langkah 2: Tentukan Persegi Panjang Pemangkasan
```csharp
// Buat instance kelas Rectangle dengan meneruskan x, y, lebar, dan tinggi
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## Langkah 3: Pangkas Gambar
```csharp
// Panggil metode crop pada kelas Image dan teruskan instance kelas persegi panjang
image.Crop(cropRectangle);
```
## Langkah 4: Tentukan Opsi PNG
```csharp
// Buat sebuah instance dari kelas PNGOptions
PngOptions pngOptions = new PngOptions();
```
## Langkah 5: Simpan Gambar yang Dipotong sebagai PNG
```csharp
// Panggil metode penyimpanan, berikan jalur keluaran, dan pngOptions untuk mengonversi file PSD ke PNG dan menyimpan hasilnya
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara memotong file PSD saat mengonversinya ke PNG menggunakan Aspose.PSD untuk .NET. Kemampuan ini sangat berharga dalam berbagai skenario pemrosesan gambar.

## FAQ

### Q1: Bisakah saya menggunakan perpustakaan ini dalam proyek komersial?

 A1: Ya, Aspose.PSD untuk .NET tersedia untuk penggunaan komersial. Lihat[Lisensi Aspose.PSD](https://purchase.aspose.com/buy) untuk detailnya.

### Q2: Apakah tersedia uji coba gratis?

A2: Tentu saja! Anda dapat menjelajahi versi uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat menemukan dukungan untuk Aspose.PSD untuk .NET?

 A3: Kunjungi[Forum Asumsikan.PSD](https://forum.aspose.com/c/psd/34) untuk bantuan atau pertanyaan apa pun.

### Q4: Bagaimana cara mendapatkan lisensi sementara?

 A4: Jika Anda memerlukan lisensi sementara, Anda bisa mendapatkannya[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Apakah ada contoh atau tutorial yang tersedia di dokumentasi?

 A5: Ya, Anda dapat menemukan dokumentasi dan contoh yang komprehensif[Di Sini](https://reference.aspose.com/psd/net/).