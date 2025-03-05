---
title: Mengubah ukuran dengan Resize Type Enumeration di Aspose.PSD untuk Java
linktitle: Mengubah ukuran dengan Resize Type Enumeration
second_title: Asumsikan.PSD Java API
description: Ubah ukuran gambar master di Java dengan Aspose.PSD. Panduan langkah demi langkah menggunakan Resize Type Enumeration.
type: docs
weight: 18
url: /id/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## Perkenalan

Dalam lanskap pengembangan Java yang terus berkembang, pemrosesan gambar yang efisien adalah aspek penting yang sering dihadapi oleh pengembang. Aspose.PSD untuk Java muncul sebagai solusi ampuh, memberikan pengalaman mulus untuk mengubah ukuran gambar dengan keuntungan tambahan dari Resize Type Enumeration. Dalam tutorial ini, kita akan mempelajari seluk-beluk mengubah ukuran gambar menggunakan Aspose.PSD untuk Java, menguraikan setiap langkah untuk memastikan pemahaman yang komprehensif.

## Prasyarat

Sebelum memulai tutorial ini, pastikan Anda memiliki prasyarat berikut:

1. Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.

2. Perpustakaan Aspose.PSD: Unduh dan instal perpustakaan Aspose.PSD dari[situs web](https://releases.aspose.com/psd/java/).

3.  Contoh File PSD: Siapkan contoh file PSD untuk eksperimen. Anda dapat menggunakan[sample.psd](Direktori Dokumen Anda/sample.psd) untuk tutorial ini.

## Paket Impor

Untuk memulai, impor paket yang diperlukan ke proyek Java Anda:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Langkah 1: Muat Gambar

 Mulailah dengan memuat gambar yang ada ke dalam instance`RasterImage` kelas. Gunakan cuplikan kode berikut:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Muat gambar yang ada ke dalam instance kelas RasterImage
Image image = Image.load(sourceFile);
```

## Langkah 2: Ubah ukuran Gambar

Sekarang, ubah ukuran gambar yang dimuat menggunakan Resize Type Enumeration. Dalam contoh ini, kami menggunakan metode Lanczos Resample:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Langkah 3: Simpan Gambar yang Diubah Ukurannya

Setelah diubah ukurannya, simpan gambar dengan dimensi yang ditentukan dan jenis pengubahan ukuran yang dipilih. Di sini, kami menyimpannya sebagai file JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

Dan itu dia! Anda telah berhasil mengubah ukuran gambar menggunakan Resize Type Enumeration di Aspose.PSD untuk Java.

Kesimpulannya, Aspose.PSD untuk Java menyediakan platform yang kuat untuk manipulasi gambar, dan Resize Type Enumeration menambahkan lapisan fleksibilitas pada proses ini. Baik Anda sedang mengerjakan proyek kecil atau aplikasi berskala besar, menguasai langkah-langkah ini akan memberdayakan Anda untuk menangani pengubahan ukuran gambar dengan lancar.

## FAQ

### Q1: Apakah Aspose.PSD untuk Java cocok untuk proyek skala kecil dan besar?

A1: Tentu saja! Aspose.PSD untuk Java dirancang untuk memenuhi proyek dari semua ukuran, memberikan skalabilitas dan efisiensi.

### Q2: Dapatkah saya menggunakan jenis pengubahan ukuran selain Lanczos Resample?

A2: Ya, Aspose.PSD untuk Java menawarkan berbagai tipe pengubahan ukuran, seperti Nearest Neighbor, Bicubic, dan banyak lagi. Jelajahi dokumentasi untuk daftar lengkap.

### Q3: Di mana saya dapat menemukan dukungan tambahan untuk Aspose.PSD untuk Java?

 A3: Untuk pertanyaan atau bantuan apa pun, kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q4: Apakah tersedia uji coba gratis untuk Aspose.PSD untuk Java?

 A4: Ya, Anda dapat mengakses versi uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q5: Bagaimana cara mendapatkan lisensi sementara Aspose.PSD untuk Java?

 A5: Untuk mendapatkan lisensi sementara, kunjungi[tautan ini](https://purchase.aspose.com/temporary-license/).