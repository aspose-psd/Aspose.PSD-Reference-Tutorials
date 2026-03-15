---
date: 2026-03-15
description: Pelajari cara memfilter gambar PNG menggunakan Aspose.PSD untuk Java.
  Panduan langkah demi langkah ini mencakup optimasi PNG di Java dan mengonversi PSD
  ke PNG dengan tipe filter.
linktitle: How to Filter PNG Files in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Cara Menyaring File PNG di Aspose.PSD untuk Java
url: /id/java/optimizing-png-files/apply-filters-png-files/
weight: 10
---

 Fix. Should translate those headings? The instruction says translate all text content. Table headers are text, so translate them. Keep the pipe separators.

Also bullet lists.

Let's produce final translation.

Be careful: The "Quick Answers" bullet list includes question sentences; translate them but keep code formatting like **...**. Keep bold.

Also keep URLs unchanged.

Also keep "## Introduction" etc.

Now produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Memfilter File PNG di Aspose.PSD untuk Java

## Pendahuluan
Jika Anda bertanya‑tanya **cara memfilter PNG** saat bekerja dengan Java, Anda berada di tempat yang tepat. Pada tutorial ini kami akan menjelaskan cara menerapkan tipe filter PNG dengan Aspose.PSD untuk Java, sebuah pustaka yang juga membantu Anda **mengonversi PSD ke PNG** dan melakukan **optimasi png java**. Pada akhir tutorial Anda akan dapat menyesuaikan kompresi, meningkatkan kualitas visual, dan mengintegrasikan proses ini ke dalam proyek Java apa pun.

## Jawaban Cepat
- **Pustaka apa yang mendukung pemfilteran PNG di Java?** Aspose.PSD untuk Java.  
- **Filter mana yang memberikan kompresi terbaik untuk kebanyakan gambar?** Filter Paeth (digunakan dalam contoh ini).  
- **Apakah saya memerlukan lisensi untuk menjalankan kode?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi diperlukan untuk produksi.  
- **Bisakah saya mengonversi PSD ke PNG dalam alur kerja yang sama?** Ya – muat PSD dan simpan sebagai PNG dengan filter yang diinginkan.  
- **Versi Java apa yang diperlukan?** Java 8 atau yang lebih baru.

## Apa itu “cara memfilter png” dalam praktik?
Memfilter file PNG berarti memilih algoritma pra‑pemrosesan yang menyiapkan data piksel sebelum kompresi. Tipe filter memengaruhi ukuran file dan seberapa baik warna dipertahankan setelah PNG disimpan. Aspose.PSD memberi Anda kontrol langsung atas langkah ini melalui metode `PngOptions.setFilterType`.

## Mengapa menggunakan Aspose.PSD untuk Java dalam optimasi PNG?
- **Dukungan PSD lengkap:** Buka, edit, dan ekspor lapisan PSD tanpa kehilangan fidelitas.  
- **Pemilihan filter bawaan:** Pilih antara Paeth, Sub, Up, Average, atau None.  
- **Lintas‑platform:** Berfungsi di Windows, Linux, dan macOS dengan JDK standar apa pun.  
- **Tanpa ketergantungan native eksternal:** Implementasi murni Java mempermudah penyebaran.

## Prasyarat
1. **Java Development Kit (JDK) 8+** – pastikan `java -version` menampilkan 1.8 atau lebih tinggi.  
2. **IDE (IntelliJ IDEA, Eclipse, atau VS Code)** – lingkungan apa pun yang Anda sukai.  
3. **Pustaka Aspose.PSD untuk Java** – unduh dari [sini](https://releases.aspose.com/psd/java/).  
4. **Pengetahuan dasar Java** – familiar dengan kelas, metode, dan I/O file.

## Impor Paket
Pertama, masukkan kelas Aspose.PSD yang diperlukan ke dalam file Java Anda:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngFilterType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

> **Tips profesional:** Tambahkan JAR Aspose.PSD ke jalur build proyek Anda atau ke dependensi Maven/Gradle agar impor dapat diselesaikan tanpa error.

## Langkah 1: Siapkan Direktori Dokumen
Tentukan folder yang berisi PSD sumber Anda dan tempat PNG yang telah difilter akan disimpan.

```java
String dataDir = "Your Document Directory"; // Adjust this path
```

Ganti `"Your Document Directory"` dengan jalur absolut atau relatif di mesin Anda.

## Langkah 2: Muat Gambar PSD
Buka file PSD yang ingin Anda proses. Casting ke `PsdImage` memberi Anda kemampuan khusus PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Jika file tidak ditemukan, `Image.load` akan melempar exception – pastikan jalurnya benar.

## Langkah 3: Buat Opsi PNG (Optimasi PNG Java)
Konfigurasikan pengaturan ekspor PNG, termasuk tipe filter yang secara langsung menjawab **cara memfilter png**.

```java
PngOptions options = new PngOptions();
options.setFilterType(PngFilterType.Paeth);
```

Anda dapat bereksperimen dengan tipe filter lain (`Sub`, `Up`, `Average`, `None`) untuk melihat bagaimana mereka memengaruhi ukuran dan kualitas. Langkah ini juga menggambarkan **optimasi png java** karena filter yang dipilih memengaruhi efisiensi kompresi.

## Langkah 4: Simpan Gambar PNG
Akhirnya, tulis gambar yang telah diproses kembali ke disk menggunakan opsi yang telah Anda definisikan.

```java
psdImage.save(dataDir + "ApplyFilterMethod_out.png", options);
```

File yang dihasilkan, `ApplyFilterMethod_out.png`, akan menjadi PNG yang telah difilter siap pakai untuk web atau desktop.

## Masalah Umum dan Solusinya
| Gejala | Penyebab Kemungkinan | Solusi |
|--------|----------------------|--------|
| `FileNotFoundException` | Jalur `dataDir` salah | Pastikan string direktori diakhiri dengan pemisah (`/` atau `\\`). |
| Tidak ada efek filter terlihat | Menggunakan `PngFilterType.None` | Ganti ke `Paeth` atau tipe filter lain. |
| Error out‑of‑memory pada PSD besar | Memuat file besar tanpa streaming | Gunakan `PsdImage` dengan `loadOptions` untuk membatasi penggunaan memori. |

## Pertanyaan yang Sering Diajukan

**T: Apa itu Aspose.PSD untuk Java?**  
J: Aspose.PSD untuk Java adalah API kuat yang memungkinkan pengembang membaca, mengedit, dan mengonversi file PSD, menerapkan filter, serta melakukan optimasi gambar tanpa memerlukan Adobe Photoshop.

**T: Bagaimana cara mengunduh Aspose.PSD untuk Java?**  
J: Anda dapat mengunduhnya dari halaman rilis Aspose [sini](https://releases.aspose.com/psd/java/).

**T: Bisakah saya mencoba Aspose.PSD secara gratis?**  
J: Ya, versi percobaan gratis tersedia [sini](https://releases.aspose.com/).

**T: Jenis filter apa yang dapat saya terapkan pada gambar PNG?**  
J: Aspose.PSD mendukung Paeth, Sub, Up, Average, dan None. Pilih yang paling cocok antara ukuran dan fidelitas visual.

**T: Di mana saya dapat menemukan dukungan untuk masalah Aspose.PSD?**  
J: Anda dapat mendapatkan bantuan dengan mengunjungi Forum Aspose [sini](https://forum.aspose.com/c/psd/34).

## Kesimpulan
Anda kini mengetahui **cara memfilter file PNG** menggunakan Aspose.PSD untuk Java, cara **mengonversi PSD ke PNG**, dan cara melakukan **optimasi png java** dengan berbagai tipe filter. Bereksperimenlah dengan berbagai filter, integrasikan alur kerja ini ke dalam pipeline pemrosesan gambar Anda, dan nikmati aset PNG yang lebih kecil dengan kualitas tinggi.

---

**Terakhir Diperbarui:** 2026-03-15  
**Diuji Dengan:** Aspose.PSD untuk Java 24.10  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}