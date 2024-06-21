---
title: Menambahkan Layer Stroke dengan Warna Solid di Aspose.PSD untuk .NET
linktitle: Menambahkan Layer Stroke dengan Warna Solid
second_title: Asumsikan.PSD .NET API
description: Tingkatkan keterampilan manipulasi gambar .NET Anda dengan Aspose.PSD. Pelajari cara menambahkan lapisan guratan dengan warna solid langkah demi langkah.
type: docs
weight: 11
url: /id/net/layer-effects/adding-stroke-layer-solid-color/
---
## Perkenalan

Dalam bidang pengembangan .NET, membuat gambar yang menarik secara visual merupakan kebutuhan umum. Aspose.PSD untuk .NET menyediakan seperangkat alat canggih untuk memanipulasi dan menyempurnakan gambar dengan mulus. Salah satu fitur penting adalah menambahkan lapisan guratan dengan warna solid, yang menghadirkan semangat dan kedalaman pada gambar Anda. Dalam tutorial ini, kami akan memandu Anda melalui proses langkah demi langkah menggunakan Aspose.PSD untuk .NET.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Pengetahuan dasar tentang pengembangan .NET.
- Visual Studio diinstal pada mesin Anda.
- Aspose.PSD untuk perpustakaan .NET. Anda dapat mengunduhnya dari[situs web](https://releases.aspose.com/psd/net/).

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.PSD untuk .NET:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## Langkah 1: Muat File PSD

Mulailah dengan memuat file PSD yang ingin Anda tingkatkan dengan lapisan guratan. Pastikan Anda memiliki jalur file yang benar:

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Kode untuk langkah selanjutnya akan ditambahkan di sini
}
```

## Langkah 2: Akses Properti Efek Stroke

Ambil properti efek stroke dari file PSD:

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## Langkah 3: Sesuaikan Pengaturan Stroke

Ubah pengaturan goresan sesuai preferensi Anda. Dalam contoh ini, kita mengubah warna menjadi kuning, mengatur opacity menjadi 127, dan menggunakan mode perpaduan Warna:

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## Langkah 4: Simpan Gambar yang Diedit

Simpan gambar setelah menerapkan perubahan lapisan guratan:

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## Langkah 5: Verifikasi Perubahannya

Pastikan perubahan diterapkan dengan benar dengan memuat dan memeriksa gambar yang diedit:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // Kode untuk memverifikasi perubahan akan ditambahkan di sini
}
```

Ulangi langkah-langkah ini untuk penyesuaian tambahan atau bereksperimen dengan efek guratan berbeda untuk mencapai dampak visual yang diinginkan.

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara menambahkan layer guratan dengan warna solid menggunakan Aspose.PSD untuk .NET. Fitur canggih ini membuka banyak kemungkinan untuk menyempurnakan gambar Anda di lingkungan .NET.

## FAQ

### Q1: Apakah Aspose.PSD untuk .NET kompatibel dengan versi kerangka .NET terbaru?

A1: Ya, Aspose.PSD untuk .NET diperbarui secara berkala untuk memastikan kompatibilitas dengan versi kerangka .NET terbaru.

### Q2: Dapatkah saya menggunakan Aspose.PSD untuk .NET untuk proyek komersial?

A2: Tentu saja! Aspose.PSD untuk .NET adalah produk komersial, dan Anda dapat menggunakannya dalam proyek Anda dengan membeli lisensi.

### Q3: Di mana saya dapat menemukan lebih banyak contoh dan dokumentasi untuk Aspose.PSD untuk .NET?

 A3: Jelajahi[dokumentasi](https://reference.aspose.com/psd/net/) untuk contoh dan bimbingan yang komprehensif.

### Q4: Apakah ada uji coba gratis yang tersedia untuk Aspose.PSD untuk .NET?

 A4: Ya, Anda bisa mendapatkan uji coba gratis dari[halaman rilis](https://releases.aspose.com/).

### Q5: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.PSD untuk .NET?

 A5: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk mencari bantuan dan berhubungan dengan masyarakat.