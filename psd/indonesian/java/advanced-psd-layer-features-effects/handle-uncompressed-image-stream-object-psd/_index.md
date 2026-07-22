---
date: 2026-02-17
description: Pelajari cara mengekspor PSD ke PNG dan menangani aliran gambar tidak
  terkompresi dengan Aspose.PSD untuk Java.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Ekspor PSD ke PNG – Buat Objek Grafik PSD – Aliran Tidak Terkompresi di Java
url: /id/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor PSD ke PNG – Membuat Objek Grafik PSD – Aliran Tidak Terkompresi di Java

## Perkenalan
Selamat datang di dunia manipulasi gambar di Java! Dalam tutorial ini Anda akan **membuat objek grafik PSD**, menangani objek aliran gambar tidak terkompresi, dan mempelajari cara **mengekspor PSD ke PNG** menggunakan Aspose.PSD untuk Java. Baik Anda seorang desainer grafis yang ingin mengotomatisasi alur kerja atau pengembang perangkat lunak yang ingin mengintegrasikan kemampuan pemrosesan gambar yang kuat ke dalam aplikasi Anda, panduan ini dibuat khusus untuk Anda. Kami akan membahas semua hal mulai dari persyaratan hingga ekspor akhir, memastikan Anda memiliki pemahaman yang solid tentang seluruh proses.

## Jawaban Cepat
- **Apa arti “membuat objek grafis PSD”?** Ini merujuk pada pembuatan konteks grafik untuk file PSD sehingga Anda dapat menggambar atau mengedit isinya.
- **Library mana yang menangani aliran tidak terkompresi?** Aspose.PSD untuk Java menyediakan dukungan penuh untuk data gambar mentah (tidak terkompresi).
- **Apakah saya dapat mengekspor PSD ke PNG setelah mengedit?** Ya—setelah Anda memiliki objek `Graphics`, Anda dapat merender PSD dan menyimpannya sebagai PNG.
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.
- **Apakah ekspor bersifat lossless?** Mengekspor ke PNG mempertahankan kualitas gambar, sementara ukuran file lebih besar dari JPEG tetapi lebih kecil dari PSD yang tidak terkompresi.

## Cara mengekspor PSD ke PNG menggunakan Aspose.PSD untuk Java
Ketika Anda perlu **mengekspor PSD ke PNG**, alur kerja tipikalnya adalah:

1. Muat file PSD (atau buat baru).
2. Lakukan gambar atau manipulasi lapisan apa pun dengan objek `Graphics`.
3. Simpan gambar yang dihasilkan menggunakan `PngOptions` (contoh `Graphics` yang sama dapat digunakan kembali).

Meskipun tutorial ini fokus pada penanganan aliran tidak terkompresi, objek `Graphics` yang Anda buat dapat digunakan kembali untuk merender PSD menjadi file PNG di kemudian hari dalam alur kerja Anda.

## Prasyarat
Sebelum kita melompat ke kode, pastikan Anda memiliki semua yang diperlukan untuk memulai perjalanan ini. Berikut adalah prasyaratnya:

### Kit Pengembangan Java (JDK)
Pastikan Anda telah menginstal JDK di mesin Anda. Anda dapat mengunduhnya dari situs web Oracle atau menggunakan OpenJDK.

### Aspose.PSD untuk Java
Anda perlu dan mengunduh pustaka Aspose.PSD. Pustaka yang kuat ini memungkinkan Anda memanipulasi file PSD dengan mudah. Anda dapat mendapatkan versi terbaru dari [tautan ini](https://releases.aspose.com/psd/java/).

### Lingkungan Pengembangan Terintegrasi (IDE)
Disarankan menggunakan IDE untuk menulis dan menguji kode Java Anda. Anda dapat menggunakan IntelliJ IDEA, Eclipse, atau IDE lain yang sesuai dengan preferensi Anda.

### Pemahaman Dasar Java
Pemahaman dasar tentang pemrograman Java akan membuat proses ini lebih lancar. Pastikan Anda mengetahui hal‑hal dasar seperti kelas, metode, dan penanganannya.

Setelah semua siap, mari **menggulung** lengan kita dan masuk ke bagian yang menarik – kode menulis!

## Impor Paket
Untuk memulai, kita perlu mengimpor paket-paket yang diperlukan untuk bekerja dengan Aspose.PSD. Di bawah ini, Anda akan menemukan impor yang biasanya diperlukan untuk menangani file PSD.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Sekarang, mari kita uraikan kode menjadi langkah‑langkah yang mudah dipahami agar Anda dapat mengikutinya dengan mudah. Kami akan menyiapkan, memuat file PSD, memanipulasinya, dan menyimpan hasilnya.

## Langkah 1: Tentukan Direktori Dokumen Anda
Sebelum Anda mulai menulis kode, Anda perlu menentukan di mana file PSD Anda berada. Ini pada dasarnya menyiapkan panggung untuk proyek Anda.

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur sebenarnya tempat file PSD Anda (misalnya, layers.psd) berada. Ini membantu menemukan file Anda tanpa kesulitan.

## Langkah 2: Buat Aliran Output Array Byte
Anda memerlukan tempat untuk menyimpan gambar yang telah dimodifikasi sebelum melakukan apa pun dengannya. `ByteArrayOutputStream` akan membantu Anda menangkap data gambar dengan mudah.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Baris ini menginisialisasi objek `ByteArrayOutputStream` baru bernama `ms`. Anda akan menggunakan objek ini untuk menyimpan gambar tidak terkompresi Anda.

## Langkah 3: Muat File PSD
Sekarang, saatnya memuat file PSD yang sebenarnya. Di sinilah keajaiban dimulai!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Baris ini memuat file PSD Anda ke dalam objek `PsdImage`. Pastikan Anda memiliki jalur yang benar; jika tidak, akan muncul error seperti kuis mendadak yang tidak tercek.

## Langkah 4: Atur PsdOptions untuk Menyimpan
Anda perlu menentukan cara menyimpan gambar — tidak terkompresi, tentu saja!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Di sini, Anda membuat objek `PsdOptions` dan mengatur metode kompresi menjadi `Raw`. Metode ini memastikan gambar mempertahankan kualitas penuh dan disimpan tanpa kompresi apa pun.

## Langkah 5: Simpan Gambar ke Aliran Output
```java
psdImage.save(ms, saveOptions);
```

Baris ini menyimpan gambar yang telah dimodifikasi ke dalam `ByteArrayOutputStream` yang Anda buat pada Langkah 2, menggunakan opsi yang didefinisikan pada Langkah 4. Metode `save` menangani pengkodean gambar dengan tepat berdasarkan pengaturan Anda.

## Langkah 6: Atur Ulang Aliran Output
Setelah menyimpan, aliran output Anda berada di akhir. Anda perlu meresetnya agar dapat membaca dari awal.

```java
ms.reset();
```

Metode `reset` ini menyiapkan `ByteArrayOutputStream` Anda untuk dibaca kembali dari awal. Anggap saja seperti memutar ulang pita sebelum mendengarkan lagu favorit Anda!

## Langkah 7: Muat Gambar yang Baru Dibuat
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Di sini, kami memuat kembali gambar dari `ByteArrayOutputStream` ke dalam objek `PsdImage` baru. Di sinilah Anda dapat memeriksa hasil kerja sebelumnya.

## Langkah 8: Buat Objek Grafis
Untuk memodifikasi atau merender gambar lebih lanjut, Anda perlu membuat objek grafik.

```java
Graphics graphics = new Graphics(psdImage);
```

Baris ini menginisialisasi objek `Graphics` menggunakan `psdImage` Anda. Sekarang Anda dapat menggunakan objek grafik ini untuk menggambar atau memanipulasi gambar sesuai kebutuhan. Ini seperti memiliki kuas cat di tangan Anda!

## Memanipulasi Lapisan PSD dengan Objek Grafik
Sekarang Anda memiliki instance **Graphics**, Anda dapat **memanipulasi lapisan PSD**—misalnya, menggambar bentuk, menambahkan teks, atau menerapkan filter pada lapisan tertentu. Konteks grafik bekerja langsung pada piksel data di bawahnya, memberi Anda kontrol detail atas tampilan setiap lapisan.

## Masalah Umum dan Solusinya
- **NullPointerException saat memuat file** – periksa kembali jalur `dataDir` dan pastikan nama file sudah benar.
- **Output terkompresi meskipun menggunakan Raw** – pastikan `saveOptions.setCompressionMethod(CompressionMethod.Raw);` dipanggil sebelum metode `save`.
- **Objek Graphics muncul kosong** – pastikan Anda menggambar pada instance `PsdImage` yang tepat (gunakan yang Anda muat, bukan yang baru dibuat kecuali memang terkandung).

## FAQ
### Apa itu Aspose.PSD?
Aspose.PSD adalah pustaka .NET yang memungkinkan pengembang untuk membuat, mengedit, dan memanipulasi file Photoshop PSD serta format gambar terkait secara programatis.

### Bagaimana cara mengunduh Aspose.PSD untuk Java?
Anda dapat mengunduhnya dari [halaman rilis](https://releases.aspose.com/psd/java/).

### Apakah ada uji coba gratis untuk Aspose.PSD?
Ya, Anda dapat memperoleh versi percobaan gratis dari [sini](https://releases.aspose.com/).

### Bisakah saya mendapatkan dukungan untuk Aspose.PSD?
Tentu saja! Anda dapat mencari bantuan di [forum dukungan Aspose](https://forum.aspose.com/c/psd/34).

### Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?
Cukup kunjungi [halaman lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk memulai.

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya menggunakan objek grafis untuk mengedit hanya satu lapisan tertentu?**
J: Ya. Setelah memuat PSD, pilih lapisan yang diinginkan melalui `psdImage.getLayers().get_Item(index)` dan berikan ke konstruktor `Graphics`.

**T: Apakah metode kompresi Raw memengaruhi ukuran file?**
J: Raw menyimpan data piksel tanpa kompresi, sehingga ukuran file akan lebih besar daripada PSD yang dikompresi, tetapi kualitas gambar tetap tidak berubah.

**T: Apakah mungkin untuk mengekspor PSD yang diedit ke format lain (misalnya, PNG)?**
J: Tentu saja. Gunakan overload `Image.save` yang sesuai dengan `PngOptions` setelah pengeditan—ini adalah cara standar untuk **mengekspor PSD ke PNG**.

**T: Versi Java apa yang dibutuhkan?**
J: Aspose.PSD untuk Java mendukung JDK8 dan yang lebih baru.

**T: Bagaimana cara melepaskan sumber daya setelah pemrosesan?**
J: Panggil `psdImage.dispose()` dan tutup semua aliran untuk membebaskan sumber daya asli.

---

**Terakhir Diperbarui:** 17-02-2026
**Diuji Dengan:** Aspose.PSD for Java (rilisan terbaru)
**Penulis:** Berasumsi  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}