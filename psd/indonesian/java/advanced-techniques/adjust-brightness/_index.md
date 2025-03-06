---
title: Sesuaikan Kecerahan Gambar dengan Aspose.PSD untuk Java
linktitle: Sesuaikan Kecerahan Gambar
second_title: Asumsikan.PSD Java API
description: Tingkatkan kecerahan gambar di Java dengan Aspose.PSD. Panduan langkah demi langkah untuk menyesuaikan kecerahan gambar secara terprogram.
weight: 21
url: /id/java/advanced-techniques/adjust-brightness/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sesuaikan Kecerahan Gambar dengan Aspose.PSD untuk Java

## Perkenalan

Meningkatkan gambar adalah persyaratan umum dalam desain grafis dan fotografi digital. Aspose.PSD untuk Java memberikan solusi ampuh untuk menyesuaikan kecerahan gambar secara terprogram. Dalam tutorial ini, kita akan menjelajahi cara memanfaatkan perpustakaan Aspose.PSD untuk Java untuk menyesuaikan kecerahan gambar, langkah demi langkah.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk Java Library: Unduh dan instal perpustakaan dari[Aspose.PSD untuk dokumentasi Java](https://reference.aspose.com/psd/java/).

## Paket Impor

Untuk memulai, impor paket yang diperlukan ke proyek Java Anda. Dalam contoh ini, kita akan menggunakan yang berikut ini:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Sekarang, mari kita uraikan proses penyesuaian kecerahan gambar menjadi beberapa langkah sederhana:

## Langkah 1: Muat Gambar

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Muat gambar yang ada ke dalam instance kelas RasterImage
Image image = Image.load(sourceFile);
// Keluarkan objek Gambar ke RasterImage
RasterImage rasterImage = (RasterImage) image;

// Periksa apakah RasterImage di-cache dan Cache RasterImage untuk kinerja yang lebih baik
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Pada langkah ini, kami memuat gambar target dan mentransmisikannya ke a`RasterImage` untuk diproses lebih lanjut.

## Langkah 2: Sesuaikan Kecerahan

```java
// Sesuaikan kecerahan
rasterImage.adjustBrightness(-50);
```

 Di sini, kami menggunakan`adjustBrightness`metode untuk mengubah kecerahan gambar. Dalam contoh ini, kami mengurangi kecerahan sebanyak 50 unit, namun Anda dapat menyesuaikan nilai ini berdasarkan kebutuhan Anda.

## Langkah 3: Tetapkan TiffOptions

```java
int[] ushort = {8, 8, 8};
// Buat instance TiffOptions untuk gambar yang dihasilkan
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Konfigurasikan`TiffOptions` untuk menyimpan gambar yang disesuaikan. Sesuaikan`bitsPerSample` Dan`photometric` properti berdasarkan kebutuhan spesifik Anda.

## Langkah 4: Simpan Gambar yang Dihasilkan

```java
// Simpan gambar yang dihasilkan
rasterImage.save(destName, tiffOptions);
```

 Terakhir, simpan gambar yang dimodifikasi menggunakan yang ditentukan`TiffOptions`.

## Kesimpulan

Menyesuaikan kecerahan gambar secara terprogram menjadi mudah dengan Aspose.PSD untuk Java. Tutorial ini telah memberikan panduan komprehensif tentang penerapan fungsi ini di aplikasi Java Anda.

## FAQ

### Q1: Dapatkah saya menyesuaikan kecerahan dalam format gambar lain selain PSD?

A1: Ya, Aspose.PSD untuk Java mendukung berbagai format gambar seperti JPEG, PNG, dan TIFF.

### Q2: Bagaimana cara menangani kesalahan selama proses penyesuaian gambar?

A2: Anda dapat menerapkan penanganan kesalahan menggunakan blok coba-tangkap untuk mengelola pengecualian yang mungkin terjadi.

### Q3: Apakah ada batasan rentang penyesuaian kecerahan?

A3: Kisaran penyesuaian bergantung pada konten dan format gambar, tetapi Aspose.PSD memberikan fleksibilitas dalam penyesuaian.

### Q4: Dapatkah saya menggunakan Aspose.PSD untuk Java dalam proyek komersial?

 A4: Ya, Aspose.PSD untuk Java adalah perpustakaan komersial, dan Anda dapat memperoleh lisensi darinya[Di Sini](https://purchase.aspose.com/buy).

### Q5: Apakah tersedia uji coba gratis untuk Aspose.PSD untuk Java?

 A5: Ya, Anda dapat menjelajahi perpustakaan dengan uji coba gratis[Di Sini](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
