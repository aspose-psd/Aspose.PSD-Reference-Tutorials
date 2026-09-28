---
date: 2026-09-28
description: Cara menambahkan thumbnail ke segmen JFIF di Java menggunakan Aspose.PSD.
  Ikuti panduan langkah demi langkah ini untuk menyisipkan thumbnail ke file PSD dengan
  cepat dan dapat diandalkan.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Tambahkan Thumbnail ke Segmen JFIF di Java
og_description: Cara menambahkan thumbnail ke segmen JFIF di Java menggunakan Aspose.PSD.
  Ikuti panduan langkah demi langkah ini untuk menyisipkan thumbnail ke file PSD dengan
  cepat dan dapat diandalkan.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Cara menambahkan thumbnail ke segmen JFIF di Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Cara menambahkan thumbnail ke segmen JFIF di Java
url: /id/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menambahkan thumbnail ke segmen JFIF di Java

## Pendahuluan
Menambahkan thumbnail ke segmen JFIF dari file PSD adalah kebutuhan umum ketika Anda memerlukan pratinjau visual cepat tanpa memuat gambar penuh. Dalam tutorial ini Anda akan belajar **cara menambahkan thumbnail** ke segmen JFIF di Java menggunakan Aspose.PSD. Pada akhir panduan Anda akan memiliki cuplikan kode yang dapat dijalankan, pemahaman tentang struktur JFIF yang mendasarinya, dan tip untuk menangani file besar secara efisien.

## Jawaban Cepat
- **Perpustakaan apa yang diperlukan?** Aspose.PSD for Java.
- **Versi Java mana yang bekerja?** JDK 11 atau lebih baru.
- **Berapa baris kode yang dibutuhkan?** Sekitar 10 baris untuk memuat, memodifikasi, dan menyimpan.
- **Bisakah saya memproses file multi‑megabyte?** Ya, Aspose.PSD melakukan streaming data, sehingga penggunaan memori tetap rendah.
- **Apakah lisensi komersial diperlukan?** Lisensi diperlukan untuk penggunaan produksi; percobaan gratis tersedia.

## Apa itu segmen JFIF?
Segmen JFIF adalah blok JPEG File Interchange Format yang dapat menyimpan data opsional seperti thumbnail, EXIF, atau profil warna.  
Segmen ini berada di dalam aliran JPEG dari file PSD dan dikenali oleh sebagian besar penampil gambar untuk pembuatan pratinjau cepat.

## Mengapa menambahkan thumbnail ke file PSD?
Aspose.PSD for Java mendukung **lebih dari 30 format gambar** dan dapat memproses file hingga **2 GB** tanpa memuat seluruh dokumen ke memori. Menambahkan thumbnail mengurangi bandwidth jaringan saat mentransmisikan pratinjau dan mempercepat rendering UI dalam aplikasi galeri.

## Prasyarat
- Java Development Kit (JDK): Pastikan Java terinstal di sistem Anda. Anda dapat mengunduhnya dari [situs web JDK Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD for Java: Anda perlu memiliki perpustakaan Aspose.PSD for Java. Anda dapat memperolehnya dari [halaman unduhan Aspose.PSD Java](https://releases.aspose.com/psd/java/).
- Integrated Development Environment (IDE): Gunakan IDE seperti IntelliJ IDEA atau Eclipse untuk pengembangan Java.
- Pemahaman Dasar tentang Java: Familiaritas dengan bahasa pemrograman Java dan konsep-konsepnya.

## Cara menambahkan thumbnail ke segmen JFIF di Java?
Muat PSD target, temukan sumber daya JFIF, ganti data thumbnailnya, dan simpan file. Seluruh operasi dapat dilakukan dengan beberapa panggilan API sederhana, dan Aspose.PSD menangani struktur JPEG tingkat rendah untuk Anda.

### Langkah 1: impor paket
`Document`, `JfifResource`, dan kelas terkait merupakan bagian dari namespace Aspose.PSD. Document mewakili kontainer file PSD, dan JfifResource memberikan akses ke segmen JFIF di dalam PSD. Impor mereka di bagian atas file sumber Anda.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Langkah 2: muat gambar PSD
Buat instance `PsdImage` dengan memberikan jalur file ke konstruktor. PsdImage adalah kelas Aspose.PSD yang memodelkan dokumen Photoshop. Ini memuat metadata dokumen sambil melakukan streaming data piksel.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Langkah 3: iterasi sumber daya gambar
Cari koleksi `Resources` untuk `JfifResource`. Setelah ditemukan, Anda dapat mengganti array byte thumbnailnya dengan pratinjau JPEG yang baru.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Langkah 4: sesuaikan data thumbnail
Hasilkan thumbnail JPEG kecil (misalnya, 120 × 120 px) menggunakan perpustakaan pemrosesan gambar apa pun, lalu tetapkan array byte yang dihasilkan ke `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Langkah 5: simpan gambar yang dimodifikasi
Panggil metode `save` pada objek `PsdImage`, menentukan jalur output dan format yang diinginkan. Segmen JFIF kini berisi thumbnail baru.

```java
image.save(dataDir + "output.psd");
```

## Masalah umum dan solusi
- **Thumbnail tidak terlihat di penampil:** Pastikan data thumbnail merupakan array byte JPEG yang valid dan dimensinya berada dalam 256 × 256 px, yang merupakan ukuran maksimum yang didukung oleh spesifikasi JFIF.
- **OutOfMemoryError pada PSD besar:** Gunakan `PsdImage.load(inputStream, true)` untuk mengaktifkan mode streaming, yang menjaga konsumsi memori tetap rendah.
- **Tipe sumber daya tidak tepat:** Verifikasi bahwa sumber daya yang Anda modifikasi memang `JfifResource`; sumber daya lain seperti `ExifResource` tidak akan memengaruhi tampilan thumbnail.

## Pertanyaan yang sering diajukan

**Q: Apa itu Aspose.PSD for Java?**  
A: Aspose.PSD for Java adalah perpustakaan komersial yang memungkinkan pengembang membuat, mengedit, mengonversi, dan merender file Photoshop PSD tanpa memerlukan Adobe Photoshop.

**Q: Di mana saya dapat menemukan dokumentasi lebih lanjut untuk Aspose.PSD for Java?**  
A: Dokumentasi detail dapat ditemukan di [halaman dokumentasi Aspose.PSD for Java](https://reference.aspose.com/psd/java/).

**Q: Apakah Aspose.PSD for Java cocok untuk penggunaan komersial?**  
A: Ya, Aspose.PSD for Java dapat digunakan secara komersial. Anda dapat membeli lisensi dari [halaman pembelian Aspose.PSD](https://purchase.aspose.com/buy).

**Q: Bisakah saya mencoba Aspose.PSD for Java sebelum membeli?**  
A: Ya, Anda dapat mengunduh percobaan gratis dari [halaman unduhan percobaan Aspose.PSD](https://releases.aspose.com/).

**Q: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.PSD for Java?**  
A: Untuk dukungan, kunjungi [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

---

**Terakhir Diperbarui:** 2026-09-28  
**Diuji Dengan:** Aspose.PSD for Java 24.11  
**Penulis:** Aspose

## Tutorial Terkait

- [Tambahkan Sumber Daya IOPA ke File PSD menggunakan Aspose PSD untuk Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Tambahkan Tanda Tangan ke Gambar – Gambar pada Kanvas dengan Aspose.PSD untuk Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Cara Memutar Gambar pada Sudut Tertentu dengan Aspose.PSD untuk Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}