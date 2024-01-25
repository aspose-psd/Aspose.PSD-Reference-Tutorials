---
title: Memotong File PSD dengan Aspose.PSD untuk .NET
linktitle: Memotong File PSD dengan Aspose.PSD untuk .NET
second_title: Asumsikan.PSD .NET API
description: Jelajahi seni pemotongan file PSD di .NET dengan Aspose.PSD, perangkat serbaguna. Tingkatkan permainan manipulasi gambar Anda dengan mudah.
type: docs
weight: 19
url: /id/net/psd-file-manipulation/crop-psd-file/
---
## Perkenalan
Dalam bidang pengembangan .NET, Aspose.PSD menonjol sebagai perangkat yang ampuh untuk menangani file PSD (Photoshop Document) dengan mulus. Dalam hal memanipulasi gambar, pemotongan adalah operasi mendasar, dan Aspose.PSD menyederhanakan proses ini untuk pengembang .NET. Dalam tutorial ini, kita akan mempelajari cara memotong file PSD menggunakan Aspose.PSD untuk .NET, memberi Anda panduan langkah demi langkah.
## Prasyarat
Sebelum mempelajari tutorial, pastikan Anda memiliki prasyarat berikut:
-  Aspose.PSD untuk .NET: Pastikan Anda telah menginstal perpustakaan. Anda dapat mengunduhnya dari[Aspose.PSD untuk dokumentasi .NET](https://reference.aspose.com/psd/net/).
- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET Anda, termasuk Visual Studio atau IDE pilihan lainnya.
## Impor Namespace
Mulailah dengan mengimpor namespace yang diperlukan ke proyek Anda:
```csharp
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.ImageOptions;
```
## Langkah 1: Siapkan Proyek Anda
Buat proyek .NET baru atau buka proyek yang sudah ada di IDE pilihan Anda.
## Langkah 2: Sertakan Perpustakaan Aspose.PSD
 Tambahkan referensi ke perpustakaan Aspose.PSD di proyek Anda. Anda dapat melakukan ini dengan mengunduh perpustakaan dari[Halaman unduhan Aspose.PSD](https://releases.aspose.com/psd/net/).
## Langkah 3: Inisialisasi Aspose.PSD
Dalam kode Anda, inisialisasi Aspose.PSD dengan memuat file PSD:
```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "1.psd";
using (RasterImage image = Image.Load(sourceFileName) as RasterImage)
{
    // Kode Anda di sini
}
```
## Langkah 4: Pangkas File PSD
Terapkan metode Pangkas yang benar untuk file PSD. Tentukan parameter pemotongan menggunakan objek Rectangle:
```csharp
image.Crop(new Rectangle(10, 30, 100, 100));
```
Sesuaikan nilai dalam konstruktor Rectangle sesuai dengan kebutuhan pemangkasan Anda.
## Langkah 5: Simpan Gambar yang Dipotong
Simpan gambar yang dipotong dalam format PSD dan PNG:
```csharp
string exportPathPsd = dataDir + "CropTest.psd";
string exportPathPng = dataDir + "CropTest.png";
image.Save(exportPathPsd, new PsdOptions());
image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
```
## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara memotong file PSD menggunakan Aspose.PSD untuk .NET. Proses sederhana namun kuat ini dapat diintegrasikan dengan mulus ke dalam aplikasi .NET Anda untuk manipulasi gambar yang efisien.

## FAQ

### Q1: Apakah Aspose.PSD kompatibel dengan kerangka .NET terbaru?

A1: Ya, Aspose.PSD diperbarui secara berkala untuk memastikan kompatibilitas dengan kerangka .NET terbaru.

### Q2: Dapatkah saya menggunakan Aspose.PSD untuk proyek komersial?

 A2: Tentu saja! Aspose.PSD tersedia untuk penggunaan komersial. Anda dapat membelinya[Di Sini](https://purchase.aspose.com/buy).

### Q3: Apakah tersedia uji coba gratis?

 A3: Ya, Anda dapat menjelajahi Aspose.PSD dengan uji coba gratis. Unduh itu[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dukungan untuk Aspose.PSD?

 A4: Untuk pertanyaan atau bantuan apa pun, kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Apakah saya memerlukan lisensi sementara untuk tujuan pengujian?

 A5: Ya, jika Anda memerlukan lisensi sementara, Anda bisa mendapatkannya[Di Sini](https://purchase.aspose.com/temporary-license/).