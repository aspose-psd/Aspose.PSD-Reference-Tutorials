---
title: Menambahkan Efek Stroke ke Lapisan di Aspose.PSD untuk .NET
linktitle: Menambahkan Efek Stroke ke Layers
second_title: Asumsikan.PSD .NET API
description: Tingkatkan estetika gambar dengan Aspose.PSD untuk .NET. Pelajari cara menambahkan efek guratan selangkah demi selangkah. Unduh, beli, atau coba uji coba gratis sekarang.
type: docs
weight: 10
url: /id/net/layer-effects/adding-stroke-effects/
---
## Perkenalan

Selamat datang di tutorial langkah demi langkah tentang menambahkan efek guratan ke lapisan di Aspose.PSD untuk .NET. Meningkatkan daya tarik visual gambar Anda sangatlah mudah dengan efek guratan, dan Aspose.PSD menjadikannya lancar bagi pengembang .NET. Dalam panduan ini, kami akan memandu Anda melalui prosesnya, memberikan langkah-langkah dan contoh yang jelas untuk membantu Anda menguasai fitur canggih ini.

## Prasyarat

Sebelum kita masuk ke tutorialnya, pastikan Anda memiliki prasyarat berikut:

- Aspose.PSD untuk .NET: Unduh dan instal perpustakaan Aspose.PSD dari[situs web](https://releases.aspose.com/psd/net/).

- Direktori Dokumen: Siapkan direktori yang berisi dokumen PSD tempat Anda ingin menerapkan efek guratan.

- Direktori Keluaran: Memiliki direktori terpisah untuk menyimpan gambar keluaran dengan efek guratan.

- Visual Studio: Pastikan Anda telah menyiapkan Visual Studio atau lingkungan pengembangan .NET pilihan lainnya.

## Impor Namespace

Dalam proyek .NET Anda, sertakan namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Langkah 1: Muat Dokumen PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Kode Anda untuk memuat dokumen PSD ada di sini
}
```

## Langkah 2: Tambahkan Efek Goresan Warna

```csharp
// Menambahkan isian Warna, pada posisi Di Dalam
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Langkah 3: Posisi Luar

```csharp
// Menambahkan isian Warna, pada posisi Luar
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Langkah 4: Posisi Tengah

```csharp
// Menambahkan isian Warna, pada posisi Tengah
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Ulangi langkah serupa untuk pengisian Gradien dan Pola, sesuaikan pengaturannya.

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara menambahkan efek guratan ke lapisan menggunakan Aspose.PSD untuk .NET. Bereksperimenlah dengan pengaturan berbeda untuk mencapai dampak visual yang diinginkan pada gambar Anda.

## FAQ

### Q1: Dapatkah saya menerapkan efek guratan pada lapisan tertentu saja?

A1: Ya, Anda dapat menargetkan lapisan tertentu dengan menyesuaikan indeks lapisan dalam kode.

### Q2: Apakah Aspose.PSD kompatibel dengan kerangka .NET terbaru?

A2: Tentu saja! Aspose.PSD dirancang untuk berintegrasi secara mulus dengan kerangka .NET terbaru.

### Q3: Bagaimana cara menyesuaikan warna guratan?

 A3: Cukup modifikasi`Color` properti dalam kode untuk mencapai warna guratan yang diinginkan.

### Q4: Apakah Aspose.PSD mendukung pemrosesan batch untuk beberapa file PSD?

A4: Ya, Anda dapat mengulang beberapa file PSD dan menerapkan efek guratan menggunakan pendekatan serupa.

### Q5: Dapatkah saya menggunakan versi uji coba sebelum membeli Aspose.PSD?

 A5: Tentu saja! Ambil itu[uji coba gratis](https://releases.aspose.com/) untuk mengeksplorasi kemampuan Aspose.PSD sebelum melakukan pembelian.