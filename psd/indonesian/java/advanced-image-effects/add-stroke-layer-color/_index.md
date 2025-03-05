---
title: Tambahkan Warna Layer Stroke di Aspose.PSD untuk Java
linktitle: Tambahkan Warna Lapisan Goresan
second_title: Asumsikan.PSD Java API
description: Jelajahi kekuatan Aspose.PSD untuk Java dengan panduan langkah demi langkah kami dalam menambahkan warna lapisan guratan. Tingkatkan desain grafis Anda dengan mudah.
type: docs
weight: 14
url: /id/java/advanced-image-effects/add-stroke-layer-color/
---
## Perkenalan

Buka potensi desain grafis aplikasi Java Anda dengan Aspose.PSD. Dalam tutorial ini, kita akan mempelajari dunia menarik dalam menambahkan warna lapisan guratan menggunakan Aspose.PSD untuk Java. Sempurnakan grafis Anda dengan guratan yang menonjol, ciptakan desain yang menarik secara visual dengan mudah.

## Prasyarat

Sebelum memulai perjalanan kreatif ini, pastikan Anda memiliki prasyarat berikut:

-  Perpustakaan Aspose.PSD: Unduh dan atur perpustakaan Aspose.PSD dengan mengikuti[dokumentasi](https://reference.aspose.com/psd/java/).

- Java Development Kit (JDK): Pastikan Anda telah menginstal Java di sistem Anda.

- Lingkungan Pengembangan Terpadu (IDE): Pilih IDE pilihan Anda; Eclipse atau IntelliJ adalah pilihan populer.

## Paket Impor

Mari kita mulai dengan mengimpor paket yang diperlukan untuk mewujudkan keajaiban Aspose.PSD.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Langkah 1: Siapkan Proyek Anda

Mulailah dengan membuat proyek Java baru di IDE pilihan Anda. Pastikan perpustakaan Aspose.PSD ditambahkan ke proyek Anda.

## Langkah 2: Muat File PSD

Muat file PSD menggunakan Aspose.PSD, memungkinkan pemuatan sumber daya efek.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Langkah 3: Akses Lapisan Stroke

Akses lapisan efek guratan dalam file PSD.

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Langkah 4: Validasi Properti Stroke

Pastikan properti goresan sesuai yang diharapkan.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Langkah 5: Atur Warna dan Opasitas

Ubah warna dan opacity dari layer stroke.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Langkah 6: Simpan PSD yang Dimodifikasi

Simpan file PSD yang dimodifikasi dengan warna lapisan guratan yang baru ditambahkan.

```java
im.save(exportPath);
```

## Kesimpulan

Selamat! Anda telah berhasil menambahkan warna lapisan guratan ke file PSD Anda menggunakan Aspose.PSD untuk Java. Bereksperimenlah dengan berbagai warna dan pengaturan untuk menghidupkan desain grafis Anda.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.PSD dengan perpustakaan grafis Java lainnya?

A1: Ya, Aspose.PSD dapat diintegrasikan dengan perpustakaan grafis Java lainnya untuk meningkatkan fungsionalitas.

### Q2: Apakah Aspose.PSD kompatibel dengan format file PSD terbaru?

A2: Tentu saja! Aspose.PSD mengikuti spesifikasi format file PSD terbaru, memastikan kompatibilitas.

### Q3: Bagaimana cara menangani pengecualian saat menggunakan Aspose.PSD?

 A3: Lihat[forum dukungan](https://forum.aspose.com/c/psd/34) untuk bantuan dalam menangani pengecualian dan pemecahan masalah.

### Q4: Dapatkah saya mencoba Aspose.PSD sebelum membeli?

 A4: Tentu saja! Ambil a[uji coba gratis](https://releases.aspose.com/) untuk menjelajahi fitur Aspose.PSD sebelum membuat komitmen.

### Q5: Di mana saya bisa mendapatkan lisensi sementara untuk Aspose.PSD?

 A5: Dapatkan a[izin sementara](https://purchase.aspose.com/temporary-license/) untuk Aspose.PSD untuk mengevaluasi kemampuannya dalam proyek Anda.