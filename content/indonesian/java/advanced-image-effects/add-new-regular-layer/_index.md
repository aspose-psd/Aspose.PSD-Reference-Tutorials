---
title: Tambahkan Lapisan Reguler Baru ke PSD dengan Aspose.PSD untuk Java
linktitle: Tambahkan Layer Reguler Baru ke PSD
second_title: Aspose.PSD Java API
description: Pelajari cara menambahkan lapisan reguler baru ke file PSD menggunakan Aspose.PSD untuk Java. Ikuti panduan langkah demi langkah kami untuk manipulasi PSD yang lancar.
type: docs
weight: 11
url: /id/java/advanced-image-effects/add-new-regular-layer/
---
## Perkenalan

Selamat datang di tutorial komprehensif tentang penggunaan Aspose.PSD untuk Java untuk menambahkan lapisan reguler baru ke file PSD. Aspose.PSD adalah perpustakaan Java yang kuat yang memungkinkan pengembang untuk memanipulasi dan bekerja dengan file PSD secara efisien. Dalam tutorial ini, kami akan memandu Anda melalui proses menambahkan lapisan reguler baru ke file PSD, memberikan langkah-langkah rinci dan contoh kode.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di sistem Anda.
-  Perpustakaan Aspose.PSD: Unduh dan instal perpustakaan Aspose.PSD untuk Java. Anda dapat menemukan perpustakaan[Di Sini](https://releases.aspose.com/psd/java/).

## Paket Impor

Untuk memulai, impor paket yang diperlukan ke proyek Java Anda. Paket-paket ini penting untuk bekerja dengan fungsionalitas Aspose.PSD. Sertakan baris berikut di awal file Java Anda:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Langkah 1: Muat File PSD

Muat file PSD yang ingin Anda edit menggunakan kode berikut:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Langkah 2: Siapkan Array Data dan Persegi Panjang

Siapkan dua array int dan dua objek Rectangle sebagai berikut:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Langkah 3: Inisialisasi Data Lapisan

Inisialisasi array data dengan nilai default:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Langkah 4: Tambahkan Lapisan Reguler

Tambahkan dua lapisan biasa ke gambar PSD:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Langkah 5: Simpan PSD dan PNG

Simpan PSD yang dimodifikasi dan file PNG tambahan:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Selamat! Anda telah berhasil menambahkan lapisan reguler baru ke file PSD menggunakan Aspose.PSD untuk Java.

## Kesimpulan

Dalam tutorial ini, kita membahas proses menambahkan lapisan reguler baru ke file PSD menggunakan Aspose.PSD untuk Java. Pustaka yang kuat ini menyederhanakan manipulasi PSD, sehingga dapat diakses oleh pengembang Java. Bereksperimenlah dengan berbagai parameter dan fungsi untuk mengeksplorasi potensi penuh Aspose.PSD.

## FAQ

### Q1: Apakah Aspose.PSD kompatibel dengan Java 8?

A1: Ya, Aspose.PSD mendukung Java 8 dan versi yang lebih baru.

### Q2: Bisakah saya menerapkan transformasi ke lapisan yang ditambahkan?

A2: Tentu saja! Aspose.PSD menyediakan berbagai opsi transformasi untuk lapisan.

### Q3: Di mana saya dapat menemukan dokumentasi Aspose.PSD tambahan?

 A3: Anda dapat merujuk ke dokumentasi[Di Sini](https://reference.aspose.com/psd/java/).

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?

 A4: Kunjungi[Link ini](https://purchase.aspose.com/temporary-license/) untuk opsi lisensi sementara.

### Q5: Apakah ada forum komunitas untuk dukungan Aspose.PSD?

 A5: Ya, Anda dapat menemukan dukungan dan diskusi[Di Sini](https://forum.aspose.com/c/psd/34).