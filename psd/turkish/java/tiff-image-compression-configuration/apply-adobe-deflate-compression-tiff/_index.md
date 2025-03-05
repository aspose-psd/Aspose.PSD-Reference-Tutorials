---
title: Adobe Deflate Sıkıştırmasını TIFF'e Uygulama - Java
linktitle: Adobe Deflate Sıkıştırmasını TIFF'e Uygulama - Java
second_title: Aspose.PSD Java API'si
description: Aspose.PSD for Java kullanarak Adobe Deflate sıkıştırmasını TIFF görüntülerine nasıl uygulayacağınızı öğrenin. Verimli görüntü işleme için adım adım kılavuz.
type: docs
weight: 12
url: /tr/java/tiff-image-compression-configuration/apply-adobe-deflate-compression-tiff/
---
## giriiş

Kaliteden ödün vermeden TIFF görüntülerinizi verimli bir şekilde nasıl sıkıştıracağınızı hiç merak ettiniz mi? Büyük görüntü dosyalarıyla uğraşıyorsanız, muhtemelen yavaş yükleme sürelerinin ve depolama sorunlarının acısını biliyorsunuzdur. İşte burada Adobe Deflate sıkıştırma devreye giriyor ve Aspose.PSD for Java ile bunu projelerinize kolayca uygulayabilirsiniz. Bu eğitim, Adobe Deflate sıkıştırmasını bir TIFF görüntüsüne adım adım uygulama konusunda size yol gösterecektir. Dalmaya hazır mısınız? Hadi başlayalım!

## Önkoşullar

Gerçek koda geçmeden önce her şeyin ayarlandığından emin olalım. İşte ihtiyacınız olan şey:

1. Java Geliştirme Kiti (JDK): Makinenizde JDK'nın en son sürümünün kurulu olduğundan emin olun.
2.  Aspose.PSD for Java: Aspose.PSD for Java kütüphanesini indirin ve projenize entegre edin. Şu adresten alabilirsiniz:[Burada](https://releases.aspose.com/psd/java/).
3. Geliştirme Ortamı: IntelliJ IDEA, Eclipse veya NetBeans gibi bir IDE.
4.  Geçici Lisans (İsteğe bağlı): Satın almaya hazır değilseniz,[geçici lisans](https://purchase.aspose.com/temporary-license/) Özellikleri denemek için.

## Paketleri İçe Aktar

Gerekli paketleri Java projenize aktararak başlayalım. Bu içe aktarmalar, Aspose.PSD kütüphanesi ve Java yardımcı programları ile çalışmanıza izin verdiği için çok önemlidir.

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.TiffRational;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.fileformats.tiff.enums.TiffPlanarConfigs;
import com.aspose.psd.fileformats.tiff.enums.TiffResolutionUnits;
import com.aspose.psd.imageoptions.TiffOptions;
```

Artık temel konuları ele aldığımıza göre, süreci takip edilmesi kolay adımlara ayıralım.

## 1. Adım: TIFF Seçeneklerini Ayarlayın

 İlk önce bir örnek oluşturmanız gerekir:`TiffOptions` ve ihtiyaçlarınıza göre yapılandırın. Bu seçenekler, çözünürlüğü, renk şeması ve sıkıştırma dahil olmak üzere TIFF dosyasının nasıl işleneceğini tanımlar.

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
```

Burada bir yaratıyoruz`TiffOptions` varsayılan formatta nesne. Ama bu sadece başlangıç! 

## 2. Adım: Görüntü Özelliklerini Yapılandırın

 Daha sonra, TIFF görüntüsünün aşağıdaki gibi çeşitli özelliklerini ayarlamanız gerekir:`BitsPerSample`, `Photometric`, `Resolution` , Ve`PlanarConfiguration`. Bu ayarlar, görüntü verilerinin nasıl saklanacağını ve görüntüleneceğini belirler.

```java
int[] ushort = { 8, 8, 8 };
options.setBitsPerSample(ushort);
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
```

İşte her mülkün yaptığı şey:
- BitsPerSample: Her renk kanalı için örnek başına bit sayısını ayarlar.
- Fotometrik: Renk modelini tanımlar (bu durumda RGB).
- Çözünürlük: Görüntünün yatay ve dikey çözünürlüğünü belirtir.
- PlanarConfiguration: Piksel verilerinin nasıl saklanacağını belirler.

## 3. Adım: Adobe Deflate Sıkıştırmasını Uygulayın

Şimdi sihir geliyor! TIFF görüntünüze, görüntü kalitesini kaybetmeden dosya boyutunu küçültmenize yardımcı olan Adobe Deflate sıkıştırmasını uygulayacaksınız.

```java
options.setCompression(TiffCompressions.AdobeDeflate);
```

Adobe Deflate, dosya boyutunu küçültürken yüksek kaliteyi korumanız gereken görüntüler için mükemmel olan kayıpsız bir sıkıştırma yöntemidir.

## 4. Adım: TIFF Görüntüsünü Oluşturun ve Düzenleyin

Seçenekler ayarlandığında, yeni bir TIFF görüntüsü oluşturma ve onu değiştirme zamanı geldi. Bu adımda 100x100 boyutunda basit bir görsel oluşturup onu kırmızı piksellerle dolduracağız.

```java
PsdImage tiffImage = new PsdImage(100, 100);

for (int j = 0; j < tiffImage.getHeight(); j++) {
    for (int i = 0; i < tiffImage.getWidth(); i++) {
        tiffImage.setPixel(i, j, Color.getRed());
    }
}
```

Burada görüntünün her pikseli arasında döngü yapıyoruz ve rengini kırmızıya ayarlıyoruz. Elbette daha karmaşık görseller oluşturmak için bu kısmı özelleştirebilirsiniz.

## Adım 5: Sıkıştırılmış TIFF Görüntüsünü Kaydetme

Son olarak görüntüyü yapılandırıp oluşturduktan sonra son adım, uygulanan sıkıştırmayla kaydetmektir. Doğru dizin yolunu belirttiğinizden emin olun.

```java
String dataDir = "Your Document Directory";
tiffImage.save(dataDir + "TIFFwithAdobeDeflateCompression_output.tif");
```

İşte bu! Aspose.PSD for Java kullanarak Adobe Deflate sıkıştırmasını bir TIFF görüntüsüne başarıyla uyguladınız.

## Çözüm

Ve işte karşınızda! Aspose.PSD for Java ile Adobe Deflate sıkıştırmasını TIFF görüntülerine uygulamak basit bir işlemdir. Web siteniz, dijital medyanız veya başka bir projeniz için büyük görsellerle çalışıyor olsanız da, bu yöntem dosyalarınızın yüksek kalitede kalmasını ve boyut olarak daha yönetilebilir olmasını sağlar. Aspose.PSD for Java'nın gücü, basitliği ve verimliliğinde yatıyor; bu da onu karmaşık görüntü formatlarıyla çalışan geliştiricilerin başvuracağı bir araç haline getiriyor.

## SSS'ler

### Adobe Deflate sıkıştırması nedir?
Adobe Deflate, kaliteyi kaybetmeden TIFF görüntülerinin boyutunu küçültmek için kullanılan kayıpsız bir sıkıştırma yöntemidir.

### Aspose.PSD for Java ile diğer sıkıştırma yöntemlerini kullanabilir miyim?
Evet, Aspose.PSD, LZW, CCITT ve JPEG gibi çeşitli sıkıştırma yöntemlerini destekler.

### Aspose.PSD kütüphanesi ücretsiz mi?
 Aspose.PSD ücretsiz deneme sürümü sunar ancak tam işlevsellik için lisans gereklidir. Alabilirsin[geçici lisans](https://purchase.aspose.com/temporary-license/) denemek için.

### Çözünürlük ayarı TIFF görüntüsünü nasıl etkiler?
Çözünürlük, yazdırıldığında veya görüntülendiğinde görüntünün netliğini belirler. Daha yüksek çözünürlükler daha iyi kalite sağlar ancak daha büyük dosya boyutlarına neden olur.

### Aspose.PSD for Java ile diğer görüntü formatlarını değiştirebilir miyim?
Kesinlikle! Aspose.PSD, PSD, PNG, JPEG ve daha fazlası gibi çeşitli formatları destekler.