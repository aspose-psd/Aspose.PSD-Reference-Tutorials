---
title: Aspose.PSD for Java'da Gaussian ve Wiener Filtrelerini Uygulayın
linktitle: Gauss ve Wiener Filtrelerini Uygula
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java görüntü işlemenizi geliştirin. Çarpıcı görsel sonuçlar için Gauss ve Wiener filtrelerini adım adım uygulamayı öğrenin.
weight: 10
url: /tr/java/image-processing/apply-gaussian-wiener-filters/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java'da Gaussian ve Wiener Filtrelerini Uygulayın

## giriiş

Aspose.PSD for Java'da Gauss ve Wiener filtrelerinin uygulanmasına ilişkin kapsamlı eğitimimize hoş geldiniz! Bu kılavuzda, bu güçlü filtreleri kullanarak görsellerinizi geliştirme sürecinde size yol göstereceğiz. Aspose.PSD for Java, görüntü işleme için güçlü bir dizi özellik sunar ve Gaussian ve Wiener filtrelerinin uygulanmasıyla daha pürüzsüz ve daha rafine görüntüler elde edebilirsiniz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.

- Aspose.PSD for Java Library: Aspose.PSD for Java kütüphanesini indirip yükleyin. İndirme linkini bulabilirsiniz[Burada](https://releases.aspose.com/psd/java/).

## Paketleri İçe Aktar

Aspose.PSD için gerekli paketleri Java projenize aktarın. Başlamanıza yardımcı olacak örnek bir içe aktarma ifadesini burada bulabilirsiniz:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Şimdi Gaussian ve Wiener filtrelerini uygulamak için örneği birden fazla adıma ayıralım.

## 1. Adım: Resmi Yükleyin

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

Bu adımda PSD imaj dosyasını belirtilen dizinden yüklüyoruz.

## Adım 2: RasterImage'ı kontrol edin

```java
if (rasterImage == null) {
    return;
}
```

Yüklenen görüntünün geçerli bir RasterImage olduğundan emin olun; aksi takdirde süreç sonlandırılır.

## 3. Adım: Filtre Seçeneklerini Yapılandırın

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

Bir GaussWienerFilterOptions örneği oluşturun, yarıçap boyutunu ve düzgün değeri ayarlayın ve filtreyi gri tonlamalı olarak uygulamak isteyip istemediğinizi belirtin.

## 4. Adım: Filtre Uygula ve Kaydet

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

Son olarak, yapılandırılmış Gaussian ve Wiener filtrelerini RasterImage'a uygulayın ve ortaya çıkan görüntüyü GIF formatında kaydedin.

## Çözüm

Tebrikler! Aspose.PSD for Java'yı kullanarak Gauss ve Wiener filtrelerini nasıl uygulayacağınızı başarıyla öğrendiniz. İstenilen görüntü iyileştirmelerini elde etmek için farklı parametrelerle denemeler yapın.

## SSS'ler

### S1: Bu filtreleri PSD dışındaki formatlardaki görsellere uygulayabilir miyim?

Cevap1: Evet, Aspose.PSD for Java, PSD'nin ötesinde çeşitli görüntü formatlarını destekler.

### S2: Aspose.PSD for Java'nın deneme sürümünde herhangi bir kısıtlama var mı?

Cevap2: Deneme sürümünün sınırlamaları vardır ve geçerli bir lisans alarak tüm özellikleri keşfedebilirsiniz.

### S3: Aspose.PSD for Java desteğini nasıl alabilirim?

 A3: Ziyaret edin[Aspose.PSD Forumu](https://forum.aspose.com/c/psd/34) topluluk desteği ve tartışmalar için.

### S4: Test amaçlı geçici bir lisans mevcut mu?

 Cevap4: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Aspose.PSD for Java'nın ayrıntılı belgelerini nerede bulabilirim?

 A5: Bkz.[dokümantasyon](https://reference.aspose.com/psd/java/) derinlemesine bilgi için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
