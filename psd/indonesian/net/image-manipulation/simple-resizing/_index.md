---
title: Mengubah Ukuran Gambar Secara Sederhana di Aspose.PSD untuk .NET
linktitle: Mengubah Ukuran Gambar Secara Sederhana
second_title: Asumsikan.PSD .NET API
description: Ubah ukuran gambar master dengan Aspose.PSD untuk .NET. Efisien, mulus, dan kuat. Tingkatkan proyek .NET Anda dengan mudah.
weight: 17
url: /id/net/image-manipulation/simple-resizing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengubah Ukuran Gambar Secara Sederhana di Aspose.PSD untuk .NET

## Perkenalan

Dalam dunia dinamis pengembangan .NET, memanipulasi gambar adalah kebutuhan umum. Aspose.PSD untuk .NET hadir untuk menyelamatkan dengan kemampuannya yang kuat, memberikan pengalaman yang mulus untuk mengubah ukuran gambar. Dalam tutorial ini, kita akan mempelajari proses sederhana namun penting dalam mengubah ukuran gambar menggunakan Aspose.PSD untuk .NET. Bersiaplah saat kami memulai perjalanan untuk meningkatkan keterampilan pemrosesan gambar Anda.

## Prasyarat

Sebelum kita masuk ke tutorialnya, pastikan Anda sudah menyiapkan segalanya untuk pengalaman yang lancar:

## Impor Namespace

Pastikan Anda telah mengimpor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.PSD untuk .NET:

```csharp
using Aspose.PSD.ImageOptions;
```

Sekarang, mari kita uraikan proses mengubah ukuran gambar menjadi beberapa langkah:

## Langkah 1: Atur Direktori Dokumen Anda

Mulailah dengan mengatur jalur ke direktori dokumen Anda:

```csharp
string dataDir = "Your Document Directory";
```

## Langkah 2: Muat Gambar

Muat gambar yang ada ke dalam instance kelas RasterImage:

```csharp
string sourceFile = dataDir + @"sample.psd";
using (Image image = Image.Load(sourceFile))
{
    // Kode Anda di sini
}
```

## Langkah 3: Ubah ukuran Gambar

 Mengubah ukuran gambar semudah memanggil`Resize` metode pada objek gambar:

```csharp
image.Resize(300, 300);
```

## Langkah 4: Simpan Gambar yang Diubah Ukurannya

Simpan gambar yang diubah ukurannya dengan format dan opsi pilihan Anda. Dalam contoh ini, kami menyimpannya sebagai JPEG:

```csharp
string destName = dataDir + @"SimpleResizing_out.jpg";
image.Save(destName, new JpegOptions());
```

Dan itu saja! Anda berhasil mengubah ukuran gambar menggunakan Aspose.PSD untuk .NET.

## Kesimpulan

Menguasai pengubahan ukuran gambar adalah keterampilan mendasar dalam perangkat pengembang .NET mana pun. Dengan Aspose.PSD untuk .NET, prosesnya tidak hanya menjadi efisien tetapi juga menyenangkan. Sekarang, berbekal pengetahuan ini, maju dan tingkatkan kemampuan manipulasi gambar Anda di proyek .NET Anda.

## FAQ

### Q1: Bisakah saya mengubah ukuran gambar ke rasio aspek tertentu menggunakan Aspose.PSD untuk .NET?

A1: Ya, Anda dapat mempertahankan rasio aspek tertentu sambil mengubah ukuran gambar dengan menyesuaikan lebar atau tinggi.

### Q2: Apakah Aspose.PSD untuk .NET mendukung format gambar lain selain JPEG?

A2: Tentu saja! Aspose.PSD untuk .NET mendukung berbagai format gambar, termasuk PNG, GIF, BMP, dan banyak lagi.

### Q3: Apakah lisensi sementara tersedia untuk Aspose.PSD untuk .NET?

A3: Ya, Anda bisa mendapatkan lisensi sementara Aspose.PSD untuk .NET guna mengevaluasi kemampuannya sebelum melakukan pembelian.

### Q4: Di mana saya dapat menemukan dokumentasi komprehensif untuk Aspose.PSD untuk .NET?

 A4: Jelajahi dokumentasi terperinci di[Aspose.PSD untuk Dokumentasi .NET](https://reference.aspose.com/psd/net/).

### Q5: Bagaimana saya bisa mendapatkan dukungan atau terhubung dengan komunitas Aspose.PSD untuk .NET?

 A5: Kunjungi[Aspose.PSD untuk Forum .NET](https://forum.aspose.com/c/psd/34) untuk dukungan dan diskusi komunitas.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
