---
title: Memotong Gambar dengan Pergeseran di Aspose.PSD untuk .NET
linktitle: Memotong Gambar secara Bergeser
second_title: Asumsikan.PSD .NET API
description: Pelajari cara memotong gambar dengan mudah menggunakan Aspose.PSD untuk .NET. Ikuti panduan langkah demi langkah kami untuk penyesuaian gambar yang tepat.
type: docs
weight: 12
url: /id/net/image-manipulation/crop-image-shifts/
---
## Perkenalan

Di bidang pengembangan .NET, Aspose.PSD menonjol sebagai perangkat yang ampuh untuk tugas pemrosesan gambar. Salah satu fitur utamanya adalah kemampuan memotong gambar dengan presisi, berkat fungsi 'Cropping by Shifts'. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses memotong gambar dengan lancar menggunakan Aspose.PSD untuk .NET.

## Prasyarat

Sebelum mempelajari tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk .NET Library: Pastikan Anda telah menginstal perpustakaan. Jika belum, Anda dapat mendownloadnya dari[halaman rilis](https://releases.aspose.com/psd/net/).

- Lingkungan .NET: Pastikan Anda telah menyiapkan lingkungan pengembangan .NET di mesin Anda.

- Contoh Gambar: Siapkan contoh gambar dalam format PSD yang ingin Anda gunakan.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan ke proyek .NET Anda. Namespace ini menyediakan akses ke kelas Aspose.PSD dan metode yang diperlukan untuk pemotongan gambar.

```csharp
using Aspose.PSD.ImageOptions;
```

## Langkah 1: Tentukan Direktori Dokumen Anda

Tetapkan jalur ke direktori dokumen Anda tempat file sumber dan tujuan akan ditempatkan.

```csharp
string dataDir = "Your Document Directory";
```

## Langkah 2: Muat Gambar Sumber

Muat gambar PSD yang ingin Anda potong. Pastikan untuk mengganti "sample.psd" dengan nama file sumber Anda.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Langkah 3: Cache Data Gambar untuk Performa Lebih Baik

Sebelum memotong, disarankan untuk menyimpan data gambar dalam cache untuk meningkatkan kinerja.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Langkah 4: Tentukan Nilai Pergeseran untuk Pemangkasan

Tentukan nilai pergeseran sisi kiri, kanan, atas, dan bawah gambar. Sesuaikan nilai-nilai ini berdasarkan kebutuhan pemangkasan Anda.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Langkah 5: Terapkan Pemangkasan dan Simpan Hasil

 Memanfaatkan`Crop` metode untuk menerapkan pergeseran yang ditentukan dan menyimpan gambar yang dipotong ke file tujuan.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara memotong gambar secara bergiliran menggunakan Aspose.PSD untuk .NET. Fungsionalitas canggih ini memberi Anda presisi dan kontrol yang diperlukan untuk berbagai tugas pemrosesan gambar.

## FAQ

### Q1: Bisakah saya memotong gambar dengan format berbeda, bukan hanya PSD?

A1: Ya, Aspose.PSD mendukung berbagai format gambar, memungkinkan Anda memotong gambar dalam format seperti JPEG, PNG, dan lainnya.

### Q2: Apakah ada versi uji coba yang tersedia sebelum membeli Aspose.PSD untuk .NET?

 A2: Tentu saja! Anda dapat menjelajahi perangkat ini dengan uji coba gratis yang tersedia[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana cara mendapatkan lisensi sementara Aspose.PSD untuk .NET?

 A3: Anda dapat memperoleh lisensi sementara untuk tujuan pengujian.[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q4: Di mana saya dapat menemukan dukungan dan diskusi tambahan terkait Aspose.PSD?

 A4: Kunjungi[Forum Asumsikan.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan dan diskusi yang menarik.

### Q5: Bisakah saya membeli Aspose.PSD untuk .NET langsung dari situs web?

 A5: Ya, Anda dapat membeli perpustakaan dengan aman dari[halaman pembelian](https://purchase.aspose.com/buy).
