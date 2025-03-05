---
title: Memperluas dan Memotong Gambar di Aspose.PSD untuk .NET
linktitle: Memperluas dan Memotong Gambar
second_title: Asumsikan.PSD .NET API
description: Pelajari cara memperluas dan memotong gambar secara dinamis menggunakan Aspose.PSD untuk .NET. Ikuti panduan langkah demi langkah kami untuk manipulasi gambar yang lancar.
type: docs
weight: 13
url: /id/net/image-manipulation/expand-crop-images/
---
## Perkenalan

Aspose.PSD untuk .NET adalah perpustakaan pencitraan komprehensif yang memungkinkan pengembang bekerja dengan berbagai format gambar dalam aplikasi .NET mereka. Salah satu fitur menonjolnya adalah kemampuan memanipulasi gambar dengan mudah. Dalam tutorial ini, kami akan fokus pada memperluas dan memotong gambar, memberi Anda panduan praktis untuk mencapai tugas ini menggunakan Aspose.PSD.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk Perpustakaan .NET: Pastikan Anda telah menginstal perpustakaan Aspose.PSD untuk .NET. Anda dapat mengunduhnya dari[Aspose.PSD untuk dokumentasi .NET](https://reference.aspose.com/psd/net/).

- Contoh Gambar: Siapkan contoh file gambar (misalnya, "example1.psd") yang akan Anda gunakan untuk tutorial.

Sekarang, mari kita mulai dengan panduan langkah demi langkah.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan untuk memanfaatkan fungsionalitas yang disediakan oleh Aspose.PSD untuk .NET. Tambahkan namespace berikut ke kode Anda:

```csharp
using Aspose.PSD.ImageOptions;
```

## Langkah 1: Siapkan Proyek

 Pastikan Anda memiliki proyek yang disiapkan dengan Aspose.PSD untuk .NET terintegrasi. Jika tidak, ikuti[dokumentasi](https://reference.aspose.com/psd/net/) untuk bimbingan.

## Langkah 2: Muat Gambar

Muat gambar sampel menggunakan kode berikut:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// Muat gambar
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // Kode tambahan untuk pemrosesan gambar akan ditempatkan di sini
}
```

## Langkah 3: Cache Data Gambar

Simpan data gambar dalam cache untuk mengoptimalkan kinerja:

```csharp
rasterImage.CacheData();
```

## Langkah 4: Tentukan Persegi Panjang Tujuan

Buat instance kelas Rectangle dan tentukan X, Y, Lebar, dan Tinggi persegi panjang. Ini akan menjadi area dimana gambar akan diperluas atau dipotong.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## Langkah 5: Simpan Gambar Keluaran

Simpan gambar keluaran dengan opsi yang ditentukan dan persegi panjang tujuan:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara memperluas dan memotong gambar menggunakan Aspose.PSD untuk .NET. Pustaka yang kuat ini membuka banyak kemungkinan untuk manipulasi gambar dalam aplikasi .NET Anda.

## FAQ

### Q1: Bisakah Aspose.PSD menangani format gambar lain selain PSD?

A1: Ya, Aspose.PSD mendukung berbagai format gambar, termasuk JPEG, PNG, GIF, dan banyak lagi.

### Q2: Di mana saya dapat menemukan dukungan untuk Aspose.PSD?

 A2: Anda dapat menemukan dukungan dan terlibat dengan komunitas di[Forum Asumsikan.PSD](https://forum.aspose.com/c/psd/34).

### Q3 Apakah ada uji coba gratis yang tersedia untuk Aspose.PSD untuk .NET?

 A3: Ya, Anda dapat menjelajahi fitur-fiturnya dengan uji coba gratis yang tersedia di[Uji Coba Gratis Aspose.PSD](https://releases.aspose.com/).

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?

 A4: Anda bisa mendapatkan lisensi sementara dari[Lisensi Sementara Aspose.PSD](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat membeli Aspose.PSD untuk .NET?

 A5: Anda dapat membeli perpustakaan di[Halaman Pembelian Aspose.PSD](https://purchase.aspose.com/buy).