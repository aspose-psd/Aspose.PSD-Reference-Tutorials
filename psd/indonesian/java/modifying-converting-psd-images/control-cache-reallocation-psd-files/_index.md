---
date: 2026-03-13
description: Pelajari cara membuat proyek Java gambar PSD sambil mengelola alokasi
  ulang cache dengan Aspose.PSD untuk Java. Optimalkan penggunaan memori dan disk
  secara efisien.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Buat Gambar PSD Java – Kontrol Pengalokasian Ulang Cache
url: /id/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengontrol Realokasi Cache dalam File PSD

## Pendahuluan
Jika Anda perlu **create PSD image java** proyek secara efisien, mengontrol realokasi cache sangat penting. Saat bekerja dengan gambar dan file Photoshop secara programatik, efisiensi menjadi faktor kunci. Aspose.PSD for Java menawarkan fitur kuat untuk mengelola dan memanipulasi file PSD dengan mulus. Salah satu aspek fundamental dalam mengoptimalkan kinerja adalah mengontrol realokasi cache. Manajemen cache membantu menjaga keseimbangan antara penggunaan memori dan disk, memastikan aplikasi Anda berjalan lancar, tanpa crash atau perlambatan yang tidak terduga. 

## Jawaban Cepat
- **Apa yang dilakukan reallocasi cache?** Itu menyeimbangkan penggunaan memori dan disk saat memproses file PSD besar.  
- **Jenis cache apa yang terbaik untuk gambar besar?** `CacheOnDiskOnly` menjaga memori tetap bebas dengan menyimpan cache di disk.  
- **Berapa banyak ruang disk yang dapat saya alokasikan?** Hingga 1 GB (atau ukuran apa pun yang Anda atur dengan `setMaxDiskSpaceForCache`).  
- **Apakah saya memerlukan lisensi untuk menggunakan fitur ini?** Lisensi menghapus batasan trial; lihat halaman pembelian Aspose.  
- **Bisakah saya memantau penggunaan cache saat runtime?** Ya, gunakan `Cache.getAllocatedDiskBytesCount()` dan `Cache.getAllocatedMemoryBytesCount()`.

## Mengapa Mengontrol Realokasi Cache?
Mengelola cache sangat penting ketika Anda **create PSD image java** aplikasi yang menangani file beresolusi tinggi atau multi‑layer. Pengaturan cache yang tepat mencegah kesalahan out‑of‑memory, mengurangi jeda GC, dan memberikan kinerja yang dapat diprediksi pada server atau aplikasi desktop.

## Prasyarat
Sebelum kita masuk ke bagian coding, ada beberapa hal yang perlu Anda pastikan agar semuanya berjalan lancar:
1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di mesin Anda. Anda dapat mengunduhnya dari [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Anda perlu mengunduh pustaka Aspose.PSD. Anda dapat menemukan rilis terbaru [here](https://releases.aspose.com/psd/java/).
3. IDE Setup: Integrated Development Environment (IDE) seperti IntelliJ IDEA atau Eclipse akan memudahkan Anda mengelola kode.
4. Basic Understanding of Java: Familiaritas dengan pemrograman Java akan membantu Anda memahami konsep dan potongan kode dengan lebih baik.
5. Aspose License (Optional): Jika Anda ingin menghapus watermark dan mendapatkan fungsionalitas penuh, pertimbangkan membeli lisensi [here](https://purchase.aspose.com/buy) atau mencoba trial gratis [here](https://releases.aspose.com/).

## Impor Paket
Sebelum kita mulai menulis kode, pastikan kita telah mengimpor paket yang diperlukan. Berikut adalah daftar singkat apa yang harus disertakan di awal file Java Anda:
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

## Cara Membuat PSD Image Java dengan Kontrol Cache
Berikut adalah langkah‑demi‑langkah yang mengaitkan konfigurasi cache langsung dengan proses pembuatan gambar PSD di Java.

### Langkah 1: Menyiapkan Direktori Data Anda
Hal pertama yang perlu dilakukan, Anda harus menyiapkan direktori tempat file cache akan disimpan. Ini penting untuk mengelola cache secara efektif.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Mendefinisikan direktori untuk cache dokumen Anda.  
- `Cache.setCacheFolder(dataDir)`: Metode ini mengatur folder cache ke direktori yang ditentukan. Semua cache yang dibuat oleh Aspose kini akan disimpan di sini alih‑alih direktori temporer default.

### Langkah 2: Mengonfigurasi Cache ke Disk
Selanjutnya, kita akan menentukan bahwa cache harus disimpan hanya di disk. Ini sangat berguna jika aplikasi Anda menggunakan file besar dan Anda ingin memastikan memori tetap bebas.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Opsi ini memastikan cache tidak disimpan di memori, yang menguntungkan untuk menangani file PSD besar tanpa mengonsumsi terlalu banyak RAM.

### Langkah 3: Menetapkan Ukuran Maksimum Cache Disk dan Memori
Sekarang, mari batasi ukuran cache kita. Ini penting karena cache tak terbatas dapat menyebabkan masalah kinerja.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Ini menetapkan batas 1 GB untuk cache di disk. Anda dapat menyesuaikan ukuran ini sesuai kebutuhan.  
- `Cache.setMaxMemoryForCache(1073741824)`: Demikian pula, ini membatasi cache di memori, memastikan aplikasi Anda tidak menggunakan memori berlebih.

### Langkah 4: Mengelola Strategi Realokasi Cache
Mengelola cara cache direalokasikan penting untuk menjaga kinerja. Berikut cara mengaturnya.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Ketika diatur ke `false`, ini memungkinkan Aspose mengelola reallocasi cache secara lebih fleksibel, yang dapat meningkatkan kinerja.

### Langkah 5: Memeriksa Ukuran Cache yang Dialokasikan
Langkah ini tentang memantau berapa banyak byte yang saat ini dialokasikan untuk cache di memori atau di disk. Mari implementasikan:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Menyimpan jumlah byte yang dialokasikan di disk.  
- `long l2`: Menyimpan jumlah byte yang dialokasikan di memori.  
Anda dapat memeriksa nilai‑nilai ini kapan saja untuk memastikan aplikasi Anda mengelola penggunaan memori dan disk sebagaimana mestinya.

### Langkah 6: Membuat Gambar PSD
Setelah konfigurasi cache selesai, mari buat gambar PSD sederhana.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Objek ini memungkinkan Anda menentukan opsi saat membuat gambar Photoshop.  
- `Color[] color`: Sebuah array yang berisi warna‑warna yang akan digunakan dalam palet gambar.

### Langkah 7: Menyimpan Data Piksel ke Gambar
Sekarang, mari isi gambar dengan data piksel dan simpan.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Ini adalah array objek warna. Di sini, kami mengisinya dengan piksel putih.  
- `image.savePixels(image.getBounds(), pixels)`: Metode ini menyimpan data piksel ke gambar. Ini memperbarui gambar dengan warna yang telah kami definisikan.

### Langkah 8: Memantau Cache yang Dialokasikan Setelah Pembuatan Gambar
Setelah membuat gambar, sebaiknya periksa kembali berapa banyak byte yang dialokasikan untuk cache.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Menangkap alokasi saat ini di disk setelah pembuatan gambar.  
- `long memoryBytes`: Menangkap alokasi saat ini di memori.  
Langkah ini akan membantu Anda menentukan berapa banyak cache yang dikonsumsi setelah operasi Anda.

### Langkah 9: Memeriksa Pembuangan yang Tepat
Terakhir, penting memastikan semua objek Aspose.PSD dibuang dengan benar untuk menghindari kebocoran memori.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` dan `l2`: Variabel ini akan membantu Anda memeriksa alokasi akhir. Jika tidak nol, itu menunjukkan beberapa objek belum dibuang dengan benar.

## Masalah Umum dan Solusinya
- **Folder cache tidak dibuat** – Pastikan aplikasi memiliki izin menulis untuk path yang Anda berikan ke `Cache.setCacheFolder`.  
- **Kesalahan out‑of‑memory** – Periksa kembali bahwa `Cache.setCacheType(CacheType.CacheOnDiskOnly)` diterapkan sebelum memuat file PSD besar.  
- **Ukuran cache tidak terduga** – Gunakan metode `Cache.getAllocated*BytesCount()` setelah setiap operasi utama untuk melacak pertumbuhan.

## Pertanyaan yang Sering Diajukan

**Q: Apa itu Aspose.PSD?**  
A: Aspose.PSD adalah pustaka untuk pengembang .NET dan Java untuk membuat, memanipulasi, dan mengonversi file Photoshop (PSD) secara programatik.

**Q: Bagaimana cara memeriksa ukuran cache yang dialokasikan?**  
A: Gunakan metode seperti `Cache.getAllocatedDiskBytesCount()` dan `Cache.getAllocatedMemoryBytesCount()` untuk memantau penggunaan cache saat ini.

**Q: Bisakah saya menentukan direktori khusus untuk cache?**  
A: Ya, Anda dapat menentukan direktori berbeda dengan menggunakan `Cache.setCacheFolder("Your Directory Path")`.

**Q: Apakah Aspose.PSD gratis untuk digunakan?**  
A: Aspose.PSD adalah pustaka berbayar, tetapi Anda dapat memulai dengan trial gratis yang tersedia di [website](https://releases.aspose.com/).

**Q: Apa yang terjadi jika saya tidak membuang objek?**  
A: Tidak membuang objek dapat menyebabkan kebocoran memori, membuat aplikasi Anda menggunakan lebih banyak sumber daya daripada yang diperlukan.

## Kesimpulan
Mengontrol realokasi cache saat Anda **create PSD image java** aplikasi dapat membuat perbedaan signifikan dalam kinerja. Dengan mengikuti langkah‑langkah di atas, Anda akan mengelola cache secara efisien, meminimalkan konsumsi memori, dan menghasilkan file PSD berkualitas tinggi dengan Aspose.PSD for Java. Terapkan teknik ini, dan proyek Anda akan berjalan lebih mulus serta skalabel.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}