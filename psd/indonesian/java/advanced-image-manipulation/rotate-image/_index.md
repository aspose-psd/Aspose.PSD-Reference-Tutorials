---
title: Putar Gambar di Aspose.PSD untuk Java
linktitle: Memutar Gambar
second_title: Asumsikan.PSD Java API
description: Jelajahi rotasi gambar di Java dengan mudah menggunakan Aspose.PSD. Putar, balik, dan simpan file PSD dengan mudah.
weight: 19
url: /id/java/advanced-image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Putar Gambar di Aspose.PSD untuk Java

## Perkenalan

Aspose.PSD untuk Java menyediakan serangkaian fitur canggih untuk bekerja dengan gambar, memungkinkan pengembang memanipulasi dan memproses file PSD secara efisien. Dalam tutorial ini, kita akan fokus pada satu tugas spesifik: memutar gambar. Baik Anda sedang membuat aplikasi pengeditan foto atau hanya perlu menyesuaikan orientasi gambar, Aspose.PSD membuat prosesnya mudah.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.PSD untuk Perpustakaan Java: Pastikan Anda telah mengunduh dan menginstal perpustakaan Aspose.PSD untuk Java. Anda dapat menemukan perpustakaan dan dokumentasi terperinci[Di Sini](https://reference.aspose.com/psd/java/).

- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.

-  Contoh File PSD: Siapkan contoh file PSD yang ingin Anda putar. Sesuaikan`sourceFile` variabel dalam kode contoh dengan jalur ke file PSD Anda.

## Paket Impor

Mulailah dengan mengimpor paket yang diperlukan untuk memanfaatkan kemampuan Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Langkah 1: Muat Gambar

 Muat gambar yang ada ke dalam instance`Image` kelas:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Langkah 2: Putar Gambar

 Putar gambar menggunakan`rotateFlip` metode. Dalam contoh ini, kita memutar gambar sebesar 270 derajat:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Langkah 3: Simpan Gambar yang Diputar

 Simpan gambar yang diputar menggunakan`save` metode dan menentukan format keluaran (JPEG, dalam hal ini):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Kesimpulan

Selamat! Anda berhasil memutar gambar menggunakan Aspose.PSD untuk Java. Pustaka sederhana namun kuat ini membuka banyak kemungkinan untuk manipulasi gambar dalam aplikasi Java Anda.

## FAQ

### Q1: Apakah Aspose.PSD kompatibel dengan format gambar yang berbeda?

A1: Ya, Aspose.PSD mendukung berbagai format gambar, termasuk PSD, JPEG, PNG, dan lainnya.

### Q2: Dapatkah saya menerapkan rotasi khusus, bukan hanya membalik yang telah ditentukan sebelumnya?

A2: Tentu saja! Aspose.PSD memberikan fleksibilitas untuk menerapkan rotasi khusus untuk memenuhi kebutuhan spesifik Anda.

### Q3: Di mana saya bisa mendapatkan dukungan atau bantuan tambahan?

 A3: Untuk pertanyaan atau masalah apa pun, kunjungi[Forum Asumsikan.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan masyarakat.

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda dapat menjelajahi Aspose.PSD dengan a[uji coba gratis](https://releases.aspose.com/).

### Q5: Bagaimana cara mendapatkan lisensi sementara?

 A5: Jika Anda memerlukan lisensi sementara, Anda bisa mendapatkannya[Di Sini](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
