---
date: 2025-12-13
description: Pelajari cara membuat objek grafik PSD dan memanipulasi lapisan PSD dengan
  menangani aliran gambar tidak terkompresi menggunakan Aspose.PSD untuk Java.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Buat Objek Grafik PSD – Aliran Tidak Terkompresi di Java
url: /id/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Membuat Objek Grafik PSD – Stream Tidak Terkompresi di Java

## Introduction
Selamat datang di dunia manipulasi gambar dengan Java! Pada tutorial ini Anda akan **membuat objek grafik PSD** dan menangani objek stream gambar tidak terkompresi menggunakan Aspose.PSD for Java. Baik Anda seorang desainer grafis yang ingin mengotomatisasi alur kerja atau pengembang perangkat lunak yang ingin mengintegrasikan kemampuan pemrosesan gambar yang kuat ke dalam aplikasi, panduan ini dirancang khusus untuk Anda. Kami akan membahas semua hal mulai dari prasyarat hingga kesimpulan, memastikan Anda memiliki pemahaman yang solid tentang cara memulai dengan Aspose.PSD.

## Quick Answers
- **Apa arti “create PSD graphics object”?** Itu merujuk pada pembuatan konteks grafik untuk file PSD sehingga Anda dapat menggambar atau mengedit isinya.  
- **Perpustakaan mana yang menangani stream tidak terkompresi?** Aspose.PSD for Java menyediakan dukungan penuh untuk data gambar mentah (tidak terkompresi).  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis cukup untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya memanipulasi lapisan PSD setelah membuat objek grafik?** Ya – instance Graphics memungkinkan Anda menggambar pada lapisan mana pun.  

## Prerequisites
Sebelum kita melompat ke kode, pastikan Anda memiliki semua yang diperlukan untuk memulai perjalanan ini. Berikut adalah prasyaratnya:

### Java Development Kit (JDK)
Pastikan JDK terpasang di mesin Anda. Anda dapat mengunduhnya dari situs web Oracle atau menggunakan OpenJDK.

### Aspose.PSD for Java
Anda perlu mengunduh dan menginstal perpustakaan Aspose.PSD. Perpustakaan yang kuat ini memungkinkan Anda memanipulasi file PSD dengan mudah. Dapatkan versi terbaru dari [tautan ini](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Sebaiknya gunakan IDE untuk menulis dan menguji kode Java Anda. Anda dapat memakai IntelliJ IDEA, Eclipse, atau IDE lain yang Anda sukai.

### Basic Understanding of Java
Pemahaman dasar tentang pemrograman Java akan membuat proses ini lebih lancar. Pastikan Anda mengerti konsep dasar seperti kelas, metode, dan penanganan pengecualian.

Dengan semua persiapan selesai, mari kita gulung lengan dan masuk ke bagian yang menarik – menulis kode!

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
Sebelum mulai menulis kode, tentukan dulu di mana file PSD Anda berada. Ini pada dasarnya menyiapkan panggung untuk proyek Anda.

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur sebenarnya tempat file PSD Anda (misalnya layers.psd) berada. Ini membantu menemukan file Anda tanpa kesulitan.

## Step 2: Create a Byte Array Output Stream
Anda memerlukan tempat untuk menyimpan gambar yang telah dimodifikasi sebelum melakukan apa pun dengannya. `ByteArrayOutputStream` akan membantu Anda menangkap data gambar dengan mudah.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Baris ini menginisialisasi objek `ByteArrayOutputStream` baru bernama `ms`. Anda akan menggunakan objek ini untuk menyimpan gambar tidak terkompresi Anda.

## Step 3: Load the PSD File
Sekarang saatnya memuat file PSD yang sebenarnya. Di sinilah keajaiban dimulai!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Baris ini memuat file PSD Anda ke dalam objek `PsdImage`. Pastikan jalurnya benar; jika tidak, akan muncul error seperti kuis tak terduga.

## Step 4: Set Up the PsdOptions for Saving
Anda perlu menentukan cara menyimpan gambar — tentu saja tidak terkompresi!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Di sini, Anda membuat objek `PsdOptions` dan mengatur metode kompresi ke `Raw`. Metode ini memastikan gambar mempertahankan kualitas penuh dan disimpan tanpa kompresi.

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

Baris ini menyimpan gambar yang telah dimodifikasi ke dalam `ByteArrayOutputStream` yang Anda buat pada Langkah 2, menggunakan opsi yang didefinisikan pada Langkah 4. Metode `save` menangani enkoding gambar secara tepat berdasarkan pengaturan Anda.

## Step 6: Reset the Output Stream
Setelah menyimpan, stream output berada di akhir. Anda perlu meresetnya agar dapat dibaca dari awal.

```java
ms.reset();
```

Metode `reset` ini menyiapkan `ByteArrayOutputStream` Anda untuk dibaca kembali dari awal. Anggap saja seperti memutar ulang pita sebelum mendengarkan lagu favorit Anda!

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Di sini, kami memuat kembali gambar dari `ByteArrayOutputStream` ke dalam objek `PsdImage` baru. Ini memungkinkan Anda memeriksa hasil kerja sebelumnya.

## Step 8: Create Graphics Object
Untuk memodifikasi atau merender gambar lebih lanjut, Anda perlu membuat objek grafik.

```java
Graphics graphics = new Graphics(psdImage);
```

Baris ini menginisialisasi objek `Graphics` menggunakan `psdImage` Anda. Sekarang Anda dapat menggunakan objek grafik ini untuk menggambar atau memanipulasi gambar sesuai kebutuhan. Seperti memegang kuas cat di tangan!

## Manipulate PSD Layers with Graphics Object
Setelah Anda memiliki instance **Graphics**, Anda dapat **memanipulasi lapisan PSD**—misalnya, menggambar bentuk, menambahkan teks, atau menerapkan filter pada lapisan tertentu. Konteks grafik bekerja langsung pada data piksel yang mendasari, memberi Anda kontrol detail atas tampilan setiap lapisan.

## Common Issues and Solutions
- **NullPointerException saat memuat file** – periksa kembali jalur `dataDir` dan pastikan nama file sudah benar.  
- **Output tetap terkompresi meskipun menggunakan Raw** – pastikan `saveOptions.setCompressionMethod(CompressionMethod.Raw);` dipanggil sebelum metode `save`.  
- **Objek Graphics muncul kosong** – pastikan Anda menggambar pada instance `PsdImage` yang tepat (gunakan yang Anda muat, bukan yang baru dibuat kecuali memang diinginkan).

## FAQ's
### What is Aspose.PSD?
Aspose.PSD adalah perpustakaan .NET yang memungkinkan pengembang membuat, mengedit, dan memanipulasi file Photoshop PSD serta format gambar terkait secara programatik.

### How can I download Aspose.PSD for Java?
Anda dapat mengunduhnya dari [halaman rilis](https://releases.aspose.com/psd/java/).

### Is there a free trial for Aspose.PSD?
Ya, Anda dapat memperoleh versi percobaan gratis dari [sini](https://releases.aspose.com/).

### Can I get support for Aspose.PSD?
Tentu! Anda dapat mencari bantuan di [forum dukungan Aspose](https://forum.aspose.com/c/psd/34).

### How can I obtain a temporary license for Aspose.PSD?
Kunjungi [halaman lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk memulai.

## Frequently Asked Questions

**Q: Can I use the graphics object to edit only one specific layer?**  
A: Ya. Setelah memuat PSD, pilih lapisan yang diinginkan melalui `psdImage.getLayers().get_Item(index)` dan berikan ke konstruktor `Graphics`.

**Q: Does the Raw compression method affect file size?**  
A: Raw menyimpan data piksel tanpa kompresi, sehingga ukuran file akan lebih besar dibandingkan PSD terkompresi, tetapi kualitas gambar tetap tidak berubah.

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: Tentu. Gunakan overload `Image.save` yang sesuai dengan `PngOptions` setelah selesai mengedit.

**Q: What Java version is required?**  
A: Aspose.PSD for Java mendukung JDK 8 dan versi lebih baru.

**Q: How do I release resources after processing?**  
A: Panggil `psdImage.dispose()` dan tutup semua stream untuk membebaskan sumber daya native.

---  

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}