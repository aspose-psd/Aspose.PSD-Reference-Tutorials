---
date: 2026-10-24
description: Pelajari cara membuat stroke layer Java dengan Aspose.PSD untuk Java.
  Panduan langkah demi langkah ini menunjukkan cara menambahkan stroke layer, mengubah
  warnanya, menyesuaikan opasitas, dan menyimpan PSD.
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: Tambah Warna Stroke Layer
og_description: Buat stroke layer Java menggunakan Aspose.PSD untuk Java. Ikuti tutorial
  singkat ini untuk menambahkan stroke layer, mengubah warnanya, menyesuaikan opasitas,
  dan mengekspor file PSD.
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: Buat stroke layer Java dengan Aspose.PSD – Panduan Cepat
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: Cara membuat stroke layer Java menggunakan Aspose.PSD
url: /id/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara membuat lapisan stroke Java menggunakan Aspose.PSD

## Pendahuluan

Jika Anda perlu **create stroke layer Java** dalam dokumen Photoshop secara programatik, Aspose.PSD untuk Java memberikan pendekatan bersih berbasis kode. Dalam tutorial ini Anda akan belajar cara menambahkan lapisan stroke baru, mengubah warnanya, menyesuaikan opacity, dan menyimpan hasilnya—semua tanpa meluncurkan Photoshop. Pada akhirnya Anda juga akan tahu cara mengedit stroke pada lapisan yang sudah ada, memberi Anda kontrol kreatif penuh langsung dari aplikasi Java Anda.

## Jawaban Cepat
- **Library apa yang diperlukan?** Aspose.PSD for Java (versi terbaru).  
- **Apakah saya dapat mengubah warna stroke?** Ya – gunakan `ColorFillSettings` untuk mengatur `Color` apa pun.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara dapat digunakan untuk evaluasi; lisensi penuh diperlukan untuk produksi.  
- **Versi Java mana yang didukung?** Java 8 atau lebih tinggi.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk perubahan stroke dasar.

## Apa itu lapisan stroke dalam PSD?
Lapisan stroke adalah efek vektor yang menggambar garis tepi di sekitar isi sebuah lapisan. Efek ini dapat disesuaikan dengan warna, ketebalan, opacity, dan mode campuran. Memodifikasi efek ini secara programatik memungkinkan otomatisasi branding, pemrosesan batch, atau pembuatan grafik dinamis.

## Mengapa menggunakan Aspose.PSD untuk mengubah warna stroke?
Aspose.PSD mendukung **150+** fitur PSD—termasuk masker vektor, smart object, dan efek lapisan—sementara memproses file berukuran ratusan halaman tanpa memuat seluruh dokumen ke memori. Perpustakaan ini berjalan di semua OS dengan JVM, memberikan kinerja sub‑detik untuk aset tipikal, dan tidak memerlukan instalasi Photoshop.

## Cara membuat lapisan stroke Java?

Muat PSD, tambahkan efek stroke, konfigurasikan tampilannya, dan simpan file—semua dalam beberapa baris kode sederhana. Jawaban di bawah ini memberi tahu Anda langkah demi langkah sebelum kita masuk ke tutorial detail.

**Direct answer (40‑70 words):**  
`PsdImage` mewakili dokumen PSD dan menyediakan metode untuk memuat serta menyimpan file. Mulailah dengan memuat PSD Anda menggunakan `PsdImage.load("input.psd", loadOptions)`. Buat `StrokeEffect` baru, atur `ColorFillSettings`‑nya ke `Color` yang diinginkan, sesuaikan opacity dan ukuran, lalu lampirkan efek ke `BlendingOptions` lapisan target. Akhirnya, panggil `psd.save("output.psd", SaveFormat.PSD)`. Urutan ini membuat lapisan stroke di Java dengan Aspose.PSD.

### Prasyarat

- **Aspose.PSD library** – unduh dari [official documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – versi 8 atau lebih baru.  
- **IDE** – Eclipse, IntelliJ IDEA, atau editor kompatibel Java apa pun.

### Impor paket

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

### Langkah 1: siapkan proyek Anda

Buat proyek Java baru, tambahkan JAR Aspose.PSD ke jalur build, dan pastikan perpustakaan dimuat tanpa error.

### Langkah 2: muat file PSD

Aktifkan pemuatan sumber daya efek sehingga informasi stroke tersedia.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Langkah 3: akses lapisan efek stroke

`StrokeEffect` adalah kelas Aspose.PSD yang mewakili outline vektor yang diterapkan pada sebuah lapisan. Ambil efek stroke pertama dari lapisan kedua (indeks 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### Langkah 4: validasi properti stroke

`ColorFillSettings` menyimpan nilai warna dan opacity untuk sebuah stroke. Pastikan properti yang ada sebelum melakukan perubahan untuk menghindari hasil yang tidak terduga.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### Langkah 5: atur warna dan opacity (cara mengubah warna stroke)

Di sini kami **change stroke color** menjadi kuning dan mengurangi opacity menjadi 50 % (127 / 255). `ColorFillSettings` juga memungkinkan Anda menentukan mode campuran dan ukuran.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### Langkah 6: simpan PSD yang dimodifikasi

Tulis kembali gambar yang telah diperbarui ke disk. File baru kini berisi stroke yang telah dimodifikasi.

```java
im.save(exportPath);
```

## Cara mengubah warna stroke Java?

`Color` mewakili nilai warna ARGB. Muat PSD Anda, temukan lapisan target, perbarui `ColorFillSettings` dengan `Color` baru, dan simpan file. Operasi ini hanya memerlukan beberapa baris kode dan selesai dalam kurang dari satu detik untuk aset tipikal, menjadikannya cepat dan efisien.

**Direct answer (40‑70 words):**  
Gunakan `layer.getEffects().getStrokeEffect()` untuk memperoleh stroke yang ada, panggil `stroke.getColorFillSettings().setColor(Color.getRed())` (atau `Color` apa pun yang Anda perlukan), opsional sesuaikan `setOpacity((byte)200)` untuk opacity 78 %, lalu simpan PSD dengan `psd.save("output.psd", SaveFormat.PSD)`. Perubahan diterapkan secara instan tanpa merender ulang seluruh dokumen.

## Cara memodifikasi opacity stroke?

Jika Anda hanya perlu menyesuaikan opacity sambil mempertahankan warna asli, ubah nilai `setOpacity` (0‑255) pada `ColorFillSettings`. Misalnya, `colorStroke.setOpacity((byte)200);` akan membuat stroke kira‑kira 78 % opaque. Menyesuaikan opacity memungkinkan Anda membuat outline halus atau stroke sepenuhnya solid, tergantung pada kebutuhan desain Anda.

**Direct answer (40‑70 words):**  
Ambil `StrokeEffect` dari lapisan yang diinginkan, lalu panggil `stroke.getColorFillSettings().setOpacity((byte)desiredValue)`, di mana `desiredValue` berada dalam rentang 0 (transparan) hingga 255 (sepenuhnya opaque). Simpan PSD dan opacity baru akan terlihat segera. Pendekatan ini berlaku untuk stroke apa pun yang sudah ada, terlepas dari warna aslinya.

## Cara menerapkan efek stroke?

Untuk menambahkan efek stroke baru ke lapisan yang belum memilikinya, buat instance `StrokeEffect`, konfigurasikan `ColorFillSettings`‑nya, dan lampirkan ke `BlendingOptions` lapisan. Metode `setColor` dan `setOpacity` yang sama digunakan untuk menentukan tampilan secara keseluruhan.

**Direct answer (40‑70 words):**  
Instansiasi `StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);`. Setelah melampirkan efek, simpan PSD. Ini menambahkan lapisan stroke baru yang sepenuhnya dapat disesuaikan ke lapisan apa pun dalam dokumen Anda.

## Kasus penggunaan umum untuk mengubah warna stroke
- **Automasi branding:** Terapkan warna korporat ke logo pada ratusan aset PSD dalam satu batch.  
- **Generasi UI dinamis:** Ubah warna stroke secara real‑time berdasarkan tema yang dipilih pengguna dalam alat desain berbasis web.  
- **Persiapan pra‑cetak:** Pastikan semua warna stroke memenuhi spesifikasi cetak sebelum mengirim file ke percetakan.

## Kesalahan umum & tips

- **Pemeriksaan null** – selalu pastikan `getEffects()` mengembalikan array non‑null sebelum casting.  
- **Indeks lapisan** – lapisan PSD menggunakan indeks berbasis nol; pastikan Anda menargetkan lapisan yang tepat.  
- **Format warna** – `Color.getYellow()` hanya contoh; Anda dapat membuat warna kustom dengan `new Color(r, g, b)`.  
- **Rentang opacity** – opacity adalah byte (0–255); nilai di atas 255 akan dipotong.  
- **Pemuat sumber daya** – lupa `loadOptions.setLoadEffectsResource(true)` akan menghasilkan array efek `null`.

## Pertanyaan yang sering diajukan

**Q: Dapatkah saya menggunakan Aspose.PSD dengan perpustakaan grafis Java lainnya?**  
A: Ya, Aspose.PSD dapat digabungkan dengan perpustakaan seperti Apache Commons Imaging atau Java2D untuk fungsionalitas tambahan.

**Q: Apakah Aspose.PSD kompatibel dengan format file PSD terbaru?**  
A: Tentu saja. Perpustakaan ini mendukung spesifikasi Photoshop terbaru dan lebih dari 150 fitur PSD.

**Q: Bagaimana cara menangani pengecualian saat menggunakan Aspose.PSD?**  
A: Bungkus kode Anda dalam blok try‑catch dan kunjungi [support forum](https://forum.aspose.com/c/psd/34) untuk contoh pemecahan masalah yang detail.

**Q: Dapatkah saya mencoba Aspose.PSD sebelum membeli?**  
A: Tentu! Dapatkan [free trial](https://releases.aspose.com/) untuk menjelajahi semua fitur.

**Q: Di mana saya dapat memperoleh lisensi sementara untuk Aspose.PSD?**  
A: Dapatkan [temporary license](https://purchase.aspose.com/temporary-license/) untuk mengevaluasi perpustakaan di lingkungan pengembangan Anda.

---

**Last Updated:** 2026-10-24  
**Tested with:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Tutorial Terkait

- [How to Change Stroke Color Java Using Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [How to Add Shadow in PSD Using Java – Advanced Layer Effects](/psd/java/advanced-psd-layer-features-effects/)
- [Pattern Overlay PSD: Add Effects with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}