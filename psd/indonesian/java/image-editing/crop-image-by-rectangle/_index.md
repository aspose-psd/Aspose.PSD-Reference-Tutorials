---
date: 2026-01-01
description: Jelajahi cara memotong gambar Java menggunakan Aspose.PSD untuk Java.
  Ikuti panduan langkah demi langkah kami untuk memuat file PSD, memotong persegi
  panjang gambar, dan mengonversi PSD ke JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Java Memotong Gambar: Memotong Gambar dengan Persegi Panjang menggunakan Aspose.PSD'
url: /id/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Potong Gambar Java: Memotong Gambar dengan Persegi Panjang menggunakan Aspose.PSD

## Pendahuluan

## Jawaban Cepat
- **Apa arti “crop image java”?** Ini merujuk pada pemotongan gambar ke persegi panjang yang ditentukan menggunakan kode Java.  
- **Library mana yang menangani operasi ini?** Aspose.PSD for Java menyediakan kelas yang diperlukan.  
- **Apakah saya memerlukan lisensi untuk pengujian?** Versi percobaan gratis tersedia; lisensi diperlukan untuk produksi.  
- **Bisakah saya mengonversi PSD yang dipotong ke JPEG?** Ya—gunakan `JpegOptions` saat menyimpan.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk skenario dasar.

## Apa itu pemotongan persegi panjang gambar di Java?

Memotong persegi panjang gambar berarti memilih area tertentu (ditentukan oleh X, Y, lebar, dan tinggi) dan membuang semua yang berada di luar area tersebut. Operasi ini umum ketika Anda perlu memfokuskan pada wilayah tertentu dari dokumen PSD yang lebih besar.

## Mengapa menggunakan Aspose.PSD untuk tugas ini?

- **Tidak ada dependensi eksternal** – bekerja dengan Java murni.  
- **Mendukung PSD, PNG, JPEG, dan banyak format lainnya** – Anda dapat **mengonversi PSD ke JPEG** secara instan.  
- **Rendering fidelity tinggi** – mempertahankan informasi lapisan dan profil warna selama pemotongan.  

## Prasyarat

- Java Development Kit (JDK) terinstal.  
- Aspose.PSD for Java library – unduh dari [website](https://releases.aspose.com/psd/java/).  

## Impor Paket

Pastikan untuk menyertakan paket yang diperlukan dalam proyek Java Anda untuk memanfaatkan kemampuan Aspose.PSD untuk Java. Tambahkan pernyataan impor berikut di awal file Java Anda:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Sekarang, mari kita uraikan proses menjadi beberapa langkah untuk memandu Anda memotong gambar dengan persegi panjang menggunakan Aspose.PSD untuk Java.

## Langkah 1: Siapkan Direktori Dokumen Anda

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur sebenarnya tempat file PSD Anda berada.

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

Di sini kami **memuat file PSD** ke dalam instance `RasterImage` dan meng-cache datanya untuk meningkatkan kinerja.

## Langkah 4: Buat dan Definisikan Persegi Panjang Pemotongan

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

Buat instance dari kelas `Rectangle` dengan ukuran yang diinginkan untuk pemotongan. Parameter tersebut mewakili **X**, **Y**, **lebar**, dan **tinggi** secara berurutan.

## Langkah 5: Potong dan Simpan Gambar

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Lakukan operasi pemotongan menggunakan persegi panjang yang ditentukan dan **mengonversi PSD ke JPEG** dengan menyimpan hasilnya menggunakan `JpegOptions`.

Ulangi langkah-langkah ini sesuai kebutuhan, menyesuaikan parameter sesuai dengan kebutuhan spesifik Anda.

## Masalah Umum & Tips

- **Persegi panjang di luar batas gambar** – pastikan koordinat persegi panjang berada dalam dimensi gambar sumber.  
- **Konsumsi memori** – panggil `rasterImage.dispose()` setelah selesai untuk membebaskan sumber daya native.  
- **Kontrol kualitas** – Anda dapat mengatur `JpegOptions.setQuality(int)` untuk mengontrol tingkat kompresi JPEG output.  

## Kesimpulan

Dalam tutorial ini kami menjelaskan proses **crop image java** dengan persegi panjang menggunakan Aspose.PSD untuk Java. Dengan mengikuti langkah-langkah ini Anda dapat dengan mudah mengintegrasikan kemampuan manipulasi gambar yang kuat—memuat file PSD, memotong wilayah tertentu, dan mengonversi hasilnya ke JPEG—ke dalam aplikasi Java apa pun.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.PSD untuk Java dengan kerangka kerja Java lainnya?

A1: Ya, Aspose.PSD untuk Java dapat diintegrasikan dengan berbagai kerangka kerja Java, memberikan fleksibilitas dalam proyek pengembangan Anda.

### Q2: Apakah tersedia versi percobaan gratis untuk Aspose.PSD untuk Java?

A2: Ya, Anda dapat mengakses versi percobaan gratis [di sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat menemukan dukungan atau bantuan tambahan?

A3: Kunjungi [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan komunitas dan diskusi.

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD untuk Java?

A4: Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

### Q5: Apa format gambar yang didukung untuk pemotongan di Aspose.PSD untuk Java?

A5: Aspose.PSD untuk Java mendukung berbagai format gambar, termasuk PSD, PNG, JPEG, dan lainnya.

---

**Terakhir Diperbarui:** 2026-01-01  
**Diuji Dengan:** Aspose.PSD for Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}