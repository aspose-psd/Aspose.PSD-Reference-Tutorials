---
date: 2026-03-02
description: Pelajari cara menambahkan isian dengan membuat lapisan isian warna dalam
  file PSD menggunakan Java dan Aspose.PSD. Ikuti panduan langkah demi langkah kami
  untuk mengatur warna lapisan isian dengan cepat.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'Cara Menambahkan Isi: Menambahkan Lapisan Isi Warna ke File PSD menggunakan
  Java'
url: /id/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tambahkan Layer Isi Warna ke File PSD menggunakan Java

## Introduction
Pernahkah Anda perlu memanipulasi file Photoshop secara programatik, mungkin untuk menambahkan sentuhan warna pada sebuah desain? Jika Anda bertanya‑tanya **how to add fill** ke sebuah PSD, Anda berada di tempat yang tepat. Pada tutorial ini kami akan menjelaskan cara menambahkan layer isi warna ke file PSD (Photoshop Document) menggunakan Java dan pustaka Aspose.PSD. Anggap PSD Anda sebagai kanvas digital—pada akhir Anda akan tahu cara membuat layer isi warna, mengatur warna layer isi, dan menyimpan file yang telah diperbarui hanya dengan beberapa baris kode.

## Quick Answers
- **What library is needed?** Aspose.PSD for Java  
- **Primary use case?** Programmatically add or change PSD fill colors  
- **How long does implementation take?** About 10‑15 minutes for a basic scenario  
- **Do I need a license?** A free trial works for evaluation; a commercial license is required for production  
- **Supported Java version?** Java 8 and above  

## What is a Color Fill Layer?
Layer isi warna adalah lapisan overlay berwarna solid yang berada di atas lapisan lain dalam dokumen Photoshop. Biasanya digunakan untuk menambahkan warna latar belakang, membuat masker, atau dengan cepat mengubah tema visual sebuah desain tanpa mengedit piksel secara individual.

## Why add a color fill layer with code?
- **Automation:** Menghasilkan aset merek yang konsisten di banyak file.  
- **Batch processing:** Memperbarui puluhan PSD dalam hitungan detik alih‑alih melakukannya secara manual.  
- **Dynamic designs:** Mengubah warna secara dinamis berdasarkan masukan pengguna atau sumber data.

## Prerequisites
Sebelum kita masuk ke kode, pastikan Anda memiliki semua yang diperlukan:

1. **Java Development Kit (JDK)** – JDK 8 atau lebih baru terpasang.  
2. **Aspose.PSD Library** – Unduh JAR terbaru dari [Aspose Releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans, atau editor apa pun yang Anda sukai.  
4. **Basic Java knowledge** – Familiarity with objects, loops, and exception handling.

## Import Packages
Sekarang setelah dasar‑dasarnya tercakup, mari impor kelas‑kelas yang diperlukan. Impor ini memberi kita akses ke penanganan PSD dan manipulasi layer isi.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## How to Add Fill – Step‑by‑Step Guide

### Step 1: Set Up Your Environment
Tentukan di mana PSD sumber berada dan ke mana file yang telah diedit akan disimpan, lalu muat dokumennya.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` menunjuk ke folder yang berisi PSD Anda.  
- `sourceFileName` adalah file asli yang akan Anda modifikasi.  
- `exportPath` adalah lokasi file baru dengan **add color fill layer** yang akan ditulis.  

### Step 2: Loop Through the Layers
Kita perlu menemukan setiap layer isi yang ada sehingga dapat memodifikasinya atau membuat yang baru.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- Loop `for` mengiterasi setiap layer dalam PSD.  
- Pemeriksaan `instanceof FillLayer` memastikan kita hanya bekerja dengan layer isi.

### Step 3: Verify the Fill Type
Pastikan layer yang kita temukan adalah **color fill layer** sebelum mencoba mengubah warnanya.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

Jika tipe isi bukan `FillType.Color`, proses dihentikan untuk menghindari perubahan tidak sengaja pada isi gradien atau pola.

### Step 4: Set the Fill Color
Di sinilah kita **set fill layer color**. Contoh ini mengubah layer menjadi merah, tetapi Anda dapat mengganti `Color.getRed()` dengan `Color` lain yang Anda butuhkan (misalnya `Color.getBlue()`, `new Color(255, 165, 0)` untuk oranye).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` mengubah warna isi yang sebenarnya.  
- `fillLayer.update()` memperbarui layer sehingga warna baru diterapkan.  

### Step 5: Save the Changes
Akhirnya, tulis kembali PSD yang telah dimodifikasi ke disk.

```java
im.save(exportPath);
break;
```

- `break` menghentikan loop setelah layer isi pertama yang cocok diperbarui, yang biasanya yang Anda inginkan ketika hanya perlu **change PSD fill color** sekali.

## Common Issues & Tips
- **No FillLayer found:** Jika PSD Anda tidak mengandung layer isi, Anda perlu membuatnya menggunakan `new FillLayer(im)` dan menambahkannya ke `im.getLayers()`.  
- **Color not updating:** Pastikan Anda memanggil `fillLayer.update()` setelah mengatur warna.  
- **File not saved:** Verifikasi bahwa `exportPath` mengarah ke direktori yang dapat ditulisi dan Anda memiliki izin menulis file di sana.  

## Frequently Asked Questions

**Q: What is Aspose.PSD?**  
A: Aspose.PSD is a robust Java library that lets you create, edit, and convert Photoshop PSD files without needing Adobe Photoshop.

**Q: Can I use Aspose.PSD for free?**  
A: Yes, a free trial is available on the [Aspose Releases page](https://releases.aspose.com/).  

**Q: Which file formats can I work with besides PSD?**  
A: Aspose.PSD supports PSD, PSB, BMP, JPEG, PNG, GIF, TIFF, and more.

**Q: How do I get support if I run into problems?**  
A: You can ask questions on the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).  

**Q: Where can I purchase a full license?**  
A: Licenses are sold through the [Aspose Purchase page](https://purchase.aspose.com/buy).

## Conclusion
Anda kini tahu **how to add fill** ke dokumen Photoshop secara programatik dengan Java. Dengan membuat atau menemukan layer isi warna, mengatur warnanya, dan menyimpan hasilnya, Anda dapat mengotomatiskan tugas desain berulang, menghasilkan aset dinamis, atau mengintegrasikan manipulasi PSD ke dalam aplikasi Java yang lebih besar. Cobalah—eksperimen dengan warna berbeda, tambahkan beberapa layer isi, atau gabungkan teknik ini dengan fitur Aspose.PSD lainnya untuk pipeline pemrosesan gambar yang kuat.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose