---
title: Mendukung Efek Gradient Overlay di Aspose.PSD untuk .NET
linktitle: Mendukung Efek Gradient Overlay
second_title: Asumsikan.PSD .NET API
description: Tingkatkan grafis di .NET dengan Aspose.PSD. Tutorial ini memandu Anda dalam mendukung Efek Gradient Overlay.
type: docs
weight: 18
url: /id/net/image-manipulation/supporting-gradient-overlay-effect/
---
## Perkenalan

Selamat datang di tutorial komprehensif tentang mendukung Efek Gradient Overlay di Aspose.PSD untuk .NET! Jika Anda ingin meningkatkan kemampuan grafis aplikasi .NET Anda, panduan langkah demi langkah ini siap membantu Anda. Kami akan mempelajari seluk-beluk membuat dan mengedit Efek Gradient Overlay di lapisan menggunakan Aspose.PSD, perpustakaan canggih yang menyederhanakan pemrosesan gambar.

## Prasyarat

Sebelum kita memulai perjalanan ini, pastikan Anda memiliki hal berikut:

- Pemahaman dasar tentang pemrograman C# dan .NET.
-  Aspose.PSD untuk .NET diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/psd/net/).
- Lingkungan pengembangan yang diatur dengan IDE pilihan Anda.

## Impor Namespace

Untuk memulai, mari impor namespace yang diperlukan dalam kode C# Anda:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
```

Sekarang setelah kita membahas dasar-dasarnya, mari kita uraikan setiap langkah secara mendetail:

## Langkah 1: Muat Gambar PSD

```csharp
// Jalur ke direktori dokumen.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFilePath = Path.Combine(SourceDir, "psdnet256.psd");
string outputFilePath = Path.Combine(OutputDir, "psdnet256.psd_output.psd");

using (var psdImage = (PsdImage)Image.Load(sourceFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Kode untuk langkah selanjutnya ada di sini...
}
```

## Langkah 2: Akses Opsi Pencampuran Lapisan

```csharp
BlendingOptions layerBlendOptions = psdImage.Layers[1].BlendingOptions;
```

## Langkah 3: Temukan atau Buat Efek Gradient Overlay

```csharp
GradientOverlayEffect gradientOverlayEffect = null;

foreach (ILayerEffect effect in layerBlendOptions.Effects)
{
    gradientOverlayEffect = effect as GradientOverlayEffect;
    if (gradientOverlayEffect != null)
    {
        break;
    }
}

if (gradientOverlayEffect == null)
{
    gradientOverlayEffect = layerBlendOptions.AddGradientOverlay();
}
```

## Langkah 4: Konfigurasikan Efek Gradient Overlay

```csharp
gradientOverlayEffect.Opacity = 200;
gradientOverlayEffect.BlendMode = BlendMode.Hue;

GradientFillSettings settings = gradientOverlayEffect.Settings;

settings.ColorPoints = new IGradientColorPoint[]
{
    new GradientColorPoint(Color.GreenYellow, 0, 50),
    new GradientColorPoint(Color.BlueViolet, 4096, 50),
};

settings.Angle = 80;
settings.Scale = 150;
settings.GradientType = GradientType.Linear;

settings.TransparencyPoints[0].Opacity = 100;
settings.TransparencyPoints[1].Opacity = 100;
```

## Langkah 5: Simpan Gambar yang Dimodifikasi

```csharp
psdImage.Save(outputFilePath);
```

Itu dia! Anda telah berhasil menambahkan Efek Gradient Overlay ke lapisan menggunakan Aspose.PSD untuk .NET.

## Kesimpulan

Dalam tutorial ini, kami menjelajahi proses mendukung Efek Gradient Overlay di Aspose.PSD untuk .NET. Dengan mengikuti panduan langkah demi langkah, Anda dapat dengan mudah mengintegrasikan fitur ini ke dalam aplikasi .NET Anda, sehingga meningkatkan daya tarik visual gambar Anda.

## FAQ

### Q1: Apakah Aspose.PSD kompatibel dengan semua versi .NET?

A1: Aspose.PSD untuk .NET kompatibel dengan .NET Framework dan .NET Core.

### Q2: Dapatkah saya menerapkan banyak efek pada satu lapisan?

A2: Ya, Anda dapat menerapkan berbagai efek, termasuk Gradient Overlay, ke satu layer.

### Q3: Di mana saya dapat menemukan contoh dan dokumentasi lainnya?

 A3: Kunjungi[dokumentasi](https://reference.aspose.com/psd/net/) untuk contoh dan pedoman rinci.

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda dapat mengakses uji coba gratis.[Di Sini](https://releases.aspose.com/).

### Q5: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.PSD?

 A5: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan masyarakat.