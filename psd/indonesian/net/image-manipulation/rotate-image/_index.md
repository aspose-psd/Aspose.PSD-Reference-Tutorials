---
title: Memutar Gambar di Aspose.PSD untuk .NET
linktitle: Memutar Gambar
second_title: Asumsikan.PSD .NET API
description: Pelajari cara memutar gambar dengan mudah di .NET dengan Aspose.PSD. Ikuti tutorial langkah demi langkah kami.
type: docs
weight: 15
url: /id/net/image-manipulation/rotate-image/
---
## Perkenalan

Jika Anda terjun ke dunia manipulasi gambar menggunakan .NET, Aspose.PSD adalah alat bantu Anda untuk pemrosesan gambar yang lancar dan efisien. Dalam tutorial ini, kita akan fokus pada tugas mendasar – memutar gambar menggunakan Aspose.PSD untuk .NET. Ikuti kami saat kami memecah prosesnya menjadi langkah-langkah sederhana dan dapat ditindaklanjuti.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk .NET Library: Unduh dan instal perpustakaan dari[Dokumentasi Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Direktori Dokumen Anda: Siapkan direktori tempat gambar Anda disimpan. Ganti "Direktori Dokumen Anda" di cuplikan kode dengan jalur ke direktori ini.

## Impor Namespace

Pastikan untuk menyertakan namespace yang diperlukan untuk mengakses fungsionalitas Aspose.PSD. Tambahkan baris berikut di awal proyek .NET Anda:

```csharp
using Aspose.PSD.ImageOptions;
```

## Langkah 1: Muat Gambar

```csharp
string sourceFile = dataDir + @"sample.psd";

// Muat gambar yang ada ke dalam instance kelas RasterImage
using (Image image = Image.Load(sourceFile))
{
```

## Langkah 2: Putar Gambar

```csharp
    // Putar gambar 270 derajat searah jarum jam
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Langkah 3: Simpan Gambar yang Diputar

```csharp
    // Simpan gambar yang diputar sebagai file JPEG
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

Itu saja! Hanya dengan beberapa baris kode, Anda telah berhasil memutar gambar menggunakan Aspose.PSD untuk .NET.

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi dasar-dasar memutar gambar menggunakan Aspose.PSD untuk .NET. Aspose.PSD menyediakan seperangkat alat canggih untuk manipulasi gambar, menjadikannya perpustakaan penting bagi pengembang .NET. Bereksperimenlah dengan rotasi berbeda dan jelajahi kemampuan lebih lanjut untuk menyempurnakan alur kerja pemrosesan gambar Anda.

## FAQ

### Q1: Bisakah saya memutar gambar dengan sudut khusus menggunakan Aspose.PSD?

 Ya, Aspose.PSD memungkinkan Anda menentukan sudut khusus untuk rotasi. Cukup ganti`RotateFlipType.Rotate270FlipNone` sejajar dengan sudut rotasi yang Anda inginkan.

### Q2: Apakah Aspose.PSD kompatibel dengan berbagai format gambar?

 Sangat. Aspose.PSD mendukung berbagai format gambar, termasuk PSD, JPEG, PNG, dan banyak lagi. Periksa[dokumentasi](https://reference.aspose.com/psd/net/) untuk daftar lengkapnya.

### Q3: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?

 Kunjungi[halaman lisensi sementara](https://purchase.aspose.com/temporary-license/) di situs web Aspose untuk mendapatkan lisensi sementara untuk tujuan evaluasi.

### Q4: Di mana saya dapat menemukan dukungan untuk Aspose.PSD?

 Untuk pertanyaan atau bantuan apa pun, kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) dan terhubung dengan komunitas.

### Q5: Bisakah saya membeli Aspose.PSD untuk penggunaan komersial?

 Tentu. Jelajahi[halaman pembelian](https://purchase.aspose.com/buy) untuk memperoleh lisensi yang disesuaikan dengan kebutuhan Anda.