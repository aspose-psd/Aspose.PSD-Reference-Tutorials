---
title: Memutar Gambar pada Sudut Tertentu di Aspose.PSD untuk .NET
linktitle: Memutar Gambar pada Sudut Tertentu
second_title: Asumsikan.PSD .NET API
description: Jelajahi kekuatan Aspose.PSD untuk .NET. Putar gambar dengan mudah pada sudut tertentu. Unduh perpustakaan dan mulailah memanipulasi gambar dengan lancar.
type: docs
weight: 16
url: /id/net/image-manipulation/rotate-image-specific-angle/
---
Jika Anda mendalami dunia manipulasi gambar dengan .NET, Aspose.PSD memberikan solusi yang ampuh. Dalam tutorial ini, kami akan memandu Anda melalui proses memutar gambar pada sudut tertentu menggunakan Aspose.PSD. Sebelum kita masuk ke langkah-langkahnya, mari kita siapkan tahapannya dengan pendahuluan.

## Perkenalan

Aspose.PSD untuk .NET adalah perpustakaan serbaguna yang memberdayakan pengembang untuk bekerja dengan PSD dan format gambar raster dengan lancar. Salah satu fitur utamanya adalah kemampuan memutar gambar pada sudut yang tepat, memberikan fleksibilitas dalam manipulasi gambar. Tutorial ini akan memandu Anda melalui langkah-langkah untuk memutar gambar pada sudut tertentu menggunakan Aspose.PSD untuk .NET.

## Prasyarat

Sebelum kita memulai perjalanan ini, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk .NET Library: Unduh dan instal perpustakaan dari[halaman unduh](https://releases.aspose.com/psd/net/).
- Direktori Dokumen: Siapkan direktori untuk menyimpan file sumber dan keluaran Anda.

## Impor Namespace

Untuk memulai, impor namespace yang diperlukan dalam proyek .NET Anda:

```csharp
using Aspose.PSD.ImageOptions;
```

Sekarang, mari kita bagi contoh ini menjadi beberapa langkah dalam format panduan langkah demi langkah.

## Langkah 1: Atur Direktori Dokumen Anda

```csharp
string dataDir = "Your Document Directory";
```

 Mengganti`"Your Document Directory"` dengan jalur ke direktori tempat Anda menyimpan file sumber dan output.

## Langkah 2: Muat Gambar

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // Langkah tambahan akan disisipkan di sini
}
```

 Muat gambar yang ingin Anda putar menjadi sebuah instance`RasterImage`.

## Langkah 3: Cache Data Gambar

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Simpan data gambar dalam cache untuk kinerja yang lebih baik selama rotasi.

## Langkah 4: Putar Gambar

```csharp
image.Rotate(20f, true, Color.Red);
```

Putar gambar sebesar 20 derajat, pertahankan ukuran proporsional, dan gunakan latar belakang merah.

## Langkah 5: Simpan Hasilnya

```csharp
image.Save(destName, new JpegOptions());
```

Simpan gambar yang diputar dengan opsi tertentu (dalam hal ini, sebagai JPEG).

## Kesimpulan

 Selamat! Anda telah berhasil memutar gambar pada sudut tertentu menggunakan Aspose.PSD untuk .NET. Pustaka ini menyediakan seperangkat alat canggih untuk manipulasi gambar, dan tutorial ini hanyalah puncak gunung es. Jelajahi[dokumentasi](https://reference.aspose.com/psd/net/) untuk lebih banyak fitur dan opsi.

## FAQ

### Q1: Bisakah saya memutar gambar dengan sudut selain 20 derajat?

 A1: Ya, Anda dapat menyesuaikan parameter sudut di`image.Rotate` metode ke nilai apa pun yang diinginkan.

### Q2: Apakah Aspose.PSD mendukung format gambar lain selain JPEG?

A2: Tentu saja! Aspose.PSD mendukung berbagai format, termasuk PNG, GIF, BMP, dan TIFF.

### Q3: Apakah data gambar perlu disimpan dalam cache sebelum rotasi?

J3: Meskipun tidak wajib, data cache dapat meningkatkan performa secara signifikan, terutama untuk gambar yang lebih besar.

### Q4: Di mana saya bisa mendapatkan dukungan untuk pertanyaan terkait Aspose.PSD?

 A4: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan dan diskusi komunitas.

### Q5: Dapatkah saya mencoba Aspose.PSD sebelum membeli?

 A5: Tentu saja! Ambil milikmu[uji coba gratis](https://releases.aspose.com/)untuk mengeksplorasi kemampuan perpustakaan.