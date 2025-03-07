---
title: Sesuaikan Gamma suatu Gambar dengan Aspose.PSD untuk Java
linktitle: Sesuaikan Gamma suatu Gambar
second_title: Asumsikan.PSD Java API
description: Pelajari cara menyesuaikan gamma gambar dengan mudah menggunakan Aspose.PSD untuk Java. Ikuti panduan langkah demi langkah kami untuk hasil optimal.
weight: 23
url: /id/java/advanced-techniques/adjust-gamma/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sesuaikan Gamma suatu Gambar dengan Aspose.PSD untuk Java

## Perkenalan

Dalam bidang pemrosesan gambar, menyesuaikan gamma suatu gambar merupakan langkah penting untuk meningkatkan daya tarik visualnya. Aspose.PSD untuk Java menawarkan solusi ampuh bagi pengembang Java untuk memanipulasi gamma gambar dengan mudah. Dalam tutorial ini, kita akan mempelajari cara menyesuaikan gamma menggunakan Aspose.PSD, menguraikan setiap langkah untuk memastikan implementasi yang lancar.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda telah menyiapkan prasyarat berikut:

1. Lingkungan Pengembangan Java: Pastikan Anda memiliki lingkungan pengembangan Java yang terinstal di sistem Anda.
2.  Perpustakaan Aspose.PSD: Unduh dan integrasikan perpustakaan Aspose.PSD ke dalam proyek Java Anda. Anda dapat menemukan sumber daya yang diperlukan di[dokumentasi](https://reference.aspose.com/psd/java/).
3. Contoh Gambar: Siapkan contoh gambar PSD yang akan Anda gunakan untuk menerapkan penyesuaian gamma.

## Paket Impor

Untuk memulai prosesnya, impor paket yang diperlukan ke proyek Java Anda. Ini menetapkan landasan untuk memanfaatkan fungsionalitas Aspose.PSD dengan lancar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Langkah 1: Muat Gambar

 Mulailah dengan memuat contoh gambar PSD ke dalam instance`RasterImage` kelas. Ini adalah dasar untuk penyesuaian gamma selanjutnya.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Muat gambar yang ada ke dalam instance kelas RasterImage
Image image = Image.load(sourceFile);

// Keluarkan objek Gambar ke RasterImage
RasterImage rasterImage = (RasterImage)image;

// Periksa apakah RasterImage di-cache untuk kinerja yang lebih baik
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Langkah 2: Sesuaikan Gamma

 Sekarang, sesuaikan gamma gambar yang dimuat menggunakan`adjustGamma` metode. Sesuaikan nilai gamma sesuai dengan kebutuhan Anda.

```java
// Sesuaikan gammanya
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Langkah 3: Buat TiffOptions

 Buat sebuah contoh dari`TiffOptions` untuk gambar yang dihasilkan. Tetapkan berbagai properti, seperti bit per sampel dan opsi fotometrik, untuk menyesuaikan keluaran dengan spesifikasi Anda.

```java
// Buat instance TiffOptions untuk gambar yang dihasilkan
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Langkah 4: Simpan Gambar yang Dihasilkan

 Simpan gambar yang dimanipulasi ke format TIFF menggunakan yang telah ditentukan sebelumnya`TiffOptions`.

```java
// Simpan gambar yang dihasilkan ke format TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil menyesuaikan gamma gambar menggunakan Aspose.PSD untuk Java. Proses ini memberdayakan pengembang untuk meningkatkan kualitas gambar dengan mudah, berkontribusi pada pengalaman pengguna yang menarik secara visual.

## FAQ

### Q1: Di mana saya dapat menemukan dokumentasi Aspose.PSD?

 A1: Anda dapat mengakses dokumentasinya di[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Bagaimana cara mengunduh Aspose.PSD untuk Java?

 A2: Unduh perpustakaan dari[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Dimana saya bisa membeli Aspose.PSD?

 A3: Kunjungi[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) untuk membeli Aspose.PSD.

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda dapat menjelajahi uji coba gratis di[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Di mana saya dapat mencari dukungan untuk Aspose.PSD?

 A5: Untuk dukungan, kunjungi forum Aspose.PSD di[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
