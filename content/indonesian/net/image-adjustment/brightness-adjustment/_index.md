---
title: Menerapkan Penyesuaian Kecerahan di Aspose.PSD untuk .NET
linktitle: Menerapkan Penyesuaian Kecerahan
second_title: Asumsikan.PSD .NET API
description: Jelajahi kekuatan Aspose.PSD untuk .NET dalam menyesuaikan kecerahan gambar. Ikuti panduan langkah demi langkah kami untuk penerapan yang lancar.
type: docs
weight: 10
url: /id/net/image-adjustment/brightness-adjustment/
---
## Perkenalan

Meningkatkan dan menyesuaikan atribut gambar merupakan persyaratan umum dalam berbagai aplikasi, dan Aspose.PSD untuk .NET memberikan solusi canggih untuk memanipulasi file PSD dengan lancar. Salah satu manipulasi tersebut adalah penyesuaian kecerahan, memungkinkan Anda mengubah kecerahan gambar dengan mudah.

Dalam tutorial ini, kita akan memandu proses penerapan penyesuaian kecerahan menggunakan Aspose.PSD untuk .NET. Ikuti langkah-langkah di bawah ini untuk mendapatkan pemahaman komprehensif tentang cara memasukkan penyesuaian kecerahan ke dalam file PSD Anda.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk .NET Library: Unduh dan instal Aspose.PSD untuk .NET Library dari[tautan unduhan](https://releases.aspose.com/psd/net/).

-  Direktori Dokumen: Siapkan direktori untuk menyimpan file PSD Anda dan perbarui`dataDir` variabel dalam cuplikan kode yang disediakan dengan jalur ke direktori dokumen Anda.

## Impor Namespace

Dalam proyek .NET Anda, sertakan namespace yang diperlukan untuk mengakses fungsionalitas Aspose.PSD. Tambahkan namespace berikut ke kode Anda:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

Sekarang, mari kita bagi contoh ini menjadi beberapa langkah:

## Langkah 1: Muat File PSD

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// Muat file PSD menggunakan Aspose.PSD
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // Kode Anda untuk langkah selanjutnya ada di sini
}
```

## Langkah 2: Dapatkan Gambar Raster

```csharp
// Dapatkan gambar raster dari file PSD yang dimuat
RasterCachedImage rasterImage = image;
```

## Langkah 3: Sesuaikan Kecerahan

```csharp
// Tetapkan nilai kecerahan. Nilai kecerahan yang diterima berada dalam kisaran [-255, 255].
rasterImage.AdjustBrightness(-50);
```

## Langkah 4: Simpan Gambar yang Dimodifikasi

```csharp
// Simpan gambar yang dimodifikasi dengan kecerahan yang disesuaikan
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

Sekarang kami telah membagi contoh menjadi langkah-langkah yang dapat dikelola, Anda dapat dengan mudah mengintegrasikan penyesuaian kecerahan ke dalam proyek .NET Anda menggunakan Aspose.PSD.

## Kesimpulan

Aspose.PSD untuk .NET menyederhanakan proses penerapan penyesuaian kecerahan dalam file PSD. Dengan mengikuti panduan langkah demi langkah yang disediakan di atas, Anda dapat dengan mudah meningkatkan daya tarik visual gambar Anda. Bereksperimenlah dengan nilai kecerahan yang berbeda untuk mencapai hasil yang diinginkan.

## FAQ

### Q1: Di mana saya dapat menemukan dokumentasi Aspose.PSD untuk .NET?

 A1: Dokumentasi tersedia[Di Sini](https://reference.aspose.com/psd/net/).

### Q2: Bagaimana cara mengunduh perpustakaan Aspose.PSD untuk .NET?

 A2: Anda dapat mengunduh perpustakaan dari[halaman rilis](https://releases.aspose.com/psd/net/).

### Q3: Apakah ada uji coba gratis yang tersedia untuk Aspose.PSD untuk .NET?

 A3: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya bisa mendapatkan dukungan untuk Aspose.PSD untuk .NET?

 A4: Untuk dukungan, kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Bagaimana cara mendapatkan lisensi sementara Aspose.PSD untuk .NET?

 A5: Anda dapat memperoleh lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).