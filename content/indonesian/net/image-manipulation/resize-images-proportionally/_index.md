---
title: Mengubah Ukuran Gambar Secara Proporsional di Aspose.PSD untuk .NET
linktitle: Mengubah Ukuran Gambar Secara Proporsional
second_title: Asumsikan.PSD .NET API
description: Jelajahi pengubahan ukuran gambar tanpa hambatan dengan Aspose.PSD untuk .NET. Unduh perpustakaan, ikuti tutorial kami, dan tingkatkan kemampuan pemrosesan gambar Anda.
type: docs
weight: 14
url: /id/net/image-manipulation/resize-images-proportionally/
---
Dalam bidang manipulasi gambar, Aspose.PSD untuk .NET menonjol sebagai perangkat canggih yang memberikan pengembang kemampuan untuk mengubah ukuran gambar secara proporsional dengan mudah. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses mengubah ukuran gambar menggunakan Aspose.PSD untuk .NET, memastikan gambar Anda mempertahankan proporsinya dengan sempurna.

## Perkenalan

Mengubah ukuran gambar secara proporsional adalah tugas umum di banyak aplikasi, dan Aspose.PSD untuk .NET menyederhanakan proses ini bagi pengembang. Baik Anda sedang mengerjakan aplikasi web, perangkat lunak desktop, atau aplikasi seluler, memahami cara mengubah ukuran gambar sambil mempertahankan rasio aspeknya sangat penting untuk menjaga daya tarik visual dan konsistensi.

## Prasyarat

Sebelum mendalami keajaiban pengubahan ukuran dengan Aspose.PSD untuk .NET, pastikan Anda memiliki prasyarat berikut:

1.  Aspose.PSD untuk Perpustakaan .NET: Pastikan Anda telah menginstal perpustakaan Aspose.PSD untuk .NET. Anda dapat mengunduhnya dari[Aspose.PSD untuk rilis .NET](https://releases.aspose.com/psd/net/) halaman.

2. Direktori Dokumen: Buat direktori untuk menyimpan dokumen Anda, dan ganti "Direktori Dokumen Anda" dalam kode yang disediakan dengan jalur sebenarnya ke direktori ini.

Sekarang setelah Anda menyiapkan prasyaratnya, mari beralih ke panduan langkah demi langkah.

## Impor Namespace

```csharp
using Aspose.PSD.ImageOptions;
```

Impor namespace yang diperlukan untuk mengakses kelas dan metode yang diperlukan.

## Langkah 1: Muat Gambar

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Muat gambar yang ada ke dalam instance kelas RasterImage
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Langkah selanjutnya ada di sini
}
```

 Muat gambar sumber menggunakan`Image.Load` metode.

## Langkah 2: Tentukan Lebar dan Tinggi

```csharp
// Menentukan lebar dan tinggi
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Tentukan lebar dan tinggi baru untuk gambar yang diubah ukurannya. Dalam contoh ini, lebar dan tinggi dibelah dua, tetapi Anda dapat menyesuaikan nilai ini berdasarkan kebutuhan Anda.

## Langkah 3: Simpan Gambar yang Diubah Ukurannya

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Simpan gambar yang diubah ukurannya menggunakan`Save` metode dengan opsi yang ditentukan. Dalam hal ini, kami menyimpannya sebagai file PNG.

## Kesimpulan

Mengubah ukuran gambar secara proporsional di Aspose.PSD untuk .NET adalah proses mudah yang menambah nilai pada alur kerja pemrosesan gambar Anda. Panduan ini telah membekali Anda dengan pengetahuan untuk mengintegrasikan fungsi ini ke dalam aplikasi Anda dengan lancar.

## FAQ

### Q1: Dapatkah saya mengubah ukuran gambar ke dimensi tertentu?

A1: Ya, Anda dapat menyesuaikan lebar dan tinggi baru sesuai dengan kebutuhan Anda dalam kode.

### Q2: Apakah Aspose.PSD untuk .NET cocok untuk mengubah ukuran gambar batch?

A2: Tentu saja! Anda dapat memasukkan langkah-langkah ini ke dalam satu lingkaran untuk memproses banyak gambar secara batch.

### Q3: Apakah ada fitur manipulasi gambar lainnya di Aspose.PSD untuk .NET?

A3: Ya, Aspose.PSD untuk .NET menawarkan berbagai fitur, termasuk memotong, memutar, dan menerapkan filter pada gambar.

### Q4: Apakah ada uji coba gratis yang tersedia untuk Aspose.PSD untuk .NET?

 A4: Ya, Anda dapat menjelajahi kemampuan Aspose.PSD untuk .NET dengan uji coba gratis. Mengunjungi[Di Sini](https://releases.aspose.com/) untuk memulai.

### Q5: Di mana saya dapat menemukan dukungan untuk Aspose.PSD untuk .NET?

 A5: Kunjungi[Aspose.PSD untuk forum .NET](https://forum.aspose.com/c/psd/34) untuk dukungan dan diskusi komunitas.