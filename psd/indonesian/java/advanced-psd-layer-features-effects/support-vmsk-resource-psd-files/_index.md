---
date: 2026-06-03
description: Pelajari cara mengonversi PSD ke PNG dan membuat vector mask Java menggunakan
  Aspose.PSD for Java, menambahkan vector mask PSD, dan memanipulasi sumber daya Vmsk
  secara programatis.
keywords:
- convert psd to png
- add vector mask psd
- psd vector mask tutorial
- aspose psd maven
linktitle: Konversi PSD ke PNG dan Buat Vector Mask Java – Sumber Daya Vmsk pada File
  PSD
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to convert PSD to PNG and create vector mask Java using Aspose.PSD
    for Java, add vector mask PSD, and manipulate Vmsk resources programmatically.
  headline: Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD
    Files
  type: TechArticle
- questions:
  - answer: Create a `VmskResource`, populate it with the required path records (e.g.,
      `BezierKnotRecord`), and attach it to the layer’s resources collection.
    question: How do I add a new vector mask to an existing layer?
  - answer: Yes—after saving the PSD, load it again with `Image.load()` and call `im.save("output.png")`
      specifying the PNG format.
    question: Can I convert the edited PSD directly to PNG without opening Photoshop?
  - answer: Absolutely. Since the process is pure Java, you can embed it in Maven/Gradle
      builds, Docker containers, or any CI system that supports Java.
    question: Is there a way to automate this in a CI/CD pipeline?
  - answer: All recent releases (2024‑2025) support Java 8 and above, including Java
      11, 17, and newer LTS versions.
    question: What versions of Aspose.PSD are compatible with Java 11+?
  - answer: A free evaluation license works for development and testing. For production
      deployments, a commercial license is required.
    question: Do I need a license for development builds?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Konversi PSD ke PNG dan Buat Vector Mask Java – Sumber Daya Vmsk pada File
  PSD
url: /id/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi PSD ke PNG dan Membuat Vector Mask Java – Sumber Daya Vmsk dalam File PSD

## Pendahuluan
Jika Anda perlu **mengonversi PSD ke PNG** sekaligus **membuat vector mask** (Vmsk) di dalam file Photoshop, Aspose.PSD untuk Java memberi Anda cara bersih dan programatik untuk melakukan keduanya. Baik Anda membangun alat otomasi desain, pipeline CI yang memvalidasi aset, atau memperluas alur kerja grafis dengan mask khusus, tutorial ini memandu Anda melalui setiap langkah—memuat PSD, membaca sumber daya Vmsk, menyesuaikan propertinya, mengekspor hasil ke PNG, dan menyimpan file yang telah dimodifikasi. Pada akhirnya, Anda akan nyaman menangani vector mask, mengonversi PSD → PNG, dan memperluas file dengan data vektor tambahan—semua dengan teknik **convert PSD to PNG**.

## Jawaban Cepat
- **Apa itu sumber daya Vmsk?** Itu adalah data vector mask yang disimpan di dalam file PSD, mendefinisikan bentuk vektor kompleks untuk sebuah layer.  
- **Perpustakaan mana yang mendukungnya?** Aspose.PSD untuk Java menyediakan akses baca/tulis penuh ke sumber daya Vmsk.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis tersedia; lisensi komersial diperlukan untuk penggunaan produksi.  
- **Bisakah saya mengonversi PSD yang telah diedit ke PNG?** Ya—setelah disimpan, Anda dapat memuat PSD dan mengekspor ke PNG dengan API yang sama.  
- **Apakah dukungan Maven tersedia?** Tentu saja; Aspose.PSD dapat ditambahkan sebagai dependensi Maven (lihat kata kunci “aspose psd maven”).

## Apa itu Vector Mask (Sumber Daya Vmsk)?
Vector mask (Vmsk) adalah mask non‑pixel yang menggunakan kurva Bézier dan rekaman path untuk mendefinisikan wilayah transparan dan tidak transparan pada sebuah layer. Karena berbasis vektor, ia dapat diskalakan tanpa kehilangan kualitas—sempurna untuk grafis resolusi tinggi. Ia dapat berisi banyak path, masing‑masing terdiri dari simpul Bézier, dan mendukung atribut mask seperti opacity, fill, serta penautan ke mask layer.

## Mengapa Membuat Vector Mask dengan Aspose.PSD?
Membuat vector mask secara programatik menghilangkan kebutuhan editing manual di Photoshop, memastikan konsistensi di seluruh batch file besar, dan memungkinkan integrasi ke dalam pipeline build atau deployment otomatis. Dengan Aspose.PSD Anda dapat menghasilkan geometri mask yang tepat, menerapkannya ke layer mana pun, dan mempertahankan kemampuan edit penuh, yang penting untuk generasi grafis dinamis dan alur kerja desain responsif.

- **Otomasi:** Menambahkan atau memodifikasi mask secara programatik tanpa membuka Photoshop.  
- **Konsistensi:** Memastikan setiap PSD yang Anda hasilkan mengikuti aturan mask yang sama.  
- **Cross‑platform:** Berfungsi di semua OS yang mendukung Java.  
- **Integrasi:** Menggabungkan dengan API Aspose lainnya (misalnya, convert PSD → PNG) untuk alur kerja end‑to‑end.  
- **Skalabilitas:** Vector mask tetap tajam pada ukuran apa pun, menjadikannya ideal untuk desain responsif.

## Mengapa Ini Penting bagi Pengembang Java
Menggunakan teknik **create vector mask java** memungkinkan Anda menyematkan logika grafis canggih langsung ke layanan back‑end, pipeline CI, atau utilitas desktop. Anda tidak lagi memerlukan desainer untuk menambahkan mask secara manual; kode Anda dapat menghasilkan atau menyesuaikannya secara dinamis, menghemat waktu dan mengurangi kesalahan manusia.

## Prasyarat
Sebelum kita menyelam ke kode, pastikan Anda memiliki hal‑hal berikut:

### Apa yang Anda Butuhkan
- **Java Development Kit (JDK):** Instal JDK 8 atau yang lebih baru. Anda dapat mengunduhnya dari [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Aspose.PSD for Java Library:** Perpustakaan kuat ini mengelola file PSD. Unduh dari [Aspose release page](https://releases.aspose.com/psd/java/). Untuk memulai cepat, dapatkan versi percobaan gratis dari halaman yang sama atau [free trial](https://releases.aspose.com/).  
- **IDE:** IDE Java apa pun (IntelliJ IDEA, Eclipse, NetBeans) akan berfungsi.

### Menyiapkan Lingkungan Kerja Anda
1. **Buat Proyek Java Baru** – Buka IDE pilihan Anda dan mulai proyek baru.  
2. **Tambahkan Perpustakaan Aspose** – Setelah mengunduh JAR Aspose, tambahkan ke build path proyek Anda sehingga Anda dapat mengakses semua kelas terkait PSD.

Dengan lingkungan siap, mari kita telusuri implementasi sebenarnya.

## Cara mengonversi PSD ke PNG menggunakan Aspose.PSD untuk Java?
Muat PSD sumber Anda dengan `PsdImage.load()`, opsional edit vector mask‑nya, lalu panggil `save()` dengan menentukan `ExportFormat.Png`. Aspose.PSD menangani semua profil warna, layer, dan data mask secara otomatis, menghasilkan PNG pixel‑perfect yang cocok dengan tampilan visual asli. Alur dua langkah ini bekerja untuk PSD apa pun, terlepas dari ukuran, dan berjalan di platform Java mana pun.

## Mengimpor Paket
Paket `com.aspose.psd` menyediakan kelas inti untuk menangani file PSD, termasuk pemuatan gambar, manipulasi sumber daya, dan kemampuan ekspor.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

Sekarang setelah kami menyiapkan panggung, mari kita jalani setiap operasi.

## Langkah 1: Muat File PSD Anda
Memuat file memberikan Anda objek `PsdImage` yang mewakili seluruh dokumen dalam memori.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Kami menetapkan `dataDir` ke direktori file PSD Anda.  
- Kami membuat string untuk `sourceFileName`, menggabungkan direktori dengan nama file PSD.  
- Akhirnya, kami memuat file PSD ke dalam objek `PsdImage` menggunakan `Image.load()`.

## Langkah 2: Ambil Sumber Daya Vmsk
Kelas `VmskResource` mengenkapsulasi data vector mask yang disimpan di dalam layer PSD. Mengambilnya memungkinkan Anda memeriksa atau memodifikasi path mask.

```java
VmskResource resource = getVmskResource(im);
```

- Kami memanggil metode `getVmskResource()` yang menangani pencarian dan pengambilan sumber daya Vmsk dari gambar.

## Langkah 3: Validasi Properti Sumber Daya Vmsk
Sebelum melakukan perubahan, verifikasi bahwa mask diaktifkan, berorientasi benar, dan berisi jumlah path yang diharapkan.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Di sini, kami memeriksa berbagai properti sumber daya Vmsk. Kami ingin memastikan tidak dinonaktifkan, tidak terbalik, atau tidak terhubung, serta memiliki jumlah path yang tepat.

## Langkah 4: Akses Setiap Path dan Validasi
Setiap rekaman path menggambarkan bagian dari bentuk vektor. Memeriksanya memastikan Anda bekerja dengan geometri yang benar.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Kami mengekstrak tiga rekaman path spesifik dan memvalidasi tipe serta propertinya untuk memastikan mereka memenuhi kriteria kami.

## Langkah 5: Edit Sumber Daya Vmsk
Sekarang kami masuk ke bagian modifikasi! Anda dapat mengubah flag perilaku mask sesuai alur kerja Anda.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Dalam blok ini, kami mengubah berbagai properti sumber daya Vmsk. Dengan mengaturnya ke `true`, kami dapat mengontrol bagaimana mask berperilaku dalam file PSD.

## Langkah 6: Modifikasi Titik Knot Bezier
Knot Bézier menentukan kelengkungan setiap segmen vektor. Menyesuaikannya merubah bentuk mask tanpa meraster.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Kami mengakses path `BezierKnotRecord` tertentu dan mengubah titiknya untuk kemungkinan merubah bentuk vector mask.

## Langkah 7: Simpan File PSD yang Dimodifikasi
Setelah semua edit selesai, simpan perubahan ke file PSD baru.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Kami menetapkan jalur untuk file PSD yang diekspor kemudian memanggil `im.save()` untuk menulis perubahan ke file baru ini.

## Langkah 8: Ekspor PSD sebagai PNG
Sekarang PSD berisi mask yang diperbarui, ekspor langsung ke PNG. Langkah ini menunjukkan alur kerja **convert PSD to PNG**.

```java
im.dispose();
```

- Gunakan `im.save("output.png", ExportFormat.Png)` untuk menghasilkan PNG berkualitas tinggi yang mencerminkan vector mask yang telah diedit.

## Bersihkan Sumber Daya
Akhirnya, kami perlu memastikan bahwa gambar dibuang dengan benar untuk membebaskan sumber daya.

CODE_BLOCK_PLACEHOLDER_9_END

- Selalu merupakan praktik yang baik untuk membuang sumber daya apa pun setelah selesai. Ini membantu menghindari kebocoran memori dalam aplikasi Anda.

## Masalah Umum dan Solusinya
| Masalah | Mengapa Terjadi | Cara Memperbaiki |
|---------|----------------|------------------|
| **`VmskResource` not found** | PSD tidak berisi layer vector mask. | Verifikasi bahwa PSD sumber memiliki vector mask atau tambahkan secara manual di Photoshop sebelum menjalankan kode. |
| **`ArrayIndexOutOfBoundsException` on path access** | Jumlah rekaman path yang diharapkan berbeda. | Periksa `resource.getPaths().length` dan sesuaikan penggunaan indeks sesuai kebutuhan. |
| **License exception** | Menjalankan tanpa lisensi Aspose.PSD yang valid. | Terapkan lisensi percobaan atau lisensi berbayar menggunakan `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Memory leak** | Gambar tidak dibuang dalam proses yang berjalan lama. | Selalu panggil `im.dispose()` dalam blok `finally` atau gunakan try‑with‑resources bila didukung. |

## Pertanyaan yang Sering Diajukan

**Q: Bagaimana cara menambahkan vector mask baru ke layer yang sudah ada?**  
A: Buat `VmskResource`, isi dengan rekaman path yang diperlukan (misalnya, `BezierKnotRecord`), dan lampirkan ke koleksi sumber daya layer.

**Q: Bisakah saya mengonversi PSD yang telah diedit langsung ke PNG tanpa membuka Photoshop?**  
A: Ya—setelah menyimpan PSD, muat kembali dengan `Image.load()` dan panggil `im.save("output.png")` dengan format PNG yang ditentukan.

**Q: Apakah ada cara mengotomatisasi ini dalam pipeline CI/CD?**  
A: Tentu. Karena proses ini murni Java, Anda dapat menyematkannya dalam build Maven/Gradle, kontainer Docker, atau sistem CI apa pun yang mendukung Java.

**Q: Versi Aspose.PSD mana yang kompatibel dengan Java 11+?**  
A: Semua rilis terbaru (2024‑2025) mendukung Java 8 ke atas, termasuk Java 11, 17, dan versi LTS yang lebih baru.

**Q: Apakah saya memerlukan lisensi untuk build pengembangan?**  
A: Lisensi evaluasi gratis cukup untuk pengembangan dan pengujian. Untuk penyebaran produksi, lisensi komersial diperlukan.

**Terakhir Diperbarui:** 2026-06-03  
**Diuji Dengan:** Aspose.PSD 24.11 untuk Java  
**Penulis:** Aspose

## Tutorial Terkait

- [Ekspor PSD ke PNG dengan Dukungan Layer Mask di Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Cara Mengonversi PSD ke PNG dan Mengubah Ukuran Proporsional dengan Aspose.PSD untuk Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Konversi PSD ke PNG dengan Color Overlay – Aspose.PSD untuk Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}