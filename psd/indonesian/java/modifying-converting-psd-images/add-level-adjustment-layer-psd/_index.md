---
date: 2026-03-07
description: Pelajari cara menyesuaikan level dengan menambahkan Layer Penyesuaian
  Level dalam file PSD menggunakan Aspose.PSD untuk Java. Kuasai penyesuaian tonal
  dengan cepat.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Cara Menyesuaikan Levels – Tambahkan Layer Penyesuaian Level di PSD
url: /id/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tambahkan Layer Penyesuaian Level di PSD

## Pendahuluan
Jika Anda ingin **cara menyesuaikan level** dalam dokumen Photoshop Anda, Layer Penyesuaian Level adalah alat yang sempurna. Ini memungkinkan Anda menyesuaikan bayangan, nada tengah, dan sorotan secara halus tanpa mengubah piksel asli secara permanen. Dalam tutorial ini kami akan menunjukkan cara menambahkan Layer Penyesuaian Level ke file PSD menggunakan Aspose.PSD for Java, sehingga Anda dapat mencapai kontrol tonal kelas profesional dalam beberapa langkah saja.

## Jawaban Cepat
- **Apa yang dilakukan Layer Penyesuaian Level?** Ini mengubah rentang tonal gambar secara non‑destruktif.  
- **Perpustakaan mana yang digunakan?** Aspose.PSD for Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi diperlukan untuk produksi.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk penyesuaian dasar.  
- **Bisakah saya menyesuaikan beberapa saluran?** Ya, Anda dapat mengatur level input/output untuk setiap saluran warna secara terpisah.

## Apa itu Layer Penyesuaian Level?
Layer Penyesuaian Level memungkinkan Anda memperbaiki keseimbangan tonal sebuah gambar dengan menyesuaikan bayangan input, nada tengah, dan sorotan serta level output. Karena berada pada lapisan terpisah, Anda dapat mengubah visibilitasnya atau menghapusnya tanpa memengaruhi karya seni di bawahnya.

## Mengapa menambahkan Layer Penyesuaian Level dengan Aspose.PSD?
- **Otomatisasi:** Mengintegrasikan penyesuaian level ke dalam pipeline pemrosesan batch.  
- **Lintas‑platform:** Berfungsi pada semua OS yang mendukung Java.  
- **Presisi:** Mengakses pengaturan setiap saluran secara programatik untuk hasil yang tepat.  

## Prasyarat
1. Java Development Kit (JDK). Jika Anda belum memilikinya, unduh dari [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) atau gunakan OpenJDK.  
2. Perpustakaan Aspose.PSD for Java – dapatkan JAR terbaru dari [download link](https://releases.aspose.com/psd/java/).  
3. Pengetahuan dasar pemrograman Java.  
4. IDE seperti IntelliJ IDEA, Eclipse, atau NetBeans dengan JAR Aspose.PSD yang ditambahkan ke classpath proyek.

## Impor Paket
Sebelum kita mulai menulis kode, kita perlu mengimpor paket-paket yang diperlukan dari perpustakaan Aspose.PSD. Berikut cara melakukannya:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Impor ini memberi kita akses ke kelas untuk memuat file PSD, bekerja dengan layer penyesuaian level, dan memanipulasi pengaturan masing‑masing saluran.

## Cara Menyesuaikan Level dalam File PSD
Berikut adalah panduan langkah demi langkah yang menunjukkan **cara menyesuaikan level** secara programatik.

### Langkah 1: Siapkan Jalur File Anda
Tentukan di mana PSD sumber berada dan di mana file yang telah diedit akan disimpan.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Ganti `"Your Document Directory"` dengan folder sebenarnya di mesin Anda.

### Langkah 2: Muat File PSD
Buat instance `PsdImage` dari file sumber.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Sekarang Anda memiliki akses penuh ke semua lapisan di dalam PSD.

### Langkah 3: Iterasi Melalui Lapisan
Temukan Layer Penyesuaian Level yang ingin Anda ubah.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
Pemeriksaan `instanceof LevelsLayer` memastikan kita hanya bekerja dengan layer penyesuaian level.

### Langkah 4: Sesuaikan Pengaturan Saluran Level
Sesuaikan nilai input dan output untuk saluran yang dipilih.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Level Input Midtone:** Menggeser rentang nada tengah.  
- **Level Input Shadow:** Mengeraskan atau mencerahkan bayangan.  
- **Level Input Highlight:** Mengontrol bagian paling terang.  
- **Level Output Shadow/Highlight:** Menentukan rentang output akhir.

Silakan bereksperimen dengan nilai yang berbeda untuk melihat bagaimana mereka memengaruhi gambar.

### Langkah 5: Simpan File PSD yang Dimodifikasi
Simpan perubahan Anda ke file baru.
```java
im.save(psdPathAfterChange);
```
Anda akan menemukan PSD yang diperbarui di lokasi yang Anda tentukan dalam `psdPathAfterChange`.

## Masalah Umum dan Solusinya
- **File tidak ditemukan:** Pastikan `dataDir` mengarah ke folder yang benar dan bahwa PSD sumber ada.  
- **ClassCastException:** Pastikan file yang Anda muat memang PSD; format lain memerlukan kelas yang berbeda.  
- **Kesalahan lisensi:** Gunakan lisensi Aspose.PSD yang valid untuk build produksi; versi percobaan dapat digunakan untuk pengembangan.

## Kesimpulan
Anda sekarang tahu **cara menyesuaikan level** dengan menambahkan dan mengonfigurasi Layer Penyesuaian Level dalam file PSD menggunakan Aspose.PSD for Java. Teknik ini memberi Anda kontrol yang tepat atas keseimbangan tonal sambil menjaga alur kerja Anda sepenuhnya otomatis. Terus bereksperimen dengan nilai saluran yang berbeda dan jelajahi pemrosesan batch untuk menerapkan penyesuaian yang sama pada banyak gambar.

## Pertanyaan yang Sering Diajukan

**Q: Apa itu Layer Penyesuaian Level?**  
A: Ini adalah lapisan non‑destruktif yang memungkinkan Anda mengubah rentang tonal (bayangan, nada tengah, sorotan) sebuah gambar.

**Q: Bisakah saya menggunakan Aspose.PSD tanpa membeli lisensi?**  
A: Ya, Anda dapat mengevaluasi perpustakaan dengan versi percobaan gratis, tetapi lisensi diperlukan untuk penggunaan komersial.

**Q: Di mana saya dapat menemukan dokumentasi untuk Aspose.PSD?**  
A: Anda dapat menemukan dokumentasi [di sini](https://reference.aspose.com/psd/java/).

**Q: Apakah ada dukungan komunitas untuk produk Aspose?**  
A: Tentu saja! Anda dapat mengajukan pertanyaan dan mendapatkan bantuan di [forum Aspose](https://forum.aspose.com/c/psd/34).

**Q: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?**  
A: Anda dapat mengajukan permohonan lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

---

**Terakhir Diperbarui:** 2026-03-07  
**Diuji Dengan:** Versi terbaru Aspose.PSD (Java)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}