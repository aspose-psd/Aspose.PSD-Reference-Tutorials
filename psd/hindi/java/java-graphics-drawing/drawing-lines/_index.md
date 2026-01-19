---
date: 2026-01-19
description: ASP और Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में लाइनों को कैसे
  बनाएं, सीखें। इस चरण‑दर‑चरण मार्गदर्शिका के साथ अपनी Java विकास कौशल को बढ़ाएँ।
linktitle: Drawing Lines in Java
second_title: Aspose.PSD Java API
title: asp जावा में रेखाएँ बनाना
url: /hi/java/java-graphics-drawing/drawing-lines/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# asp Drawing Lines in Java

## Introduction
आधुनिक Java विकास में, Photoshop Document (PSD) फ़ाइलों को प्रोग्रामेटिक रूप से संभालना स्वचालन की नई संभावनाएँ खोलता है। **asp** (Aspose.PSD लाइब्रेरी) आपको Java कोड से सीधे PSD फ़ाइलें बनाने, संपादित करने और रेंडर करने पर पूर्ण नियंत्रण देती है। इस ट्यूटोरियल में आप सीखेंगे **कैसे Java एप्लिकेशन में लाइनें ड्रॉ करें** Aspose.PSD for Java का उपयोग करके, चरण दर चरण।

## Quick Answers
- **कौन सी लाइब्रेरी आपको Java में PSD फ़ाइलें संपादित करने देती है?** asp (Aspose.PSD for Java)  
- **क्या मैं डॉटेड और सॉलिड दोनों लाइनों को ड्रॉ कर सकता हूँ?** हाँ, विभिन्न Pen सेटिंग्स का उपयोग करके।  
- **क्या विकास के लिए लाइसेंस चाहिए?** टेस्टिंग के लिए मुफ्त ट्रायल काम करता है; प्रोडक्शन के लिए लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** JDK 8 या उससे ऊपर।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?**  लाइन ड्रॉइंग के लिए 15 मिनोधित करने और लिखने के लिए समृद्ध API सेट प्रदान करती है, बिना Adobe Photoshop की आवश्यकता के। चाहे आपको ग्राफ़िक्स ओ करनेारी काम संभाल लेती है।

## Why use asp for drawing lines in Java?
- **Performance:** ऑप्टिमाइज़्ड नेटिव कोड बड़े PSD फ़ाइलों के लिए भी तेज़ रेंडरिंग सुनिश्चित करता है।  
- **Flexibility:** ड्रॉइंग प्रिमिटिव्स की विस्तृत रेंज—लाइन, रेक्टैंगल, एलिप्स और कस्टम पाथ्स—को सपोर्ट करता है।  
- **Cross‑platform:** किसी भी ऑपरेटिंग सिस्टम पर काम करता है जहाँ Java चलता है।  
- **No Photoshop required:** सभी ऑपरेशन्स प्रोग्रामेटिक रूप से किए जाते हैं।

## Prerequisites
शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- Java प्रोग्रामिंग का बेसिक ज्ञान।  
- स्थापित JDK (Java Development Kit)।  
- **asp** (Aspose.PSD for Java) लाइब्रेरी डाउनलोड की हुई और आपके प्रोजेक्ट डिपेंडेंसीज़ में जोड़ी हुई।  

आप लाइब्रेरी आधिकारिक डाउनलोड पेज से प्राप्त कर सकते हैं:

- [Aspose.PSD for Java Download](https://releases.aspose.com/psd/java/)

## Import आवश्यक asp क्लासेज़ को अपने Java प्रोजेक्ट में इम्पोर्ट करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Step 1: Set Up Your Project
अपने IDE में एक नया Java प्रोजेक्ट बनाएं और asp JAR फाइलों को बिल्ड पाथ में जोड़ें। इससे आप नीचे दिखाए गए सभी ड्रॉइंग API तक पहुंच पाएंगे।

## Step 2: Initialize PSD Image
इच्छित आयामों के साथ एक खाली PSD कैनवास बनाएं:

```java
String dataDir = "Your Document Directory";
String outpath = dataDir + "Lines.psd";
Image image = new PsdImage(100, 100);
```

## Step 3: Initialize Graphics Object
**Graphics** ऑब्जेक्ट एक ड्रॉइंग सतह की तरह काम करता है। ड्रॉ करने से पहले इसे बैकग्राउंड कलर से क्लियर करें:

```java
Graphics graphic = new Graphics(image);
graphic.clear(Color.getYellow());
```

## Step 4: Draw Diagonal Dotted Lines
डिफ़ॉल्ट स्टाइल वाले Pen का उपयोग करके दो डायगोनल डॉटेड लाइनों को ड्रॉ करें:

```java
graphic.drawLine(new Pen(Color.getBlue()), 9, 9, 90, 90);
graphic.drawLine(new Pen(Color.getBlue()), 9, 90, 90, 9);
```

## Step 5: Draw Continuous Lines
कस्टम रंगों के साथ सॉलिड लाइनों के लिए, SolidBrush ऑब्जेक्ट्स द्वारा समर्थित Pen इंस्टेंस बनाएं:

```java
graphic.drawLine(new Pen(new SolidBrush(Color.getRed())), new Point(9, 9), new Point(9, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getAqua())), new Point(9, 90), new Point(90, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getBlack())), new Point(90, 90), new Point(90, 9));
graphic.drawLine(new Pen(new SolidBrush(Color.getWhite())), new Point(90, 9), new Point(9, 9));
```

## Step 6: Save the Image
परिवर्तित PSD को डिस्क पर सेव करें:

```java
image.save(outpath);
```

## Conclusion
इन चरणों का पालन करके आपने सफलतापूर्वक **asp** का उपयोग करके Java में PSD फ़ाइल के अंदर लाइनों को ड्रॉ किया। अब आप जानते हैं कि कैनवास कैसे सेट करें, उसे क्लियर करें, डॉटेड और सॉलिड दोनों लाइनों को ड्रॉ करें, और परिणाम को सेव करें। यह आधार आपको अधिक जटिल ग्राफ़िक्स बनाने, टेक्स्ट लेयर्स जोड़ने, या बड़े Java एप्लिकेशन्स में PSD मैनिपुलेशन को इंटीग्रेट करने में मदद करेगा।

## Frequently Asked Questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java एक शक्तिशाली Java लाइब्रेरी है जो प्रोग्रामेटिक रूप से PSD फ़ाइलों के साथ काम करने के लिए बनाई गई है।

**Q: Where can I find the documentation for Aspose.PSD for Java?**  
A: आप डॉक्यूमेंटेशन [यहाँ](https://reference.aspose.com/psd/java/) पा सकते हैं।

**Q: Can I try Aspose.PSD for Java before purchasing?**  
A: हाँ, आप मुफ्त ट्रायल [यहाँ](https://releases.aspose.com/) ले सकते हैं।

**Q: How do I get technical support for Aspose.PSD for Java?**  
A: तकनीकी समर्थन के लिए, [Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34) पर जाएँ।

**Q: Where can I obtain a temporary license for Aspose.PSD for Java?**  
A: आप एक टेम्पररी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-19  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---