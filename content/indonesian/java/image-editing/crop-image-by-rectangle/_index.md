---
title: Pangkas Gambar dengan Rectangle di Aspose.PSD untuk Java
linktitle: Pangkas Gambar berdasarkan Persegi Panjang
second_title: Asumsikan.PSD Java API
description: Jelajahi kemampuan pemotongan gambar yang lancar di Java dengan Aspose.PSD. Ikuti panduan langkah demi langkah kami untuk memotong gambar dengan mudah menggunakan Aspose.PSD untuk Java.
type: docs
weight: 15
url: /id/java/image-editing/crop-image-by-rectangle/
---
## Perkenalan

Dalam dunia pengembangan Java, memanipulasi gambar adalah tugas umum, dan Aspose.PSD untuk Java memberikan solusi canggih untuk pemrosesan gambar. Dalam tutorial ini, kami akan memandu Anda melalui proses memotong gambar persegi panjang menggunakan Aspose.PSD untuk Java. Ikuti langkah-langkah di bawah ini untuk mencapainya dengan mudah.

## Prasyarat

Sebelum Anda menyelami tutorial ini, pastikan Anda memiliki prasyarat berikut:

- Java Development Kit (JDK) diinstal pada mesin Anda.
-  Aspose.PSD untuk perpustakaan Java. Anda dapat mengunduhnya dari[situs web](https://releases.aspose.com/psd/java/).

## Paket Impor

Pastikan untuk menyertakan paket yang diperlukan dalam proyek Java Anda untuk memanfaatkan kemampuan Aspose.PSD untuk Java. Tambahkan pernyataan import berikut di awal file Java Anda:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Sekarang, mari kita bagi prosesnya menjadi beberapa langkah untuk memandu Anda dalam memotong gambar persegi panjang menggunakan Aspose.PSD untuk Java.

## Langkah 1: Siapkan Direktori Dokumen Anda

```java
String dataDir = "Your Document Directory";
```

 Mengganti`"Your Document Directory"` dengan jalur sebenarnya tempat file PSD Anda berada.

## Langkah 2: Tentukan File Sumber dan Tujuan

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Tentukan jalur untuk file PSD sumber Anda dan file JPEG tujuan.

## Langkah 3: Muat dan Cache Gambar

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Muat gambar PSD ke dalam a`RasterImage` instance dan menyimpan datanya dalam cache.

## Langkah 4: Buat dan Tentukan Crop Rectangle

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 Buat sebuah instance dari`Rectangle` kelas dengan ukuran yang diinginkan untuk dipotong.

## Langkah 5: Pangkas dan Simpan Gambar

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Lakukan operasi pemotongan menggunakan persegi panjang yang ditentukan dan simpan hasilnya sebagai file JPEG.

Ulangi langkah-langkah ini sesuai kebutuhan, sesuaikan parameter sesuai dengan kebutuhan spesifik Anda.

## Kesimpulan

Dalam tutorial ini, kita mempelajari proses memotong gambar dengan persegi panjang menggunakan Aspose.PSD untuk Java. Dengan mengikuti langkah-langkah ini, Anda dapat dengan mudah mengintegrasikan kemampuan manipulasi gambar yang kuat ke dalam aplikasi Java Anda.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.PSD untuk Java dengan kerangka Java lainnya?

A1: Ya, Aspose.PSD untuk Java dapat diintegrasikan dengan berbagai kerangka kerja Java, memberikan fleksibilitas dalam proyek pengembangan Anda.

### Q2: Apakah tersedia uji coba gratis untuk Aspose.PSD untuk Java?

 A2: Ya, Anda dapat mengakses versi uji coba gratis.[Di Sini](https://releases.aspose.com/).

### Q3: Di mana saya bisa mendapatkan dukungan atau bantuan tambahan?

 A3: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan dan diskusi komunitas.

### Q4: Bagaimana cara mendapatkan lisensi sementara Aspose.PSD untuk Java?

 A4: Anda dapat memperoleh lisensi sementara.[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Apa saja format gambar yang didukung untuk dipotong di Aspose.PSD untuk Java?

A5: Aspose.PSD untuk Java mendukung berbagai format gambar, termasuk PSD, PNG, JPEG, dan lainnya.