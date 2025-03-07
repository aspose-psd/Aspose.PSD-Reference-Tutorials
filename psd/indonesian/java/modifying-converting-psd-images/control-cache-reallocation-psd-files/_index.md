---
title: Kontrol Realokasi Cache di File PSD
linktitle: Kontrol Realokasi Cache di File PSD
second_title: Asumsikan.PSD Java API
description: Kelola realokasi cache di file PSD menggunakan Aspose.PSD untuk Java. Pelajari cara mengoptimalkan memori dan penanganan file secara efisien—ideal bagi pengembang.
weight: 22
url: /id/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kontrol Realokasi Cache di File PSD

## Perkenalan
Saat bekerja dengan gambar dan file Photoshop secara terprogram, efisiensi adalah faktor kuncinya. Aspose.PSD untuk Java menawarkan fitur canggih untuk mengelola dan memanipulasi file PSD dengan lancar. Salah satu aspek mendasar dalam mengoptimalkan kinerja adalah mengendalikan realokasi cache. Manajemen cache membantu menjaga keseimbangan antara penggunaan memori dan disk, memastikan aplikasi Anda berjalan dengan lancar, tanpa crash atau perlambatan yang tidak terduga. 
## Prasyarat
Sebelum kita masuk ke bagian pengkodean, ada beberapa hal yang perlu Anda pastikan agar semuanya berjalan lancar:
1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di mesin Anda. Anda dapat mengunduhnya dari[situs web Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD untuk Java: Anda perlu mengunduh perpustakaan Aspose.PSD. Anda dapat menemukan rilis terbaru[Di Sini](https://releases.aspose.com/psd/java/).
3. Penyiapan IDE: Lingkungan Pengembangan Terpadu (IDE) seperti IntelliJ IDEA atau Eclipse akan memudahkan Anda mengelola kode.
4. Pemahaman Dasar Java: Keakraban dengan pemrograman Java akan membantu Anda memahami konsep dan cuplikan kode dengan lebih baik.
5.  Lisensi Aspose (Opsional): Jika Anda ingin menghapus tanda air dan mendapatkan fungsionalitas penuh, pertimbangkan untuk membeli lisensi[Di Sini](https://purchase.aspose.com/buy) atau mencoba uji coba gratis[Di Sini](https://releases.aspose.com/).
## Paket Impor
Sebelum kita mulai menulis kode, pastikan kita telah mengimpor paket yang diperlukan. Di bawah ini adalah daftar singkat tentang apa yang harus disertakan di awal file Java Anda:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```
## Langkah 1: Menyiapkan Direktori Data Anda
Hal pertama yang pertama, Anda harus menyiapkan direktori tempat Anda ingin menyimpan file cache. Ini penting untuk mengelola cache secara efektif.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Tentukan direktori untuk cache dokumen Anda.
- Cache.setCacheFolder(dataDir): Metode ini mengatur folder cache ke direktori yang ditentukan. Setiap cache yang dibuat oleh Aspose sekarang akan disimpan di sini, bukan di direktori sementara default.
## Langkah 2: Mengonfigurasi Cache Ke Disk
Selanjutnya, kita akan menentukan bahwa kita ingin cache kita disimpan di disk saja. Hal ini sangat berguna jika aplikasi Anda menggunakan file besar dan Anda ingin memastikan memori tetap bebas.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Opsi ini memastikan bahwa cache tidak disimpan di memori, yang bermanfaat untuk menangani file PSD besar tanpa menghabiskan terlalu banyak RAM.
## Langkah 3: Mengatur Ukuran Cache Disk dan Memori Maksimum
Sekarang, mari kita batasi ukuran cache kita. Ini penting karena cache yang tidak terbatas dapat menyebabkan masalah kinerja.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabit
Cache.setMaxMemoryForCache(1073741824); // 1 gigabit
```

- Cache.setMaxDiskSpaceForCache(1073741824): Ini menetapkan batas 1 GB untuk cache pada disk. Anda dapat menyesuaikan ukuran ini tergantung kebutuhan Anda.
- Cache.setMaxMemoryForCache(1073741824): Demikian pula, ini membatasi cache dalam memori, memastikan aplikasi Anda tidak menggunakan memori berlebihan.
## Langkah 4: Kelola Strategi Realokasi Cache
Mengelola bagaimana cache dialokasikan kembali sangat penting untuk menjaga kinerja. Inilah cara Anda mengaturnya.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocationOnly(false): Jika disetel ke false, hal ini memungkinkan Aspose mengelola realokasi cache dengan lebih fleksibel, sehingga dapat menghasilkan performa yang lebih baik.
## Langkah 5: Periksa Ukuran Cache yang Dialokasikan
Langkah ini tentang memantau berapa byte yang saat ini dialokasikan untuk cache di memori atau di disk. Mari kita terapkan itu:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Menyimpan jumlah byte yang dialokasikan pada disk.
- long l2: Menyimpan jumlah byte yang dialokasikan dalam memori. 
Anda dapat memeriksa nilai-nilai ini kapan saja untuk memastikan aplikasi Anda mengelola penggunaan memori dan disk seperti yang diharapkan.
## Langkah 6: Membuat Gambar PSD
Sekarang kita sudah menyiapkan konfigurasi cache, mari buat gambar PSD sederhana.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- Opsi PsdOptions: Objek ini memungkinkan Anda menentukan opsi saat membuat gambar Photoshop.
- Warna[] warna: Array berisi warna yang akan digunakan dalam palet gambar.
## Langkah 7: Menyimpan Data Piksel ke Gambar
Sekarang, mari isi gambar kita dengan data piksel dan simpan.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Warna[] piksel: Ini adalah susunan objek berwarna. Di sini, kami mengisinya dengan piksel putih.
- image.savePixels(image.getBounds(), piksel): Metode ini menyimpan data piksel ke gambar. Ini memperbarui gambar dengan warna yang telah kita tentukan.
## Langkah 8: Memantau Cache yang Dialokasikan Setelah Pembuatan Gambar
Setelah membuat gambar, sebaiknya periksa kembali berapa banyak byte yang dialokasikan untuk cache.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- diskBytes panjang: Menangkap alokasi saat ini pada disk setelah pembuatan gambar.
- long memoryBytes: Menangkap alokasi saat ini di memori. 
Langkah ini akan membantu Anda menentukan berapa banyak cache yang digunakan setelah operasi Anda.
## Langkah 9: Periksa Pembuangan yang Benar
Terakhir, penting untuk memastikan bahwa semua objek Aspose.PSD dibuang dengan benar untuk menghindari kebocoran memori.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 dan l2: Variabel-variabel ini akan membantu Anda memeriksa alokasi akhir. Jika nilainya tidak nol, ini menunjukkan beberapa benda belum dibuang dengan benar.
## Kesimpulan
Mengontrol realokasi cache di Aspose.PSD untuk Java dapat membuat perbedaan signifikan dalam performa aplikasi Anda. Dengan mengikuti langkah-langkah yang diuraikan di atas, Anda dapat mengelola cache secara efektif, meminimalkan penggunaan memori, dan membuat file PSD yang indah secara efisien. Gunakan teknik ini, dan saksikan aplikasi Anda berkembang dengan kinerja optimal!
## FAQ
### Apa itu Aspose.PSD?
Aspose.PSD adalah perpustakaan bagi pengembang .NET dan Java untuk membuat, memanipulasi, dan mengonversi file Photoshop (PSD) secara terprogram.
### Bagaimana cara memeriksa ukuran cache yang dialokasikan?
 Gunakan metode seperti`Cache.getAllocatedDiskBytesCount()` Dan`Cache.getAllocatedMemoryBytesCount()` untuk memantau penggunaan cache saat ini.
### Bisakah saya menyetel direktori khusus untuk cache?
 Ya, Anda dapat menentukan direktori lain dengan menggunakan`Cache.setCacheFolder("Your Directory Path")`.
### Apakah Aspose.PSD gratis untuk digunakan?
Aspose.PSD adalah perpustakaan berbayar, tetapi Anda dapat memulai dengan uji coba gratis yang tersedia di perpustakaan mereka[situs web](https://releases.aspose.com/).
### Apa yang terjadi jika saya tidak membuang benda?
Tidak membuang objek dapat menyebabkan kebocoran memori, menyebabkan aplikasi Anda menggunakan lebih banyak sumber daya daripada yang diperlukan.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
