---
date: 2026-04-03
description: Pelajari cara mengurangi ukuran file PSD dengan meratakan lapisan menggunakan
  Aspose.PSD untuk Java. Panduan langkah demi langkah ini menunjukkan cara meratakan
  file PSD dengan cepat.
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: Kurangi Ukuran File PSD dengan Meratakan Lapisan – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: Kurangi Ukuran File PSD dengan Meratakan Lapisan – Aspose.PSD Java
url: /id/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kurangi Ukuran File PSD dengan Meratakan Lapisan – Aspose.PSD Java

## Pendahuluan

Jika Anda pernah membuka dokumen Photoshop dan bertanya-tanya bagaimana cara **reduce PSD file size**, meratakan lapisan adalah salah satu trik paling efektif. Dengan Aspose.PSD untuk Java Anda dapat secara programatis meratakan seluruh PSD atau menggabungkan hanya lapisan yang Anda pilih, memberi Anda kontrol detail atas ukuran file tanpa mengorbankan kualitas visual. Dalam tutorial ini kami akan membahas kedua pendekatan—meratakan seluruh gambar dan menggabungkan lapisan tertentu—sehingga Anda dapat dengan cepat memperkecil file PSD Anda dan menjaga alur kerja tetap lancar.

## Jawaban Cepat
- **Apa yang dilakukan flattening?** Ia menggabungkan lapisan yang terlihat menjadi satu lapisan latar belakang, menghapus informasi lapisan dan sering mengurangi ukuran file.  
- **Apakah saya dapat meratakan hanya lapisan yang dipilih?** Ya, Anda dapat menggabungkan lapisan tertentu sambil membiarkan yang lain tidak tersentuh.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Versi Java apa yang diperlukan?** JDK 8 atau lebih tinggi.  
- **Apakah flattening akan memengaruhi kualitas gambar?** Tidak, tampilan visual tetap sama; hanya struktur lapisan yang berubah.

## Apa itu “reduce PSD file size”?

Mengurangi ukuran file PSD berarti menghapus data yang tidak diperlukan—seperti lapisan tambahan, saluran tersembunyi, atau metadata berlebih—sehingga file menjadi lebih ringan dan lebih cepat dimuat, dibagikan, atau diproses. Meratakan lapisan adalah teknik umum karena membuang objek lapisan terpisah sambil mempertahankan gambar komposit akhir.

## Mengapa meratakan lapisan dengan Aspose.PSD untuk Java?

- **Otomasi:** Tidak perlu membuka Photoshop secara manual; integrasikan langsung ke dalam aplikasi Java Anda.  
- **Presisi:** Pilih untuk meratakan seluruh dokumen atau hanya lapisan yang terlihat (`flattenImage`) atau menggabungkan lapisan yang dipilih (`mergeLayers`).  
- **Kinerja:** File yang lebih kecil dimuat lebih cepat dan mengonsumsi lebih sedikit memori dalam proses selanjutnya.  
- **Lintas‑platform:** Berfungsi pada sistem operasi apa pun yang mendukung Java.

## Prasyarat

1. **Java Development Kit (JDK):** JDK 8 atau yang lebih baru terpasang.  
2. **Aspose.PSD for Java:** Unduh perpustakaan dari [here](https://releases.aspose.com/psd/java/).  
3. **IDE:** IntelliJ IDEA, Eclipse, atau IDE yang kompatibel dengan Java apa pun.  
4. **Basic Java knowledge:** Berguna tetapi tidak wajib untuk mengikuti langkah-langkah.  
5. **Sample PSD:** Sebuah file dengan beberapa lapisan (kami akan menggunakan `ThreeRegularLayersSemiTransparent.psd`).

Sekarang semua sudah siap, mari kita selami kode.

## Impor Paket

Untuk memulai, impor kelas Aspose.PSD yang penting:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Impor ini memungkinkan kami memuat file PSD, bekerja dengan lapisannya, dan menyimpan hasilnya.

## Langkah 1: Meratakan Seluruh Gambar PSD

Meratakan seluruh gambar adalah cara tercepat untuk **reduce PSD file size** karena menghapus semua data lapisan individu.

### 1.1 Muat File PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 Meratakan Gambar

```java
im.flattenImage();
```

### 1.3 Simpan Gambar yang Diratakan

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

File baru Anda kini berisi satu lapisan latar belakang, yang biasanya menghasilkan ukuran PSD yang lebih kecil.

## Langkah 2: Menggabungkan Lapisan Tertentu (Cara meratakan PSD secara selektif)

Terkadang Anda hanya ingin **flatten visible layers** atau menggabungkan sebagian lapisan sambil mempertahankan yang lain dapat diedit.

### 2.1 Muat File PSD Lagi

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 Identifikasi dan Pilih Lapisan

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 Gabungkan Lapisan

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 Ganti Lapisan yang Ada dengan Lapisan yang Digabungkan

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 Simpan File PSD yang Diperbarui

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Sekarang PSD hanya berisi lapisan yang digabungkan, menghasilkan ukuran file yang lebih kecil sambil mempertahankan lapisan yang ingin Anda simpan.

## Masalah Umum & Tips

- **Cadangkan sebelum meratakan:** Setelah lapisan diratakan, operasi tidak dapat dibatalkan. Simpan salinan PSD asli.  
- **Visibilitas penting:** `flattenImage()` hanya menggabungkan lapisan *yang terlihat*. Sembunyikan lapisan apa pun yang tidak ingin Anda sertakan.  
- **Penggunaan memori:** PSD besar dapat mengonsumsi RAM yang signifikan; pertimbangkan memprosesnya pada mesin dengan memori yang cukup.  
- **Mode pencampuran:** Penggabungan menghormati mode pencampuran setiap lapisan, sehingga hasil visual sesuai dengan yang Anda lihat di Photoshop.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya membatalkan perataan lapisan di Aspose.PSD?**  
A: Tidak, perataan tidak dapat dibalik. Selalu simpan cadangan file asli.

**Q: Apakah memungkinkan untuk meratakan hanya lapisan yang terlihat?**  
A: Ya. `flattenImage()` menghormati visibilitas lapisan, jadi sembunyikan lapisan yang tidak ingin Anda ratakan sebelum memanggil metode tersebut.

**Q: Apakah perataan lapisan mengurangi ukuran file?**  
A: Secara umum, ya. Menghapus data lapisan dan metadata sering menghasilkan PSD yang lebih kecil, meskipun pengurangan tepatnya tergantung pada kontennya.

**Q: Bisakah saya menggabungkan lapisan dengan mode pencampuran yang berbeda?**  
A: Tentu saja. Aspose.PSD menggabungkan lapisan sambil mempertahankan tampilan visual yang dihasilkan oleh mode pencampuran mereka.

**Q: Apa yang terjadi jika saya mencoba menggabungkan lapisan yang tidak bersebelahan?**  
A: Aspose.PSD memungkinkan penggabungan lapisan apa pun terlepas dari urutannya dalam tumpukan; hasilnya mencerminkan tampilan gabungan.

---

**Terakhir Diperbarui:** 2026-04-03  
**Diuji Dengan:** Aspose.PSD 24.11 for Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}