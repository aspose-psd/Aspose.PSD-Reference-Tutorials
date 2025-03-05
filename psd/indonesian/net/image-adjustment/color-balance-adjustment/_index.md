---
title: Menerapkan Penyesuaian Keseimbangan Warna di Aspose.PSD untuk .NET
linktitle: Menerapkan Penyesuaian Keseimbangan Warna
second_title: Asumsikan.PSD .NET API
description: Sempurnakan warna gambar PSD dengan mudah dengan Aspose.PSD untuk fitur Penyesuaian Keseimbangan Warna .NET. Ikuti panduan langkah demi langkah kami untuk hasil yang menakjubkan.
type: docs
weight: 14
url: /id/net/image-adjustment/color-balance-adjustment/
---
## Perkenalan

Selamat datang di panduan komprehensif tentang penerapan Penyesuaian Keseimbangan Warna di Aspose.PSD untuk .NET! Aspose.PSD adalah perpustakaan .NET yang kuat yang memungkinkan pengembang bekerja dengan file PSD secara efisien. Dalam tutorial ini, kami akan fokus pada fitur Penyesuaian Keseimbangan Warna, memungkinkan Anda meningkatkan keseimbangan warna gambar PSD Anda dengan mudah.

## Prasyarat

Sebelum kita masuk ke tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk .NET Library: Unduh dan instal perpustakaan dari[Situs web Aspose.PSD](https://releases.aspose.com/psd/net/).
- Lingkungan Pengembangan: Pastikan Anda memiliki lingkungan pengembangan .NET yang berfungsi di mesin Anda.
- File PSD: Siapkan file PSD yang ingin Anda terapkan Penyesuaian Keseimbangan Warna.

## Impor Namespace

Dalam proyek .NET Anda, sertakan namespace yang diperlukan untuk menggunakan fitur Aspose.PSD. Tambahkan baris berikut ke kode Anda:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Sekarang, mari kita bagi proses Penyesuaian Keseimbangan Warna menjadi beberapa langkah:

## Langkah 1: Muat File PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Kode untuk Penyesuaian Keseimbangan Warna akan ditambahkan pada langkah-langkah berikut.
}
```

## Langkah 2: Akses dan Sesuaikan Keseimbangan Warna

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Langkah 3: Simpan Gambar yang Disesuaikan

```csharp
im.Save(outputPath);
```

Sekarang, Anda telah berhasil menerapkan Penyesuaian Keseimbangan Warna pada file PSD Anda menggunakan Aspose.PSD untuk .NET!

## Kesimpulan

Selamat! Anda telah mempelajari cara meningkatkan keseimbangan warna gambar PSD Anda dengan Aspose.PSD untuk .NET. Bereksperimenlah dengan nilai keseimbangan yang berbeda untuk mencapai efek visual yang diinginkan.

## FAQ

### Q1: Bisakah saya menerapkan Penyesuaian Keseimbangan Warna ke beberapa lapisan?

A1: Ya, Anda dapat mengulangi semua lapisan di file PSD Anda dan menyesuaikan keseimbangan warna sesuai kebutuhan.

### Q2: Apakah Aspose.PSD untuk .NET cocok untuk pemrosesan batch file PSD?

A2: Tentu saja! Aspose.PSD menyediakan kemampuan pemrosesan batch yang efisien untuk file PSD.

### Q3: Bagaimana saya bisa mendapatkan lisensi sementara Aspose.PSD untuk .NET?

 A3: Kunjungi[Lisensi Sementara Aspose.PSD](https://purchase.aspose.com/temporary-license/) untuk izin sementara.

### Q4: Di mana saya dapat menemukan contoh dan dokumentasi lainnya?

 A4: Jelajahi[Dokumentasi Aspose.PSD](https://reference.aspose.com/psd/net/) untuk contoh dan panduan rinci.

### Q5: Opsi dukungan apa yang tersedia untuk Aspose.PSD untuk .NET?

 A5: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan dan diskusi komunitas.
