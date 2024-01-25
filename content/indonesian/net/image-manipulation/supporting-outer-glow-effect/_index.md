---
title: Mendukung Efek Cahaya Luar di Aspose.PSD untuk .NET
linktitle: Mendukung Efek Cahaya Luar
second_title: Asumsikan.PSD .NET API
description: Jelajahi kekuatan Efek Cahaya Luar di Aspose.PSD untuk .NET. Tingkatkan desain gambar Anda dengan tutorial langkah demi langkah ini.
type: docs
weight: 16
url: /id/net/image-manipulation/supporting-outer-glow-effect/
---
## Perkenalan

Selamat datang di panduan langkah demi langkah kami dalam mendukung Efek Cahaya Luar di Aspose.PSD untuk .NET. Aspose.PSD adalah perpustakaan canggih yang memungkinkan manipulasi file PSD dengan lancar dalam aplikasi .NET. Dalam tutorial ini, kita akan mengeksplorasi penerapan Efek Cahaya Luar dan memberikan panduan mendetail untuk mengintegrasikannya ke dalam proyek Anda.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk .NET Library: Unduh perpustakaan dari[Dokumentasi Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET pilihan Anda.

- Direktori Dokumen dan Keluaran: Tentukan direktori dokumen dan keluaran Anda dalam kode yang disediakan.

## Impor Namespace

Di bagian ini, kita akan mengimpor namespace yang diperlukan untuk memulai implementasi Outer Glow Effect. Ikuti langkah ini:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

Sekarang, mari kita bagi contoh yang diberikan menjadi beberapa langkah untuk mencapai Efek Cahaya Luar.

## Langkah 1: Tetapkan Jalur Dokumen dan Keluaran

```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```

## Langkah 2: Muat Gambar PSD

```csharp
string src = Path.Combine(baseDir, "GreenLayer.psd");
using (var image = (PsdImage)Image.Load(src))
{
    // Langkah-langkah implementasi akan ditambahkan di bawah ini.
}
```

## Langkah 3: Tambahkan Efek Cahaya Luar

```csharp
OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
```

## Langkah 4: Konfigurasikan Parameter Cahaya Luar

```csharp
effect.Range = 10;
effect.Spread = 10;
((IColorFillSettings)effect.FillColor).Color = Color.Red;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

## Langkah 5: Simpan Gambar

```csharp
string outputPng = Path.Combine(outputDir, "output261.png");
image.Save(outputPng, new PngOptions());
```

## Langkah 6: Bersihkan

```csharp
File.Delete(outputPng);
```

## Langkah 7: Tampilkan Pesan Sukses

```csharp
Console.WriteLine("SupportOfOuterGlowEffect executed successfully");
```

## Kesimpulan

Selamat! Anda telah berhasil mengimplementasikan Efek Outer Glow menggunakan Aspose.PSD untuk .NET. Fitur canggih ini meningkatkan daya tarik visual gambar Anda, memberikan sentuhan unik pada desain Anda.

## FAQ

### Q1: Apakah Aspose.PSD kompatibel dengan semua kerangka .NET?

A1: Ya, Aspose.PSD mendukung berbagai kerangka .NET, memastikan kompatibilitas dengan berbagai lingkungan pengembangan.

### Q2: Di mana saya dapat menemukan dokumentasi tambahan untuk Aspose.PSD?

 A2: Lihat[Dokumentasi Aspose.PSD .NET](https://reference.aspose.com/psd/net/) untuk informasi lengkap dan contoh.

### Q3: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?

 A3: Kunjungi[Lisensi Sementara Aspose.PSD](https://purchase.aspose.com/temporary-license/) untuk opsi lisensi sementara.

### Q4: Dukungan apa yang tersedia untuk pengguna Aspose.PSD?

 A4: Bergabunglah dengan[Forum Asumsikan.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan dan diskusi komunitas.

### Q5: Dapatkah saya membeli Aspose.PSD untuk .NET?

 A5: Ya, jelajahi opsi lisensi dan lakukan pembelian[Di Sini](https://purchase.aspose.com/buy).