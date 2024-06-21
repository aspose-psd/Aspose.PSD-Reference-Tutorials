---
title: Menambahkan Layer Stroke dengan Gradient di Aspose.PSD untuk .NET
linktitle: Menambahkan Layer Stroke dengan Gradien
second_title: Asumsikan.PSD .NET API
description: Pelajari cara menambahkan lapisan guratan gradien di Aspose.PSD untuk .NET. Tingkatkan keterampilan manipulasi gambar Anda dengan tutorial komprehensif ini.
type: docs
weight: 12
url: /id/net/layer-effects/adding-stroke-layer-gradient/
---
## Perkenalan

Jika Anda ingin menyempurnakan aplikasi .NET Anda dengan efek grafis yang menakjubkan, Aspose.PSD untuk .NET adalah solusi tepat Anda. Dalam tutorial ini, kita akan mempelajari proses menambahkan lapisan guratan dengan gradien menggunakan Aspose.PSD untuk .NET. Panduan langkah demi langkah ini akan memberdayakan Anda untuk meningkatkan daya tarik visual gambar Anda dengan mudah.

## Prasyarat

Sebelum kita memulai perjalanan ini, pastikan Anda memiliki prasyarat berikut:

- Pengetahuan tentang pengembangan C# dan .NET.
-  Aspose.PSD untuk perpustakaan .NET diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/psd/net/).
- Editor kode, seperti Visual Studio, untuk mengimplementasikan contoh yang diberikan.

## Impor Namespace

Untuk memulai, mari impor namespace yang diperlukan ke dalam proyek kita. Namespace ini sangat penting untuk memanfaatkan fungsionalitas Aspose.PSD untuk .NET.

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## Langkah 1: Siapkan Direktori Dokumen

Mulailah dengan menentukan jalur ke direktori dokumen Anda dalam kode. Ini memastikan bahwa file yang diperlukan dimuat dan disimpan dari lokasi yang benar.

```csharp
string dataDir = "Your Document Directory";
```

## Langkah 2: Muat File PSD

Muat file PSD sumber menggunakan Aspose.PSD untuk .NET. Pastikan sumber daya efek dimuat untuk memanipulasi lapisan secara efektif.

```csharp
string sourceFileName = dataDir + "Stroke.psd";
string exportPath = dataDir + "StrokeGradientChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Kode untuk menangani file PSD ada di sini
}
```

## Langkah 3: Verifikasi Pengaturan Goresan Gradien

Pastikan lapisan guratan dengan gradien dikonfigurasikan dengan benar dengan memeriksa berbagai pengaturan seperti mode campuran, opacity, dan visibilitas.

```csharp
var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

// Penegasan memeriksa pengaturan guratan gradien
AssertIsTrue(gradientStroke.BlendMode == BlendMode.Normal);
AssertIsTrue(gradientStroke.Opacity == 255);
AssertIsTrue(gradientStroke.IsVisible);

// Lebih banyak pemeriksaan pernyataan untuk pengaturan pengisian
// ...
```

Terus terapkan pemeriksaan pernyataan untuk pengaturan pengisian lainnya, termasuk titik warna dan titik transparansi.

## Langkah 4: Edit Pengaturan Goresan Gradien

Sekarang, mari kita buat beberapa perubahan pada pengaturan guratan gradien. Ubah parameter seperti warna, opacity, mode campuran, dan tipe gradien untuk mencapai efek visual yang diinginkan.

```csharp
// Kode untuk mengubah pengaturan guratan gradien
// ...
```

## Langkah 5: Simpan File PSD yang Diedit

Simpan file PSD yang telah diedit ke jalur ekspor yang ditentukan.

```csharp
im.Save(exportPath);
```

## Kesimpulan

Selamat! Anda telah berhasil menambahkan lapisan guratan dengan gradien menggunakan Aspose.PSD untuk .NET. Tutorial ini telah membekali Anda dengan pengetahuan untuk menyempurnakan gambar Anda secara terprogram.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.PSD untuk .NET dengan kerangka .NET lainnya?

A1: Ya, Aspose.PSD untuk .NET kompatibel dengan berbagai kerangka .NET.

### Q2: Apakah ada uji coba gratis yang tersedia untuk Aspose.PSD untuk .NET?

 A2: Ya, Anda dapat mengakses uji coba gratis.[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.PSD untuk .NET?

 A3: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan masyarakat.

### Q4: Di mana saya dapat menemukan dokumentasi komprehensif untuk Aspose.PSD untuk .NET?

 A4: Lihat[dokumentasi](https://reference.aspose.com/psd/net/) untuk informasi rinci.

### Q5: Bagaimana cara membeli lisensi Aspose.PSD untuk .NET?

 A5: Anda dapat membeli lisensi.[Di Sini](https://purchase.aspose.com/buy).