---
title: Menambahkan Layer Stroke dengan Pola di Aspose.PSD untuk .NET
linktitle: Menambahkan Layer Stroke dengan Pola
second_title: Asumsikan.PSD .NET API
description: Sempurnakan file PSD Anda dengan lapisan dan pola guratan menggunakan Aspose.PSD untuk .NET. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
type: docs
weight: 13
url: /id/net/layer-effects/adding-stroke-layer-pattern/
---
## Perkenalan

Meningkatkan file PSD (Photoshop Document) Anda dengan lapisan dan pola guratan dapat menambahkan sentuhan dinamis pada desain Anda. Dalam tutorial ini, kita akan mempelajari cara memanfaatkan Aspose.PSD untuk .NET untuk dengan mudah menambahkan lapisan guratan dengan pola ke file PSD Anda. Aspose.PSD adalah perpustakaan .NET yang kuat yang menyediakan dukungan komprehensif untuk memanipulasi file PSD, menjadikannya alat yang sangat berharga bagi pengembang dan desainer.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Pengetahuan dasar bahasa pemrograman C#.
- Visual Studio diinstal pada mesin Anda.
-  Aspose.PSD untuk perpustakaan .NET, yang dapat Anda unduh[Di Sini](https://releases.aspose.com/psd/net/).

## Impor Namespace

Pastikan Anda mengimpor namespace yang diperlukan dalam kode C# Anda:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## Langkah 1: Siapkan Lingkungan Anda

Mulailah dengan menentukan direktori sumber dan keluaran dalam kode C# Anda:

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## Langkah 2: Muat File PSD

Muat file PSD menggunakan kelas PsdImage Aspose.PSD:

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Kode Anda untuk memproses file PSD ada di sini
}
```

## Langkah 3: Siapkan Data Pola Baru

Tentukan pola baru dan batasannya:

```csharp
var newPattern = new int[]
{
    // Warna pola Anda ada di sini
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## Langkah 4: Ubah Layer Stroke

Akses layer stroke dan perbarui propertinya:

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

// Periksa dan perbarui properti guratan
// ...

// Perbarui opacity dan mode campuran
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## Langkah 5: Perbarui Informasi Pola

Perbarui informasi pola dalam file PSD:

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        // Kode Anda untuk memperbarui informasi pola ada di sini
    }
}

// Simpan file PSD yang dimodifikasi
im.Save(exportPath);
```

## Langkah 6: Verifikasi Perubahannya

Muat file PSD yang dimodifikasi dan verifikasi perubahannya:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    // Kode Anda untuk memverifikasi perubahan ada di sini
}
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara menambahkan lapisan guratan dengan pola di Aspose.PSD untuk .NET. Pustaka serbaguna ini memberdayakan pengembang untuk membuat desain yang menarik secara visual dan meningkatkan fleksibilitas file PSD.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.PSD untuk .NET dengan versi Visual Studio apa pun?

A1: Ya, Aspose.PSD untuk .NET kompatibel dengan berbagai versi Visual Studio.

### Q2: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?

 A2: Kunjungi[Di Sini](https://purchase.aspose.com/temporary-license/) untuk mendapatkan izin sementara.

### Q3: Apakah ada contoh file PSD yang tersedia untuk pengujian?

 A3: Anda dapat menemukan contoh file PSD di dokumentasi[Di Sini](https://reference.aspose.com/psd/net/).

### Q4: Apakah Aspose.PSD cocok untuk pemrosesan batch file PSD?

A4: Tentu saja, Aspose.PSD untuk .NET memberikan dukungan kuat untuk pemrosesan batch.

### Q5: Dimana saya bisa mencari bantuan atau berpartisipasi dalam diskusi komunitas?

 A5: Kunjungi[Forum Asumsikan.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan dan interaksi komunitas.