---
date: 2025-11-30
description: Aspose.PSD for Java का उपयोग करके स्ट्रोक जोड़ना और PSD स्ट्रोक रंग बदलना
  सीखें। स्ट्रोक लेयर के रंग और अपारदर्शिता को संशोधित करने के लिए इस चरण‑दर‑चरण गाइड
  का पालन करें।
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java में स्ट्रोक लेयर रंग कैसे जोड़ें
url: /hi/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java में Stroke Layer Color कैसे जोड़ें

## परिचय

यदि आपको प्रोग्रामेटिक रूप से Photoshop दस्तावेज़ में **stroke जोड़ना** है, तो Aspose.PSD for Java इसे सरल बनाता है। इस ट्यूटोरियल में हम stroke layer color जोड़ने, उसकी opacity समायोजित करने, और परिणाम को सहेजने की प्रक्रिया को देखेंगे। अंत में आप देखेंगे कि **stroke color कैसे बदलें** (या *PSD stroke color बदलें*) किसी भी मौजूदा लेयर के लिए, जिससे आप अपने Java कोड से पूरी रचनात्मक नियंत्रण प्राप्त कर सकें।

## त्वरित उत्तर
- **कौन सा लाइब्रेरी आवश्यक है?** Aspose.PSD for Java (नवीनतम संस्करण)।  
- **क्या मैं stroke color बदल सकता हूँ?** हाँ – `ColorFillSettings` का उपयोग करके कोई भी `Color` सेट कर सकते हैं।  
- **क्या लाइसेंस चाहिए?** मूल्यांकन के लिए एक अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** सामान्यतः बुनियादी stroke परिवर्तन के लिए 10 मिनट से कम।

## PSD में Stroke Layer क्या है?
एक stroke layer वह वेक्टर इफ़ेक्ट है जो लेयर की सामग्री के चारों ओर एक रूपरेखा बनाता है। इसे रंग, मोटाई, opacity, और blend mode के साथ कस्टमाइज़ किया जा सकता है। इस इफ़ेक्ट को प्रोग्रामेटिक रूप से बदलने से स्वचालित ब्रांडिंग, बैच प्रोसेसिंग, या डायनेमिक ग्राफ़िक्स जेनरेशन संभव होता है।

## Aspose.PSD से Stroke Color बदलने के फायदे
- **Photoshop की आवश्यकता नहीं** – पूरी तरह Java में काम करें।  
- **पूर्ण PSD स्पेक अनुपालन** – सभी आधुनिक PSD फीचर समर्थित।  
- **उच्च प्रदर्शन** – बड़े फ़ाइलों को तेज़ी से प्रोसेस करें।  
- **क्रॉस‑प्लेटफ़ॉर्म** – JVM वाले किसी भी OS पर चलाएँ।

## पूर्वापेक्षाएँ

- **Aspose.PSD लाइब्रेरी** – [आधिकारिक दस्तावेज़](https://reference.aspose.com/psd/java/) से डाउनलोड करें।  
- **Java Development Kit (JDK)** – संस्करण 8 या नया।  
- **IDE** – Eclipse, IntelliJ IDEA, या कोई भी Java‑संगत एडिटर।

## पैकेज इम्पोर्ट करें

सबसे पहले, उन क्लासेज़ को इम्पोर्ट करें जिनकी आपको आवश्यकता होगी। यह आपके प्रोजेक्ट को PSD हैंडलिंग और stroke‑effect API तक पहुँच प्रदान करता है।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## चरण 1: प्रोजेक्ट सेट अप करें

एक नया Java प्रोजेक्ट बनाएं, Aspose.PSD JAR को बिल्ड पाथ में जोड़ें, और सुनिश्चित करें कि लाइब्रेरी बिना त्रुटि के लोड हो रही है।

## चरण 2: PSD फ़ाइल लोड करें

इफ़ेक्ट रिसोर्सेज़ को लोड करने के लिए सक्षम करें ताकि stroke जानकारी उपलब्ध हो।

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## चरण 3: Stroke Effect Layer तक पहुँचें

दूसरी लेयर (इंडेक्स 1) से पहला stroke effect प्राप्त करें।

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## चरण 4: Stroke प्रॉपर्टीज़ वैलिडेट करें

परिवर्तन करने से पहले मौजूदा प्रॉपर्टीज़ की पुष्टि करें। यह अप्रत्याशित परिणामों से बचाता है।

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## चरण 5: रंग और Opacity सेट करें (Stroke Color कैसे बदलें)

यहाँ हम **PSD stroke color** को पीला बदलते हैं और opacity को 50 % (127 / 255) तक घटाते हैं।

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## चरण 6: संशोधित PSD सहेजें

अपडेटेड इमेज को डिस्क पर वापस लिखें। नई फ़ाइल में अब संशोधित stroke शामिल होगा।

```java
im.save(exportPath);
```

## सामान्य समस्याएँ एवं टिप्स

- **Null जांच** – हमेशा सुनिश्चित करें कि `getEffects()` एक non‑null एरे लौटाता है, फिर कास्ट करें।  
- **लेयर इंडेक्स** – PSD लेयर्स शून्य‑आधारित होती हैं; सही लेयर को टार्गेट करना न भूलें।  
- **रंग फ़ॉर्मेट** – `Color.getYellow()` केवल एक उदाहरण है; आप `new Color(r, g, b)` से कस्टम रंग बना सकते हैं।  
- **Opacity रेंज** – opacity एक बाइट (0–255) है; 255 से ऊपर के मान क्लैंप हो जाएंगे।

## निष्कर्ष

आपने अब **stroke जोड़ना** और **stroke color बदलना** Aspose.PSD for Java का उपयोग करके सीख लिया है। विभिन्न रंग, blend mode, और opacity के साथ प्रयोग करें ताकि आपके प्रोजेक्ट की सटीक दृश्य शैली प्राप्त हो सके।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं Aspose.PSD को अन्य Java ग्राफ़िक लाइब्रेरीज़ के साथ उपयोग कर सकता हूँ?**  
उत्तर: हाँ, Aspose.PSD को Apache Commons Imaging या Java2D जैसी लाइब्रेरीज़ के साथ मिलाकर विस्तारित कार्यक्षमता प्राप्त की जा सकती है।

**प्रश्न: क्या Aspose.PSD नवीनतम PSD फ़ाइल फ़ॉर्मेट के साथ संगत है?**  
उत्तर: बिल्कुल। लाइब्रेरी को नियमित रूप से अपडेट किया जाता है ताकि नवीनतम Photoshop स्पेसिफ़िकेशन का समर्थन हो।

**प्रश्न: Aspose.PSD का उपयोग करते समय अपवादों को कैसे संभालें?**  
उत्तर: विस्तृत ट्रबलशूटिंग और नमूना एरर‑हैंडलिंग कोड के लिए [सपोर्ट फ़ोरम](https://forum.aspose.com/c/psd/34) देखें।

**प्रश्न: क्या मैं Aspose.PSD को खरीदने से पहले आज़मा सकता हूँ?**  
उत्तर: बिल्कुल! सभी फीचर का अन्वेषण करने के लिए एक [फ्री ट्रायल](https://releases.aspose.com/) प्राप्त करें।

**प्रश्न: Aspose.PSD के लिए अस्थायी लाइसेंस कहाँ प्राप्त करूँ?**  
उत्तर: विकास पर्यावरण में लाइब्रेरी का मूल्यांकन करने के लिए एक [अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) प्राप्त करें।

---

**अंतिम अपडेट:** 2025-11-30  
**परीक्षण किया गया:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}