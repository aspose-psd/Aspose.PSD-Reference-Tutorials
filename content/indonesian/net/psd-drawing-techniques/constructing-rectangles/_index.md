---
title: Membangun Persegi Panjang di Aspose.PSD untuk .NET
linktitle: Membangun Persegi Panjang
second_title: Asumsikan.PSD .NET API
description: Jelajahi seni menggambar persegi panjang di .NET dengan Aspose.PSD. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar. Tingkatkan permainan manipulasi gambar Anda dengan mudah.
type: docs
weight: 15
url: /id/net/psd-drawing-techniques/constructing-rectangles/
---
## Perkenalan

Dalam ranah dinamis pengembangan .NET, Aspose.PSD menonjol sebagai alat yang ampuh untuk menangani manipulasi gambar. Tutorial ini berfokus pada tugas mendasar: membuat persegi panjang menggunakan Aspose.PSD untuk .NET. Baik Anda seorang pengembang berpengalaman atau baru memulai, panduan langkah demi langkah ini akan memandu Anda melalui prosesnya, memastikan Anda memahami setiap konsep secara menyeluruh.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Pengaturan Lingkungan: Miliki lingkungan pengembangan .NET yang berfungsi dengan Aspose.PSD terintegrasi. Jika Anda belum melakukannya, lihat[dokumentasi](https://reference.aspose.com/psd/net/) untuk petunjuk pemasangan.

-  Unduh Aspose.PSD: Pastikan Anda telah mengunduh perpustakaan Aspose.PSD dari[tautan unduhan](https://releases.aspose.com/psd/net/).

-  Dapatkan Lisensi: Jika Anda menggunakan Aspose.PSD di lingkungan produksi, pastikan Anda memiliki lisensi yang valid. Anda bisa mendapatkannya[Di Sini](https://purchase.aspose.com/buy) atau gunakan a[izin sementara](https://purchase.aspose.com/temporary-license/) untuk pengujian.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan ke proyek .NET Anda. Namespace ini menyediakan akses ke fungsionalitas Aspose.PSD yang diperlukan untuk menggambar persegi panjang.

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

## Langkah 1: Inisialisasi Direktori Dokumen

Tetapkan jalur ke direktori dokumen Anda tempat gambar keluaran akan disimpan.

```csharp
string dataDir = "Your Document Directory";
```

## Langkah 2: Menggambar Persegi Panjang

Sekarang, mari selami proses menggambar persegi panjang menggunakan Aspose.PSD.

### Langkah 2.1: Buat Instance BmpOptions

```csharp
string outpath = dataDir + "Rectangle.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

### Langkah 2.2: Buat Instance Gambar

```csharp
using (Image image = new PsdImage(100, 100))
{
    // Langkah 2.3: Inisialisasi Kelas Grafik dan Hapus Permukaan Grafik
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);

    // Langkah 2.4: Gambar Persegi Panjang
    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Langkah 2.5: Ekspor Gambar ke Format File BMP
    image.Save(outpath, saveOptions);
}
```

## Kesimpulan

Selamat! Anda telah berhasil membuat persegi panjang menggunakan Aspose.PSD untuk .NET. Tutorial ini membekali Anda dengan pengetahuan untuk mengintegrasikan manipulasi gambar dengan mulus ke dalam aplikasi .NET Anda.

## FAQ

### Q1: Apakah Aspose.PSD kompatibel dengan semua lingkungan .NET?

A1: Ya, Aspose.PSD dirancang untuk bekerja dengan berbagai lingkungan .NET, memastikan kompatibilitas di berbagai platform.

### Q2: Dapatkah saya menggunakan Aspose.PSD untuk proyek komersial tanpa lisensi?

 A2: Tidak, diperlukan lisensi yang valid untuk penggunaan komersial. Dapatkan lisensi Anda[Di Sini](https://purchase.aspose.com/buy).

### Q3: Bagaimana cara mencari bantuan atau berbagi pengalaman saya dengan Aspose.PSD?

 A3: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk berhubungan dengan masyarakat dan mendapatkan bantuan.

### Q4: Apa manfaat yang ditawarkan 32 bit per piksel (Bpp) di BmpOptions?

A4: Menggunakan 32 Bpp memungkinkan representasi warna yang lebih kaya, memungkinkan gambar yang lebih detail dan hidup.

### Q5: Apakah ada uji coba gratis yang tersedia untuk Aspose.PSD?

 A5: Ya, Anda dapat menjelajahi Aspose.PSD dengan uji coba gratis. Unduh itu[Di Sini](https://releases.aspose.com/).