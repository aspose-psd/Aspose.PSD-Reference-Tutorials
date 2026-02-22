---
date: 2026-02-22
description: Pelajari cara membuat mask vektor menggunakan Aspose.PSD untuk Java,
  menambahkan mask vektor PSD, dan memanipulasi sumber daya Vmsk secara programatis.
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: Membuat Vector Mask Java – Sumber Daya Vmsk dalam File PSD
url: /id/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Membuat Vector Mask Java – Sumber Daya Vmsk dalam File PSD

## Pendahuluan
Jika Anda perlu **create vector mask** (Vmsk) sumber daya di dalam file Photoshop (PSD), Aspose.PSD for Java memberikan cara yang bersih dan programatis untuk melakukannya. Baik Anda sedang membangun alat otomasi desain atau menambahkan dukungan mask khusus ke pipeline grafis yang ada, tutorial ini memandu Anda melalui setiap langkah—memuat PSD, membaca sumber daya Vmsk, menyesuaikan propertinya, dan menyimpan hasilnya. Pada akhir tutorial, Anda akan nyaman menangani vector masks, mengonversi PSD ke PNG, dan memperluas file dengan data vektor tambahan—semua dengan teknik **create vector mask java**.

## Jawaban Cepat
- **What is a Vmsk resource?** Itu adalah data vector mask yang disimpan di dalam file PSD, yang mendefinisikan bentuk vektor kompleks untuk sebuah layer.  
- **Which library supports it?** Aspose.PSD for Java menyediakan akses baca/tulis penuh ke sumber daya Vmsk.  
- **Do I need a license?** Tersedia trial gratis; lisensi komersial diperlukan untuk penggunaan produksi.  
- **Can I convert the edited PSD to PNG?** Ya—setelah disimpan, Anda dapat memuat PSD dan mengekspor ke PNG dengan API yang sama.  
- **Is Maven support available?** Tentu; Aspose.PSD dapat ditambahkan sebagai dependensi Maven (lihat kata kunci “aspose psd maven”).

## Apa itu Vector Mask (Sumber Daya Vmsk)?
Vector mask (Vmsk) adalah mask yang tidak berbasis piksel yang menggunakan kurva Bézier dan catatan jalur untuk mendefinisikan area transparan dan opak pada sebuah layer. Karena berbasis vektor, ia dapat diskalakan tanpa kehilangan kualitas—sempurna untuk grafis resolusi tinggi.

## Mengapa Membuat Vector Mask dengan Aspose.PSD?
- **Automation:** Menambahkan atau memodifikasi mask secara programatis tanpa membuka Photoshop.  
- **Consistency:** Memastikan setiap PSD yang Anda hasilkan mengikuti aturan mask yang sama.  
- **Cross‑platform:** Berfungsi pada sistem operasi apa pun yang mendukung Java.  
- **Integration:** Menggabungkan dengan API Aspose lainnya (mis., mengonversi PSD → PNG) untuk alur kerja end‑to‑end.  
- **Scalability:** Vector mask tetap tajam pada ukuran apa pun, menjadikannya ideal untuk desain responsif.

## Mengapa Hal Ini Penting bagi Pengembang Java
Menggunakan teknik **create vector mask java** memungkinkan Anda menyematkan logika grafis canggih langsung ke layanan back‑end, pipeline CI, atau utilitas desktop. Anda tidak lagi memerlukan desainer untuk menambahkan mask secara manual; kode Anda dapat menghasilkan atau menyesuaikannya secara dinamis, menghemat waktu dan mengurangi kesalahan manusia.

## Prasyarat
Sebelum kita menyelami kode, pastikan Anda memiliki hal berikut:

### Apa yang Anda Butuhkan
- Java Development Kit (JDK): Pastikan Anda memiliki JDK terpasang di mesin Anda. Jika belum, Anda dapat mengunduhnya dari [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD for Java Library: Ini adalah pustaka kuat untuk mengelola file PSD. Anda dapat mengunduhnya dari [Aspose release page](https://releases.aspose.com/psd/java/). Bagi yang ingin mencoba sebelum membeli, Anda juga dapat memulai dengan [free trial](https://releases.aspose.com/).
- An IDE: IDE apa pun untuk Java (seperti IntelliJ IDEA, Eclipse, dll.) akan berfungsi untuk proyek ini.

### Menyiapkan Workspace Anda
1. **Create a New Java Project** – Buka IDE pilihan Anda dan buat proyek baru.  
2. **Add the Aspose Library** – Setelah mengunduh JAR Aspose, tambahkan ke jalur build proyek Anda sehingga Anda dapat mengakses semua kelas terkait PSD.

Dengan lingkungan siap, mari kita masuk ke implementasi sebenarnya.

## Cara membuat vector mask dalam file PSD dengan Java
Berikut adalah panduan langkah demi langkah. Blok kode tidak diubah dari tutorial asli; kami hanya menambahkan teks penjelasan agar setiap langkah menjadi sangat jelas.

### Mengimpor Paket
Sebelum kita dapat bekerja dengan file PSD, kita perlu mengimpor kelas yang diperlukan dari pustaka Aspose.PSD.

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

Sekarang setelah kami menyiapkan semuanya, mari kita jalani setiap operasi.

### Langkah 1: Muat File PSD Anda
Hal pertama yang harus Anda lakukan adalah memuat file PSD Anda. Di sinilah semua keajaiban dimulai.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Kami menetapkan `dataDir` ke direktori file PSD Anda.  
- Kami membuat string untuk `sourceFileName`, menggabungkan direktori dengan nama file PSD.  
- Akhirnya, kami memuat file PSD ke dalam objek `PsdImage` menggunakan `Image.load()`.

### Langkah 2: Ambil Sumber Daya Vmsk
Setelah gambar PSD kami dimuat, mari ambil sumber daya Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- Kami memanggil metode `getVmskResource()` yang menangani pencarian dan pengambilan sumber daya Vmsk dari gambar.

### Langkah 3: Validasi Properti Sumber Daya Vmsk
Sebelum melanjutkan dengan modifikasi, penting untuk memvalidasi bahwa sumber daya Vmsk kami berada dalam keadaan yang diharapkan.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Di sini, kami memeriksa berbagai properti dari sumber daya Vmsk. Kami ingin memastikan bahwa ia tidak dinonaktifkan, tidak terbalik, atau tidak terhubung, serta memiliki jumlah jalur yang tepat.

### Langkah 4: Akses Setiap Jalur dan Validasi
Mari selami lebih dalam dan periksa jalur-jalur dalam sumber daya Vmsk.

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

### Langkah 5: Edit Sumber Daya Vmsk
Sekarang kami masuk ke bagian modifikasi! Anda dapat menyesuaikan properti sumber daya Vmsk sesuai kebutuhan.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Pada blok ini, kami mengubah berbagai properti sumber daya Vmsk. Dengan mengaturnya ke `true`, kami dapat mengontrol bagaimana mask berperilaku dalam file PSD.

### Langkah 6: Modifikasi Titik Knot Bézier
Knot Bézier sangat penting untuk jalur vektor. Mari ubah beberapa nilai di sini.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Kami mengakses jalur `BezierKnotRecord` tertentu dan mengubah titik-titiknya untuk kemungkinan mengubah bentuk vector mask.

### Langkah 7: Simpan File PSD yang Dimodifikasi
Setelah semua edit selesai, saatnya menyimpan file PSD yang telah dimodifikasi.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Kami menetapkan jalur untuk file PSD yang diekspor dan kemudian memanggil `im.save()` untuk menulis perubahan ke file baru ini.

### Langkah 8: Bersihkan Sumber Daya
Akhirnya, kami perlu memastikan bahwa gambar dibuang dengan benar untuk membebaskan sumber daya.

```java
im.dispose();
```

- Selalu merupakan praktik yang baik untuk membuang semua sumber daya setelah selesai. Ini membantu menghindari kebocoran memori dalam aplikasi Anda.

## Masalah Umum dan Solusinya
| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **`VmskResource` not found** | PSD tidak berisi layer vector mask. | Pastikan PSD sumber memiliki vector mask atau tambahkan secara manual di Photoshop sebelum menjalankan kode. |
| **`ArrayIndexOutOfBoundsException` on path access** | Jumlah catatan jalur yang diharapkan berbeda. | Periksa `resource.getPaths().length` dan sesuaikan penggunaan indeks sesuai kebutuhan. |
| **License exception** | Menjalankan tanpa lisensi Aspose.PSD yang valid. | Terapkan lisensi trial atau lisensi berbayar menggunakan `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Memory leak** | Gambar tidak dibuang dalam proses yang berjalan lama. | Selalu panggil `im.dispose()` dalam blok `finally` atau gunakan try‑with‑resources jika didukung. |

## Pertanyaan yang Sering Diajukan

**Q: Bagaimana cara menambahkan vector mask baru ke layer yang ada?**  
A: Buat `VmskResource`, isi dengan catatan jalur yang diperlukan (mis., `BezierKnotRecord`), dan lampirkan ke koleksi sumber daya layer.

**Q: Bisakah saya mengonversi PSD yang telah diedit langsung ke PNG tanpa membuka Photoshop?**  
A: Ya—setelah menyimpan PSD, muat kembali dengan `Image.load()` dan panggil `im.save("output.png")` dengan menentukan format PNG.

**Q: Apakah ada cara mengotomatisasi ini dalam pipeline CI/CD?**  
A: Tentu. Karena proses ini murni Java, Anda dapat menyematkannya dalam build Maven/Gradle, kontainer Docker, atau sistem CI apa pun yang mendukung Java.

**Q: Versi Aspose.PSD mana yang kompatibel dengan Java 11+?**  
A: Semua rilis terbaru (2024‑2025) mendukung Java 8 ke atas, termasuk Java 11, 17, dan versi LTS yang lebih baru.

**Q: Apakah saya memerlukan lisensi untuk build pengembangan?**  
A: Lisensi evaluasi gratis dapat digunakan untuk pengembangan dan pengujian. Untuk penyebaran produksi, lisensi komersial diperlukan.

---

**Terakhir Diperbarui:** 2026-02-22  
**Diuji Dengan:** Aspose.PSD 24.11 untuk Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}