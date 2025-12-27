---
date: 2025-12-27
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में लाल आयत और अन्य आकार
  कैसे बनाएं, सीखें। यह चरण‑दर‑चरण गाइड दस्तावेज़ बनाना, लेयर जोड़ना और कोड उदाहरणों
  के साथ ड्रॉ करना कवर करता है।
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ लाल आयत बनाएं
url: /hi/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ लाल आयत बनाएं

## परिचय

इस चरण‑दर‑चरण गाइड में आपका स्वागत है, जहाँ हम **लाल आयत** को Aspose.PSD for Java का उपयोग करके कैसे बनाते हैं, यह सीखेंगे! इस ट्यूटोरियल में हम नया PSD दस्तावेज़ बनाना, एक लेयर जोड़ना, और कस्टम रंगों के साथ आकार बनाना देखेंगे। चाहे आप ग्राफ़िक एसेट्स को ऑटोमेट कर रहे हों या डिज़ाइन‑टूल बैकएंड बना रहे हों, यह ट्यूटोरियल आपको आवश्यक बिल्डिंग ब्लॉक्स प्रदान करता है।

## त्वरित उत्तर
- **PSD फ़ाइल बनाने के लिए मुख्य क्लास कौन सी है?** `PsdImage`
- **कौन सा मेथड लेयर की पृष्ठभूमि का रंग साफ़ करता है?** `Graphics.clear(Color)`
- **लाल आयत कैसे बनाते हैं?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **क्या विकास के लिए लाइसेंस चाहिए?** परीक्षण के लिए मुफ्त ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।
- **क्या मैं उसी API से मौजूदा PSD फ़ाइलों को भी संशोधित कर सकता हूँ?** हाँ, Aspose.PSD पूर्ण PSD संपादन का समर्थन करता है।

## PSD फ़ाइल में लाल आयत बनाना क्या है?
लाल आयत बनाना का अर्थ है `Graphics` ऑब्जेक्ट का उपयोग करके एक आयताकार आकार को लाल रंग में भरना या उसकी रूपरेखा बनाना, जो PSD छवि की किसी विशिष्ट लेयर पर रेंडर किया जाता है। यह ऑपरेशन अक्सर क्षेत्रों को हाइलाइट करने, प्लेसहोल्डर बनाने, या प्रोग्रामेटिक रूप से सरल ग्राफ़िक्स जोड़ने के लिए उपयोग किया जाता है।

## PSD फ़ाइलों को संभालने के लिए Aspose.PSD for Java का उपयोग क्यों करें?
Aspose.PSD एक शुद्ध‑Java API प्रदान करता है जो आपको Photoshop स्थापित किए बिना Photoshop PSD फ़ाइलों को पढ़ने, संपादित करने और लिखने की अनुमति देता है। यह लेयर प्रबंधन, रंग हेरफेर, और वेक्टर ड्राइंग को समर्थन देता है, जिससे यह सर्वर‑साइड इमेज प्रोसेसिंग, स्वचालित एसेट पाइपलाइन, और कस्टम ग्राफ़िक जेनरेशन के लिए आदर्श बनता है।

## पूर्वापेक्षाएँ

- आपके मशीन पर Java Development Kit (JDK) स्थापित हो।  
- Aspose.PSD for Java लाइब्रेरी। आप इसे [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) से डाउनलोड कर सकते हैं।

## पैकेज आयात करें

शुरू करने के लिए, आवश्यक क्लासेज़ को अपने Java प्रोजेक्ट में इम्पोर्ट करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## चरण 1: नया दस्तावेज़ बनाएं

पहले, इच्छित कैनवास आकार के साथ एक नया PSD दस्तावेज़ बनाएं। यह दस्तावेज़ उस लेयर की मेज़बानी करेगा जिस पर हम ड्रॉ करेंगे।

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## चरण 2: लेयर जोड़ें

अगला, एक नई खाली लेयर जोड़ें जो छवि की पूरी चौड़ाई और ऊँचाई को कवर करे। लेयर्स ड्रॉइंग ऑपरेशन्स को अलग रखने के लिए आवश्यक हैं।

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## चरण 3: आकार बनाएं

हम `Graphics` क्लास का उपयोग करके लेयर के पिक्सेल डेटा को हेरफेर करेंगे। नीचे तीन उदाहरण हैं जो पृष्ठभूमि को साफ़ करने और विभिन्न रंगों के साथ आयतें ड्रॉ करने को दर्शाते हैं।

### लेयर का रंग साफ़ करें (पृष्ठभूमि को पीला सेट करें)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### लाल आयत बनाएं (मुख्य फोकस)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### नीली आयत बनाएं (अतिरिक्त उदाहरण)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## चरण 4: परिवर्तन सहेजें

अंत में, संशोधित PSD छवि को डिस्क पर लिखें। फ़ाइल में नई लेयर और ड्रॉ किए गए आकार शामिल होंगे।

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## सामान्य समस्याएँ और समाधान

- **लेयर ड्रॉ करने के बाद दिखाई नहीं दे रहा:** सुनिश्चित करें कि `Graphics` ऑब्जेक्ट बनाने **से पहले** लेयर को इमेज में जोड़ा गया है।
- **रंग गलत दिख रहे हैं:** पुष्टि करें कि आप `Color.getRed()` (या अन्य स्थैतिक मेथड) का उपयोग कर रहे हैं, न कि ऐसी कस्टम RGB वैल्यूज़ जो रेंज से बाहर हों।
- **फ़ाइल सहेजी नहीं गई:** पुष्टि करें कि `outputDir` पाथ मौजूद है और एप्लिकेशन के पास लिखने की अनुमति है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं Aspose.PSD for Java का उपयोग मौजूदा PSD फ़ाइलों को संशोधित करने के लिए कर सकता हूँ?

A1: हाँ, Aspose.PSD for Java मौजूदा PSD फ़ाइलों को संपादित और हेरफेर करने के लिए व्यापक कार्यक्षमता प्रदान करता है।

### प्रश्न 2: Aspose.PSD for Java के लिए समर्थन कहाँ मिल सकता है?

A2: आप किसी भी समर्थन‑संबंधी प्रश्न के लिए [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) पर जा सकते हैं।

### प्रश्न 3: क्या Aspose.PSD for Java का मुफ्त ट्रायल उपलब्ध है?

A3: हाँ, आप मुफ्त ट्रायल संस्करण [यहाँ](https://releases.aspose.com/) से एक्सेस कर सकते हैं।

### प्रश्न 4: मैं Aspose.PSD for Java का लाइसेंस कैसे खरीद सकता हूँ?

A4: आप लाइसेंस [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy) से खरीद सकते हैं।

### प्रश्न 5: क्या Aspose.PSD for Java के लिए अस्थायी लाइसेंस उपलब्ध हैं?

A5: हाँ, आप अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

## अतिरिक्त अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं आयतों के अलावा अन्य आकार बना सकता हूँ?**  
**उत्तर:** हाँ, `Graphics` क्लास एलिप्स, लाइन्स, और कस्टम पाथ्स को ड्रॉ करने का भी समर्थन करता है।

**प्रश्न: क्या Aspose.PSD ड्रॉ किए गए आकारों में ट्रांसपैरेंसी का समर्थन करता है?**  
**उत्तर:** बिल्कुल; आप `SolidBrush` को ARGB रंग के साथ उपयोग करके अल्फा ट्रांसपैरेंसी शामिल कर सकते हैं।

**प्रश्न: क्या लेयर की अपारदर्शिता (opacity) को संपादित करना संभव है?**  
**उत्तर:** हाँ, प्रत्येक `Layer` ऑब्जेक्ट में `setOpacity` मेथड है जो 0 से 255 तक का मान स्वीकार करता है।

**प्रश्न: नई फ़ाइल बनाने के बजाय मौजूदा PSD फ़ाइल को कैसे लोड करूँ?**  
**उत्तर:** लेयर्स को हेरफेर करने से पहले `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` का उपयोग करें।

## निष्कर्ष

आपने अब Aspose.PSD for Java का उपयोग करके **लाल आयत** और अन्य बुनियादी आकारों को PSD फ़ाइल में कैसे बनाना है, सीख लिया है। एक दस्तावेज़ बनाकर, लेयर जोड़कर, उसकी पृष्ठभूमि साफ़ करके, और `Graphics` API से ड्रॉ करके आप कई ग्राफ़िक‑डिज़ाइन कार्यों को ऑटोमेट कर सकते हैं। विभिन्न ब्रश, लेयर इफ़ेक्ट्स, और फ़ाइल फ़ॉर्मेट्स के साथ प्रयोग करके आगे अन्वेषण करें।

---

**अंतिम अपडेट:** 2025-12-27  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.12 (लेखन के समय नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}