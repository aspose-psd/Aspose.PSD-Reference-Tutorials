---
date: 2026-10-03
description: Aspose.PSD for Java के साथ इस चरण‑दर‑चरण गाइड में Java में इमेज मेटाडेटा
  पढ़ने और JPEG EXIF टैग्स को संशोधित करने के तरीके सीखें, जो इमेज मेटाडेटा को कुशलता
  से संभालने वाले डेवलपर्स के लिए उपयुक्त है।
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Java में JPEG EXIF टैग्स को पढ़ें और संशोधित करें
og_description: Aspose.PSD for Java के साथ Java में इमेज मेटाडेटा पढ़ने और JPEG EXIF
  टैग्स को संशोधित करने के तरीके सीखें। यह गाइड EXIF जानकारी को निकालने और अपडेट करने
  के लिए चरण‑दर‑चरण कोड दिखाता है।
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Java में इमेज मेटाडेटा कैसे पढ़ें और JPEG EXIF टैग्स को संशोधित करें
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Java में इमेज मेटाडेटा कैसे पढ़ें और JPEG EXIF टैग्स को संशोधित करें
url: /hi/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JPEG EXIF टैग पढ़ें और संशोधित करें Java में

## परिचय
यदि आपको JPEG फ़ाइलों से **java read image metadata** पढ़ना है और इसे प्रोग्रामेटिकली बदलना है, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम Aspose.PSD for Java का उपयोग करके EXIF टैग निकालने और अपडेट करने की प्रक्रिया देखेंगे। अंत तक आप कैमरा विवरण, ओरिएंटेशन, और कस्टम फ़ील्ड्स को निकाल सकेंगे, फिर उन्हें फ़ाइल में वापस लिख सकेंगे—बिना किसी ग्राफ़िकल एडिटर के।

## त्वरित उत्तर
- **Java में JPEG EXIF को संभालने वाली लाइब्रेरी कौन सी है?** Aspose.PSD for Java.  
- **EXIF पढ़ने के लिए कितनी पंक्तियों का कोड चाहिए?** इमेज लोड करने के बाद लगभग तीन पंक्तियाँ।  
- **क्या आप EXIF टैग संशोधित कर सकते हैं?** हाँ, आप किसी भी मानक या कस्टम टैग को बदल सकते हैं और परिणाम सहेज सकते हैं।  
- **समर्थित इमेज फ़ॉर्मेट?** 150 से अधिक फ़ॉर्मेट, जिसमें PSD, JPEG, PNG, TIFF, और BMP शामिल हैं।  
- **न्यूनतम Java संस्करण?** Java 7 या उससे ऊपर।

## Aspose.PSD for Java का उपयोग क्यों करें?
Aspose.PSD **150+ इमेज फ़ॉर्मेट** को सपोर्ट करता है और फ़ाइलों को **2 GB** तक प्रोसेस कर सकता है बिना पूरे दस्तावेज़ को मेमोरी में लोड किए, जिससे बड़े फोटो संग्रह पर तेज़, कम‑मेमोरी मेटाडेटा ऑपरेशन संभव होते हैं। यह EXIF, IPTC, और XMP डेटा को पढ़ने‑लिखने के लिए एक सरल API भी प्रदान करता है, जिससे हजारों इमेज की बैच प्रोसेसिंग प्रभावी और विश्वसनीय बनती है।

## पूर्वापेक्षाएँ
1. **Java Development Kit (JDK)** – सुनिश्चित करें कि आपके पास JDK 11 या नया है। आप इसे [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड कर सकते हैं।  
2. **Aspose.PSD for Java library** – नवीनतम JAR को [Aspose releases page](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी एडिटर जो आप पसंद करते हैं।  
4. **Basic Java knowledge** – आपको प्रोजेक्ट बनाने और एक्सटर्नल JAR जोड़ने में सहज होना चाहिए।

## Java में इमेज मेटाडेटा पढ़ना क्या है?
Java में इमेज मेटाडेटा पढ़ना वह प्रक्रिया है जिसमें आप प्रोग्रामेटिकली इमेज फ़ाइलों के भीतर एम्बेडेड जानकारी (जैसे EXIF, IPTC, और XMP) तक पहुँचते हैं। यह मेटाडेटा कैमरा सेटिंग्स, टाइमस्टैम्प, GPS कॉर्डिनेट्स, कॉपीराइट नोटिस, और उपयोगकर्ता टिप्पणियों को शामिल कर सकता है, जिससे एप्लिकेशन इमेज को उनके वर्णनात्मक डेटा के आधार पर व्यवस्थित, खोज और संशोधित कर सकते हैं।

## पैकेज आयात करें
सबसे पहले, Aspose.PSD JAR को अपने प्रोजेक्ट की क्लासपाथ में जोड़ें और आवश्यक क्लासेस को इम्पोर्ट करें।

`com.aspose.psd` पैकेज इमेज लोड करने और उनके रिसोर्सेज़ तक पहुँचने के लिए कोर API प्रदान करता है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Java में JPEG फ़ाइलों से इमेज मेटाडेटा कैसे पढ़ें?
`PsdImage.load("image.jpg")` के साथ JPEG लोड करें, थंबनेल रिसोर्स को खोजें जो EXIF डेटा रखता है, और फिर `ExifData.read()` को कॉल करके एक पूर्ण `ExifData` ऑब्जेक्ट प्राप्त करें। यह एक‑स्टेप प्रक्रिया आपको सभी मानक EXIF फ़ील्ड्स और किसी भी कस्टम टैग तक पूर्ण पहुँच देती है।

## चरण 1: PSD इमेज लोड करें
PsdImage Aspose.PSD की वह क्लास है जो PSD फ़ाइल का प्रतिनिधित्व करती है और इसके रिसोर्सेज़ तथा मेटाडेटा तक पहुँचने के मेथड्स प्रदान करती है।  
इस चरण में, हम उस PSD इमेज को लोड करेंगे जिससे हम EXIF डेटा पढ़ना चाहते हैं। सुनिश्चित करें कि आपकी इमेज सही डायरेक्टरी में है।

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## चरण 2: इमेज संसाधनों पर इटररेट करें
ThumbnailResource एक थंबनेल इमेज को दर्शाता है जो अक्सर PSD फ़ाइल में एम्बेडेड EXIF डेटा रखता है।  
इमेज लोड होने के बाद, अगला कदम इसका रिसोर्सेज़ पर इटररेट करना है ताकि थंबनेल रिसोर्स मिल सके, जिसमें आमतौर पर EXIF डेटा होता है।

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## चरण 3: EXIF डेटा निकालें
JpegExifData वह क्लास है जो JPEG इमेज से निकाले गए EXIF जानकारी को रखता है, जिससे आप व्यक्तिगत टैग पढ़ और संशोधित कर सकते हैं।  
अब जब हमारे पास थंबनेल रिसोर्स है, हम उससे EXIF डेटा निकाल सकते हैं। EXIF डेटा में कैमरा मालिक का नाम, अपर्चर वैल्यू, ओरिएंटेशन आदि महत्वपूर्ण जानकारी शामिल होती है।

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## चरण 4: EXIF डेटा संशोधित करें
EXIF डेटा पढ़ने के बाद, आप कुछ फ़ील्ड्स को बदलना चाह सकते हैं। इसे करने का तरीका नीचे दिया गया है:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## चरण 5: परिवर्तन सहेजें
अंत में, EXIF डेटा संशोधित करने के बाद, परिवर्तनों को एक नई PSD फ़ाइल में सहेजें।

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## सामान्य समस्याएँ और समाधान
- **Missing thumbnail resource** – कुछ JPEG सीधे मुख्य इमेज हेडर में EXIF स्टोर करते हैं। यदि थंबनेल रिसोर्स अनुपलब्ध है, तो `image.getExifData()` का उपयोग करें।  
- **Large files cause OutOfMemoryError** – JVM को पर्याप्त हीप (`-Xmx2g`) के साथ चलाएँ या `PsdImage.load(inputStream, loadOptions)` का उपयोग करके स्ट्रीमिंग मोड में इमेज प्रोसेस करें।  
- **Unsupported tag types** – Aspose.PSD सभी मानक EXIF टैग्स को सपोर्ट करता है; कस्टम टैग्स को मैन्युअल बाइट‑लेवल हैंडलिंग की आवश्यकता हो सकती है।

## अक्सर पूछे जाने वाले प्रश्न

**Q: EXIF डेटा क्या है?**  
A: EXIF (Exchangeable Image File Format) मेटाडेटा कैमरा सेटिंग्स, टाइमस्टैम्प, GPS कॉर्डिनेट्स, और अन्य जानकारी को JPEG तथा अन्य इमेज फ़ाइलों में एम्बेडेड रूप में संग्रहीत करता है।

**Q: क्या मैं Aspose.PSD for Java को मुफ्त में उपयोग कर सकता हूँ?**  
A: आप मुफ्त ट्रायल [Aspose releases page](https://releases.aspose.com/) से प्राप्त कर सकते हैं।

**Q: क्या Aspose.PSD for Java सभी Java संस्करणों के साथ संगत है?**  
A: Aspose.PSD for Java Java SE 7 और उससे ऊपर को सपोर्ट करता है।

**Q: Aspose.PSD for Java पर अधिक दस्तावेज़ कहाँ मिलेंगे?**  
A: अधिक विवरण के लिए [documentation](https://reference.aspose.com/psd/java/) देखें।

**Q: Aspose.PSD for Java के लिए सपोर्ट कैसे प्राप्त करें?**  
A: आप [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/) से सपोर्ट ले सकते हैं।

## निष्कर्ष
इन चरणों का पालन करके आप किसी भी JPEG से **java read image metadata** निकाल सकते हैं, आवश्यक EXIF फ़ील्ड्स को समायोजित कर सकते हैं, और अपडेटेड डेटा को फ़ाइल में वापस लिख सकते हैं—सिर्फ कुछ ही लाइनों के साफ़ Java कोड के साथ। Aspose.PSD का समृद्ध API मेटाडेटा हैंडलिंग को विश्वसनीय और तेज़ बनाता है, जिससे आप इसे बैच प्रोसेसिंग पाइपलाइन, फोटो‑मैनेजमेंट टूल्स, या किसी भी एप्लिकेशन में एकीकृत कर सकते हैं जो इमेज जानकारी के साथ काम करता है।

---

**अंतिम अपडेट:** 2026-10-03  
**परीक्षण किया गया:** Aspose.PSD for Java 24.5  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Java में Aspose (asp) के साथ विशिष्ट EXIF टैग जानकारी पढ़ें](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में XMP मेटाडेटा बनाएं](/psd/java/image-editing/create-xmp-metadata/)
- [Aspose.PSD for Java के साथ इमेज का आकार बदलें – आकृतियाँ बनाएं और बुनियादी इमेज ऑपरेशन्स](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}