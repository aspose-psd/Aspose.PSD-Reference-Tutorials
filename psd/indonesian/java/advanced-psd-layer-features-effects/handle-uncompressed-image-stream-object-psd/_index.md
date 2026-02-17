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

## Introduction
Selamat datang di dunia manipulasi gambar di Java! Dalam tutorial ini Anda akan **membuat objek grafik PSD**, menangani objek aliran gambar tidak terkompresi, dan mempelajari cara **mengekspor PSD ke PNG** menggunakan Aspose.PSD untuk Java. Baik Anda seorang desainer grafis yang ingin mengotomatisasi alur kerja atau pengembang perangkat lunak yang ingin mengintegrasikan kemampuan pemrosesan gambar yang kuat ke dalam aplikasi Anda, panduan ini dibuat khusus untuk Anda. Kami akan membahas semua hal mulai dari prasyarat hingga ekspor akhir, memastikan Anda memiliki pemahaman yang solid tentang seluruh proses.

## Quick Answers
- **Apa arti “create PSD graphics object”?** Ini merujuk pada pembuatan konteks grafik untuk file PSD sehingga Anda dapat menggambar atau mengedit isinya.  
- **Library mana yang menangani aliran tidak terkompresi?** Aspose.PSD untuk Java menyediakan dukungan penuh untuk data gambar mentah (tidak terkompresi).  
- **Apakah saya dapat mengekspor PSD ke PNG setelah mengedit?** Ya—setelah Anda memiliki objek `Graphics`, Anda dapat merender PSD dan menyimpannya sebagai PNG.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Apakah ekspor bersifat lossless?** Mengekspor ke PNG mempertahankan kualitas gambar, sementara ukuran file lebih besar daripada JPEG tetapi lebih kecil daripada PSD yang tidak terkompresi.  

## How to export PSD to PNG using Aspose.PSD for Java
Ketika Anda perlu **mengekspor PSD ke PNG**, alur kerja tipikal adalah:

1. Muat file PSD (atau buat baru).  
2. Lakukan gambar atau manipulasi lapisan apa pun dengan objek `Graphics`.  
3. Simpan gambar yang dihasilkan menggunakan `PngOptions` (instance `Graphics` yang sama dapat digunakan kembali).  

Walaupun tutorial ini berfokus pada penanganan aliran tidak terkompresi, objek `Graphics` yang Anda buat dapat digunakan kembali untuk merender PSD menjadi file PNG di kemudian hari dalam alur kerja Anda.

## Prerequisites
Sebelum kita melompat ke kode, pastikan Anda memiliki semua yang diperlukan untuk memulai perjalanan ini. Berikut adalah prasyaratnya:

### Java Development Kit (JDK)
Pastikan Anda telah menginstal JDK di mesin Anda. Anda dapat mengunduhnya dari situs web Oracle atau menggunakan OpenJDK.

### Aspose.PSD for Java
Anda perlu mengunduh dan menginstal pustaka Aspose.PSD. Pustaka yang kuat ini memungkinkan Anda memanipulasi file PSD dengan mudah. Anda dapat mendapatkan versi terbaru dari [tautan ini](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Disarankan menggunakan IDE untuk menulis dan menguji kode Java Anda. Anda dapat menggunakan IntelliJ IDEA, Eclipse, atau IDE lain yang sesuai dengan preferensi Anda.

### Basic Understanding of Java
Pemahaman dasar tentang pemrograman Java akan membuat proses ini lebih lancar. Pastikan Anda mengetahui hal‑hal dasar seperti kelas, metode, dan penanganan pengecualian.

Setelah semua siap, mari **menggulung** lengan kita dan masuk ke bagian yang menarik – menulis kode!

## Import Packages
Untuk memulai, kita perlu mengimpor paket-paket yang diperlukan untuk bekerja dengan Aspose.PSD. Di bawah ini, Anda akan menemukan impor yang biasanya dibutuhkan untuk menangani file PSD.

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

## Step 1: Define Your Document Directory
Sebelum Anda mulai menulis kode, Anda perlu menentukan di mana file PSD Anda berada. Ini pada dasarnya menyiapkan panggung untuk proyek Anda.

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur sebenarnya tempat file PSD Anda (misalnya, layers.psd) berada. Ini membantu menemukan file Anda tanpa kesulitan.

## Step 2: Create a Byte Array Output Stream
Anda memerlukan tempat untuk menyimpan gambar yang telah dimodifikasi sebelum melakukan apa pun dengannya. `ByteArrayOutputStream` akan membantu Anda menangkap data gambar dengan mudah.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Baris ini menginisialisasi objek `ByteArrayOutputStream` baru bernama `ms`. Anda akan menggunakan objek ini untuk menyimpan gambar tidak terkompresi Anda.

## Step 3: Load the PSD File
Sekarang, saatnya memuat file PSD yang sebenarnya. Di sinilah keajaiban dimulai!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Baris ini memuat file PSD Anda ke dalam objek `PsdImage`. Pastikan Anda memiliki jalur yang benar; jika tidak, akan muncul error seperti kuis mendadak yang tidak tercek.

## Step 4: Set Up the PsdOptions for Saving
Anda perlu menentukan cara menyimpan gambar — tidak terkompresi, tentu saja!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Di sini, Anda membuat objek `PsdOptions` dan mengatur metode kompresi menjadi `Raw`. Metode ini memastikan gambar mempertahankan kualitas penuh dan disimpan tanpa kompresi apa pun.

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

Baris ini menyimpan gambar yang telah dimodifikasi ke dalam `ByteArrayOutputStream` yang Anda buat pada Langkah 2, menggunakan opsi yang didefinisikan pada Langkah 4. Metode `save` menangani pengkodean gambar dengan tepat berdasarkan pengaturan Anda.

## Step 6: Reset the Output Stream
Setelah menyimpan, aliran output Anda berada di akhir. Anda perlu meresetnya agar dapat membaca dari awal.

```java
ms.reset();
```

Metode `reset` ini menyiapkan `ByteArrayOutputStream` Anda untuk dibaca kembali dari awal. Anggap saja seperti memutar ulang pita sebelum mendengarkan lagu favorit Anda!

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Di sini, kami memuat kembali gambar dari `ByteArrayOutputStream` ke dalam objek `PsdImage` baru. Di sinilah Anda dapat memeriksa hasil kerja sebelumnya.

## Step 8: Create Graphics Object
Untuk memodifikasi atau merender gambar lebih lanjut, Anda perlu membuat objek grafik.

```java
Graphics graphics = new Graphics(psdImage);
```

Baris ini menginisialisasi objek `Graphics` menggunakan `psdImage` Anda. Sekarang Anda dapat menggunakan objek grafik ini untuk menggambar atau memanipulasi gambar sesuai kebutuhan. Ini seperti memiliki kuas cat di tangan Anda!

## Manipulate PSD Layers with Graphics Object
Sekarang Anda memiliki instance **Graphics**, Anda dapat **memanipulasi lapisan PSD**—misalnya, menggambar bentuk, menambahkan teks, atau menerapkan filter pada lapisan tertentu. Konteks grafik bekerja langsung pada data piksel di bawahnya, memberi Anda kontrol detail atas tampilan setiap lapisan.

## Common Issues and Solutions
- **NullPointerException saat memuat file** – periksa kembali jalur `dataDir` dan pastikan nama file sudah benar.  
- **Output terkompresi meskipun menggunakan Raw** – pastikan `saveOptions.setCompressionMethod(CompressionMethod.Raw);` dipanggil sebelum metode `save`.  
- **Objek Graphics muncul kosong** – pastikan Anda menggambar pada instance `PsdImage` yang tepat (gunakan yang Anda muat, bukan yang baru dibuat kecuali memang dimaksudkan).

## FAQ's
### What is Aspose.PSD?
Aspose.PSD adalah pustaka .NET yang memungkinkan pengembang untuk membuat, mengedit, dan memanipulasi file Photoshop PSD serta format gambar terkait secara programatis.

### How can I download Aspose.PSD for Java?
Anda dapat mengunduhnya dari [halaman rilis](https://releases.aspose.com/psd/java/).

### Is there a free trial for Aspose.PSD?
Ya, Anda dapat memperoleh versi percobaan gratis dari [sini](https://releases.aspose.com/).

### Can I get support for Aspose.PSD?
Tentu saja! Anda dapat mencari bantuan di [forum dukungan Aspose](https://forum.aspose.com/c/psd/34).

### How can I obtain a temporary license for Aspose.PSD?
Cukup kunjungi [halaman lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk memulai.

## Frequently Asked Questions

**Q: Can I use the graphics object to edit only one specific layer?**  
A: Yes. After loading the PSD, select the desired layer via `psdImage.getLayers().get_Item(index)` and pass it to the `Graphics` constructor.

**Q: Does the Raw compression method affect file size?**  
A: Raw stores pixel data without compression, so the file size will be larger than compressed PSDs, but image quality remains untouched.

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: Absolutely. Use the appropriate `Image.save` overload with `PngOptions` after editing—this is the standard way to **export PSD to PNG**.

**Q: What Java version is required?**  
A: Aspose.PSD for Java supports JDK 8 and later.

**Q: How do I release resources after processing?**  
A: Call `psdImage.dispose()` and close any streams to free native resources.

---

**Terakhir Diperbarui:** 2026-02-17  
**Diuji Dengan:** Aspose.PSD for Java (rilisan terbaru)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}