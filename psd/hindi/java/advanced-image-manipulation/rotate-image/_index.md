---
date: 2026-05-19
description: Aspose.PSD for Java का उपयोग करके PSD को JPEG में बदलना और इमेज को 270
  डिग्री घुमाना सीखें। यह गाइड दिखाता है कि PSD फ़ाइलों को कैसे घुमाएँ, इमेज को कैसे
  फ़्लिप करें, और PSD को JPEG में कैसे बदलें।
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: इमेज को 270 डिग्री घुमाएँ
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ PSD को JPEG में बदलें और 270° घुमाएँ
url: /hi/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD को JPEG में बदलें और Aspose.PSD for Java के साथ इमेज को 270 डिग्री घुमाएँ

## परिचय

इस **Java इमेज‑प्रोसेसिंग ट्यूटोरियल** में, आप सीखेंगे कि **PSD को JPEG में कैसे बदलें** और Aspose.PSD for Java का उपयोग करके इमेज को 270 डिग्री घुमाएँ। चाहे आप बैच‑प्रोसेसिंग पाइपलाइन, वेब‑आधारित एडिटर, या डेस्कटॉप यूटिलिटी बना रहे हों, यह लाइब्रेरी आपको Photoshop के बिना PSD लेयर्स को मैनीपुलेट करने देती है। हम वैकल्पिक फ्लिपिंग को भी कवर करेंगे और PSD फ़ाइल को लोड करने से JPEG सेव करने तक का पूरा एंड‑टू‑एंड फ्लो दिखाएंगे।

## त्वरित उत्तर
- **रोटेशन को संभालने वाली लाइब्रेरी कौन सी है?** Aspose.PSD for Java  
- **उदाहरण में कौन सा रोटेशन एंगल उपयोग किया गया है?** 270 degrees  
- **क्या मैं इमेज को फ्लिप भी कर सकता हूँ?** हाँ – `RotateFlipType` विकल्प जैसे `Rotate90FlipX` का उपयोग करें  
- **परिणाम को कैसे सहेजें?** उदाहरण में हम `JpegOptions` का उपयोग करके JPEG के रूप में सहेजते हैं  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** व्यावसायिक उपयोग के लिए एक वैध Aspose.PSD लाइसेंस आवश्यक है  

## “इमेज को 270 डिग्री घुमाना” क्या है?
इमेज को 270 डिग्री घुमाना मतलब चित्र को पूरी सर्कल का तीन‑चौथाई भाग घड़ी की दिशा में (या 90 डिग्री घड़ी के विपरीत दिशा में) घुमाना है। यह अभिविन्यास अक्सर पूर्व परिवर्तन के बाद मूल पोर्ट्रेट लेआउट को पुनर्स्थापित करता है, और आमतौर पर तब उपयोग किया जाता है जब इमेज लैंडस्केप मोड में ली गई हों लेकिन पोर्ट्रेट में दिखाने की आवश्यकता हो। परिणामस्वरूप एक सही दिशा में व्यवस्थित दृश्य मिलता है बिना गुणवत्ता की हानि के।

## इस कार्य के लिए Aspose.PSD क्यों उपयोग करें?
Aspose.PSD **50+ इनपुट और आउटपुट फॉर्मैट्स** का समर्थन करता है—जिसमें PSD, JPEG, PNG, BMP, GIF, और TIFF शामिल हैं—और **2 GB** तक की फ़ाइलों को पूरी दस्तावेज़ को मेमोरी में लोड किए बिना प्रोसेस कर सकता है। API किसी भी Java रनटाइम (JDK 8+) पर काम करता है, किसी भी नेटीव Photoshop इंस्टॉलेशन की आवश्यकता नहीं होती, और एक ही `rotateFlip` कॉल प्रदान करता है जो रोटेशन और फ्लिपिंग दोनों को एक कदम में संभालता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

- **Aspose.PSD for Java** लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं और पूरी API रेफ़रेंस [यहाँ](https://reference.aspose.com/psd/java/) देख सकते हैं।  
- एक Java विकास वातावरण (JDK 8 या उससे ऊपर)।  
- एक सैंपल PSD फ़ाइल जिसे आप घुमाना चाहते हैं। कोड में `sourceFile` वेरिएबल को अपनी फ़ाइल के सही पथ से अपडेट करें।

## पैकेज इम्पोर्ट करें

`Image`, `RotateFlipType`, और `JpegOptions` क्लासेज़ फ़ाइल को लोड करने, ट्रांसफ़ॉर्म करने और सेव करने के लिए आवश्यक हैं।  
`Image` वह कोर क्लास है जो मेमोरी में PSD दस्तावेज़ का प्रतिनिधित्व करती है।  
`RotateFlipType` समर्थित रोटेशन और फ्लिप ऑपरेशन्स को एनेमरेट करता है।  
`JpegOptions` JPEG आउटपुट सेटिंग्स जैसे क्वालिटी को कॉन्फ़िगर करता है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## रोटेशन के बाद PSD को JPEG में कैसे बदलें?

स्रोत PSD को लोड करें, 270‑डिग्री रोटेशन लागू करें, और तुरंत इसे JPEG के रूप में सेव करें। यह तीन‑स्टेप फ्लो आधुनिक CPU पर सामान्य 10‑MP इमेज के लिए एक सेकंड से कम समय में चलता है, जिससे यह हाई‑थ्रूपुट बैच जॉब्स के लिए आदर्श बनता है। केवल आवश्यक इमेज डेटा को प्रोसेस करके, मेमोरी खपत कम रहती है, और परिणामी JPEG दृश्य फ़िडेलिटी को बनाए रखता है जबकि फ़ाइल आकार घटाता है।

### चरण 1: PSD फ़ाइल लोड करें

`Image` Aspose.PSD की कोर क्लास है जो मेमोरी में एकल PSD दस्तावेज़ का प्रतिनिधित्व करती है। इसे इंस्टैंशिएट करने से केवल हेडर जानकारी पढ़ी जाती है, जिससे मेमोरी उपयोग कम रहता है।

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### चरण 2: इमेज को 270 डिग्री घुमाएँ

`rotateFlip` इमेज पर निर्दिष्ट रोटेशन और वैकल्पिक फ्लिप को लागू करता है। `RotateFlipType.Rotate270FlipNone` कैनवास को 270 डिग्री घड़ी की दिशा में घुमाता है जबकि इमेज की ओरिएंटेशन को अपरिवर्तित रखता है।

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **प्रो टिप:** यदि आपको इमेज को क्षैतिज या लंबवत रूप से भी फ्लिप करने की आवश्यकता है, तो `RotateFlipType` में से कोई अलग विकल्प चुनें जैसे `Rotate90FlipX` या `Rotate180FlipY`।

### चरण 3: PSD को JPEG में बदलें और सेव करें

`JpegOptions` JPEG‑विशिष्ट पैरामीटर जैसे कम्प्रेशन क्वालिटी को परिभाषित करता है। `save` मेथड ट्रांसफ़ॉर्म्ड इमेज को इच्छित फॉर्मैट में डिस्क पर लिखता है।

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

फ़ाइल `RotatedImage_out.jpg` अब मूल PSD कंटेंट को 270 डिग्री घुमाकर JPEG के रूप में सहेजा गया है।

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **इमेज उल्टा दिख रहा है** | जाँचें कि आपने `Rotate270FlipNone` उपयोग किया है। 90‑डिग्री घड़ी की दिशा में रोटेशन के लिए `Rotate90FlipNone` उपयोग करें। |
| **आउटपुट फ़ाइल भ्रष्ट है** | सुनिश्चित करें कि लक्ष्य फ़ोल्डर मौजूद है और आपके पास लिखने की अनुमति है। |
| **लाइसेंस अपवाद** | प्रोडक्शन में इमेज लोड करने से पहले एक अस्थायी या स्थायी Aspose.PSD लाइसेंस इंस्टॉल करें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या Aspose.PSD विभिन्न इमेज फॉर्मैट्स के साथ संगत है?**  
**उत्तर:** हाँ, Aspose.PSD PSD, JPEG, PNG, BMP, GIF, TIFF, और कई अन्य रास्टर फॉर्मैट्स का समर्थन करता है।

**प्रश्न: क्या मैं कस्टम रोटेशन लागू कर सकता हूँ, न कि केवल प्री‑डिफाइंड फ्लिप्स?**  
**उत्तर:** बिल्कुल! जबकि `RotateFlipType` सामान्य एंगल्स प्रदान करता है, आप कई कॉल्स को चेन कर सकते हैं या मनमाने एंगल्स के लिए ट्रांसफ़ॉर्मेशन मैट्रिसेज़ का उपयोग कर सकते हैं।

**प्रश्न: घुमाए गए PSD को किसी अन्य फॉर्मैट, जैसे PNG, में कैसे बदलूँ?**  
**उत्तर:** `save` मेथड में `JpegOptions` को `PngOptions` (या उपयुक्त विकल्प क्लास) से बदलें।

**प्रश्न: अतिरिक्त समर्थन या सहायता कहाँ मिल सकती है?**  
**उत्तर:** समुदाय सहायता के लिए, [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) देखें।

**प्रश्न: क्या कोई फ्री ट्रायल उपलब्ध है?**  
**उत्तर:** हाँ, आप एक [फ्री ट्रायल](https://releases.aspose.com/) के साथ Aspose.PSD का अन्वेषण कर सकते हैं।

**प्रश्न: अस्थायी लाइसेंस कैसे प्राप्त करूँ?**  
**उत्तर:** यदि आपको अस्थायी लाइसेंस चाहिए, तो आप इसे [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

---

**अंतिम अपडेट:** 2026-05-19  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.12  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल्स

- [Aspose.PSD for Java के साथ PSD को रास्टर इमेज फॉर्मैट्स में बदलें](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Java का उपयोग करके PSD को PNG में बदलें और PSD फ़ाइलों में लेयर्स को घुमाएँ](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Aspose.PSD के साथ Java में इमेज को कैसे घुमाएँ](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}