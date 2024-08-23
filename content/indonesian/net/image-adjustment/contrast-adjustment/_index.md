---
title: Menerapkan Penyesuaian Kontras di Aspose.PSD untuk .NET
linktitle: Menerapkan Penyesuaian Kontras
second_title: Asumsikan.PSD .NET API
description: Pelajari cara menerapkan penyesuaian kontras di Aspose.PSD untuk .NET dengan panduan langkah demi langkah ini.
type: docs
weight: 11
url: /id/net/image-adjustment/contrast-adjustment/
---
## Perkenalan

Selamat datang di panduan komprehensif tentang penerapan penyesuaian kontras di Aspose.PSD untuk .NET! Dalam tutorial ini, kita akan menjelajahi proses meningkatkan kontras gambar menggunakan Aspose.PSD, pustaka pencitraan .NET yang canggih. Di akhir panduan ini, Anda akan memiliki pemahaman yang kuat tentang cara menerapkan penyesuaian kontras pada gambar Anda dengan mulus.

## Prasyarat

Sebelum kita mendalami proses langkah demi langkah, pastikan Anda memiliki prasyarat berikut:

1.  Aspose.PSD untuk .NET Library: Unduh dan instal Aspose.PSD untuk .NET Library. Anda dapat menemukan tautan unduhan[Di Sini](https://releases.aspose.com/psd/net/).

2. Direktori Dokumen: Siapkan direktori tempat file sumber dan tujuan Anda akan disimpan. Ganti "Direktori Dokumen Anda" pada kode yang disediakan dengan jalur ke direktori ini.

Sekarang kita sudah menyiapkan prasyaratnya, mari kita lanjutkan ke penerapannya.

## Impor Namespace

Pada langkah ini, kita akan mengimpor namespace yang diperlukan untuk mengakses fungsionalitas yang disediakan oleh perpustakaan Aspose.PSD.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Langkah 1: Muat Gambar

Muat gambar sumber ke dalam instance`RasterImage` kelas.

```csharp
//ExStart: LoadImage
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // Lanjutkan ke langkah berikutnya...
}
//ExEnd: LoadImage
```

## Langkah 2: Sesuaikan Kontras

Pada langkah ini, kita akan menyesuaikan kontras gambar yang dimuat.

```csharp
//ExStart: Sesuaikan Kontras
rasterImage.AdjustContrast(50); // Sesuaikan kontras sebesar 50%
// Lanjutkan ke langkah berikutnya...
//ExEnd: Sesuaikan Kontras
```

## Langkah 3: Buat Opsi TIFF

 Buat sebuah contoh dari`TiffOptions` untuk gambar yang dihasilkan, atur berbagai properti, dan simpan gambar dalam format TIFF.

```csharp
//ExStart:BuatTiffOptions
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd:BuatTiffOptions
```

Selamat! Anda telah berhasil menerapkan penyesuaian kontras menggunakan Aspose.PSD untuk .NET.

## Kesimpulan

Dalam tutorial ini, kami menjelajahi proses meningkatkan kontras gambar dengan Aspose.PSD untuk .NET. Pustaka menyediakan cara mudah untuk memanipulasi properti gambar, memungkinkan pengembang membuat gambar yang menarik secara visual dengan mudah.

## FAQ

### Q1: Apakah Aspose.PSD untuk .NET cocok untuk pemula?

A1: Aspose.PSD untuk .NET dirancang agar ramah pengembang, sehingga cocok untuk pemula dan pengembang berpengalaman.

### Q2: Dapatkah saya menggunakan Aspose.PSD untuk proyek komersial?

 A2: Ya, Aspose.PSD untuk .NET dapat digunakan dalam proyek komersial. Untuk detail lisensi, kunjungi[Di Sini](https://purchase.aspose.com/buy).

### Q3: Apakah tersedia uji coba gratis?

 A3: Ya, Anda dapat menjelajahi uji coba gratis Aspose.PSD untuk .NET[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dukungan untuk Aspose.PSD untuk .NET?

 A4: Kunjungi forum dukungan Aspose.PSD untuk .NET[Di Sini](https://forum.aspose.com/c/psd/34) untuk bantuan.

### Q5: Bagaimana cara mendapatkan lisensi sementara?

 A5: Jika diperlukan, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).