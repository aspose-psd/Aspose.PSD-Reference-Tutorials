---
title: Aspose.PSD for Java'yı kullanarak Görüntüleri Birleştirin
linktitle: Görselleri Birleştir
second_title: Aspose.PSD Java API'si
description: Aspose.PSD ile Java'daki görüntüleri nasıl birleştireceğinizi öğrenin. Sorunsuz görüntü kombinasyonu için adım adım kılavuzumuzu izleyin.
type: docs
weight: 11
url: /tr/java/image-editing/combine-images/
---
## giriiş

Java programlama alanında Aspose.PSD, görüntüleri değiştirmek ve işlemek için güçlü bir araç olarak öne çıkıyor. Dikkate değer özelliklerinden biri, birden fazla görüntüyü kusursuz bir şekilde birleştirme yeteneğidir. Bu eğitim, Aspose.PSD for Java kullanarak iki görüntüyü tek bir PSD dosyasında birleştirme sürecinde size rehberlik edecektir.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1.  Aspose.PSD Kütüphanesi: Java ortamınızda Aspose.PSD kütüphanesinin kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/psd/java/).

2. Java Geliştirme Kiti (JDK): Aspose.PSD'nin çalışması için Java gerekir. Makinenize en son JDK'yı yükleyin.

3. Belge Dizini: Resimlerinizin ve elde edilen PSD dosyasının saklanacağı bir dizin ayarlayın.

## Paketleri İçe Aktar

Java projeniz için gerekli paketleri içe aktararak başlayın. Aspose.PSD kütüphanesini aşağıda gösterildiği gibi projenize ekleyin:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## 1. Adım: PSD Seçenekleri Oluşturun

Bir PsdOptions örneği oluşturarak ve çeşitli özelliklerini ayarlayarak başlayın:

```java
PsdOptions imageOptions = new PsdOptions();
```

## Adım 2: FileCreateSource'u ayarlayın

FileCreateSource örneğini oluşturun ve bunu Source özelliğine atayın:

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

## 3. Adım: Görüntü Örneği Oluşturun

Belirtilen seçenekler ve boyutlarla bir Image nesnesinin örneğini oluşturun:

```java
Image image = Image.create(imageOptions, 600, 600);
```

## Adım 4: Grafikleri Başlatın

Bir Graphics örneği oluşturun ve başlatın, görüntü yüzeyini beyaz renkle temizleyin ve ilk görüntüyü çizin:

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

## Adım 5: İkinci Resmi Çizin

İkinci görüntüyü oluşturulan PSD tuvaline çizin:

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

## Adım 6: Ortaya Çıkan Resmi Kaydedin

Son birleştirilmiş görüntüyü kaydedin:

```java
image.save();
```

Tebrikler! Aspose.PSD for Java'yı kullanarak iki görüntüyü tek bir PSD dosyasında başarıyla birleştirdiniz.

## Çözüm

Aspose.PSD, Java'da görüntü işlemeyi basitleştirerek görüntüleri zahmetsizce birleştirmek için sağlam bir çözüm sunar. Bu eğitimi takip ederek, görsel olarak çekici kompozisyonlar oluşturmak için Aspose.PSD'nin gücünden yararlandınız.

## SSS'ler

### S1: Aspose.PSD tüm görüntü formatlarıyla uyumlu mu?

Cevap1: Aspose.PSD öncelikle PSD dosya formatına odaklanır. Ancak giriş ve çıkış için diğer çeşitli formatları destekler.

### S2: Birleştirilmiş görüntüde ek değişiklikler yapabilir miyim?

A2: Kesinlikle! Görüntüleri birleştirdikten sonra Aspose.PSD'nin kapsamlı özelliklerini kullanarak ortaya çıkan PSD'yi daha da değiştirebilirsiniz.

### S3: Aspose.PSD'yi kullanmak için herhangi bir lisans gereksinimi var mı?

 C3: Evet, ticari kullanım için geçerli bir lisans gereklidir. Şu adresten edinin:[Burada](https://purchase.aspose.com/buy).

### S4: Aspose.PSD için ücretsiz deneme sürümü mevcut mu?

 Cevap4: Evet, Aspose.PSD'yi ücretsiz deneme sürümüyle keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S5: Aspose.PSD ile ilgili sorgular için desteği nerede bulabilirim?

 A5: ziyaret edin[Aspose.PSD forumu](https://forum.aspose.com/c/psd/34) topluluk desteği ve tartışmalar için.