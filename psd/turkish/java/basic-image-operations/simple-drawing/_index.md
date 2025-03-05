---
title: Aspose.PSD for Java ile Basit Çizim Gerçekleştirin
linktitle: Basit Çizim Gerçekleştirin
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java'yı kullanarak PSD dosyalarında nasıl şekil çizeceğinizi öğrenin. Bu adım adım kılavuz, kod örnekleriyle katman oluşturmayı, eklemeyi ve çizim yapmayı kapsar.
type: docs
weight: 10
url: /tr/java/basic-image-operations/simple-drawing/
---
## giriiş

Aspose.PSD for Java kullanarak basit çizim yapmayı anlatan bu adım adım kılavuza hoş geldiniz! Bu derste yeni bir PSD belgesi oluşturmanın, katman eklemenin ve farklı renklerle şekiller çizmenin temellerini keşfedeceğiz. Aspose.PSD for Java, PSD dosyalarını programlı olarak değiştirmenizi sağlayan, grafik tasarım görevleri için kapsamlı işlevsellik sağlayan güçlü bir kütüphanedir.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Makinenizde Java Geliştirme Kiti (JDK) yüklü.
- Java kütüphanesi için Aspose.PSD. adresinden indirebilirsiniz.[Java Belgelendirmesi için Aspose.PSD](https://reference.aspose.com/psd/java/).

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Java projenize aktarın. Java dosyanızın başına aşağıdaki kodu ekleyin:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## 1. Adım: Yeni Bir Belge Oluşturun

Belirtilen genişlik ve yükseklikte yeni bir PSD belgesi oluşturarak başlayalım:

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:Belge Oluştur
```

## 2. Adım: Katman Ekleme

Şimdi bağımsız değişken içermeyen yapıcıyı kullanarak belgeye bir katman ekleyelim:

```java
//ExStart:Katman Ekle
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:Katman Ekle
```

## Adım 3: Şekiller Çizin

Bu adımda, oluşturulan katmana şekiller çizmek için Graphics sınıfını kullanacağız:

### Sarı Renkli Bir Dikdörtgen Çizin

```java
//ExStart:ÇizimDikdörtgenSarı
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:ÇizimDikdörtgenSarı
```

### Kırmızı Bir Dikdörtgen Çizin

```java
//ExStart:ÇizimKırmızıDikdörtgen
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:ÇizimKırmızıDikdörtgen
```

### Mavi Bir Dikdörtgen Çizin

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueDikdörtgen
```

## 4. Adım: Değişiklikleri Kaydedin

Son olarak, yüklenen PSD dosyasının bir kopyasını değişikliklerle birlikte kaydedin:

```java
//ExStart:Değişiklikleri Kaydet
image.save(outPsdFilePath);
//ExEnd:Değişiklikleri Kaydet
```

## Çözüm

Tebrikler! Aspose.PSD for Java'yı kullanarak basit çizimleri başarıyla gerçekleştirdiniz. Bu eğitimde yeni bir belge oluşturma, katman ekleme ve farklı renklerde dikdörtgenler çizme konuları yer alıyordu. Grafik tasarım ihtiyaçlarınız için kütüphanenin sunduğu daha gelişmiş özellikleri keşfetmekten çekinmeyin.

## SSS'ler

### S1: Mevcut PSD dosyalarını değiştirmek için Aspose.PSD for Java'yı kullanabilir miyim?

Cevap1: Evet, Aspose.PSD for Java, mevcut PSD dosyalarını düzenlemek ve değiştirmek için kapsamlı işlevsellik sağlar.

### S2: Aspose.PSD for Java desteğini nerede bulabilirim?

 A2: ziyaret edebilirsiniz[Java Forumu için Aspose.PSD](https://forum.aspose.com/c/psd/34) Destekle ilgili tüm sorularınız için.

### S3: Aspose.PSD for Java'nın ücretsiz deneme sürümü mevcut mu?

 Cevap3: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.PSD for Java lisansını nasıl satın alabilirim?

 Cevap4: Lisansı şuradan satın alabilirsiniz:[Aspose.PSD Satın Alma Sayfası](https://purchase.aspose.com/buy).

### S5: Aspose.PSD for Java için geçici lisanslar mevcut mu?

 Cevap5: Evet, adresinden geçici lisans alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).