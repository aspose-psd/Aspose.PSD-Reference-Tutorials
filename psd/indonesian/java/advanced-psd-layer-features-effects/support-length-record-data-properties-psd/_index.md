---
date: 2026-09-23
description: Pelajari cara memodifikasi bentuk vektor PSD dan memproses file PSD secara
  batch menggunakan Aspose.PSD untuk Java. Langkah‑langkah terperinci, tip, dan placeholder
  kode untuk solusi lengkap.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Dukungan Properti Data Record Panjang dalam PSD - Java
og_description: Pelajari cara memodifikasi bentuk vektor PSD dan memproses file PSD
  secara batch menggunakan Aspose.PSD untuk Java. Panduan langkah demi langkah dengan
  placeholder kode dan tip ahli.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Modifikasi bentuk vektor PSD dengan Aspose.PSD untuk Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Modifikasi bentuk vektor PSD dengan Aspose.PSD untuk Java
url: /id/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifikasi Bentuk Vektor PSD dengan Aspose.PSD untuk Java

## Pendahuluan
Jika Anda perlu **memodifikasi bentuk vektor PSD** secara programatis, Aspose.PSD untuk Java memberi Anda kontrol penuh atas file Photoshop langsung dari kode Java Anda. Tutorial ini memandu Anda melalui dukungan properti rekaman panjang—langkah penting saat mengedit lapisan bentuk vektor. Pada akhir tutorial, Anda akan dapat membuka PSD, menyesuaikan data bentuk vektornya, dan menyimpan file yang diperbarui tanpa pernah membuka Photoshop.

## Jawaban Cepat
- **Apa arti “modify PSD vector shapes”?** Menyesuaikan geometri, operasi jalur, atau atribut lain dari lapisan berbasis vektor di dalam file PSD.  
- **Perpustakaan mana yang menangani ini?** Aspose.PSD untuk Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk produksi.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk skrip modifikasi bentuk dasar.  
- **Apa prasyarat utama?** Java JDK, Aspose.PSD untuk Java, dan file PSD contoh.

## Apa itu “mendukung properti rekaman panjang”?
Mendukung properti rekaman panjang berarti mengakses dan memperbarui objek `LengthRecord` yang menggambarkan setiap jalur vektor di dalam PSD. Rekaman ini menyimpan informasi seperti panjang jalur, tipe, dan cara bergabung dengan jalur lain. Mengubahnya memungkinkan Anda mengontrol bagaimana bentuk digabungkan, berpotongan, atau dikurangkan satu sama lain, sehingga memungkinkan penyuntingan vektor yang presisi.

## Mengapa menggunakan Aspose.PSD untuk Java untuk mendukung properti rekaman panjang?
Muat PSD Anda, edit data vektor, dan simpan—semua tanpa Photoshop. Aspose.PSD memproses PSD berukuran ratusan halaman dalam kurang dari 2 detik pada server tipikal, menawarkan lebih dari 150 kelas (termasuk lebih dari 30 tipe terkait vektor), dan berjalan di Windows, Linux, atau macOS dengan JDK 11+ apa pun. Perpustakaan yang berfokus pada kinerja ini menghilangkan kebutuhan akan perangkat lunak desktop yang mahal.

## Prasyarat
1. **Java Development Kit (JDK)** – unduh dari [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) atau gunakan manajer paket pilihan Anda.  
2. **Aspose.PSD untuk Java** – dapatkan JAR terbaru dari [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor kompatibel Java apa pun.  
4. **File PSD** – buat satu di Photoshop atau ambil contoh PSD untuk bereksperimen.  
5. **Pengetahuan Java dasar** – familiaritas dengan kelas, objek, dan penanganan pengecualian.

## Impor paket
Pernyataan impor membawa kelas inti Aspose.PSD ke dalam ruang lingkup, seperti `PsdImage`, `VsmsResource`, dan `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Langkah 1: Siapkan direktori sumber dan output Anda
Tentukan di mana PSD asli berada dan di mana file yang dimodifikasi akan ditulis.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Langkah 2: Muat file PSD
Gunakan `Image.load` untuk membuka file dan cast ke `PsdImage` untuk fitur khusus PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Langkah 3: Temukan sumber Vsms di lapisan
`VsmsResource` adalah kontainer yang menyimpan data bentuk vektor untuk sebuah lapisan. Loop melalui sumber daya lapisan kedua untuk menemukannya.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Langkah 4: Akses rekaman panjang
`LengthRecord` mewakili jalur vektor yang terpisah. Ambil rekaman yang ingin Anda modifikasi.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Langkah 5: Modifikasi properti operasi jalur
`PathOperations` menentukan bagaimana bentuk individual berinteraksi (mis., eksklusi, interseksi, pengurangan). Mengubah nilai ini memperbarui komposisi visual lapisan vektor.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Langkah 6: Simpan file PSD yang dimodifikasi
Persist perubahan Anda ke file baru.

```java
psdImage.save(outPsdFilePath);
```

## Langkah 7: Bersihkan sumber daya
Dispose instance `PsdImage` untuk membebaskan memori dan menghindari kebocoran sumber daya.

```java
psdImage.dispose();
```

## Cara memproses batch file PSD dengan mendukung properti rekaman panjang
Bungkus alur kerja satu‑file dalam loop yang mengiterasi direktori PSD, memperbarui `inPsdFilePath` dan `outPsdFilePath` untuk setiap file. Pendekatan ini memungkinkan Anda menerapkan penyesuaian bentuk vektor yang identik ke puluhan atau ratusan file dalam hitungan menit, ideal untuk pipeline aset otomatis.

## Kesulitan umum & tips
- **Pemeriksaan null** – selalu pastikan `resource` tidak `null` sebelum mengakses anggotanya.  
- **Batas indeks jalur** – pastikan indeks yang Anda gunakan (mis., `[2]`, `[7]`, `[11]`) ada untuk PSD spesifik yang sedang Anda edit.  
- **Lisensi** – menjalankan tanpa lisensi yang valid akan menambahkan watermark pada PSD yang disimpan.

## Kesimpulan
Anda kini memiliki contoh lengkap end‑to‑end tentang cara **memodifikasi bentuk vektor PSD** dengan mendukung properti rekaman panjang menggunakan Aspose.PSD untuk Java. Baik Anda mengotomatisasi pipeline aset atau membangun alat desain khusus, API ini memberi fleksibilitas untuk memanipulasi lapisan vektor tanpa pekerjaan manual di Photoshop. Bereksperimenlah dengan nilai `PathOperations` lain atau gabungkan beberapa edit `LengthRecord` untuk membuat bentuk kompleks.

## Pertanyaan yang Sering Diajukan

**Q: Bagaimana saya menangani PSD yang tidak mengandung lapisan bentuk vektor?**  
A: `VsmsResource` tidak akan ada, sehingga `resource` tetap `null`. Tambahkan pemeriksaan dan lewati langkah modifikasi atau beri tahu pengguna.

**Q: Bisakah saya mengubah properti lain seperti warna isi atau lebar garis?**  
A: Ya, `LengthRecord` menyediakan setter untuk isi, garis, dan opasitas. Lihat dokumentasi API untuk daftar lengkapnya.

**Q: Apakah memungkinkan memproses batch beberapa file PSD?**  
A: Tentu saja. Bungkus kode di dalam loop yang mengiterasi direktori file PSD, menyesuaikan jalur input dan output setiap kali.

**Q: Apakah saya perlu menutup stream secara manual saat memuat dari jalur file?**  
A: `Image.load` menangani stream file secara otomatis, tetapi jika Anda memuat dari `InputStream`, ingatlah untuk menutupnya setelah penggunaan.

**Q: Versi Aspose.PSD apa yang diperlukan untuk API ini?**  
A: Kelas `LengthRecord` dan `PathOperations` telah tersedia sejak Aspose.PSD 20.10. Menggunakan versi terbaru (24.11 pada saat penulisan) disarankan.

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Tutorial Terkait

- [Konversi PSD ke PNG dan Buat Masker Vektor Java – Sumber Daya Vmsk dalam File PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Konversi PSD ke PNG dengan Dukungan Masker Lapisan Menggunakan Aspose.PSD untuk Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Tambahkan Dukungan Lapisan pada File PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}