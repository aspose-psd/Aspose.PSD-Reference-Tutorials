---
title: Sesuaikan Kontras Gambar dengan Aspose.PSD untuk Java
linktitle: Sesuaikan Kontras Gambar
second_title: Asumsikan.PSD Java API
description: Jelajahi dunia penyesuaian kontras gambar di Java dengan Aspose.PSD. Ikuti panduan langkah demi langkah kami untuk manipulasi gambar yang lancar.
type: docs
weight: 22
url: /id/java/advanced-techniques/adjust-contrast/
---
## Perkenalan

Di bidang pemrosesan gambar dengan Java, Aspose.PSD menonjol sebagai alat yang ampuh. Di antara segudang fiturnya, menyesuaikan kontras gambar merupakan persyaratan umum. Tutorial ini akan memandu Anda melalui proses penyesuaian kontras gambar menggunakan Aspose.PSD untuk Java. Baik Anda seorang pengembang berpengalaman atau baru memulai, panduan ini akan membantu Anda menguasai aspek penting dalam manipulasi gambar.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Pemahaman dasar pemrograman Java.
-  Aspose.PSD untuk perpustakaan Java diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/psd/java/).

## Paket Impor

Untuk memulai, Anda perlu mengimpor paket yang diperlukan ke proyek Java Anda. Tambahkan baris berikut ke kode Anda:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Langkah 1: Muat Gambar

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Muat gambar yang ada ke dalam instance kelas RasterImage
Image image = Image.load(sourceFile);
```

 Pada langkah ini, kita memuat gambar sampel ("sample.psd") menggunakan`Image.load` metode.

## Langkah 2: Transmisikan ke RasterImage dan Data Cache

```java
// Keluarkan objek Gambar ke RasterImage
RasterImage rasterImage = (RasterImage)image;

// Periksa apakah RasterImage di-cache dan Cache RasterImage untuk kinerja yang lebih baik
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Di sini, kami menggunakan generiknya`Image` keberatan dengan a`RasterImage` untuk pemrosesan tertentu. Menyimpan data gambar dalam cache akan meningkatkan kinerja.

## Langkah 3: Sesuaikan Kontras

```java
// Sesuaikan kontrasnya
rasterImage.adjustContrast(50);
```

 Itu`adjustContrast`Metode ini digunakan untuk mengubah kontras gambar. Dalam contoh ini, kontrasnya ditingkatkan sebesar 50%.

## Langkah 4: Buat TiffOptions dan Simpan

```java
// Buat instance TiffOptions untuk gambar yang dihasilkan
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Simpan gambar yang dihasilkan ke format TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Di sini, kami menyiapkannya`TiffOptions` untuk gambar keluaran, menentukan format dan properti lainnya. Gambar akhir kemudian disimpan ke file TIFF.

## Kesimpulan

Selamat! Anda telah berhasil menyesuaikan kontras gambar menggunakan Aspose.PSD untuk Java. Tutorial ini mencakup langkah-langkah penting, mulai dari mengimpor paket hingga menyimpan gambar yang diproses.

## FAQ

### Q1: Apakah Aspose.PSD kompatibel dengan format gambar yang berbeda?

A1: Ya, Aspose.PSD mendukung berbagai format gambar, memberikan fleksibilitas dalam proyek Anda.

### Q2: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?

 A2: Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q3: Di mana saya dapat menemukan dokumentasi Aspose.PSD?

A3: Dokumentasi tersedia[Di Sini](https://reference.aspose.com/psd/java/).

### Q4: Opsi dukungan apa yang tersedia untuk Aspose.PSD?

 A4: Untuk dukungan, kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Bisakah saya membeli Aspose.PSD?

 A5: Ya, Anda dapat membeli Aspose.PSD[Di Sini](https://purchase.aspose.com/buy).