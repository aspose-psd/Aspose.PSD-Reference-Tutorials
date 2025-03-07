---
title: Terapkan Efek Stroke dengan Isian Warna di PSD - Java
linktitle: Terapkan Efek Stroke dengan Isian Warna di PSD - Java
second_title: Asumsikan.PSD Java API
description: Pelajari cara menerapkan efek guratan dengan isian warna ke file PSD Anda menggunakan Aspose.PSD untuk Java. Ikuti panduan langkah demi langkah ini untuk menyempurnakan gambar Anda dengan mudah.
weight: 21
url: /id/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Terapkan Efek Stroke dengan Isian Warna di PSD - Java

## Perkenalan

Dalam panduan ini, kami akan memandu Anda melalui proses penerapan efek guratan dengan isian warna ke file PSD Anda menggunakan Aspose.PSD untuk Java. Baik Anda seorang pengembang berpengalaman atau baru memulai, tutorial langkah demi langkah ini akan memudahkan Anda menyelesaikan pekerjaan. Kami akan membahas semuanya mulai dari menyiapkan lingkungan Anda hingga menyimpan gambar akhir dengan efek yang diterapkan.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki semua yang perlu Anda ikuti bersama dengan tutorial ini:

1. Java Development Kit (JDK) Terpasang: Pastikan Anda telah menginstal JDK 8 atau lebih tinggi di sistem Anda.
2.  Aspose.PSD untuk Perpustakaan Java: Anda memerlukan perpustakaan Aspose.PSD untuk Java. Anda dapat mengunduhnya dari[situs web](https://releases.aspose.com/psd/java/).
3. Lingkungan Pengembangan Terpadu (IDE): IDE seperti IntelliJ IDEA, Eclipse, atau lainnya pilihan Anda.
4. Contoh File PSD: Contoh file PSD tempat Anda dapat menerapkan efek guratan. Jika Anda tidak memilikinya, Anda dapat membuat file PSD sederhana di Photoshop atau mendownloadnya dari internet.
5. Pengetahuan Dasar tentang Java: Meskipun tutorial ini ramah bagi pemula, memiliki beberapa pengetahuan dasar tentang Java akan bermanfaat.

Setelah Anda memiliki prasyarat ini, Anda siap untuk mulai menerapkan efek guratan dengan isian warna pada file PSD Anda.

## Paket Impor

Untuk mulai bekerja dengan Aspose.PSD untuk Java, Anda perlu mengimpor paket yang diperlukan ke proyek Java Anda. Inilah cara Anda melakukannya:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Impor ini menghadirkan semua kelas yang Anda perlukan untuk bekerja dengan file PSD, menerapkan efek, dan menyimpan gambar dalam format yang Anda inginkan.

## Langkah 1: Muat File PSD

 Langkah pertama dalam proses kami adalah memuat file PSD yang ingin Anda modifikasi. Aspose.PSD untuk Java menjadikan ini sangat sederhana dengan`PsdImage` kelas. Inilah cara Anda melakukannya:

### 1.1 Tetapkan Jalur Direktori

Pertama, tentukan jalur direktori tempat file PSD Anda disimpan:

```java
String dataDir = "Your Document Directory";
```

 Mengganti`"Your Document Directory"` dengan jalur sebenarnya tempat file PSD Anda berada.

### 1.2 Muat Gambar PSD

 Sekarang, muat file PSD menggunakan`PsdLoadOptions` Dan`PsdImage` kelas:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

 Di sini, itu`PsdLoadOptions`dikonfigurasi untuk memuat sumber daya efek, memastikan bahwa setiap efek yang ada dalam PSD dapat diakses.

## Langkah 2: Terapkan Efek Stroke dengan Color Fill

Setelah file PSD dimuat, langkah selanjutnya adalah menerapkan efek guratan pada lapisan gambar. Di sinilah keajaiban sesungguhnya terjadi.

Setiap file PSD mungkin berisi beberapa lapisan, dan Anda harus menerapkan efeknya pada masing-masing lapisan. Berikut cara melakukannya:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

Dalam lingkaran ini:

- `im.getLayers()`: Mengambil semua lapisan dalam file PSD.
- `StrokeEffect effect`: Mengekstrak efek guratan yang diterapkan pada lapisan.
- `ColorFillSettings settings`: Memodifikasi pengaturan isian untuk efek guratan.
- `settings.setColor(Color.getDeepPink())`: Mengatur warna guratan menjadi merah muda tua. Anda dapat mengubahnya ke warna apa pun yang Anda inginkan.

## Langkah 3: Simpan PSD yang Dimodifikasi dan Ekspor sebagai PNG

Setelah Anda menerapkan efek guratan, sekarang saatnya menyimpan perubahan dan mengekspor gambar.

### 3.1 Simpan File PSD

Untuk menyimpan file PSD yang dimodifikasi, gunakan kode berikut:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

Ini menyimpan file dengan efek guratan yang diterapkan ke jalur yang ditentukan.

### 3.2 Ekspor sebagai PNG

Agar gambar lebih mudah diakses, Anda mungkin ingin mengekspornya sebagai file PNG. Begini caranya:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

Cuplikan kode ini menyimpan gambar sebagai PNG dengan warna asli dan transparansi alfa, sehingga siap digunakan dalam aplikasi web atau platform lain.

## Kesimpulan

Menerapkan efek guratan dengan isian warna pada file PSD Anda menggunakan Aspose.PSD untuk Java tidak hanya mudah tetapi juga sangat hebat. Hanya dengan beberapa baris kode, Anda dapat mengotomatiskan tugas pemrosesan gambar yang rumit, sehingga menghemat waktu dan tenaga.

Baik Anda sedang mengerjakan gambar dalam jumlah besar atau hanya perlu mengubah beberapa file, metode ini memberikan solusi yang fleksibel dan efisien. Sekarang setelah Anda menguasai dasar-dasarnya, Anda dapat mulai bereksperimen dengan berbagai efek dan penyesuaian untuk membuat gambar Anda benar-benar menonjol.

Siap mencobanya? Ambil contoh file PSD Anda dan mulailah menambahkan efek menakjubkan itu hari ini!

## FAQ

### Bisakah saya menerapkan banyak efek ke satu lapisan menggunakan Aspose.PSD untuk Java?
Ya, Anda dapat menerapkan banyak efek ke satu lapisan dengan mengakses opsi pencampuran lapisan dan menambahkan efek yang diinginkan.

### Apakah mungkin untuk mengotomatiskan proses sekumpulan file PSD?
Sangat! Anda dapat menelusuri direktori file PSD, menerapkan efek guratan, dan menyimpan hasilnya secara otomatis.

### Bagaimana cara mengembalikan perubahan yang dibuat pada file PSD menggunakan Aspose.PSD untuk Java?
Untuk mengembalikan perubahan, Anda perlu memuat ulang file PSD asli sebelum menyimpan modifikasi apa pun. Tidak ada fitur undo langsung di Aspose.PSD.

### Bisakah saya menyesuaikan lebar dan posisi goresan?
 Ya, Aspose.PSD untuk Java memungkinkan Anda menyesuaikan lebar guratan, posisi, dan properti lainnya melalui`StrokeEffect` kelas.

### Apakah perpustakaan Aspose.PSD untuk Java gratis untuk digunakan?
 Aspose.PSD untuk Java menawarkan uji coba gratis, tetapi untuk akses penuh ke semua fitur, Anda perlu membeli lisensi. Anda dapat menjelajahi[membeli opsi](https://purchase.aspose.com/buy)di situs web mereka.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
