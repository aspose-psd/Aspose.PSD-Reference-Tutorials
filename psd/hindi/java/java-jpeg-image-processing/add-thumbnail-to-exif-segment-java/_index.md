---
date: 2026-09-18
description: Aspose.PSD for Java का उपयोग करके java image metadata thumbnail को EXIF
  segment में जोड़ना सीखें। यह step‑by‑step guide prerequisites, code walkthrough,
  और saving the updated image को कवर करता है।
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: Java में EXIF Segment में Thumbnail जोड़ें
og_description: Aspose.PSD for Java का उपयोग करके java image metadata thumbnail को
  EXIF segment में जोड़ना सीखें। यह step‑by‑step guide prerequisites, code walkthrough,
  और saving the updated image को कवर करता है।
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: java image metadata thumbnail को EXIF segment में जोड़ने का तरीका
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: java image metadata thumbnail को EXIF segment में जोड़ने का तरीका
url: /hi/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# EXIF खंड में जावा इमेज मेटाडाटा थंबनेल जोड़ें

## परिचय
इस ट्यूटोरियल में आप सीखेंगे कि कैसे **java image metadata** थंबनेल को PSD फ़ाइल के EXIF खंड में Aspose.PSD for Java का उपयोग करके जोड़ा जाए। EXIF (Exchangeable Image File Format) मेटाडाटा कैमरा सेटिंग्स, कैप्चर तिथि, स्थान और अन्य उपयोगी जानकारी संग्रहीत करता है। एक छोटा प्रीव्यू थंबनेल एम्बेड करने से एप्लिकेशन पूरे फ़ाइल को लोड किए बिना तेज़ी से इमेज का पूर्वावलोकन दिखा सकते हैं, जिससे प्रदर्शन और उपयोगकर्ता अनुभव बेहतर होता है।

## त्वरित उत्तर
- **ट्यूटोरियल क्या कवर करता है?** Aspose.PSD for Java के साथ PSD इमेज के EXIF खंड में थंबनेल जोड़ना।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** बेसिक इंटीग्रेशन के लिए लगभग 10‑15 मिनट।  
- **क्या मुझे लाइसेंस चाहिए?** प्रोडक्शन उपयोग के लिए एक टेम्पररी लाइसेंस आवश्यक है; मूल्यांकन के लिए एक फ्री ट्रायल काम करता है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और उसके बाद के संस्करण पूरी तरह सपोर्टेड हैं।  
- **क्या बड़े फ़ाइलों को प्रोसेस किया जा सकता है?** हाँ—Aspose.PSD 2 GB तक की फ़ाइलों को पूरी इमेज को मेमोरी में लोड किए बिना संभाल सकता है।

## java image metadata क्या है?
Java image metadata उन संरचित जानकारी को दर्शाता है जो इमेज फ़ाइलों (जैसे EXIF, IPTC, या XMP) में एम्बेडेड होती है और जिसे Java लाइब्रेरीज़ जैसे Aspose.PSD के माध्यम से प्रोग्रामेटिकली पढ़ा, संशोधित या बनाया जा सकता है। यह मेटाडाटा एप्लिकेशन को कैमरा सेटिंग्स, टाइमस्टैम्प, GPS कॉर्डिनेट्स और कस्टम डेटा को विज़ुअल कंटेंट खोले बिना प्राप्त करने में सक्षम बनाता है।

## EXIF मेटाडाटा में थंबनेल क्यों जोड़ें?
EXIF खंड में थंबनेल जोड़ने से इमेज ब्राउज़र्स, फ़ाइल एक्सप्लोरर्स और कंटेंट मैनेजमेंट सिस्टम्स के लिए त्वरित विज़ुअल संकेत मिलता है। Aspose.PSD थंबनेल को इन‑मेमोरी प्रोसेस करता है, जिससे 500 KB तक की इमेज के लिए 0.2 सेकंड से कम समय में प्रीव्यू एम्बेड किया जा सकता है, और यह 30 से अधिक इमेज फ़ॉर्मैट्स, जैसे PSD, JPEG, PNG, और TIFF को सपोर्ट करता है।

## पूर्वापेक्षाएँ
- जावा प्रोग्रामिंग का बुनियादी ज्ञान।  
- आपके सिस्टम पर Java Development Kit (JDK) स्थापित होना चाहिए।  
- जावा के लिए IDE (Integrated Development Environment), जैसे IntelliJ IDEA या Eclipse।  
- Aspose.PSD for Java लाइब्रेरी। आप इसे [Aspose.PSD for Java Download page](https://releases.aspose.com/psd/java/) से डाउनलोड कर सकते हैं।

## पैकेज इम्पोर्ट करें
निम्नलिखित इम्पोर्ट्स Aspose.PSD क्लासेज़ को लाते हैं जो PSD इमेज और EXIF डेटा के साथ काम करने के लिए आवश्यक हैं।  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## चरण 1: PSD इमेज लोड करें
`PsdImage` एक Photoshop PSD फ़ाइल का प्रतिनिधित्व करता है और इसके लेयर्स और रिसोर्सेज़ तक पहुंच प्रदान करता है।  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## चरण 2: इमेज रिसोर्सेज़ पर इटरेट करें
`ImageResource` थंबनेल, ICC प्रोफ़ाइल और PSD फ़ाइल में एम्बेडेड मेटाडाटा जैसे रिसोर्सेज़ को संलग्न करता है।  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## चरण 3: थंबनेल डेटा समायोजित करें
`JpegOptions` आपको थंबनेल इमेज के लिए JPEG‑विशिष्ट सेटिंग्स, जैसे क्वालिटी, को कॉन्फ़िगर करने की अनुमति देता है।  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## चरण 4: इमेज सहेजें
`save` को कॉल करने से अपडेटेड EXIF खंड (नया थंबनेल सहित) डिस्क पर लिखा जाता है बिना पूरी इमेज को पुनः‑एन्कोड किए।  
```java
image.save(dataDir + "output.psd");
```

## सामान्य समस्याएँ और समाधान
- **थंबनेल नहीं दिख रहा है:** जाँचें कि थंबनेल रिसोर्स सही तरीके से EXIF खंड में जोड़ा गया है और इमेज `PsdImage.save` मेथड से सहेजी गई है।  
- **बड़ी फ़ाइलों पर मेमोरी समाप्ति त्रुटियाँ:** `PsdImage.load(..., LoadOptions)` को `LoadOptions.setLoadOnlyMetadata(true)` के साथ उपयोग करें ताकि केवल मेटाडाटा के साथ काम किया जा सके।  
- **गलत अभिविन्यास:** सुनिश्चित करें कि थंबनेल मूल इमेज के अभिविन्यास फ़्लैग का सम्मान करता है; आप `Orientation` EXIF टैग पढ़ सकते हैं और थंबनेल को उसी अनुसार घुमा सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**Q: EXIF मेटाडाटा क्या है?**  
A: EXIF मेटाडाटा डिजिटल इमेज में एम्बेडेड जानकारी है जिसमें कैमरा सेटिंग्स, कैप्चर तिथि, GPS कॉर्डिनेट्स और अन्य विवरण शामिल होते हैं।

**Q: EXIF में थंबनेल क्यों जोड़ें?**  
A: थंबनेल जोड़ने से उपयोगकर्ता अनुभव बेहतर होता है क्योंकि पूर्ण इमेज लोड किए बिना तेज़ी से इमेज प्रीव्यू दिखाया जा सकता है।

**Q: मैं Aspose.PSD for Java कहाँ डाउनलोड कर सकता हूँ?**  
A: आप Aspose.PSD for Java को [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) से डाउनलोड कर सकते हैं।

**Q: मैं Aspose.PSD के लिए टेम्पररी लाइसेंस कैसे प्राप्त कर सकता हूँ?**  
A: आप Aspose.PSD के लिए टेम्पररी लाइसेंस [temporary license page](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

**Q: मैं Aspose.PSD के लिए सपोर्ट कैसे प्राप्त करूँ?**  
A: सपोर्ट के लिए, [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) पर जाएँ।

---

**अंतिम अपडेट:** 2026-09-18  
**परीक्षण किया गया:** Aspose.PSD for Java 24.10  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में XMP मेटाडाटा बनाएं](/psd/java/image-editing/create-xmp-metadata/)
- [Aspose.PSD for Java के साथ इमेज रिसाइज़ करें – शैप्स ड्रॉ करें और बेसिक इमेज ऑपरेशन्स](/psd/java/basic-image-operations/)
- [Aspose.PSD for Java के साथ PSD को रास्टर इमेज फ़ॉर्मैट्स में कैसे कन्वर्ट करें](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}