---
date: 2026-04-05
description: Pelajari cara mengekspor PSD ke PNG dan dengan mudah meningkatkan kontras
  gambar menggunakan Aspose.PSD untuk Java. Kuasai Lapisan Penyesuaian Levels dengan
  panduan langkah demi langkah ini.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: Ekspor PSD ke PNG dan Render Lapisan Penyesuaian Level di Java
second_title: Aspose.PSD Java API
title: Ekspor PSD ke PNG dan Render Lapisan Penyesuaian Level dalam Java
url: /id/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor PSD ke PNG dan Render Lapisan Penyesuaian Tingkat di Java

## Pendahuluan

Pernah membuka file PSD dan menyadari bahwa warnanya tampak datar atau kontrasnya tidak tepat? Anda dapat dengan cepat **mengekspor PSD ke PNG** sambil menyempurnakan gambar dengan Lapisan Penyesuaian Tingkat menggunakan Aspose.PSD untuk Java. Dalam tutorial ini kami akan membahas seluruh proses—dari memuat PSD, menyesuaikan tingkatnya, hingga menyimpan hasilnya sebagai PNG—sehingga Anda dapat meningkatkan kecerahan dan menyiapkan aset siap web dalam hitungan menit.

## Jawaban Cepat
- **Apa arti “ekspor PSD ke PNG”?** Itu mengonversi dokumen Photoshop menjadi gambar PNG lossless sambil mempertahankan transparansi.  
- **Bisakah saya menyesuaikan tingkat sebelum mengekspor?** Ya, Aspose.PSD memungkinkan Anda memodifikasi tingkat input dan output secara programatis.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Apakah pemrosesan batch memungkinkan?** Tentu—Anda dapat menempatkan kode dalam sebuah loop untuk menangani banyak file PSD.  
- **Versi Java apa yang diperlukan?** Java 8 atau yang lebih baru disarankan.

## Apa itu “ekspor PSD ke PNG”?
Mengekspor PSD ke PNG berarti mengambil file Photoshop berlapis dan meratakannya menjadi gambar Portable Network Graphics. PNG mendukung kompresi lossless dan saluran alfa, menjadikannya ideal untuk grafik web dan aset UI.

## Mengapa menyesuaikan tingkat sebelum mengekspor?
Menyesuaikan tingkat memungkinkan Anda mengontrol bayangan, nada tengah, dan sorotan, meningkatkan kontras keseluruhan serta keseimbangan warna. Langkah ini memastikan PNG akhir terlihat halus tanpa perlu penyuntingan manual di Photoshop.

## Prasyarat

- **Java Development Kit (JDK)** – unduh versi terbaru dari situs Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – dapatkan dari halaman unduhan resmi ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Versi percobaan gratis tersedia ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## Impor Paket

Sebelum menyelam ke kode, impor kelas-kelas yang memberi kami akses ke manipulasi PSD dan ekspor PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Tentukan Jalur File (Cara mengotomatiskan pemrosesan PSD)

Tetapkan variabel yang jelas dan deskriptif untuk PSD sumber, PSD yang dimodifikasi, dan lokasi ekspor PNG akhir.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Langkah 2: Muat Gambar PSD

Gunakan `Image.load` untuk membaca file PSD ke dalam objek `PsdImage`. Aspose.PSD secara otomatis mendeteksi formatnya.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Langkah 3: Iterasi Melalui Lapisan (Cara menyesuaikan tingkat)

Lakukan loop pada setiap lapisan untuk menemukan Lapisan Penyesuaian Tingkat.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Langkah 4: Identifikasi Lapisan Tingkat

Periksa setiap lapisan dengan `instanceof LevelsLayer`. Saat ditemukan, lakukan cast agar kami dapat memodifikasi propertinya.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Langkah 5: Penyempurnaan Tingkat (Cara menyesuaikan tingkat)

Sesuaikan tingkat input dan output untuk saluran pertama (biasanya saluran komposit). Nilai-nilai ini hanya contoh; silakan bereksperimen.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Langkah 6: Simpan PSD yang Dimodifikasi (Cara mengotomatiskan PSD)

Simpan perubahan kembali ke file PSD baru.

```java
im.save(psdPathAfterChange);
```

### Langkah 7: Ekspor sebagai PNG (Ekspor PSD ke PNG)

Jika Anda memerlukan versi PNG, konfigurasikan `PngOptions` dan simpan gambar.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Kasus Penggunaan Umum

- **Persiapan aset web:** Mengonversi mockup PSD yang disediakan desainer menjadi PNG siap untuk browser.  
- **Pemrosesan batch:** Mengotomatiskan konversi puluhan file PSD dalam pipeline CI.  
- **Pembuatan gambar dinamis:** Menyesuaikan tingkat secara langsung berdasarkan masukan pengguna sebelum mengekspor.

## Pemecahan Masalah & Tips

- **Null pointer saat mengakses lapisan:** Pastikan PSD memang berisi Lapisan Penyesuaian Tingkat; jika tidak, tambahkan pemeriksaan null.  
- **Warna tak terduga setelah ekspor:** Pastikan tipe warna PNG diatur ke `TruecolorWithAlpha` untuk mempertahankan transparansi.  
- **Kinerja dengan banyak file:** Gunakan kembali instance `PsdImage` yang sama saat memproses batch untuk mengurangi beban memori.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menyesuaikan saluran warna individual (RGB) secara terpisah?**  
A: Ya. Gunakan `levelsLayer.getChannel(index)` dimana `index` = 0 (Merah), 1 (Hijau), 2 (Biru) untuk mengubah setiap saluran secara independen.

**Q: Bagaimana saya menangani beberapa Lapisan Penyesuaian Tingkat dalam satu PSD?**  
A: Loop memproses setiap lapisan; setiap `LevelsLayer` yang ditemukan akan disesuaikan sesuai kode di dalam blok `if`.

**Q: Apakah ada cara lain untuk meningkatkan kontras selain Tingkat?**  
A: Aspose.PSD juga menawarkan penyesuaian Curves, Brightness/Contrast, dan Histogram Equalization.

**Q: Bisakah saya mengotomatiskan ini untuk folder berisi file PSD?**  
A: Bungkus seluruh alur kerja dalam loop `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` dan proses setiap file secara berurutan.

**Q: Di mana saya dapat menemukan dokumentasi dan dukungan lebih lanjut?**  
A: Kunjungi referensi resmi ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) dan forum komunitas ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## Kesimpulan

Dengan menguasai alur kerja **ekspor PSD ke PNG** dan mempelajari **cara menyesuaikan tingkat** secara programatis, Anda mendapatkan kontrol penuh atas kualitas gambar tanpa meninggalkan lingkungan Java Anda. Baik Anda menyiapkan aset untuk web, mengotomatiskan pipeline desain, atau membangun pemroses batch, Aspose.PSD untuk Java membuat pekerjaan menjadi sederhana dan dapat diandalkan.

---

**Last Updated:** 2026-04-05  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}