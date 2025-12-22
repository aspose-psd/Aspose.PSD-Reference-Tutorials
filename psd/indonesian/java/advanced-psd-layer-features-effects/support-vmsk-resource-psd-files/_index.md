---
date: 2025-12-18
description: Pelajari cara membuat vektor mask (sumber daya Vmsk) dalam file PSD menggunakan
  Aspose.PSD untuk Java. Tutorial langkah demi langkah ini menunjukkan cara menambahkan
  vektor mask, mengonversi PSD ke PNG, dan lainnya.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Buat Masker Vektor (Sumber Daya Vmsk) dalam File PSD dengan Java
url: /id/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat Mask Vektor (Sumber Daya Vmsk) dalam File PSD dengan Java

## Perkenalan
Jika Anda perlu **membuat mask vektor** (Vmsk) di dalam file Photoshop (PSD), Aspose.PSD untuk Java memberikan cara yang bersih dan terprogram untuk melakukannya. Baik Anda sedang membangun alat otomatisasi desain atau menambahkan dukungan mask khusus ke pipeline grafis yang sudah ada, tutorial ini akan memandu Anda melalui setiap langkah—memuat PSD, membaca sumber daya Vmsk, menyesuaikan propertinya, dan menyimpan hasilnya. Pada akhir tutorial, Anda akan merasa nyaman menangani mask vektor, mengubah PSD menjadi PNG, dan memperluas file dengan tambahan data vektor.

## Jawaban Cepat
- **Apa itu sumber daya Vmsk?** Ini adalah data mask vektor yang disimpan di dalam file PSD, mendefinisikan bentuk vektor kompleks untuk sebuah layer.
- **Perpustakaan mana yang mendukungnya?** Aspose.PSD untuk Java menyediakan akses baca/tulis penuh ke sumber daya Vmsk.
- **Apakah saya memerlukan lisensi?** Tersedia versi percobaan gratis; lisensi komersial diperlukan untuk penggunaan produksi.
- ** mendorong saya mengonversi PSD yang telah diedit ke PNG?** Ya—setelah disimpan, Anda dapat memuat PSD dan mengekspor ke PNG dengan API yang sama.
- **Apakah dukungan Maven tersedia?** Tentu saja; Aspose.PSD dapat ditambahkan sebagai dependensi Maven (lihat kata kunci “aspose psd maven”).

## Apa itu Masker Vektor (Sumber Daya Vmsk)?
Mask vector (Vmsk) adalah mask yang tidak berbasis piksel yang menggunakan kurva Bézier dan catatan jalur untuk mendefinisikan wilayah transparan dan opak pada sebuah layer. Karena berbasis vektor, masker ini dapat diskalakan tanpa kehilangan kualitas—sempurna untuk grafis resolusi tinggi.

## Mengapa Membuat Masker Vektor dengan Aspose.PSD?
- **Automation:** Menambahkan atau memodifikasi mask secara terprogram tanpa membuka Photoshop.
- **Consistency:** memutar setiap PSD yang Anda hasilkan mengikuti aturan mask yang sama.
- **Lintas‑platform:** Berfungsi pada sistem operasi apa pun yang mendukung Java.
- **Integrasi:** Menggabungkan dengan API Aspose lainnya (misalnya, mengubah PSD→PNG) untuk alur kerja end‑to‑end.

## Prasyarat
Sebelum kita masuk ke kode, pastikan Anda memiliki hal‑hal berikut:

### Yang Anda Butuhkan
- Java Development Kit (JDK): Pastikan JDK terpasang di mesin Anda. Jika belum, Anda dapat mengunduhnya dari [situs web Oracle](https://www.Oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD untuk Java Library: Ini adalah perpustakaan yang kuat untuk mengelola file PSD. Anda dapat mengunduhnya dari [halaman rilis Aspose](https://releases.aspose.com/psd/java/). Bagi yang ingin mencoba sebelum membeli, Anda juga dapat memulai dengan [uji coba gratis](https://releases.aspose.com/).
- Sebuah IDE: IDE apa pun untuk Java (seperti IntelliJ IDEA, Eclipse, dll.) akan berfungsi untuk proyek ini.

### Menyiapkan Ruang Kerja Anda
1. **Buat Proyek Java Baru** – Buka IDE pilihan Anda dan buat proyek baru.
2. **Tambahkan Perpustakaan Aspose** – Setelah mengunduh JAR Aspose, tambahkan ke jalur build proyek Anda sehingga Anda dapat mengakses semua kelas terkait PSD.

Dengan lingkungan yang siap, mari kita lanjutkan ke implementasi sebenarnya.

## Cara membuat topeng vektor di file PSD dengan Java
Berikut adalah panduan langkah‑demi‑langkah. Blok kode tidak diubah dari tutorial asli; kami hanya menambahkan teks penjelasan untuk membuat setiap langkah menjadi sangat jelas.

## Impor Paket
Sebelum kita dapat bekerja dengan file PSD, kita perlu mengimpor kelas‑kelas yang diperlukan dari perpustakaan Aspose.PSD.

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

Sekarang setelah semua persiapan selesai, mari kita jelajahi setiap operasi.

## Langkah 1: Muat File PSD Anda
Hal pertama yang harus Anda lakukan adalah mengunduh file PSD Anda. Di semua keajaiban dimulai.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Kami mengatur `dataDir` ke direktori file PSD Anda.  
- Kami membuat string untuk `sourceFileName`, menggabungkan direktori dengan nama file PSD.  
- Akhirnya, kami memuat file PSD ke dalam objek `PsdImage` menggunakan `Image.load()`.

## Langkah 2: Mengambil Sumber Daya Vmsk
Setelah gambar PSD dimuat, mari ambil sumber daya Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- Kami memanggil metode `getVmskResource()` yang menangani pencarian dan pengambilan sumber daya Vmsk dari gambar.

## Langkah 3: Validasi Properti Sumber Daya Vmsk
Sebelum melanjutkan dengan modifikasi, penting untuk memvalidasi bahwa sumber daya Vmsk berada dalam keadaan yang diharapkan.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Di sini, kami memeriksa berbagai properti dari sumber daya Vmsk. Kami ingin memastikan bahwa mask tidak dinonaktifkan, tidak terbalik, tidak terlepas, dan memiliki jumlah jalur yang tepat.

## Langkah 4: Akses Setiap Jalur dan Validasi
Mari selami lebih dalam dan periksa jalur‑jalur di dalam sumber daya Vmsk.

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

- Kami mengekstrak tiga catatan jalur spesifik dan memvalidasi tipe serta properti mereka untuk memastikan mereka memenuhi kriteria kami.

## Langkah 5: Edit Sumber Daya Vmsk
Sekarang kita masuk ke bagian modifikasi! Anda dapat menyesuaikan properti sumber daya Vmsk sesuai kebutuhan.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Pada blok ini, kami mengubah berbagai properti sumber daya Vmsk. Dengan mengatur mereka ke `true`, kami dapat mengontrol cara mask berperilaku dalam file PSD.

## Langkah 6: Memodifikasi Titik Simpul Bezier
Knot Bézier sangat penting untuk jalur vektor. Mari ubah beberapa nilai di sini.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Kami mengakses jalur `BezierKnotRecord` tertentu dan mengubah titik‑titiknya untuk kemungkinan mengubah bentuk mask vektor.

## Langkah 7: Simpan File PSD yang Telah Dimodifikasi
Setelah semua edit selesai, saatnya menyimpan file PSD yang telah dimodifikasi.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Kami menentukan jalur untuk file PSD yang diekspor dan kemudian memanggil `im.save()` untuk menulis perubahan ke file baru tersebut.

## Langkah 8: Bersihkan Sumber Daya
Akhirnya, kami perlu memastikan bahwa gambar dibuang dengan benar untuk membebaskan sumber daya.

```java
im.dispose();
```

- Selalu merupakan praktik yang baik untuk membuang semua sumber daya setelah selesai. Hal ini membantu menghindari kebocoran memori dalam aplikasi Anda.

## Kesimpulan
Selamat! Anda baru saja menyelesaikan proses **membuat mask vektor** (Vmsk) dalam file PSD menggunakan Aspose.PSD untuk Java. Dari memuat gambar, mengambil dan memvalidasi sumber daya Vmsk, mengedit propertinya, hingga menyimpan PSD yang telah dimodifikasi, kini Anda memiliki dasar yang kuat untuk mengotomatisasi alur kerja mask vektor. Gunakan teknik ini untuk memperkaya pipeline desain Anda, mengintegrasikan dengan API Aspose lainnya (seperti mengonversi PSD ke PNG), atau membangun alat grafis khusus.

## Pertanyaan yang Sering Diajukan
**T: Bagaimana cara menambahkan topeng vektor baru ke lapisan yang sudah ada?**
A: Buat `VmskResource`, isi catatan dengan jalur yang diperlukan (misalnya `BezierKnotRecord`), dan lampirkan ke koleksi sumber daya layer.

**Q: Dapatkah saya mengonversi PSD yang telah diedit langsung ke PNG tanpa membuka Photoshop?**
A: Ya—setelah menyimpan PSD, muat kembali dengan `Image.load()` dan panggil `im.save("output.png")` dengan format PNG.

**T: Apakah ada cara untuk mengotomatiskannya dalam pipeline CI/CD?**
J: Tentu saja. Karena proses ini murni Java, Anda dapat menyematkannya dalam build Maven/Gradle, kontainer Docker, atau sistem CI apa pun yang mendukung Java.

**T: Versi Aspose.PSD apa yang kompatibel dengan Java 11+?**
A: Semua rilis terbaru (2024‑2025) mendukung Java 8 ke atas, termasuk Java 11, 17, dan versi LTS yang lebih baru.

**T: Apakah saya memerlukan lisensi untuk pengembangan?**
A: Lisensi evaluasi gratis dapat digunakan untuk pengembangan dan pengujian. Untuk penyebaran produksi, diperlukan lisensi komersial.

---

**Terakhir Diperbarui:** 18-12-2025
**Diuji Dengan:** Aspose.PSD 24.11 untuk Java
**Penulis:** Beranggapan

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
