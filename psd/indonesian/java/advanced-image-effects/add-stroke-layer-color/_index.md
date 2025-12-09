---
date: 2025-11-30
description: Pelajari cara menambahkan goresan dan mengubah warna goresan PSD menggunakan
  Aspose.PSD untuk Java. Ikuti panduan langkah demi langkah ini untuk memodifikasi
  warna lapisan goresan dan opasitasnya.
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Cara Menambahkan Warna Lapisan Stroke di Aspose.PSD untuk Java
url: /id/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menambahkan Warna Lapisan Stroke di Aspose.PSD untuk Java

## Pendahuluan

Jika Anda perlu **cara menambahkan stroke** ke dokumen Photoshop secara programatis, Aspose.PSD untuk Java membuatnya menjadi mudah. Pada tutorial ini kami akan menjelaskan cara menambahkan warna lapisan stroke, menyesuaikan opasitasnya, dan menyimpan hasilnya. Pada akhir tutorial Anda juga akan melihat **cara mengubah warna stroke** (atau *mengubah warna stroke PSD*) untuk lapisan apa pun yang ada, memberi Anda kontrol kreatif penuh dari kode Java Anda.

## Jawaban Cepat
- **Perpustakaan apa yang dibutuhkan?** Aspose.PSD untuk Java (versi terbaru).  
- **Apakah saya dapat mengubah warna stroke?** Ya – gunakan `ColorFillSettings` untuk menetapkan warna apa pun (`Color`).  
- **Apakah saya memerlukan lisensi?** Lisensi sementara dapat digunakan untuk evaluasi; lisensi penuh diperlukan untuk produksi.  
- **Versi Java mana yang didukung?** Java 8 atau lebih tinggi.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk perubahan stroke dasar.

## Apa Itu Lapisan Stroke di PSD?
Lapisan stroke adalah efek vektor yang menggambar garis tepi di sekitar isi sebuah lapisan. Efek ini dapat disesuaikan dengan warna, ketebalan, opasitas, dan mode perpaduan. Memodifikasi efek ini secara programatis memungkinkan branding otomatis, pemrosesan batch, atau pembuatan grafik dinamis.

## Mengapa Menggunakan Aspose.PSD untuk Mengubah Warna Stroke?
- **Tidak memerlukan Photoshop** – bekerja sepenuhnya di Java.  
- **Kepatuhan penuh pada spesifikasi PSD** – semua fitur PSD modern didukung.  
- **Kinerja tinggi** – memproses file besar dengan cepat.  
- **Lintas‑platform** – dapat dijalankan di sistem operasi apa pun dengan JVM.

## Prasyarat

- **Perpustakaan Aspose.PSD** – unduh dari [dokumentasi resmi](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – versi 8 atau lebih baru.  
- **IDE** – Eclipse, IntelliJ IDEA, atau editor Java lain yang kompatibel.

## Mengimpor Paket

Pertama, impor kelas‑kelas yang diperlukan. Ini memberi proyek Anda akses ke API penanganan PSD dan efek stroke.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Langkah 1: Menyiapkan Proyek Anda

Buat proyek Java baru, tambahkan JAR Aspose.PSD ke jalur build, dan pastikan perpustakaan dimuat tanpa error.

## Langkah 2: Memuat File PSD

Aktifkan pemuatan sumber daya efek sehingga informasi stroke tersedia.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Langkah 3: Mengakses Lapisan Efek Stroke

Ambil efek stroke pertama dari lapisan kedua (indeks 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Langkah 4: Memvalidasi Properti Stroke

Konfirmasi properti yang ada sebelum melakukan perubahan. Ini membantu menghindari hasil yang tidak terduga.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Langkah 5: Menetapkan Warna dan Opasitas (Cara Mengubah Warna Stroke)

Di sini kami **mengubah warna stroke PSD** menjadi kuning dan mengurangi opasitas menjadi 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Langkah 6: Menyimpan PSD yang Telah Dimodifikasi

Tulis kembali gambar yang telah diperbarui ke disk. File baru kini berisi stroke yang telah dimodifikasi.

```java
im.save(exportPath);
```

## Kesalahan Umum & Tips

- **Pengecekan null** – selalu pastikan bahwa `getEffects()` mengembalikan array yang tidak null sebelum melakukan casting.  
- **Indeks lapisan** – lapisan PSD menggunakan indeks berbasis nol; pastikan Anda menargetkan lapisan yang tepat.  
- **Format warna** – `Color.getYellow()` hanya contoh; Anda dapat membuat warna kustom dengan `new Color(r, g, b)`.  
- **Rentang opasitas** – opasitas adalah byte (0–255); nilai di atas 255 akan dipotong.

## Kesimpulan

Anda kini telah mempelajari **cara menambahkan stroke** ke file PSD dan **cara mengubah warna stroke** menggunakan Aspose.PSD untuk Java. Bereksperimenlah dengan warna, mode perpaduan, dan opasitas yang berbeda untuk mencapai gaya visual yang tepat bagi proyek Anda.

## Pertanyaan yang Sering Diajukan

**T: Apakah saya dapat menggunakan Aspose.PSD bersama perpustakaan grafis Java lainnya?**  
J: Ya, Aspose.PSD dapat digabungkan dengan perpustakaan seperti Apache Commons Imaging atau Java2D untuk fungsionalitas tambahan.

**T: Apakah Aspose.PSD kompatibel dengan format file PSD terbaru?**  
J: Tentu saja. Perpustakaan ini secara rutin diperbarui untuk mendukung spesifikasi Photoshop terbaru.

**T: Bagaimana cara menangani pengecualian saat menggunakan Aspose.PSD?**  
J: Lihat [forum dukungan](https://forum.aspose.com/c/psd/34) untuk pemecahan masalah detail dan contoh kode penanganan error.

**T: Bisakah saya mencoba Aspose.PSD sebelum membeli?**  
J: Tentu! Dapatkan [versi percobaan gratis](https://releases.aspose.com/) untuk menjelajahi semua fitur.

**T: Di mana saya dapat memperoleh lisensi sementara untuk Aspose.PSD?**  
J: Dapatkan [lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk mengevaluasi perpustakaan di lingkungan pengembangan Anda.

---

**Terakhir Diperbarui:** 2025-11-30  
**Diuji Dengan:** Aspose.PSD 24.11 untuk Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}