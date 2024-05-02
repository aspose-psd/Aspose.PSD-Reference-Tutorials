---
title: Menerapkan Penyesuaian Gamma di Aspose.PSD untuk .NET
linktitle: Menerapkan Penyesuaian Gamma
second_title: Asumsikan.PSD .NET API
description: Jelajahi kekuatan Aspose.PSD untuk .NET dengan panduan langkah demi langkah kami dalam menerapkan Penyesuaian Gamma. Sempurnakan kecerahan dan kontras gambar dengan mudah.
type: docs
weight: 12
url: /id/net/image-adjustment/gamma-adjustment/
---
## Perkenalan

Selamat datang di panduan komprehensif tentang penerapan Penyesuaian Gamma di Aspose.PSD untuk .NET! Penyesuaian gamma adalah teknik pemrosesan gambar penting yang memungkinkan Anda menyempurnakan kecerahan dan kontras gambar. Dalam tutorial ini, kami akan memandu Anda melalui proses menggunakan perpustakaan Aspose.PSD yang kuat untuk .NET.

## Prasyarat

Sebelum mendalami penerapannya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk .NET Library: Pastikan Anda telah menginstal perpustakaan Aspose.PSD untuk .NET. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/psd/net/).

- .NET Framework: Tutorial ini mengasumsikan Anda memiliki pemahaman dasar tentang pengembangan .NET dan telah menginstal .NET Framework.

- Lingkungan Pengembangan Terpadu (IDE): Pilih IDE pilihan Anda untuk pengembangan .NET, seperti Visual Studio.

## Impor Namespace

Di proyek .NET Anda, mulailah dengan mengimpor namespace yang diperlukan untuk bekerja dengan Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Langkah 1: Siapkan Proyek Anda

Buat proyek .NET baru di IDE pilihan Anda. Pastikan untuk menambahkan referensi ke perpustakaan Aspose.PSD.

## Langkah 2: Tentukan Direktori Dokumen

```csharp
string dataDir = "Your Document Directory";
```

## Langkah 3: Muat Gambar

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Langkah-langkah tambahan akan dilakukan di dalam blok penggunaan ini.
}
```

## Langkah 4: Transmisikan ke RasterImage dan Data Cache

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Langkah 5: Sesuaikan Gamma

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Langkah 6: Buat TiffOptions dan Simpan

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil menerapkan Penyesuaian Gamma menggunakan Aspose.PSD untuk .NET. Pustaka yang kuat ini memberikan kemampuan yang kuat untuk pemrosesan gambar, menjadikannya alat yang berharga bagi pengembang .NET.

## FAQ

### Q1: Di mana saya dapat menemukan dokumentasi Aspose.PSD?

 A1: Anda dapat merujuk ke dokumentasi[Di Sini](https://reference.aspose.com/psd/net/).

### Q2: Bagaimana cara mengunduh Aspose.PSD untuk .NET?

 A2: Anda dapat mengunduh perpustakaan[Di Sini](https://releases.aspose.com/psd/net/).

### Q3: Apakah tersedia uji coba gratis?

 A3: Ya, Anda bisa mendapatkan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya bisa mendapatkan dukungan untuk Aspose.PSD?

 A4: Anda dapat mengunjungi forum dukungan[Di Sini](https://forum.aspose.com/c/psd/34).

### Q5: Apakah saya memerlukan lisensi sementara?

 A5: Jika diperlukan, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).