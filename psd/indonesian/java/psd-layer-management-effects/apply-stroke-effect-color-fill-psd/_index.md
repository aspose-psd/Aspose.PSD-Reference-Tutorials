---
date: 2026-04-03
description: Pelajari cara menyimpan PSD sebagai PNG dengan efek stroke dan isian
  warna menggunakan Aspose.PSD untuk Java. Panduan langkah demi langkah ini menunjukkan
  cara mengekspor PSD ke PNG dengan cepat.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: Simpan PSD sebagai PNG dengan Efek Garis – Java
second_title: Aspose.PSD Java API
title: Simpan PSD sebagai PNG dengan Efek Stroke – Java
url: /id/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan PSD sebagai PNG dengan Efek Garis Luar dan Isi Warna – Java

## Pendahuluan

Dalam panduan ini, Anda akan belajar cara **menyimpan PSD sebagai PNG** sambil menerapkan efek garis luar dengan isi warna menggunakan Aspose.PSD untuk Java. Baik Anda seorang pengembang berpengalaman maupun pemula, tutorial langkah‑demi‑langkah ini akan memudahkan Anda menyelesaikan tugas. Kami akan membahas semua hal mulai dari menyiapkan lingkungan hingga mengekspor gambar akhir, sehingga Anda dapat dengan cepat **mengekspor PSD ke PNG** dalam proyek Anda sendiri.

## Jawaban Cepat
- **Apa yang dicapai tutorial ini?** Menunjukkan cara menyimpan file PSD sebagai PNG setelah menerapkan efek garis luar yang dapat disesuaikan.  
- **Pustaka mana yang digunakan?** Aspose.PSD for Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi diperlukan untuk produksi.  
- **Apakah saya dapat mengubah warna garis luar?** Ya – Anda dapat mengatur warna apa pun melalui `ColorFillSettings`.  
- **Apakah pemrosesan batch memungkinkan?** Tentu – bungkus kode dalam loop untuk memproses beberapa file PSD.

## Apa itu “menyimpan PSD sebagai PNG”?
Menyimpan PSD sebagai PNG berarti mengonversi file berlapis asli Photoshop menjadi format gambar datar yang ramah web sambil mempertahankan kesetiaan visual. Ini berguna ketika Anda perlu menampilkan konten PSD di situs web, aplikasi seluler, atau platform apa pun yang tidak mendukung file PSD secara langsung.

## Mengapa menerapkan efek garis luar dengan isi warna?
Garis luar menambahkan kontur tajam di sekitar isi lapisan, membuat grafik menonjol di latar belakang yang kompleks. Menggabungkannya dengan warna isi khusus memungkinkan Anda memberi merek pada gambar, menyorot elemen UI, atau membuat thumbnail yang menarik tanpa meninggalkan Photoshop.

## Prasyarat

1. **Java Development Kit (JDK) 8+** – pastikan `java` ada di PATH Anda.  
2. **Aspose.PSD for Java** – unduh dari [website](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor apa pun yang Anda sukai.  
4. **Sample PSD** – file yang sudah berisi efek garis luar (atau tambahkan satu di Photoshop).  
5. **Basic Java knowledge** – Anda akan menulis beberapa baris kode, tetapi tidak ada yang rumit.

Setelah Anda menyiapkan semua ini, kita dapat mulai menulis kode.

## Impor Paket

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Impor ini membawa semua kelas yang diperlukan untuk memuat PSD, memodifikasi garis luar, dan menyimpan output PSD serta PNG.

## Cara Menyimpan PSD sebagai PNG dengan Efek Garis Luar

### Langkah 1: Muat File PSD

Pertama, arahkan ke folder yang berisi PSD sumber Anda.

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur sebenarnya di mesin Anda.

Sekarang muat file sambil mempertahankan semua sumber daya efek yang ada:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Langkah 2: Atur Warna Garis Luar (dan opsional sesuaikan lebar)

Loop di bawah ini melintasi setiap lapisan, mengambil `StrokeEffect` pertama, dan mengubah warna isiannya. Anda juga dapat menyesuaikan `setWidth` atau `setPosition` pada objek `StrokeEffect` jika perlu **menyesuaikan lebar garis luar**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Tip pro:** `Color.getDeepPink()` hanyalah contoh. Gunakan `new Color(r, g, b)` untuk nilai RGB khusus.

### Langkah 3: Simpan PSD yang Dimodifikasi (opsional)

Jika Anda ingin menyimpan versi PSD dengan garis luar yang diperbarui, simpan seperti ini:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Langkah 4: Ekspor Gambar sebagai PNG (langkah inti “menyimpan PSD sebagai PNG”)

Akhirnya, konversi PSD yang telah diedit menjadi file PNG yang siap digunakan di web:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

PNG mempertahankan garis luar berwarna pink tua yang Anda atur sebelumnya, dan opsi `TruecolorWithAlpha` memastikan transparansi tetap terjaga.

## Masalah Umum & Solusi

| Masalah | Alasan | Solusi |
|-------|--------|-----|
| **`ArrayIndexOutOfBoundsException`** | Layer tidak memiliki efek atau efek pertama bukan `StrokeEffect`. | Pastikan lapisan memang berisi garis luar atau iterasi melalui `getEffects()` untuk menemukan tipe yang tepat. |
| **Warna tidak berubah** | Anda mungkin mengedit salinan pengaturan alih-alih yang asli. | Pastikan Anda melakukan cast langsung ke `ColorFillSettings` dari `effect.getFillSettings()`. |
| **PNG muncul kosong** | PSD dimuat tanpa merasterisasi lapisan. | Panggil `im.save(..., new PngOptions())` setelah semua modifikasi; hindari menyimpan `im` asli sebelum perubahan. |

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menerapkan beberapa efek pada satu lapisan menggunakan Aspose.PSD untuk Java?**  
A: Ya, Anda dapat mengakses opsi pencampuran lapisan dan menambahkan sebanyak mungkin efek yang diperlukan, termasuk bayangan, cahaya, dan garis luar.

**Q: Apakah memungkinkan mengotomatisasi proses untuk sekumpulan file PSD?**  
A: Tentu. Bungkus logika pemuatan, penerapan efek, dan penyimpanan dalam loop `for‑each` yang mengiterasi file dalam sebuah direktori.

**Q: Bagaimana cara mengembalikan perubahan yang dibuat pada file PSD?**  
A: Muat ulang file asli sebelum menyimpan modifikasi apa pun; Aspose.PSD tidak menyediakan stack undo.

**Q: Bisakah saya menyesuaikan lebar dan posisi garis luar?**  
A: Ya. Gunakan `effect.setWidth(float)` dan `effect.setPosition(StrokeEffect.Position)` untuk mengontrol ketebalan dan penempatan (di dalam, di luar, atau di tengah).

**Q: Apakah pustaka Aspose.PSD untuk Java gratis untuk digunakan?**  
A: Versi percobaan gratis tersedia untuk evaluasi. Fungsi penuh memerlukan lisensi berbayar. Lihat [buy options](https://purchase.aspose.com/buy) untuk detail.

---

**Terakhir Diperbarui:** 2026-04-03  
**Diuji Dengan:** Aspose.PSD 24.12 for Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}