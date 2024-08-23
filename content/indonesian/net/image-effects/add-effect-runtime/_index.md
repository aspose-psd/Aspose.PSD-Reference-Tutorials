---
title: Menambahkan Efek saat Runtime di Aspose.PSD untuk .NET
linktitle: Menambahkan Efek pada Runtime
second_title: Asumsikan.PSD .NET API
description: Jelajahi penyempurnaan gambar dinamis menggunakan Aspose.PSD untuk .NET. Tambahkan efek saat runtime dengan mudah.
type: docs
weight: 10
url: /id/net/image-effects/add-effect-runtime/
---
## Perkenalan

Meningkatkan daya tarik visual gambar merupakan persyaratan umum dalam aplikasi desain grafis dan pemrosesan gambar. Dalam tutorial ini, kita akan mempelajari cara menambahkan efek saat runtime menggunakan Aspose.PSD untuk .NET. Aspose.PSD adalah API canggih yang memungkinkan pengembang bekerja dengan file Adobe Photoshop dengan lancar. 

## Prasyarat

Sebelum kita mendalami panduan langkah demi langkah, pastikan Anda memiliki hal berikut:

- Pengetahuan dasar tentang kerangka C# dan .NET.
-  Aspose.PSD untuk .NET diinstal. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/psd/net/).

## Impor Namespace

Untuk memulai, pastikan Anda menyertakan namespace yang diperlukan dalam proyek C# Anda. Namespace ini sangat penting untuk memanfaatkan fungsionalitas yang disediakan oleh Aspose.PSD.

```csharp
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageLoadOptions;
```

## Langkah 1: Siapkan Direktori Dokumen Anda

```csharp
string dataDir = "Your Document Directory";
```

Ganti "Direktori Dokumen Anda" dengan jalur sebenarnya tempat file PSD Anda berada.

## Langkah 2: Muat Gambar PSD dengan Sumber Daya Efek

```csharp
string sourceFileName = dataDir + "ThreeRegularLayers.psd";
string exportPath = dataDir + "ThreeRegularLayersChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

Langkah ini memuat gambar PSD, memungkinkan pemuatan sumber daya efek.

## Langkah 3: Tambahkan Efek Lapisan Warna Overlay

```csharp
var effect = im.Layers[1].BlendingOptions.AddColorOverlay();
effect.Color = Color.Green;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

Di sini, kami menambahkan efek overlay warna ke lapisan kedua gambar PSD. Anda dapat menyesuaikan warna, opacity, dan mode campuran sesuai preferensi Anda.

## Langkah 4: Simpan Gambar yang Dimodifikasi

```csharp
im.Save(exportPath);
```

Terakhir, simpan gambar dengan efek yang diterapkan ke jalur ekspor yang ditentukan.

## Kesimpulan

Menambahkan efek saat runtime di Aspose.PSD untuk .NET adalah proses yang mudah. Hanya dengan beberapa baris kode, Anda dapat meningkatkan daya tarik visual gambar Anda secara dinamis. Bereksperimenlah dengan efek dan parameter yang berbeda untuk mencapai hasil yang diinginkan.

## FAQ

### Q1: Apakah Aspose.PSD kompatibel dengan kerangka .NET terbaru?

A1: Ya, Aspose.PSD diperbarui secara berkala untuk memastikan kompatibilitas dengan versi kerangka .NET terbaru.

### Q2: Dapatkah saya menerapkan banyak efek pada satu lapisan?

A2: Tentu saja! Anda dapat merangkai beberapa efek pada satu lapisan untuk menciptakan peningkatan visual yang kompleks.

### Q3: Apakah ada batasan pada jenis efek yang dapat saya tambahkan?

A3: Aspose.PSD menawarkan beragam efek, namun disarankan untuk memeriksa dokumentasi untuk detail spesifik tentang efek yang didukung.

### Q4: Bagaimana saya bisa mendapatkan lisensi sementara untuk tujuan pengujian?

 A4: Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/) untuk pengujian dan evaluasi.

### Q5: Di mana saya bisa mendapatkan dukungan tambahan dan diskusi komunitas?

 A5: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan dan diskusi.