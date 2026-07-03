---
date: 2026-07-03
description: Pelajari cara memotong gambar Java menggunakan Aspose.PSD untuk Java.
  Tutorial pemotongan gambar langkah demi langkah ini mencakup memuat file PSD, mengatur
  nilai pergeseran, dan menyimpan hasilnya.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Potong Gambar dengan Pergeseran
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Potong Gambar Java dengan Pergeseran menggunakan Aspose.PSD
url: /id/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Memotong Gambar Java dengan Pergeseran menggunakan Aspose.PSD

## Pendahuluan

Dalam pemrosesan gambar Java, **crop image java** adalah kebutuhan umum untuk menyiapkan grafik, thumbnail, atau aset UI. Aspose.PSD untuk Java membuat tugas ini sederhana dengan menyediakan metode `crop` yang sederhana yang bekerja pada format raster yang didukung. Dalam tutorial ini Anda akan belajar cara memuat file PSD, menentukan nilai pergeseran kiri‑kanan‑atas‑bawah, menerapkan pemotongan, dan menyimpan hasilnya—semua tanpa menulis kode manipulasi piksel khusus.

## Jawaban Cepat
- **Perpustakaan apa yang menangani pemotongan?** Aspose.PSD untuk Java menyediakan metode `crop` bawaan.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara dapat digunakan untuk evaluasi; lisensi penuh diperlukan untuk produksi.  
- **Format yang didukung?** Lebih dari 30 format raster, termasuk PSD, JPEG, PNG, BMP, dan TIFF.  
- **Ukuran file maksimum?** Mendukung file hingga 2 GB tanpa memuat seluruh gambar ke memori.  
- **Berapa banyak baris kode?** Hanya lima langkah logis—memuat, meng-cache, menentukan pergeseran, memotong, dan menyimpan.

## Apa itu crop image java?
`crop image java` merujuk pada operasi memotong bitmap dalam aplikasi Java. Menggunakan Aspose.PSD, operasi ini dilakukan oleh metode `crop`, yang menerima nilai pergeseran untuk setiap sisi gambar dan mengembalikan instance gambar baru.

## Mengapa menggunakan Aspose.PSD untuk pemotongan gambar?
Aspose.PSD mendukung **30+** format gambar dan dapat memproses file PSD berisi ratusan halaman sekaligus menggunakan kurang dari 150 MB RAM, berkat arsitektur lazy‑loading-nya. Perpustakaan ini juga menjamin hasil pixel‑perfect, mempertahankan lapisan, masker, dan profil warna—sesuatu yang banyak perpustakaan gambar umum tidak dapat jamin.

## Prasyarat

### Java Development Kit (JDK)

Pastikan Anda memiliki versi terbaru JDK yang terpasang di sistem Anda. Anda dapat mengunduhnya dari [here](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java Library

Untuk memulai, Anda perlu memperoleh perpustakaan Aspose.PSD untuk Java. Kunjungi [download page](https://releases.aspose.com/psd/java/) dan dapatkan versi terbaru.

### Integrated Development Environment (IDE)

Pilih IDE Java favorit Anda, seperti Eclipse atau IntelliJ, untuk pengalaman coding yang lancar.

## Cara memotong gambar java?

Muat file sumber Anda, tentukan pergeseran piksel untuk setiap sisi, dan panggil metode `crop`—seluruh alur kerja ini dapat ditulis dalam lima baris kode yang singkat. Operasi `crop` membuat gambar baru yang hanya berisi wilayah yang Anda tentukan, meninggalkan file asli tidak berubah.

### Langkah 1: Muat Gambar

`Image` adalah kelas dasar untuk semua tipe gambar di Aspose.PSD.  
`RasterImage` mewakili gambar raster dan menyediakan kemampuan pemotongan.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Langkah 2: Cache Data Gambar

`cacheData()` memuat data gambar ke memori untuk pemrosesan yang lebih cepat.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Langkah 3: Tentukan Nilai Pergeseran

Tentukan nilai pergeseran untuk keempat sisi gambar (kiri, atas, kanan, bawah) dalam piksel.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Langkah 4: Terapkan Pemotongan

`crop(left, right, top, bottom)` memotong gambar berdasarkan pergeseran piksel yang ditentukan pada setiap sisi.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Langkah 5: Simpan Hasil

`JpegOptions` mendefinisikan pengaturan enkoding JPEG seperti kualitas dan profil warna.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Selamat! Anda telah berhasil memotong gambar menggunakan Aspose.PSD untuk Java.

## Masalah Umum dan Solusinya

- **Gambar tidak berubah:** Pastikan nilai pergeseran positif dan tidak melebihi dimensi asli.  
- **OutOfMemoryError pada file besar:** Aktifkan caching seperti yang ditunjukkan pada Langkah 2; ini memaksa Aspose.PSD menggunakan file sementara alih-alih menyimpan seluruh gambar di RAM.  
- **Pergeseran warna setelah pemotongan:** Pastikan Anda mempertahankan profil warna dengan memanggil `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` jika Anda memerlukan kesetiaan warna yang tepat.

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.PSD kompatibel dengan semua format gambar?**  
A: Ya, Aspose.PSD mendukung lebih dari 30 format raster, termasuk PSD, JPEG, PNG, BMP, TIFF, dan GIF, memastikan kompatibilitas yang luas.

**Q: Bisakah saya menerapkan beberapa operasi pemotongan pada gambar yang sama?**  
A: Tentu saja. Setelah setiap pemanggilan `crop` Anda akan menerima objek gambar baru, yang dapat Anda potong lagi sesuai kebutuhan.

**Q: Apakah ada forum komunitas untuk dukungan Aspose.PSD?**  
A: Ya, Anda dapat menemukan dukungan dan berinteraksi dengan komunitas di [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Bagaimana saya dapat memperoleh lisensi sementara untuk Aspose.PSD?**  
A: Kunjungi [here](https://purchase.aspose.com/temporary-license/) untuk memperoleh lisensi sementara.

**Q: Apakah ada proyek contoh yang menampilkan fungsionalitas Aspose.PSD?**  
A: Jelajahi dokumentasi dan contoh di [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Terakhir Diperbarui:** 2026-07-03  
**Diuji Dengan:** Aspose.PSD 24.11 for Java  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Tutorial Terkait

- [Memotong Gambar dengan Persegi Panjang di Aspose.PSD untuk Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image Java - Memperluas dan Memotong Gambar dengan Aspose.PSD untuk Java](/psd/java/image-editing/expand-and-crop-images/)
- [Ubah Ukuran Gambar Java - Menggunakan Enumerasi Resize Type di Aspose.PSD untuk Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}