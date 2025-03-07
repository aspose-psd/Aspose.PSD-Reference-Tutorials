---
title: Bekerja dengan Timeline di Aspose.PSD untuk .NET
linktitle: Bekerja dengan Garis Waktu
second_title: Asumsikan.PSD .NET API
description: Tingkatkan manipulasi gambar PSD dengan Aspose.PSD untuk kelas .NET Timeline. Kontrol properti bingkai, status lapisan, dan bebaskan kemungkinan kreatif dengan mudah.
weight: 16
url: /id/net/psd-file-manipulation/timeline/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bekerja dengan Timeline di Aspose.PSD untuk .NET

## Perkenalan
Dalam dunia desain grafis dan manipulasi gambar yang dinamis, kemampuan untuk mengontrol dan memanipulasi garis waktu gambar sangatlah penting. Aspose.PSD untuk .NET memberikan solusi yang kuat dengan kelas Timeline-nya. Fitur tingkat tinggi ini memungkinkan pengguna untuk membuat perubahan pada timeline PsdImage, seperti mengubah penundaan frame, mengedit status lapisan pada frame tertentu, dan banyak lagi.
## Prasyarat
Sebelum menyelami kemungkinan menarik yang ditawarkan kelas Timeline, pastikan Anda memiliki prasyarat berikut:
-  Aspose.PSD untuk Perpustakaan .NET: Pastikan Anda telah menginstal perpustakaan Aspose.PSD untuk .NET. Anda dapat mengunduhnya dari[Aspose.PSD untuk dokumentasi .NET](https://reference.aspose.com/psd/net/).
-  Direktori Dokumen dan Keluaran: Tentukan jalur untuk direktori dokumen dan keluaran Anda dalam kode. Sesuaikan`baseDir` Dan`outputDir` variabel sesuai dengan struktur proyek Anda.
Sekarang, mari kita jelajahi cara memanfaatkan kelas Timeline langkah demi langkah.
## Impor Namespace
Untuk mulai bekerja dengan kelas Timeline, impor namespace yang diperlukan dalam kode Anda:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Langkah 1: Muat Gambar PSD
Mulailah dengan memuat gambar PSD dari file sumber yang ditentukan. Pastikan jalur file sumber diatur dengan benar:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Kode Anda untuk operasi lebih lanjut ada di sini
}
```
## Langkah 2: Akses Timeline
Setelah gambar PSD dimuat, akses Timeline menggunakan kode berikut:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Langkah 3: Ubah Metode Pembuangan
Memanipulasi metode pembuangan pada frame tertentu. Dalam contoh ini, kita mengubah metode buang pada frame 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Langkah 4: Sesuaikan Penundaan Bingkai
Ubah penundaan frame tertentu. Di sini, kami mengubah penundaan frame 2 menjadi 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Langkah 5: Edit Status Lapisan
Ubah opacity 'Layer 1' pada frame tertentu. Dalam contoh ini, kami mengatur opacity ke 50 pada frame 2:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Langkah 6: Pindahkan Lapisan
Pindahkan 'Layer 1' ke sudut kiri bawah pada frame tertentu (frame 3 dalam contoh ini):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Langkah 7: Tambahkan Bingkai Baru
Tambahkan bingkai baru ke timeline:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Langkah 8: Ubah Mode Campuran
Ubah mode campuran 'Layer 1' pada frame tertentu (frame 4 dalam kasus ini):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Langkah 9: Simpan Perubahan
Terapkan perubahan kembali ke instance PsdImage dan simpan gambar PSD yang dimodifikasi:
```csharp
psdImage.Save(outputPsd);
```
## Langkah 10: Bersihkan
Terakhir, bersihkan dengan menghapus file keluaran sementara:
```csharp
File.Delete(outputPsd);
```
## Kesimpulan

Kesimpulannya, kelas Timeline di Aspose.PSD untuk .NET memberdayakan pengembang untuk memiliki kontrol terperinci atas timeline gambar PSD. Melalui serangkaian langkah sederhana, Anda dapat memanipulasi properti bingkai, status lapisan, dan banyak lagi, membuka kemungkinan kreatif.

## FAQ

### Q1: Apakah Aspose.PSD untuk .NET cocok untuk pemula?

A1: Tentu saja! Aspose.PSD untuk .NET menyediakan antarmuka yang ramah pengguna dan dokumentasi yang komprehensif, sehingga dapat diakses oleh pemula dan pengembang berpengalaman.

### Q2: Dapatkah saya menerapkan perubahan garis waktu pada gambar GIF?

A2: Kelas Timeline dirancang khusus untuk gambar PSD. Untuk manipulasi GIF, lihat Aspose.GIF untuk .NET.

### Q3: Di mana saya dapat menemukan dukungan tambahan atau mendiskusikan masalah?

 A3: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan komunitas dan diskusi masalah.

### Q4: Bagaimana cara mendapatkan lisensi sementara Aspose.PSD untuk .NET?

 A4: Dapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Apa manfaat utama menggunakan Aspose.PSD untuk .NET?

A5: Aspose.PSD untuk .NET menawarkan kemampuan pemrosesan gambar tingkat lanjut, manipulasi file PSD, dan rendering performa tinggi.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
