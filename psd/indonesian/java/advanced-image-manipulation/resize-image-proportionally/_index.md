---
title: Ubah Ukuran Gambar Secara Proporsional dengan Aspose.PSD untuk Java
linktitle: Ubah Ukuran Gambar Secara Proporsional
second_title: Asumsikan.PSD Java API
description: Sempurnakan aplikasi Java Anda dengan Aspose.PSD. Ikuti panduan kami untuk mengubah ukuran gambar secara proporsional dengan mudah. Tingkatkan kemampuan penanganan gambar Anda hari ini.
weight: 17
url: /id/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ubah Ukuran Gambar Secara Proporsional dengan Aspose.PSD untuk Java

## Perkenalan

Selamat datang di panduan langkah demi langkah kami tentang mengubah ukuran gambar secara proporsional menggunakan Aspose.PSD untuk Java. Jika Anda ingin menyempurnakan aplikasi Java dengan kemampuan pengubahan ukuran gambar yang efisien, Anda berada di tempat yang tepat. Dalam tutorial ini, kami akan memandu Anda melalui proses menggunakan langkah-langkah yang jelas dan ringkas.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

1. Lingkungan Java: Pastikan Anda telah menginstal Java di sistem Anda.
2.  Perpustakaan Aspose.PSD: Unduh dan instal perpustakaan Aspose.PSD. Anda dapat menemukan sumber daya yang diperlukan[Di Sini](https://releases.aspose.com/psd/java/).

## Paket Impor

Setelah prasyarat Anda diurutkan, impor paket yang diperlukan ke proyek Java Anda. Pastikan perpustakaan Aspose.PSD direferensikan dengan benar di proyek Anda.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Langkah 1: Muat Gambar

Mulailah dengan memuat gambar yang ingin Anda ubah ukurannya ke dalam aplikasi Java Anda.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Langkah 2: Tentukan Lebar dan Tinggi

Tentukan lebar dan tinggi baru untuk gambar Anda yang diubah ukurannya. Dalam contoh ini, kami akan mengubah ukuran gambar menjadi setengah dari dimensi aslinya.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Langkah 3: Simpan Gambar yang Diubah Ukurannya

Simpan gambar yang diubah ukurannya ke lokasi yang Anda inginkan, tentukan opsi format (PNG, dalam hal ini).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Dan itu dia! Anda telah berhasil mengubah ukuran gambar secara proporsional menggunakan Aspose.PSD untuk Java.

## Kesimpulan

Dalam tutorial ini, kami membahas langkah-langkah penting untuk mengubah ukuran gambar secara proporsional menggunakan perpustakaan Aspose.PSD untuk Java. Sekarang, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi Java Anda untuk meningkatkan penanganan gambar.

## FAQ

### Q1: Apakah Aspose.PSD kompatibel dengan semua format gambar?

 A1: Aspose.PSD mendukung berbagai format gambar, termasuk PSD, PNG, JPEG, dan lainnya. Periksa[dokumentasi](https://reference.aspose.com/psd/java/) untuk daftar lengkap.

### Q2: Dapatkah saya menggunakan Aspose.PSD untuk proyek komersial?

 A2: Ya, Anda bisa. Kunjungi[halaman pembelian](https://purchase.aspose.com/buy) untuk rincian perizinan.

### Q3: Apakah lisensi sementara tersedia untuk tujuan pengujian?

 A3: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/) untuk evaluasi.

### Q4: Di mana saya dapat menemukan dukungan untuk Aspose.PSD?

 A4: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan dan bantuan masyarakat.

### Q5: Bagaimana cara mengakses dokumentasi Aspose.PSD?

 A5: Lihat dokumentasi rinci[Di Sini](https://reference.aspose.com/psd/java/).
`
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
