---
date: 2026-03-15
description: Bu adım adım rehberde Aspose.PSD for Java kullanarak PSD dosyaları oluşturmayı,
  PSD renk paleti oluşturmayı ve PSD renk modunu ayarlamayı öğrenin.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java Kullanarak PSD Dosyaları Nasıl Oluşturulur
url: /tr/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

 backtop button shortcode at end.

Make sure to keep all markdown formatting.

Let's produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java Kullanarak PSD Dosyaları Nasıl Oluşturulur

## Giriş
Programatik olarak **PSD nasıl oluşturulur** diye merak ettiyseniz, doğru yerdesiniz. Aspose.PSD for Java, Photoshop belgeleri üzerinde tam kontrol sağlar; Photoshop’u hiç açmadan PSD dosyaları oluşturabilir, düzenleyebilir ve kaydedebilirsiniz. Bu öğreticide, **indeksli bir PSD** dosyası oluşturmayı, PSD renk modunu ayarlamayı ve özel bir renk paleti üretmeyi net, adım‑adım Java kodlarıyla göstereceğiz. Grafik boru hattı oluşturuyor, varlık üretimini otomatikleştiriyor ya da sadece deneme yapıyor olun, burada yer alan kavramlar görsel fikirlerinizi hayata geçirmenize yardımcı olacak.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.PSD for Java  
- **İndeksli bir PSD oluşturabilir miyim?** Evet, renk modunu `Indexed` olarak ayarlayarak  
- **Photoshop yüklü olması gerekiyor mu?** Hayır, Aspose.PSD bağımsız çalışır  
- **Hangi Java sürümü gerekli?** JDK 8 veya üzeri  
- **Tuval ne kadar büyük olabilir?** Herhangi bir boyut; bu örnek 500 × 500 px kullanıyor

## İndeksli PSD Dosyası Nedir?
İndeksli bir PSD, her piksel için tam renk değerleri yerine bir palet içinde renkleri saklar. Bu, dosya boyutunu azaltır ve ikonlar ya da UI varlıkları gibi sınırlı renkli grafikler için idealdir. Özel bir palet oluşturarak, son görüntüde hangi renklerin görüneceğini tam olarak kontrol edebilirsiniz.

## Neden PSD Renk Paleti Oluşturmalısınız?
**PSD renk paleti** oluşturmak şunları sağlar:
- Web veya mobil kullanım için dosya boyutlarını küçük tutar  
- Kurumsal paletinize sınırlı renkler ekleyerek tutarlı marka kimliği sağlar  
- İndeksli görüntüleri destekleyen uygulamalarda render süresini hızlandırır  

## Önkoşullar
Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Temel Bilgisi** – sınıflar, metodlar ve nesne oluşturma konularında rahat olmalısınız.  
2. **Java Development Kit (JDK) 8+** – IDE’nizde kurulu ve yapılandırılmış.  
3. **IDE (IntelliJ IDEA, Eclipse vb.)** – isteğe bağlı ancak hata ayıklamayı kolaylaştırdığı için şiddetle tavsiye edilir.  
4. **Aspose.PSD for Java Kütüphanesi** – **[buradan](https://releases.aspose.com/psd/java/)** indirin ve JAR dosyasını projenizin sınıf yoluna ekleyin.  
5. **Temel Grafik Tasarım Kavramları** – renk modları, paletler ve temel şekiller hakkında bilgi, içeriği daha iyi takip etmenizi sağlar.

## Paketleri İçe Aktarın
Kodlamaya başlamadan önce, Java uygulamanıza gerekli paketlerin tümünün içe aktarılmış olduğundan emin olalım. İşte ihtiyacınız olanlar:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Bu içe aktarmalar, Aspose.PSD aracılığıyla PSD seçenekleri, renkler ve grafik manipülasyonu ile çalışmanıza olanak tanır.

Şimdi, **indeksli renk moduyla PSD nasıl oluşturulur** konusunu adım‑adım inceleyelim.

## Adım 1: Belge Dizinini Ayarlayın
İlk olarak, oluşturulan PSD’nin kaydedileceği yeri tanımlayın.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini mutlak ya da göreli bir yol ile değiştirin; örnek: `"/Users/YourName/Documents/"`.

## Adım 2: PsdOptions Örneği Oluşturun
`PsdOptions`, oluşturacağınız dosyanın tüm ayarlarını tutar.

```java
PsdOptions createOptions = new PsdOptions();
```

## Adım 3: PsdOptions’ın Temel Özelliklerini Ayarlayın
Burada çıktı konumunu, **psd renk modunu** `Indexed` olarak ayarlamayı ve PSD sürümünü belirtiyoruz.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – yeni dosyanın tam yolu.  
- **Color Mode** – `Indexed`, Aspose.PSD’nin palet‑tabanlı bir görüntü kullanmasını sağlar.  
- **Version** – PSD format sürümü (5, çoğu modern Photoshop sürümü için uygundur).

## Adım 4: Renk Paleti Oluşturun (PSD Renk Paleti Oluşturma)
İndeksli görüntüde kullanılacak renkleri tanımlayın.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- `palette` dizisi en fazla 256 `Color` nesnesi tutar.  
- `CompressionMethod.RLE`, indeksli görüntüler için verimli kayıpsız sıkıştırma sağlar.

## Adım 5: PSD Görüntü Tuvalini Oluşturun
Şimdi istediğimiz boyutlarda boş bir PSD oluşturuyoruz.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Bu, daha önce tanımladığınız paleti kullanan 500 × 500 piksel bir tuval oluşturur.

## Adım 6: PSD Üzerine Grafik Çizin
Görsel içerik ekleyin—burada beyaz bir arka plan üzerine basit bir kırmızı elips çiziyoruz.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` arka planı beyaz ile doldurur.  
- `drawEllipse` 6‑piksel kalınlığında kırmızı bir elips çizer.

## Adım 7: PSD Dosyasını Kaydedin
Son olarak, görüntüyü diske kaydedin.

```java
psd.save();
```

`Newsample_out.psd` dosyası, daha önce belirttiğiniz dizinde görünecektir.

## Yaygın Sorunlar ve İpuçları
- **Palet Boyutu** – 4 renkten fazla ihtiyacınız varsa, `palette` dizisine (maksimum 256) ekleyin.  
- **Dosya İzinleri** – Java sürecinin `dataDir` üzerine yazma izni olduğundan emin olun.  
- **Yanlış Renk Modu** – `createOptions.setColorMode(ColorModes.Indexed)` ifadesini atlamak, RGB bir PSD üretir; indeksli değil.

## Sıkça Sorulan Sorular

**S: Aspose.PSD for Java nedir?**  
C: Aspose.PSD for Java, PSD (Photoshop) dosyalarını programatik olarak Java kullanarak manipüle etmeyi sağlayan bir kütüphanedir.

**S: Aspose.PSD'yi ücretsiz kullanabilir miyim?**  
C: Evet, Aspose.PSD'nin ücretsiz deneme sürümüne **[buradan](https://releases.aspose.com/)** ulaşabilirsiniz.

**S: Aspose.PSD ile çalışmak için Photoshop yüklü olması gerekir mi?**  
C: Hayır, Aspose.PSD tüm işlemleri bağımsız olarak yürütür; Photoshop’a ihtiyaç duymazsınız.

**S: Aspose.PSD için geçici bir lisans nasıl alınır?**  
C: Geçici lisans talebinde **[buradan](https://purchase.aspose.com/temporary-license/)** bulunabilirsiniz.

**S: Aspose.PSD için destek nereden alınır?**  
C: Aspose forumundan **[burada](https://forum.aspose.com/c/psd/34)** destek alabilirsiniz.

## Sonuç
Artık **indeksli renk moduyla PSD nasıl oluşturulur**, özel bir palet nasıl üretilir ve basit grafikler nasıl eklenir konularını Aspose.PSD for Java kullanarak öğrendiniz. Bu temel yapı taşlarıyla daha karmaşık çizimler, katman yönetimi ve toplu işleme gibi konulara genişletebilirsiniz. Daha derinlemesine keşif için resmi API referansına **[buradan](https://reference.aspose.com/psd/java/)** göz atın ve farklı paletler ile çizim primitive'lerini denemeye devam edin.

---

**Last Updated:** 2026-03-15  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}