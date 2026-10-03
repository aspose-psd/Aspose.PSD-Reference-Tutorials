---
date: 2026-10-03
description: Pelajari cara mengekstrak thumbnail dari PSD di Java menggunakan Aspose.PSD.
  Panduan langkah demi langkah ini mencakup penyiapan, potongan kode, dan menyimpan
  thumbnail sebagai gambar JPEG.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Ekstrak thumbnail dari PSD di Java
og_description: Pelajari cara mengekstrak thumbnail dari PSD di Java dengan Aspose.PSD.
  Panduan ini memandu Anda melalui penyiapan, memuat file, mengekstrak thumbnail,
  dan menyimpan sebagai gambar JPEG.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Ekstrak thumbnail dari PSD di Java menggunakan Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Ekstrak thumbnail dari PSD di Java
url: /id/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekstrak thumbnail dari PSD di Java

## Pendahuluan
Mengekstrak thumbnail dari file PSD memungkinkan Anda menghasilkan pratinjau cepat tanpa memuat gambar beresolusi penuh. Di Java, Aspose.PSD membuat proses ini sederhana dan berperforma tinggi. Dalam tutorial ini Anda akan belajar cara menyiapkan pustaka, menemukan sumber thumbnail, dan menyimpannya sebagai file JPEG—semua dengan hanya beberapa baris kode.

## Jawaban Cepat
- **Library mana yang menangani thumbnail PSD?** Aspose.PSD untuk Java.  
- **Berapa banyak baris kode yang diperlukan?** Sekitar lima baris untuk memuat, mengekstrak, dan menyimpan.  
- **Bisakah saya mengekstrak thumbnail dari file PSD besar?** Ya, Aspose.PSD memproses file hingga 500 MB tanpa memuat seluruh memori.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi diperlukan untuk produksi.  
- **Format output apa yang didukung?** Thumbnail yang diekstrak dapat disimpan sebagai JPEG, PNG, atau BMP.

## Apa itu ekstrak thumbnail dari PSD?
Ekstrak thumbnail dari PSD adalah proses membaca gambar pratinjau kecil yang tertanam di dalam dokumen Photoshop (PSD). Pratinjau ini disimpan sebagai sumber daya dan dapat disimpan secara terpisah untuk keperluan katalog atau tampilan. Thumbnail biasanya merupakan representasi beresolusi rendah yang digunakan aplikasi untuk menampilkan ringkasan visual cepat tanpa memuat gambar berukuran penuh.

## Mengapa menggunakan Aspose.PSD untuk tugas ini?
Aspose.PSD mendukung **lebih dari 30 format gambar** dan dapat menangani file PSD hingga **500 MB** sambil menjaga penggunaan memori tetap rendah karena membaca sumber daya sesuai permintaan. API juga menyediakan penanganan error yang kuat, sehingga Anda dapat mengekstrak thumbnail secara andal bahkan dari file yang rusak.

## Prasyarat
- Java Development Kit (JDK) terinstal.  
- Pustaka Aspose.PSD untuk Java diunduh dari [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).  
- Familiaritas dasar dengan sintaks Java dan penyiapan proyek.

## Bagaimana cara mengekstrak thumbnail dari file PSD di Java?
Muat file PSD dengan `PsdImage`, temukan `ThumbnailResource`, dan simpan data gambar sebagai JPEG. Aspose.PSD menyederhanakan parsing tingkat rendah, sehingga Anda hanya perlu memanggil `getResources()` dan kemudian `save()` pada gambar yang diekstrak. Pendekatan ini bekerja untuk semua PSD yang berisi thumbnail, terlepas dari ukuran file.

## Impor paket
`Image` adalah kelas dasar untuk memuat gambar. `PsdImage` mewakili dokumen PSD. `ThumbnailResource` dan `Thumbnail4Resource` mewakili sumber daya thumbnail. `JpegOptions` menentukan opsi penyimpanan JPEG.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Langkah 1: muat file PSD
Pertama, buat instance `PsdImage` yang menunjuk ke file PSD Anda. Konstruktor hanya membaca header dan sumber daya yang diperlukan, sehingga penggunaan memori tetap minimal.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Ganti `"Your_Document_Directory/"` dengan path direktori tempat file PSD Anda berada, dan `"your_file.psd"` dengan nama file PSD Anda.

## Langkah 2: iterasi sumber daya gambar
Aspose.PSD menyimpan thumbnail sebagai objek `ThumbnailResource` di dalam koleksi sumber daya gambar. Lakukan loop melalui koleksi, periksa tipe sumber daya, dan ambil thumbnail pertama yang Anda temui.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Langkah 3: simpan thumbnail yang diekstrak
Setelah Anda memiliki gambar thumbnail, panggil metode `save`-nya untuk menulisnya ke disk. Anda dapat memilih JPEG, PNG, atau BMP; JPEG paling umum untuk pratinjau web.

## Langkah 4: menangani berbagai tipe thumbnail
Jika sebuah PSD berisi beberapa varian thumbnail, seperti `Thumbnail4Resource`, perpanjang logika iterasi untuk memeriksa setiap tipe. API menyediakan kelas terpisah untuk setiap sumber daya, memungkinkan Anda memilih resolusi yang dibutuhkan.

## Masalah umum dan solusi
- **Thumbnail tidak ditemukan:** Tidak semua file PSD menyertakan pratinjau. Verifikasi file sumber di panel “File → File Info” Photoshop.  
- **Error format tidak didukung:** Pastikan Anda menggunakan versi Aspose.PSD terbaru; rilis lama mungkin tidak mendukung tipe sumber daya thumbnail yang baru.  
- **Kehabisan memori pada file besar:** Gunakan `PsdImage.load(..., LoadOptions)` dengan `LoadOptions.setLoadResourcesOnly(true)` untuk menghindari memuat data gambar lengkap ketika Anda hanya membutuhkan thumbnail.

## Pertanyaan yang sering diajukan

**Q: Apa itu Aspose.PSD?**  
A: Aspose.PSD adalah pustaka Java yang memungkinkan pembuatan, manipulasi, dan konversi programatik file PSD serta format gambar raster lainnya tanpa memerlukan Adobe Photoshop.

**Q: Di mana saya dapat menemukan dokumentasi lebih lanjut tentang Aspose.PSD untuk Java?**  
A: Anda dapat merujuk ke [dokumentasi](https://reference.aspose.com/psd/java/) untuk referensi API detail dan contoh.

**Q: Bisakah saya mencoba Aspose.PSD secara gratis sebelum membeli?**  
A: Ya, Anda dapat mengunduh [versi percobaan gratis](https://releases.aspose.com/) untuk mengevaluasi kemampuan pustaka.

**Q: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?**  
A: Lisensi sementara tersedia di halaman [lisensi sementara](https://purchase.aspose.com/temporary-license/).

**Q: Apakah Aspose.PSD cocok untuk penggunaan komersial?**  
A: Ya, Aspose.PSD dapat digunakan dalam proyek pribadi maupun komersial sesuai dengan ketentuan lisensinya.

---

**Terakhir Diperbarui:** 2026-10-03  
**Diuji Dengan:** Aspose.PSD for Java 24.12  
**Penulis:** Aspose

## Tutorial Terkait

- [Cara Mengonversi PSD ke Format Gambar Raster dengan Aspose.PSD untuk Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Simpan PSD sebagai JPEG dan Dukung Warna RGB dengan Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Ubah Ukuran Gambar dengan Aspose.PSD untuk Java – Menggambar Bentuk & Operasi Gambar Dasar](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}