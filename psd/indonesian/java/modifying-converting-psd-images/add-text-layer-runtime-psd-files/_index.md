---
date: 2026-03-07
description: Pelajari cara menambahkan teks ke file PSD secara runtime menggunakan
  Java dan Aspose.PSD. Ikuti panduan langkah demi langkah ini untuk membuat lapisan
  teks dalam PSD dengan cepat.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Menambahkan Teks ke File PSD pada Saat Runtime Menggunakan Java
url: /id/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menambahkan Teks ke File PSD pada Runtime Menggunakan Java

## Pendahuluan
Jika Anda pernah mengedit dokumen Photoshop secara manual, Anda tahu betapa kuatnya lapisan. Bagaimana jika Anda dapat **menambahkan teks ke PSD** secara otomatis dari aplikasi Java Anda? Dengan pustaka Aspose.PSD untuk Java, Anda dapat membuat lapisan teks dalam PSD pada runtime, membuka pintu untuk pemrosesan batch, pembuatan grafik dinamis, dan alur kerja branding otomatis. Pada tutorial ini kami akan membahas seluruh proses, mulai dari menyiapkan proyek hingga menyimpan file yang telah diperbarui.

## Jawaban Cepat
- **Pustaka apa yang saya perlukan?** Aspose.PSD untuk Java.  
- **Apakah saya dapat menambahkan teks ke PSD yang sudah ada?** Ya – cukup muat file, tambahkan `TextLayer`, dan simpan.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan untuk penggunaan non‑evaluasi.  
- **Versi Java mana yang didukung?** JDK 8 atau lebih tinggi (kami merekomendasikan LTS terbaru).  
- **Apakah ini cocok untuk backend web?** Tentu – API berfungsi di lingkungan server berbasis Java apa pun.

## Apa itu “menambahkan teks ke PSD”?
Menambahkan teks ke PSD berarti secara programatik membuat lapisan teks baru di dalam dokumen Photoshop. Lapisan tersebut berperilaku seperti lapisan teks Photoshop lainnya: Anda dapat memindahkannya, mengedit isinya, dan menerapkan gaya—semua tanpa membuka Photoshop.

## Mengapa membuat lapisan teks dalam PSD dengan Java?
- **Otomatisasi** – Menghasilkan aset pemasaran, watermark, atau label produk secara massal.  
- **Konsistensi** – Menjamin font, ukuran, dan posisi yang sama di ribuan file.  
- **Integrasi** – Digabungkan dengan layanan Java lainnya (e‑commerce, pelaporan, pipeline CI) untuk menyajikan grafik secara langsung.

## Prasyarat
Sebelum menulis kode, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – Instal JDK 8 atau yang lebih baru. Anda dapat [mengunduhnya di sini](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD untuk Java** – Dapatkan JAR terbaru dari [halaman rilis Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE (opsional tetapi membantu)** – IntelliJ IDEA, Eclipse, atau editor pilihan Anda.  
4. **Pengetahuan dasar Java** – Anda harus nyaman dengan kelas, objek, dan I/O file.  
5. **Sebuah contoh PSD** – Untuk panduan ini kami akan menggunakan `OneLayer.psd` yang ditempatkan di folder pilihan Anda.

## Impor Paket
Pertama, impor kelas yang diperlukan untuk bekerja dengan file PSD dan lapisan teks.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Impor ini memberi Anda akses ke fungsionalitas inti Aspose.PSD.

## Panduan Langkah‑per‑Langkah

### Langkah 1: Siapkan Direktori Dokumen Anda
Tentukan folder yang berisi PSD sumber Anda dan tempat output akan disimpan.

```java
String dataDir = "Your Document Directory"; 
```

Ganti `"Your Document Directory"` dengan jalur absolut atau relatif ke file Anda.

### Langkah 2: Muat File PSD Sumber Anda
Bawa PSD yang ada ke memori menggunakan `Image.load()`.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

Jika jalurnya benar, `img` kini mewakili dokumen Photoshop yang dimuat.

### Langkah 3: Cast ke `PsdImage`
Karena kita berurusan dengan fitur khusus Photoshop, cast objek `Image` generik ke `PsdImage`.

```java
PsdImage im = (PsdImage)img;
```

Cast ini membuka metode seperti `addTextLayer()`.

### Langkah 4: Tentukan Rectangle untuk Lapisan Teks
Tentukan di mana teks baru harus muncul. Rectangle mendefinisikan posisi (x, y) dan ukuran (lebar, tinggi).

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

Silakan sesuaikan perhitungan agar cocok dengan kebutuhan tata letak Anda.

### Langkah 5: Tambahkan Lapisan Teks
Buat lapisan teks sebenarnya di dalam rectangle yang telah ditentukan.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

Ganti `"Added text"` dengan string apa pun yang ingin Anda tampilkan di PSD. Inilah tempat kami **membuat lapisan teks PSD** secara programatik.

### Langkah 6: Simpan File PSD yang Telah Diperbarui
Tuliskan dokumen yang telah dimodifikasi ke file baru sehingga Anda tidak menimpa yang asli.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

Setelah dijalankan, Anda akan menemukan `ImageWithTextLayer.psd` di folder target, kini berisi lapisan teks baru.

## Masalah Umum & Solusi
| Masalah | Penyebab | Solusi |
|-------|--------|-----|
| **`NullPointerException` pada `im.addTextLayer`** | PSD tidak dimuat dengan benar (jalur salah). | Pastikan `sourceFileName` mengarah ke PSD yang ada. |
| **Teks tidak terlihat** | Rectangle berada di luar kanvas atau lapisan tersembunyi. | Sesuaikan koordinat rectangle atau periksa visibilitas lapisan dengan `layer.setVisible(true)`. |
| **LicenseException** | Menggunakan pustaka tanpa lisensi yang valid di produksi. | Dapatkan lisensi komersial dan atur dengan `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |

## Pertanyaan yang Sering Diajukan

**T: Apakah saya dapat menambahkan beberapa lapisan teks?**  
J: Ya – cukup ulangi Langkah 4 dan 5 untuk setiap teks yang ingin Anda sisipkan.

**T: Bagaimana cara menata teks (font, ukuran, warna)?**  
J: Kelas `TextLayer` menyediakan metode `getTextData()` di mana Anda dapat memodifikasi `Font`, `FontSize`, `Color`, dan properti gaya lainnya. Lihat dokumentasi API Aspose.PSD untuk detail lengkap.

**T: Bagaimana jika PSD saya sudah memiliki banyak lapisan?**  
J: Aspose.PSD bekerja dengan struktur lapisan yang kompleks. Anda dapat menargetkan grup tertentu atau menyisipkan lapisan teks baru pada indeks yang diinginkan menggunakan overload `addTextLayer`.

**T: Apakah pendekatan ini cocok untuk aplikasi web?**  
J: Tentu. Selama server Anda menjalankan Java, Anda dapat menghasilkan atau memodifikasi PSD secara langsung dan menyajikannya ke klien.

**T: Di mana saya dapat mendapatkan bantuan jika mengalami masalah?**  
J: Kunjungi [forum dukungan Aspose](https://forum.aspose.com/c/psd/34) di mana komunitas dan insinyur Aspose siap membantu.

## Kesimpulan
Anda kini telah melihat betapa mudahnya **menambahkan teks ke PSD** pada runtime menggunakan Java dan Aspose.PSD. Teknik ini memungkinkan Anda mengotomatisasi pembuatan grafik, mempersonalisasi aset, dan mengintegrasikan penyuntingan tingkat Photoshop ke dalam solusi berbasis Java apa pun. Jelajahi API Aspose.PSD lainnya untuk menambahkan bentuk, lapisan raster, atau bahkan menerapkan filter untuk otomatisasi yang lebih kaya.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2026-03-07  
**Diuji Dengan:** Aspose.PSD for Java 24.12 (terbaru pada saat penulisan)  
**Penulis:** Aspose