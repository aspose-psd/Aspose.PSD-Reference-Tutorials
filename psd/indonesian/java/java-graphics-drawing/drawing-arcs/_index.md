---
date: 2026-01-17
description: Pelajari cara menggambar busur pada grafik Java menggunakan Aspose.PSD
  untuk Java. Tutorial langkah demi langkah dengan contoh kode untuk aplikasi grafis.
linktitle: Java Graphics Draw Arc with Aspose.PSD
second_title: Aspose.PSD Java API
title: Java Graphics Menggambar Busur dengan Aspose.PSD – Panduan Langkah demi Langkah
url: /id/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Graphics Draw Arc dengan Aspose.PSD

## Pendahuluan
Dalam tutorial ini Anda akan mempelajari cara **java graphics draw arc** dengan pustaka Aspose.PSD for Java. Menggambar busur secara programatik sangat berguna untuk komponen UI khusus, visualisasi data, atau grafik apa pun yang memerlukan kontrol lengkung yang presisi. Kami akan membimbing Anda melalui setiap langkah—dari menyiapkan proyek hingga merender busur dan menyimpan hasilnya—sehingga Anda dapat menambahkan kemampuan ini ke aplikasi Java Anda segera.

## Jawaban Cepat
- **Pustaka apa yang memudahkan Java menggambar busur?** Aspose.PSD for Java.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis cukup untuk pengujian; lisensi diperlukan untuk produksi.  
- **Format output apa yang didukung?** BMP, PNG, JPEG, TIFF, GIF, dan lainnya.  
- **Bisakah saya mengubah ketebalan atau warna busur?** Ya—sesuaikan properti objek `Pen`.  
- **Apakah kode kompatibel dengan Java 8+?** Tentu saja, API menargetkan Java 8 dan yang lebih baru.

## Apa itu “java graphics draw arc”?
Istilah ini merujuk pada penggunaan kode Java untuk merender segmen melengkung (busur) pada kanvas grafis. Dengan Aspose.PSD, Anda mendapatkan kelas `Graphics` tingkat tinggi yang menyederhanakan operasi menggambar, menangani manajemen warna, anti‑aliasing, dan ekspor file di balik layar.

## Mengapa menggunakan Aspose.PSD untuk menggambar busur?
- **Dukungan PSD penuh** – Buat atau edit file Photoshop tanpa harus menginstal Photoshop.  
- **API menggambar yang kaya** – Metode seperti `drawArc` memungkinkan Anda menentukan ukuran, sudut, dan gaya dalam satu pemanggilan.  
- **Ekspor lintas format** – Simpan busur Anda ke BMP, PNG, JPEG, dll., hanya dengan beberapa baris kode.  
- **Berfokus pada kinerja** – Dioptimalkan untuk gambar berukuran besar dan pemrosesan batch.

## Prasyarat
1. **Lingkungan Pengembangan Java** – Instal Java (JDK 8 atau yang lebih baru). Unduh dari [situs Oracle](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java** – Dapatkan pustaka dari [halaman unduhan](https://releases.aspose.com/psd/java/) dan tambahkan JAR ke classpath proyek Anda.

## Impor Paket
Pertama, bawa kelas Aspose.PSD yang diperlukan ke dalam ruang lingkup:

```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

Impor ini memberi Anda akses ke definisi warna, alat menggambar, kontainer gambar, dan opsi penyimpanan file.

## Panduan Langkah‑per‑Langkah

### Langkah 1: Siapkan Proyek Java Anda
Buat proyek Maven atau Gradle baru, tambahkan JAR Aspose.PSD, dan pastikan IDE menyelesaikan impor tanpa error.

### Langkah 2: Inisialisasi Objek Image dan Graphics
Buat kanvas `PsdImage` kosong dan instance `Graphics` untuk menggambar:

```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```

Ganti `"Your Document Directory"` dengan folder tempat Anda ingin menyimpan file output.

### Langkah 3: Tentukan Parameter Busur
Tentukan dimensi dan sudut yang membentuk busur:

```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```

Silakan sesuaikan angka‑angka ini agar cocok dengan gaya visual yang Anda inginkan.

### Langkah 4: Gambar dan Simpan Busur
Gunakan metode `drawArc`, lalu ekspor gambar:

```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

Kode ini merender busur hitam pada latar belakang kuning dan menulis hasilnya ke `Arc.bmp`. Ubah `outputPath` dan `BmpOptions` jika Anda menginginkan format atau kualitas yang berbeda.

## Masalah Umum & Solusinya
- **Error file tidak ditemukan** – Pastikan `dataDir` diakhiri dengan pemisah path (`/` atau `\\`) dan direktori tersebut ada.  
- **Busur muncul sebagai garis** – Pastikan `width` dan `height` lebih besar dari nol serta `sweepAngle` bukan kelipatan 360° (yang akan menghasilkan elips penuh).  
- **Warna tidak diterapkan** – Gunakan `new Pen(Color.getRed())` atau atur `pen.setWidth(2)` agar efeknya lebih jelas.

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.PSD for Java dapat menangani bentuk lain selain busur?**  
J: Ya, ia mendukung persegi panjang, elips, garis, dan jalur khusus melalui API `Graphics` yang sama.

**T: Bagaimana cara mengubah ketebalan atau warna busur?**  
J: Buat `Pen` dengan `Color` dan `Width` yang diinginkan (misalnya `new Pen(Color.getBlue(), 3)`) dan berikan ke `drawArc`.

**T: Apakah memungkinkan mengekspor busur ke format selain BMP?**  
J: Tentu. Gunakan `PngOptions`, `JpegOptions`, `TiffOptions`, dll., menggantikan `BmpOptions`.

**T: Di mana saya dapat menemukan contoh lebih banyak dan dukungan?**  
J: Kunjungi [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk bantuan komunitas, dokumentasi resmi, dan contoh kode.

## Kesimpulan
Anda kini memiliki contoh lengkap yang siap produksi tentang cara **java graphics draw arc** menggunakan Aspose.PSD for Java. Dengan menyesuaikan parameter, pengaturan pen, dan opsi output, Anda dapat mengintegrasikan busur khusus ke dalam alur kerja grafis berbasis Java apa pun.

---

**Terakhir Diperbarui:** 2026-01-17  
**Diuji Dengan:** Aspose.PSD for Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}