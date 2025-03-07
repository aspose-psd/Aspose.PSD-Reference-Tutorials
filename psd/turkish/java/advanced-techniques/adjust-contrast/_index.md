---
title: Aspose.PSD for Java ile Görüntünün Kontrastını Ayarlama
linktitle: Bir Görüntünün Kontrastını Ayarlama
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java'da görüntü kontrastı ayarlama dünyasını keşfedin. Sorunsuz görüntü işleme için adım adım kılavuzumuzu izleyin.
weight: 22
url: /tr/java/advanced-techniques/adjust-contrast/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java ile Görüntünün Kontrastını Ayarlama

## giriiş

Java ile görüntü işleme alanında Aspose.PSD güçlü bir araç olarak öne çıkıyor. Sayısız özelliği arasında görüntü kontrastının ayarlanması ortak bir gerekliliktir. Bu eğitim, Aspose.PSD for Java kullanarak görüntü kontrastını ayarlama sürecinde size yol gösterecektir. İster deneyimli bir geliştirici olun, ister yeni başlıyor olun, bu kılavuz, görüntü manipülasyonunun bu önemli yönünde uzmanlaşmanıza yardımcı olacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

- Java programlamanın temel anlayışı.
-  Aspose.PSD for Java kütüphanesi kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/psd/java/).

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Java projenize aktarmanız gerekir. Kodunuza aşağıdaki satırları ekleyin:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 1. Adım: Görüntüyü Yükleyin

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Mevcut bir görüntüyü RasterImage sınıfının bir örneğine yükleme
Image image = Image.load(sourceFile);
```

 Bu adımda örnek görseli ("sample.psd") aşağıdaki komutu kullanarak yüklüyoruz:`Image.load` Yöntem.

## Adım 2: RasterImage ve Önbellek Verilerine Yayınlama

```java
// Image nesnesini RasterImage'a yayınla
RasterImage rasterImage = (RasterImage)image;

// Daha iyi performans için RasterImage'ın önbelleğe alınıp alınmadığını kontrol edin ve RasterImage'ı Önbelleğe Alın
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Burada geneli yayınlıyoruz`Image` bir şeye itiraz etmek`RasterImage` özel işleme için. Görüntü verilerinin önbelleğe alınması performansı artırır.

## 3. Adım: Kontrastı Ayarlayın

```java
// Kontrastı ayarlayın
rasterImage.adjustContrast(50);
```

`adjustContrast`Görüntünün kontrastını değiştirmek için kullanılan yöntem. Bu örnekte kontrast %50 artırılmıştır.

## Adım 4: TiffOptions Oluşturun ve Kaydedin

```java
// Ortaya çıkan görüntü için bir TiffOptions örneği oluşturun
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Ortaya çıkan görüntüyü TIFF formatında kaydedin
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Burada kurduk`TiffOptions` çıktı görüntüsü için formatı ve diğer özellikleri belirterek. Son görüntü daha sonra bir TIFF dosyasına kaydedilir.

## Çözüm

Tebrikler! Aspose.PSD for Java'yı kullanarak görüntünün kontrastını başarıyla ayarladınız. Bu eğitim, paketlerin içe aktarılmasından işlenen görüntünün kaydedilmesine kadar temel adımları kapsıyordu.

## SSS'ler

### S1: Aspose.PSD farklı görüntü formatlarıyla uyumlu mudur?

Cevap1: Evet, Aspose.PSD çeşitli görüntü formatlarını destekleyerek projelerinizde esneklik sağlar.

### S2: Aspose.PSD için nasıl geçici lisans alabilirim?

 Cevap2: Geçici bir lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S3: Aspose.PSD belgelerini nerede bulabilirim?

A3: Belgeler mevcut[Burada](https://reference.aspose.com/psd/java/).

### S4: Aspose.PSD için hangi destek seçenekleri mevcut?

 Cevap4: Destek için şu adresi ziyaret edin:[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34).

### S5: Aspose.PSD'yi satın alabilir miyim?

 Cevap5: Evet, Aspose.PSD'yi satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
