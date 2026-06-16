---
date: 2026-03-07
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में इमेज वॉटरमार्क बनाना
  सीखें – PSD इमेज प्रोसेसिंग और अपने ग्राफ़िक्स की सुरक्षा के लिए एक त्वरित गाइड।
linktitle: How to Create Image Watermark in PSD Files with Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ PSD फ़ाइलों में इमेज वॉटरमार्क कैसे बनाएं
url: /hi/java/modifying-converting-psd-images/add-watermark-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ PSD फ़ाइलों में वॉटरमार्क जोड़ें

## परिचय
वॉटरमार्क आपके चित्रों की सुरक्षा करने और स्वामित्व को संप्रेषित करने का एक सूक्ष्म लेकिन प्रभावी तरीका है। इस ट्यूटोरियल में, आप Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में **create image watermark** बनाना सीखेंगे। चाहे आप अपना पोर्टफ़ोलियो दिखा रहे फ़ोटोग्राफ़र हों या अपना नवीनतम काम प्रस्तुत कर रहे डिज़ाइनर, वॉटरमार्क जोड़ना ब्रांड पहचान बनाए रखने के लिए महत्वपूर्ण हो सकता है। तो, एक कप कॉफ़ी लें, आराम से बैठें, और चलिए शुरू करते हैं!

## त्वरित उत्तर
- **प्राथमिक लक्ष्य क्या है?** PSD फ़ाइल में प्रोग्रामेटिक रूप से image watermark बनाने के लिए।  
- **कौनसी लाइब्रेरी उपयोग की जाती है?** Aspose.PSD for Java.  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** बेसिक वॉटरमार्क के लिए लगभग 10‑15 मिनट।  
- **मुख्य पूर्वापेक्षाएँ क्या हैं?** Java JDK, Aspose.PSD लाइब्रेरी, और एक स्रोत PSD फ़ाइल।  
- **क्या मैं परिणाम को PNG के रूप में एक्सपोर्ट कर सकता हूँ?** हाँ – `save` मेथड को `PngOptions` के साथ उपयोग करें।  

## **create image watermark** क्या है?
इमेज वॉटरमार्क बनाना मतलब है प्रोग्रामेटिक रूप से अर्ध‑पारदर्शी टेक्स्ट या ग्राफ़िक्स को इमेज फ़ाइल पर ओवरले करना ताकि स्वामित्व की जानकारी सीधे दृश्य सामग्री में एम्बेड हो जाए।

## psd इमेज प्रोसेसिंग के लिए Aspose.PSD for Java का उपयोग क्यों करें?
Aspose.PSD **psd image processing** के लिए APIs का समृद्ध सेट प्रदान करता है, जिससे आप लेयर्स को मैनीपुलेट कर सकते हैं, इफ़ेक्ट्स लागू कर सकते हैं, और अंतिम इमेज को Photoshop की आवश्यकता के बिना रेंडर कर सकते हैं। यह हाई‑फ़िडेलिटी रेंडरिंग, बैच ऑपरेशन्स को सपोर्ट करता है, और सभी प्रमुख ऑपरेटिंग सिस्टम्स पर काम करता है।

## पूर्वापेक्षाएँ
कोड में डुबने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java Development Kit (JDK)** – कोई भी हालिया संस्करण (8 या उससे ऊपर)।  
2. **Aspose.PSD for Java Library** – इसे [Aspose website](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
3. **IDE** – Eclipse, IntelliJ IDEA, या कोई भी एडिटर जो आप पसंद करते हैं।  
4. **PSD File** – एक सैंपल फ़ाइल जिसका नाम `layers.psd` है, इसे अपने वर्किंग डायरेक्टरी में रखें।  
5. **Basic Java knowledge** – क्लासेस, ऑब्जेक्ट्स, और फ़ाइल I/O की परिचितता।  

## पैकेज इम्पोर्ट करें
अब जब आपने सब सेट कर लिया है, चलिए आवश्यक पैकेज इम्पोर्ट करते हैं। जावा में इम्पोर्ट्स आपको विभिन्न लाइब्रेरीज़ से क्लासेस और फ़ंक्शन्स लाने की अनुमति देते हैं, जिससे आपका कोड अधिक प्रभावी बनता है। नीचे वह दिया गया है जो आपको चाहिए:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## **create image watermark** कैसे बनाएं – चरण‑दर‑चरण गाइड

### चरण 1: अपनी डायरेक्टरी सेट करें
सबसे पहले, हमें अपने PSD फ़ाइल के स्थान का पाथ सेट करना होगा। यह महत्वपूर्ण है क्योंकि जावा को पता होना चाहिए कि फ़ाइलें कहाँ हैं।

```java
String dataDir = "Your Document Directory";
```

`Your Document Directory` को उस वास्तविक फ़ोल्डर से बदलें जिसमें `layers.psd` है।

### चरण 2: PSD फ़ाइल लोड करें
अगला, हम PSD फ़ाइल को लोड करेंगे और इसे `PsdImage` में कास्ट करेंगे। यह चरण फ़ाइल को ऐसे फ़ॉर्मेट में बदलता है जिसे हम मैनीपुलेट कर सकते हैं।

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

इसे एक किताब खोलने के समान समझें ताकि आप उसके पन्नों पर लिखना शुरू कर सकें।

### चरण 3: एक Graphics ऑब्जेक्ट बनाएं
अब हमारा PSD फ़ाइल लोड हो चुका है, हमें एक `Graphics` ऑब्जेक्ट बनाना होगा। यह हमें ड्रॉइंग ऑपरेशन्स करने देता है—जैसे आपके कैनवास के लिए पेंटब्रश उठाना।

```java
Graphics graphics = new Graphics(psdImage);
```

### चरण 4: अपने वॉटरमार्क के लिए फ़ॉन्ट निर्धारित करें
अब समय है तय करने का कि आपका वॉटरमार्क कैसे दिखेगा। हम Arial फ़ॉन्ट साइज 20 का उपयोग करेंगे। आप अपनी ब्रांड स्टाइल के अनुसार फ़ॉन्ट नाम या साइज बदल सकते हैं।

```java
Font font = new Font("Arial", 20.0f);
```

### चरण 5: वॉटरमार्किंग के लिए सॉलिड ब्रश बनाएं
सॉलिड ब्रश आपके वॉटरमार्क को उसका रंग और अपारदर्शिता देता है। हम अल्फा को 50 (255 में से) सेट करेंगे ताकि अर्ध‑पारदर्शी ग्रे मिल सके।

```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```

यहाँ, `Color.fromArgb(50, 128, 128, 128)` 50% अपारदर्शिता के साथ ग्रे रंग बनाता है—एक सूक्ष्म सिग्नेचर के लिए उपयुक्त।

### चरण 6: अपने वॉटरमार्क के लिए स्ट्रिंग अलाइनमेंट सेट करें
वॉटरमार्क को इमेज के केंद्र में दिखाने के लिए, हम स्ट्रिंग अलाइनमेंट विकल्प कॉन्फ़िगर करेंगे।

```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```

### चरण 7: **java graphics drawstring** का उपयोग करके वॉटरमार्क ड्रॉ करें
अब हम रोमांचक भाग पर पहुँचते हैं। ग्राफ़िक्स कॉन्टेक्स्ट तैयार होने पर, हम `java graphics drawstring` का उपयोग करके इमेज पर वॉटरमार्क टेक्स्ट ड्रॉ करेंगे।

```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```

`"Some watermark text"` को उस वास्तविक टेक्स्ट से बदलें जो आप अपने PSD में दिखाना चाहते हैं।

### चरण 8: **Save PSD as PNG** – **export psd png**
अब जब वॉटरमार्क जगह पर है, हम **save psd png** (अर्थात PSD को PNG में एक्सपोर्ट) करेंगे ताकि परिणाम किसी भी ब्राउज़र या इमेज व्यूअर में देखा जा सके।

```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```

इस लाइन को चलाने से एक नई PNG फ़ाइल बनती है जिसमें आपका वॉटरमार्क शामिल होता है।

## सामान्य समस्याएँ और समाधान
- **वॉटरमार्क दिखाई नहीं दे रहा?** `Color.fromArgb()` में अल्फा वैल्यू जांचें; कम वैल्यू वॉटरमार्क को अधिक पारदर्शी बनाती है।  
- **गलत डायमेंशन?** रेक्टेंगल के लिए `psdImage.getWidth()` और `psdImage.getHeight()` का उपयोग कर रहे हैं यह सुनिश्चित करें ताकि टेक्स्ट इमेज साइज के साथ स्केल हो।  
- **लाइसेंस एक्सेप्शन?** परीक्षण के लिए एक टेम्पररी इवैल्यूएशन लाइसेंस काम करता है, लेकिन प्रोडक्शन उपयोग के लिए पूर्ण लाइसेंस आवश्यक है।  

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं वॉटरमार्क टेक्स्ट को कस्टमाइज़ कर सकता हूँ?**  
A: बिल्कुल! बस `drawString` मेथड में स्ट्रिंग को अपने इच्छित टेक्स्ट से बदल दें।

**Q: अगर मैं अलग फ़ॉन्ट चाहता हूँ तो?**  
A: `Font` इंस्टैंसिएशन को किसी भी इंस्टॉल्ड फ़ॉन्ट में बदलें, उदाहरण के लिए `new Font("Times New Roman", 24.0f)`।

**Q: क्या अपारदर्शिता को समायोजित करने का कोई तरीका है?**  
A: हाँ—`Color.fromArgb(alpha, r, g, b)` के पहले पैरामीटर को बदलें। कम `alpha` वैल्यू पारदर्शिता बढ़ाती है।

**Q: क्या मैं PNG के अलावा अन्य इमेज फ़ॉर्मेट उपयोग कर सकता हूँ?**  
A: बिल्कुल। `new PngOptions()` को `new JpegOptions()` या `new BmpOptions()` से बदलें ताकि **save psd png** किसी अलग फ़ॉर्मेट में हो।

**Q: मैं और मदद कहाँ पा सकता हूँ?**  
A: विस्तृत प्रश्नों के लिए, [Aspose forums](https://forum.aspose.com/c/psd/34) पर जाएँ या उनकी [documentation](https://reference.aspose.com/psd/java/) देखें।

## निष्कर्ष
अब आपने Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में **create image watermark** बनाना सीख लिया है। यह तकनीक न केवल आपके कंटेंट को सुरक्षित करती है बल्कि सभी विज़ुअल एसेट्स में आपके ब्रांड की उपस्थिति को भी मजबूत करती है। विभिन्न फ़ॉन्ट्स, रंगों और अपारदर्शिता स्तरों के साथ प्रयोग करें ताकि आपका स्टाइल मेल खाए, और याद रखें कि आप **save psd png** या **export psd png** को किसी भी फ़ॉर्मेट में कर सकते हैं।

---

**अंतिम अपडेट:** 2026-03-07  
**परीक्षण किया गया:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}