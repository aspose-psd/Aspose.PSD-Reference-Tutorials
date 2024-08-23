---
title: Memburamkan Gambar di Aspose.PSD untuk .NET
linktitle: Mengaburkan Gambar
second_title: Asumsikan.PSD .NET API
description: Pelajari cara memburamkan gambar dengan mudah dengan Aspose.PSD untuk .NET. Panduan langkah demi langkah untuk manipulasi gambar yang lancar di proyek C# Anda.
type: docs
weight: 13
url: /id/net/image-adjustment/blur-image/
---
## Perkenalan

Di bidang pengembangan .NET, Aspose.PSD terbukti menjadi sekutu yang kuat untuk manipulasi gambar. Tutorial ini berfokus pada tugas tertentu: mengaburkan gambar menggunakan Aspose.PSD untuk .NET. Jika Anda ingin meningkatkan keterampilan pemrosesan gambar atau sekadar mencari cara efisien untuk memburamkan gambar secara terprogram, Anda berada di tempat yang tepat.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk .NET: Pastikan Anda telah menginstal perpustakaan Aspose.PSD. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/psd/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET, dan miliki pemahaman dasar tentang C#.

- Contoh Gambar: Siapkan contoh gambar dalam format PSD. Anda dapat menggunakan milik Anda sendiri atau mengunduhnya untuk pengujian.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan dalam kode C# Anda:

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## Langkah 1: Tentukan Direktori Dokumen Anda

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
```

## Langkah 2: Muat Gambar

```csharp
//ExStart:BluranImage

string sourceFile = dataDir + @"sample.psd";

// Muat gambar yang ada ke dalam instance kelas RasterImage
using (var image = Image.Load(sourceFile))
{
    // Lanjutkan ke langkah selanjutnya dalam blok penggunaan ini
}
```

## Langkah 3: Ubah Gambar menjadi RasterImage

```csharp
RasterImage rasterImage = (RasterImage)image;
```

## Langkah 4: Terapkan Filter Gaussian Blur

```csharp
rasterImage.Filter(rasterImage.Bounds, new GaussianBlurFilterOptions(15, 15));
```

 Di sini, itu`GaussianBlurFilterOptions` class digunakan dengan radius tertentu 15 untuk pengaburan horizontal dan vertikal.

## Langkah 5: Simpan Gambar Buram

```csharp
string destName = dataDir + @"BlurAnImage_out.gif";
rasterImage.Save(destName, new GifOptions());
```

## Kesimpulan

Selamat! Anda berhasil memburamkan gambar menggunakan Aspose.PSD untuk .NET. Tutorial ini memberikan gambaran sekilas tentang kemampuan Aspose.PSD dan membuka pintu ke berbagai kemungkinan manipulasi gambar di aplikasi .NET Anda.

## FAQ

### Q1: Dapatkah saya menerapkan intensitas keburaman yang berbeda pada bagian gambar yang berbeda?

A1: Ya, Aspose.PSD memungkinkan Anda menerapkan filter dengan berbagai parameter ke wilayah tertentu pada gambar, memberikan kontrol terperinci atas proses pemburaman.

### Q2: Apakah Aspose.PSD kompatibel dengan semua format gambar?

A2: Meskipun Aspose.PSD mendukung berbagai format gambar, disarankan untuk memeriksa dokumentasi untuk daftar lengkap dan pertimbangan khusus format apa pun.

### Q3: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?

 A3: Anda dapat memperoleh lisensi sementara dari[Di Sini](https://purchase.aspose.com/temporary-license/) untuk tujuan pengujian dan evaluasi.

### Q4: Apakah ada fitur manipulasi gambar lainnya di Aspose.PSD?

A4: Tentu saja! Aspose.PSD menawarkan serangkaian fitur lengkap, termasuk mengubah ukuran, memotong, dan penyesuaian warna. Jelajahi dokumentasi untuk daftar lengkap.

### Q5: Di mana saya dapat mencari bantuan atau terhubung dengan komunitas Aspose.PSD?

 A5: Untuk pertanyaan atau diskusi apa pun, kunjungi[Forum Asumsikan.PSD](https://forum.aspose.com/c/psd/34).