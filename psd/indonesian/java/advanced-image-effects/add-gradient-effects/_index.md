---
date: 2026-10-18
description: Pelajari cara membuat efek radial gradient pada gambar Java menggunakan
  Aspose.PSD. Ikuti panduan step‑by‑step ini untuk integrasi yang mulus.
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: Tambahkan efek gradient
og_description: Pelajari cara membuat efek radial gradient Java menggunakan Aspose.PSD.
  Tutorial ini menunjukkan cara menambahkan, menyesuaikan, dan menyimpan gradient
  overlay dalam hitungan menit.
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Buat radial gradient Java dengan Aspose.PSD – panduan step‑by‑step
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Cara membuat efek radial gradient di Aspose.PSD untuk Java
url: /id/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara membuat efek gradien radial di Aspose.PSD untuk Java

## Pendahuluan

Dalam panduan ini Anda akan belajar cara **create radial gradient java** menggunakan pustaka Aspose.PSD. Gradien radial sangat cocok untuk menambahkan kedalaman, fokus, atau cahaya halus pada lapisan PSD Anda tanpa membuka Photoshop. Pada akhir tutorial Anda akan dapat memuat PSD, menerapkan overlay gradien, menyesuaikan propertinya, dan menyimpan hasilnya—semua dari kode Java.

## Jawaban Cepat
- **Apa yang dapat saya capai?** Tambahkan, edit, dan gabungkan overlay gradien radial pada lapisan PSD.  
- **Perpustakaan mana yang diperlukan?** Aspose.PSD untuk Java (versi terbaru).  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk overlay gradien radial dasar.  
- **Apakah kompatibel dengan Java 8+?** Ya, API mendukung Java 8 dan runtime yang lebih baru.

## Prasyarat

Sebelum kita masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

1. **Aspose.PSD for Java Library** – Pastikan Anda telah mengunduh dan menginstal pustaka Aspose.PSD untuk Java. Anda dapat menemukan pustaka dan dokumentasinya di [Aspose.PSD Java documentation page](https://reference.aspose.com/psd/java/).  
2. **Java Development Environment** – Siapkan lingkungan pengembangan Java di mesin Anda (JDK 8 atau lebih tinggi, IDE pilihan Anda).  
3. **Latest Aspose.PSD release** – Unduh versi terbaru dari [Aspose releases page](https://releases.aspose.com/).  
4. **Support resources** – Jika Anda mengalami masalah, konsultasikan [Aspose.PSD Support forum](https://forum.aspose.com/c/psd/34).  
5. **License purchase** – Saat Anda siap untuk produksi, dapatkan lisensi melalui [purchase page](https://purchase.aspose.com/buy).

Setelah semua siap, mari lanjutkan dengan panduan langkah demi langkah.

## Apa itu efek overlay gradien?

Efek overlay gradien melukis transisi halus antara dua atau lebih warna di seluruh area yang dipilih pada sebuah lapisan. Di Photoshop efek ini dapat dicampur, diwarnai, dan diposisikan untuk membuat desain visual yang canggih. Kelas `GradientOverlayEffect` adalah representasi Aspose.PSD dari gaya lapisan tersebut, yang menyediakan properti seperti color stops, opacity, blend mode, dan gradient style.

## Cara membuat efek gradien radial

Muat PSD, temukan lapisan target, sesuaikan properti `GradientOverlayEffect`, dan akhirnya simpan file. Alur kerja lengkap dapat dituliskan dalam empat baris kode Java yang singkat setelah gambar dimuat.

### Langkah 1: Muat file PSD dan akses overlay gradien

`PsdLoadOptions` mengkonfigurasi cara file PSD dimuat, memungkinkan Anda mengaktifkan pemuatan sumber daya efek. `Image.load` membaca file ke dalam objek `Image`.

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

Pada langkah ini, kami memuat file PSD dan mengambil `GradientOverlayEffect` pertama dari lapisan kedua (indeks 1). Pemanggilan `loadOptions.setLoadEffectsResource(true)` memastikan sumber daya efek tersedia untuk diedit.

### Langkah 2: Verifikasi Pengaturan Awal

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

Sebelum melakukan perubahan, sebaiknya konfirmasi mode campur, opacity, dan visibilitas saat ini. Ini membantu Anda memahami keadaan dasar overlay gradien.

### Langkah 3: Modifikasi Pengaturan Gradien

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

Di sini Anda dapat menyesuaikan warna, opacity, dan blend mode gradien. Contoh mengubah warna menjadi hijau, mengurangi opacity menjadi 193 (dari 255), dan mengubah blend mode menjadi **Lighten**. Silakan bereksperimen dengan nilai `BlendMode` lain seperti `Multiply`, `Screen`, atau `Overlay`.

### Langkah 4: Simpan Gambar yang Diedit

```java
// Save the edited image
im.save(exportPath);
```

Setelah menerapkan modifikasi, simpan perubahan dengan menyimpan PSD ke file baru. Langkah ini memastikan file asli tidak berubah.

### Langkah 5: Verifikasi Perubahan

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

Potongan kode di atas menunjukkan cara membuka PSD, mengambil efek pertama pada lapisan kedua (diasumsikan overlay gradien), dan menyiapkannya untuk dimodifikasi.

### Langkah 2: Verifikasi pengaturan asli (opsional tetapi disarankan)

Sebelum mengubah apa pun, memeriksa blend mode, opacity, dan visibilitas yang ada membantu Anda memahami dasar. Pemanggilan `Assert` dalam kode mengonfirmasi bahwa efek saat ini diatur ke blend mode **Normal**, sepenuhnya opaque, dan terlihat.

### Langkah 3: Sesuaikan properti gradien untuk mencapai gaya radial

Anda dapat mengubah warna, opacity, dan blend mode gradien. Untuk efek radial yang sesungguhnya, atur gaya gradien:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Tips profesional:* Gunakan `Color.getGreen()` atau instance `java.awt.Color` apa pun untuk mendefinisikan warna awal, dan `gradientOverlay.setColor2(Color.getBlue())` untuk warna akhir.

### Langkah 4: Simpan PSD yang diedit

Pemanggilan `im.save(exportPath);` menulis gambar yang dimodifikasi ke disk. File yang disimpan mempertahankan overlay gradien radial dan dapat dibuka di Photoshop, dilihat pratinjau di browser, atau dikonversi ke format lain.

## Mengapa membuat overlay gradien radial?

Gradien radial menambah kedalaman dan fokus pada desain, membuat elemen tampak tiga dimensi atau disorot. Mereka ideal untuk:

- **Pengisian latar belakang** yang menarik perhatian ke subjek pusat.  
- **Sorotan tombol atau ikon** dimana cahaya halus diperlukan.  
- **Efek foto kreatif** seperti vignette atau cahaya ledakan.  

Aspose.PSD memproses **lebih dari 50 format input dan output** dan dapat menangani file PSD ratusan halaman tanpa memuat seluruh dokumen ke memori, memungkinkan Anda mengotomatisasi pembuatan gradien di seluruh perpustakaan aset yang besar.

## Masalah umum & tips

- **Efek tidak terlihat:** Pastikan `gradientOverlay.isVisible()` mengembalikan `true`. Beberapa file PSD menyembunyikan efek secara default.  
- **Indeks lapisan salah:** Lapisan diindeks mulai dari nol; periksa kembali bahwa Anda menargetkan lapisan yang benar (`im.getLayers()[1]` mengacu pada lapisan kedua).  
- **Casting opacity:** Metode `setOpacity` mengharapkan `byte`. Mengirim `int` akan menyebabkan error kompilasi; lakukan casting secara eksplisit seperti contoh.  
- **Pemuat sumber daya:** Jika Anda menemukan `null` saat mengakses efek, pastikan `loadOptions.setLoadEffectsResource(true)` sudah diatur sebelum memuat gambar.

## Pertanyaan yang sering diajukan

**Q: Can I apply multiple gradient effects to a single image?**  
A: Ya. Ambil `BlendingOptions` lapisan, iterasi melalui koleksi `Effects`, dan tambahkan `GradientOverlayEffect` baru untuk setiap gradien yang Anda butuhkan.

**Q: What other effects can I combine with gradient overlays?**  
A: Aspose.PSD menyediakan bayangan, cahaya, bevel, dan lainnya. Setiap efek muncul dalam array `Effects` dan dapat dikonfigurasi secara independen.

**Q: How can I troubleshoot if the effects are not rendering correctly?**  
A: Verifikasi bahwa PSD dimuat dengan `setLoadEffectsResource(true)`, periksa visibilitas lapisan, dan pastikan Anda memodifikasi indeks efek yang tepat.

**Q: Is there a trial version available for Aspose.PSD for Java?**  
A: Ya, Anda dapat mendapatkan percobaan gratis [di sini](https://releases.aspose.com/).

**Q: Where can I purchase a license for Aspose.PSD for Java?**  
A: Kunjungi [purchase page](https://purchase.aspose.com/buy) untuk informasi lisensi.

## FAQ Tambahan

**Q: Can I change the gradient direction programmatically?**  
A: Ya. Gunakan metode `GradientOverlayEffect.setAngle(float angle)` untuk mengatur sudut gradien dalam derajat. Untuk gradien radial sudut diabaikan, tetapi metode tetap harus dipanggil.

**Q: Does Aspose.PSD support radial gradients?**  
A: Tentu saja. Atur gaya gradien ke `GradientStyle.Radial` melalui properti `GradientOverlayEffect`.

**Q: Are gradient overlays preserved when converting PSD to other formats (e.g., PNG)?**  
A: Saat Anda merasterisasi PSD (misalnya, menyimpan sebagai PNG), hasil visual overlay gradien dipertahankan, tetapi efek itu sendiri menjadi bagian dari data piksel.

**Q: How do I remove a gradient overlay from a layer?**  
A: Ambil `BlendingOptions` lapisan, temukan `GradientOverlayEffect` dalam koleksi `Effects`, dan hapus dengan `remove(effect)`.

**Q: Is it possible to animate gradient changes?**  
A: Meskipun Aspose.PSD tidak langsung menangani animasi, Anda dapat menghasilkan urutan file PSD dengan parameter gradien yang berbeda lalu menyusunnya menjadi video atau GIF menggunakan pustaka lain.

## Kesimpulan

Selamat! Anda telah belajar **how to create radial gradient java** pada gambar menggunakan Aspose.PSD untuk Java. Dengan mengikuti langkah‑langkah di atas, Anda dapat secara programatis menambahkan, memodifikasi, dan menyimpan overlay gradien, memberi Anda kontrol kreatif penuh atas aset PSD. Bereksperimenlah dengan warna, blend mode, dan nilai opacity yang berbeda untuk mencapai dampak visual yang Anda butuhkan.

---

**Last Updated:** 2026-10-18  
**Tested With:** Aspose.PSD untuk Java 24.12 (versi terbaru pada saat penulisan)  
**Author:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Tutorial Terkait

- [Buat Gradient Fill PSD dengan Java menggunakan Aspose.PSD – Tambahkan Layer Gradient Fill](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Pattern Overlay PSD: Tambahkan Efek dengan Aspose.PSD untuk Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Terapkan Color Overlay dan Atur Opacity di Java dengan Aspose.PSD](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}