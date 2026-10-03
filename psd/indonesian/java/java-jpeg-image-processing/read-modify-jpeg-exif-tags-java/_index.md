---
date: 2026-10-03
description: Pelajari cara Java membaca metadata gambar dan memodifikasi tag JPEG
  EXIF dengan Aspose.PSD for Java dalam panduan langkah‑demi‑langkah ini, sempurna
  untuk pengembang yang menangani metadata gambar secara efisien.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Baca dan Modifikasi Tag JPEG EXIF di Java
og_description: Pelajari cara Java membaca metadata gambar dan memodifikasi tag JPEG
  EXIF dengan Aspose.PSD for Java. Panduan ini menampilkan kode langkah‑demi‑langkah
  untuk mengekstrak dan memperbarui informasi EXIF.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Cara Java Membaca Metadata Gambar dan Memodifikasi Tag JPEG EXIF
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Cara Java Membaca Metadata Gambar dan Memodifikasi Tag JPEG EXIF
url: /id/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Baca dan ubah tag EXIF JPEG di Java

## Pendahuluan
Jika Anda perlu **java read image metadata** dari file JPEG dan mengubahnya secara programatis, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan menjelaskan cara mengekstrak dan memperbarui tag EXIF menggunakan Aspose.PSD untuk Java. Pada akhir tutorial Anda akan dapat mengambil detail kamera, orientasi, dan bidang khusus, kemudian menuliskannya kembali ke file—semua tanpa editor grafis.

## Jawaban cepat
- **Perpustakaan mana yang menangani JPEG EXIF di Java?** Aspose.PSD for Java.
- **Berapa banyak baris kode untuk membaca EXIF?** About three lines after loading the image.
- **Bisakah Anda mengubah tag EXIF?** Yes, you can change any standard or custom tag and save the result.
- **Format gambar yang didukung?** Over 150 formats, including PSD, JPEG, PNG, TIFF, and BMP.
- **Versi Java minimum?** Java 7 or higher.

## Mengapa menggunakan Aspose.PSD untuk Java?
Aspose.PSD mendukung **lebih dari 150 format gambar** dan dapat memproses file hingga **2 GB** tanpa memuat seluruh dokumen ke memori, memberi Anda operasi metadata yang cepat dan menggunakan memori rendah pada koleksi foto besar. Ia juga menyediakan API sederhana untuk membaca dan menulis data EXIF, IPTC, dan XMP, menjadikan pemrosesan batch ribuan gambar menjadi efisien dan dapat diandalkan.

## Prasyarat
1. **Java Development Kit (JDK)** – pastikan Anda memiliki JDK 11 atau yang lebih baru. Anda dapat mengunduhnya dari [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – dapatkan JAR terbaru dari [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor apa pun yang Anda sukai.  
4. **Pengetahuan dasar Java** – Anda harus nyaman membuat proyek dan menambahkan JAR eksternal.

## Apa itu Java read image metadata?
Java read image metadata mengacu pada proses mengakses secara programatis informasi yang tertanam seperti EXIF, IPTC, dan XMP yang disimpan di dalam file gambar menggunakan kode Java. Metadata ini dapat mencakup pengaturan kamera, cap waktu, koordinat GPS, pemberitahuan hak cipta, dan komentar pengguna, memungkinkan aplikasi untuk mengatur, mencari, dan memanipulasi gambar berdasarkan data deskriptifnya.

## Impor paket
Pertama, tambahkan JAR Aspose.PSD ke classpath proyek Anda dan impor kelas yang diperlukan.

Paket `com.aspose.psd` menyediakan API inti untuk memuat gambar dan mengakses sumber dayanya.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Cara membaca metadata gambar dari file JPEG di Java?
Muat JPEG dengan `PsdImage.load("image.jpg")`, temukan sumber daya thumbnail yang menyimpan data EXIF, lalu panggil `ExifData.read()` untuk mendapatkan objek `ExifData` yang terisi. Pendekatan satu langkah ini memberi Anda akses penuh ke semua bidang EXIF standar dan tag khusus apa pun yang mungkin Anda tambahkan.

## Langkah 1: Muat gambar PSD
PsdImage adalah kelas Aspose.PSD yang mewakili file PSD dan menyediakan metode untuk mengakses sumber daya dan metadata-nya.  
Pada langkah ini, kami akan memuat gambar PSD dari mana kami ingin membaca data EXIF. Pastikan gambar Anda berada di direktori yang tepat.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Langkah 2: Iterasi sumber daya gambar
ThumbnailResource mewakili gambar thumbnail yang disimpan dalam file PSD, sering kali berisi data EXIF yang tertanam.  
Setelah gambar dimuat, langkah berikutnya adalah mengiterasi sumber dayanya untuk menemukan sumber daya thumbnail, yang biasanya berisi data EXIF.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Langkah 3: Ekstrak data EXIF
JpegExifData adalah kelas yang menyimpan informasi EXIF yang diekstrak dari gambar JPEG, memungkinkan Anda membaca dan mengubah tag individual.  
Sekarang setelah kami memiliki sumber daya thumbnail, kami dapat mengekstrak data EXIF darinya. Data EXIF mencakup informasi berharga seperti nama pemilik kamera, nilai aperture, orientasi, dan lainnya.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Langkah 4: Ubah data EXIF
Setelah membaca data EXIF, Anda mungkin ingin mengubah beberapa bidangnya. Berikut cara melakukannya:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Langkah 5: Simpan perubahan
Akhirnya, setelah mengubah data EXIF, simpan perubahan ke file PSD baru.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Masalah umum dan solusi
- **Sumber daya thumbnail tidak ada** – Beberapa JPEG menyimpan EXIF langsung di header gambar utama. Jika sumber daya thumbnail tidak ada, gunakan `image.getExifData()` sebagai gantinya.  
- **File besar menyebabkan OutOfMemoryError** – Pastikan Anda menjalankan JVM dengan heap yang cukup (`-Xmx2g`) atau memproses gambar dalam mode streaming menggunakan `PsdImage.load(inputStream, loadOptions)`.  
- **Tipe tag tidak didukung** – Aspose.PSD mendukung semua tag EXIF standar; tag khusus mungkin memerlukan penanganan tingkat byte secara manual.

## Pertanyaan yang sering diajukan

**Q: Apa itu data EXIF?**  
A: Metadata EXIF (Exchangeable Image File Format) menyimpan pengaturan kamera, cap waktu, koordinat GPS, dan informasi lain yang tertanam dalam file JPEG dan file gambar lainnya.

**Q: Bisakah saya menggunakan Aspose.PSD untuk Java secara gratis?**  
A: Anda dapat mendapatkan percobaan gratis dari [Aspose releases page](https://releases.aspose.com/).

**Q: Apakah Aspose.PSD untuk Java kompatibel dengan semua versi Java?**  
A: Aspose.PSD untuk Java mendukung Java SE 7 ke atas.

**Q: Di mana saya dapat menemukan dokumentasi lebih lanjut tentang Aspose.PSD untuk Java?**  
A: Lihat [documentation](https://reference.aspose.com/psd/java/) untuk detail lebih lanjut.

**Q: Bagaimana cara mendapatkan dukungan untuk Aspose.PSD untuk Java?**  
A: Anda dapat mendapatkan dukungan dari [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).

## Kesimpulan
Dengan mengikuti langkah‑langkah ini Anda dapat **java read image metadata** dari JPEG mana pun, menyesuaikan bidang EXIF yang Anda perlukan, dan menulis data yang diperbarui kembali ke file—semua dengan beberapa baris kode Java yang bersih. API kaya Aspose.PSD membuat penanganan metadata menjadi dapat diandalkan dan berperforma tinggi, sehingga Anda dapat mengintegrasikannya ke dalam pipeline pemrosesan batch, alat manajemen foto, atau aplikasi apa pun yang perlu bekerja dengan informasi gambar.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.5  
**Author:** Aspose

## Tutorial Terkait

- [Baca Informasi Tag EXIF Spesifik dalam Java dengan Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Buat Metadata XMP dalam File PSD Menggunakan Aspose.PSD untuk Java](/psd/java/image-editing/create-xmp-metadata/)
- [Ubah Ukuran Gambar dengan Aspose.PSD untuk Java – Gambar Bentuk & Operasi Gambar Dasar](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}