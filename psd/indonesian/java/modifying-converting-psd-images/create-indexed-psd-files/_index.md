---
date: 2026-03-15
description: Pelajari cara membuat file PSD, menghasilkan palet warna PSD, dan mengatur
  mode warna PSD menggunakan Aspose.PSD untuk Java dalam panduan langkah demi langkah
  ini.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Cara Membuat File PSD Menggunakan Aspose.PSD untuk Java
url: /id/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Membuat File PSD Menggunakan Aspose.PSD untuk Java

## Pendahuluan
Jika Anda pernah bertanya-tanya **cara membuat PSD** secara programatis, Anda berada di tempat yang tepat. Aspose.PSD untuk Java memberi Anda kontrol penuh atas dokumen Photoshop, memungkinkan Anda menghasilkan, mengedit, dan menyimpan file PSD tanpa pernah membuka Photoshop. Dalam tutorial ini kami akan membahas cara membuat file **PSD terindeks**, mengatur mode warna PSD, dan menghasilkan palet warna khusus—semua dengan kode Java yang jelas langkah demi langkah. Baik Anda membangun pipeline grafis, mengotomatisasi pembuatan aset, atau sekadar bereksperimen, konsep di sini akan membantu Anda mewujudkan ide visual Anda.

## Jawaban Cepat
- **Perpustakaan apa yang saya butuhkan?** Aspose.PSD untuk Java  
- **Bisakah saya membuat PSD terindeks?** Ya, dengan mengatur mode warna ke `Indexed`  
- **Apakah saya perlu menginstal Photoshop?** Tidak, Aspose.PSD berfungsi secara mandiri  
- **Versi Java mana yang diperlukan?** JDK 8 atau lebih baru  
- **Seberapa besar kanvas yang dapat dibuat?** Ukuran apa saja; contoh ini menggunakan 500 × 500 px  

## Apa itu File PSD Terindeks?
PSD terindeks menyimpan warna dalam sebuah palet alih-alih nilai warna penuh untuk setiap piksel. Ini mengurangi ukuran file dan ideal untuk grafis dengan warna terbatas, seperti ikon atau aset UI. Dengan menghasilkan palet khusus, Anda mengontrol tepat warna apa yang muncul dalam gambar akhir.

## Mengapa Membuat Palet Warna PSD?
Membuat **palet warna PSD** memungkinkan Anda:
- Menjaga ukuran file tetap kecil untuk penggunaan web atau seluler  
- Menjamin konsistensi merek dengan membatasi warna pada palet perusahaan Anda  
- Mempercepat proses rendering pada aplikasi yang mendukung gambar terindeks  

## Prasyarat
Sebelum kita masuk ke kode, pastikan Anda memiliki hal‑hal berikut:

1. **Pengetahuan Dasar tentang Java** – Anda harus nyaman dengan kelas, metode, dan pembuatan objek.  
2. **Java Development Kit (JDK) 8+** – terinstal dan dikonfigurasi di IDE Anda.  
3. **IDE (IntelliJ IDEA, Eclipse, dll.)** – opsional namun sangat disarankan untuk memudahkan debugging.  
4. **Aspose.PSD untuk Java Library** – unduh **[di sini](https://releases.aspose.com/psd/java/)** dan tambahkan JAR ke classpath proyek Anda.  
5. **Konsep Dasar Desain Grafis** – pemahaman tentang mode warna, palet, dan bentuk dasar akan membantu Anda mengikuti tutorial.

## Impor Paket
Sebelum melanjutkan dengan kode, pastikan semua paket yang diperlukan telah diimpor ke aplikasi Java Anda. Berikut yang Anda perlukan:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Impor ini memungkinkan Anda bekerja dengan opsi PSD, warna, dan manipulasi grafis melalui Aspose.PSD.

Sekarang, mari kita uraikan kode langkah demi langkah untuk **cara membuat PSD** dengan mode warna terindeks.

## Langkah 1: Siapkan Direktori Dokumen Anda
Pertama, tentukan di mana PSD yang dihasilkan akan disimpan.

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur absolut atau relatif, misalnya `"/Users/YourName/Documents/"`.

## Langkah 2: Buat Instance PsdOptions
`PsdOptions` menyimpan semua pengaturan untuk file yang akan Anda hasilkan.

```java
PsdOptions createOptions = new PsdOptions();
```

## Langkah 3: Atur Properti Inti PsdOptions
Di sini kami menentukan lokasi output, **mengatur mode warna psd** ke `Indexed`, dan versi PSD.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – jalur lengkap file baru.  
- **Color Mode** – `Indexed` memberi tahu Aspose.PSD untuk menggunakan gambar berbasis palet.  
- **Version** – versi format PSD (5 bekerja untuk kebanyakan versi Photoshop modern).

## Langkah 4: Buat Palet Warna (Hasilkan Palet Warna PSD)
Tentukan warna‑warna yang akan tersedia dalam gambar terindeks.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- Array `palette` dapat menampung hingga 256 objek `Color`.  
- `CompressionMethod.RLE` menyediakan kompresi lossless yang efisien untuk gambar terindeks.

## Langkah 5: Buat Kanvas Gambar PSD
Sekarang kami membuat PSD kosong dengan dimensi yang diinginkan.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Ini membuat kanvas berukuran 500 × 500 piksel yang menggunakan palet yang didefinisikan sebelumnya.

## Langkah 6: Gambar Grafik pada PSD
Tambahkan konten visual—di sini kami menggambar elips merah sederhana di atas latar putih.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` mengisi latar belakang dengan warna putih.  
- `drawEllipse` menggambar elips merah dengan ketebalan garis 6 piksel.

## Langkah 7: Simpan File PSD
Akhirnya, simpan gambar ke disk.

```java
psd.save();
```

File `Newsample_out.psd` akan muncul di direktori yang Anda tentukan sebelumnya.

## Masalah Umum & Tips
- **Ukuran Palet** – Jika Anda membutuhkan lebih dari 4 warna, cukup tambahkan ke array `palette` (maksimum 256).  
- **Izin File** – Pastikan proses Java memiliki akses menulis ke `dataDir`.  
- **Mode Warna Salah** – Lupa menambahkan `createOptions.setColorMode(ColorModes.Indexed)` akan menghasilkan PSD RGB alih‑alih yang terindeks.  

## Pertanyaan yang Sering Diajukan

**Q: Apa itu Aspose.PSD untuk Java?**  
A: Aspose.PSD untuk Java adalah perpustakaan yang memungkinkan manipulasi file PSD (Photoshop) secara programatis menggunakan Java.

**Q: Bisakah saya menggunakan Aspose.PSD secara gratis?**  
A: Ya, Anda dapat mengakses versi percobaan gratis Aspose.PSD **[di sini](https://releases.aspose.com/)**.

**Q: Apakah saya perlu menginstal Photoshop untuk bekerja dengan Aspose.PSD?**  
A: Tidak, Anda dapat membuat dan memanipulasi file PSD tanpa Photoshop, karena Aspose.PSD menangani semua operasi secara independen.

**Q: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?**  
A: Anda dapat meminta lisensi sementara **[di sini](https://purchase.aspose.com/temporary-license/)**.

**Q: Di mana saya dapat mendapatkan dukungan untuk Aspose.PSD?**  
A: Anda dapat mendapatkan dukungan dari forum Aspose **[di sini](https://forum.aspose.com/c/psd/34)**.

## Kesimpulan
Anda baru saja mempelajari **cara membuat PSD** dengan mode warna terindeks, menghasilkan palet khusus, dan menambahkan grafik sederhana—semua menggunakan Aspose.PSD untuk Java. Dengan blok‑blok dasar ini Anda dapat memperluas ke gambar yang lebih kompleks, manajemen lapisan, dan pemrosesan batch. Untuk eksplorasi lebih mendalam, lihat referensi API resmi **[di sini](https://reference.aspose.com/psd/java/)** dan terus bereksperimen dengan berbagai palet serta primitif menggambar.

---

**Last Updated:** 2026-03-15  
**Tested With:** Aspose.PSD untuk Java 24.12 (terbaru)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}