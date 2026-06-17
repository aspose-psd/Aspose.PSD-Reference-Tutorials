---
date: 2026-04-22
description: Aspose.PSD for Java के साथ जावा में स्ट्रोक रंग बदलना सीखें। स्ट्रोक
  लेयर का रंग, अपारदर्शिता और अधिक संशोधित करने के लिए इस चरण‑दर‑चरण गाइड का पालन
  करें।
keywords:
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
- add stroke layer psd
linktitle: स्ट्रोक लेयर का रंग जोड़ें
second_title: Aspose.PSD Java API
title: Aspose.PSD का उपयोग करके जावा में स्ट्रोक रंग कैसे बदलें
url: /hi/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में Aspose.PSD का उपयोग करके स्ट्रोक रंग कैसे बदलें

## परिचय

यदि आपको प्रोग्रामेटिक रूप से Photoshop दस्तावेज़ में **change stroke color java** बदलने की आवश्यकता है, तो Aspose.PSD for Java इसे सरल बनाता है। इस ट्यूटोरियल में हम एक स्ट्रोक लेयर जोड़ने, उसका रंग बदलने, अपारदर्शिता समायोजित करने और परिणाम को सहेजने की प्रक्रिया को समझेंगे। अंत तक आप यह भी देखेंगे कि किसी मौजूदा लेयर के स्ट्रोक को कैसे संशोधित किया जाए, जिससे आपको अपने Java कोड से पूरी रचनात्मक नियंत्रण मिल सके।

## त्वरित उत्तर

- **क्या लाइब्रेरी आवश्यक है?** Aspose.PSD for Java (latest version).  
- **क्या मैं स्ट्रोक रंग बदल सकता हूँ?** हाँ – किसी भी `Color` को सेट करने के लिए `ColorFillSettings` का उपयोग करें।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** सामान्यतः बुनियादी स्ट्रोक परिवर्तन के लिए 10 मिनट से कम।

## PSD में स्ट्रोक लेयर क्या है?

स्ट्रोक लेयर एक वेक्टर इफ़ेक्ट है जो लेयर की सामग्री के चारों ओर एक रूपरेखा बनाता है। इसे रंग, मोटाई, अपारदर्शिता और ब्लेंड मोड के साथ अनुकूलित किया जा सकता है। इस इफ़ेक्ट को प्रोग्रामेटिक रूप से संशोधित करने से स्वचालित ब्रांडिंग, बैच प्रोसेसिंग, या डायनेमिक ग्राफ़िक्स जेनरेशन संभव होते हैं।

## स्ट्रोक रंग बदलने के लिए Aspose.PSD क्यों उपयोग करें?

- **Photoshop की आवश्यकता नहीं** – पूरी तरह से Java में काम करें।  
- **पूर्ण PSD स्पेक अनुपालन** – सभी आधुनिक PSD सुविधाएँ समर्थित हैं।  
- **उच्च प्रदर्शन** – बड़ी फ़ाइलों को तेज़ी से प्रोसेस करें।  
- **क्रॉस‑प्लेटफ़ॉर्म** – JVM वाले किसी भी OS पर चलाएँ।

## Java में प्रोग्रामेटिक रूप से स्ट्रोक रंग कैसे बदलें

नीचे एक संक्षिप्त, चरण‑दर‑चरण मार्गदर्शिका दी गई है जो Aspose.PSD for Java का उपयोग करके स्ट्रोक रंग कैसे बदलें, इसे ठीक‑ठीक दर्शाती है। प्रत्येक चरण में एक छोटा स्पष्टीकरण और उसके बाद मूल कोड ब्लॉक (अपरिवर्तित) शामिल है।

### आवश्यकताएँ

- **Aspose.PSD लाइब्रेरी** – [official documentation](https://reference.aspose.com/psd/java/) से डाउनलोड करें।  
- **Java Development Kit (JDK)** – संस्करण 8 या नया।  
- **IDE** – Eclipse, IntelliJ IDEA, या कोई भी Java‑compatible एडिटर।

### पैकेज इम्पोर्ट करें

सबसे पहले, उन क्लासों को इम्पोर्ट करें जिनकी आपको आवश्यकता होगी। यह आपके प्रोजेक्ट को PSD हैंडलिंग और स्ट्रोक‑इफ़ेक्ट API तक पहुँच प्रदान करता है।

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

### चरण 1: अपना प्रोजेक्ट सेट अप करें

एक नया Java प्रोजेक्ट बनाएं, Aspose.PSD JAR को बिल्ड पाथ में जोड़ें, और सुनिश्चित करें कि लाइब्रेरी बिना त्रुटियों के लोड हो रही है।

### चरण 2: PSD फ़ाइल लोड करें

इफ़ेक्ट रिसोर्सेज़ को लोड करने को सक्षम करें ताकि स्ट्रोक जानकारी उपलब्ध हो सके।

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### चरण 3: स्ट्रोक इफ़ेक्ट लेयर तक पहुँचें

दूसरी लेयर (इंडेक्स 1) से पहला स्ट्रोक इफ़ेक्ट प्राप्त करें।

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### चरण 4: स्ट्रोक प्रॉपर्टीज़ को वैध करें

परिवर्तन करने से पहले मौजूदा प्रॉपर्टीज़ की पुष्टि करें। यह अप्रत्याशित परिणामों से बचने में मदद करता है।

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### चरण 5: रंग और अपारदर्शिता सेट करें (स्ट्रोक रंग कैसे बदलें)

यहाँ हम स्ट्रोक रंग को पीले में **change stroke color** करते हैं और अपारदर्शिता को 50 % (127 / 255) तक घटाते हैं।

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### चरण 6: संशोधित PSD सहेजें

अपडेटेड इमेज को डिस्क पर वापस लिखें। नई फ़ाइल में अब संशोधित स्ट्रोक शामिल है।

```java
im.save(exportPath);
```

## स्ट्रोक अपारदर्शिता कैसे संशोधित करें

यदि आपको केवल अपारदर्शिता समायोजित करनी है जबकि मूल रंग को बनाए रखना है, तो `setOpacity` मान (0‑255) बदलें। उदाहरण के लिए, `colorStroke.setOpacity((byte)200);` स्ट्रोक को लगभग 78 % अपारदर्शी बना देगा।

## स्ट्रोक इफ़ेक्ट कैसे लागू करें

किसी लेयर में नया स्ट्रोक इफ़ेक्ट जोड़ने के लिए जो पहले से नहीं है, एक `StrokeEffect` इंस्टेंस बनाएं, उसके `ColorFillSettings` को कॉन्फ़िगर करें, और इसे लेयर के `BlendingOptions` से संलग्न करें। समान `setColor` और `setOpacity` मेथड्स का उपयोग करके रूप निर्धारित किया जाता है।

## PSD स्ट्रोक ट्यूटोरियल: PSD में स्ट्रोक लेयर जोड़ें

ऊपर दिए गए चरण मौजूदा लेयर में स्ट्रोक जोड़ने को दर्शाते हैं। एक पूरी नई स्ट्रोक लेयर के लिए, लक्ष्य लेयर को डुप्लिकेट करें, फिर `StrokeEffect` लागू करें। यह तरीका उपयोगी है जब आप मूल लेयर को अपरिवर्तित रखना चाहते हैं।

## स्ट्रोक रंग बदलने के सामान्य उपयोग केस

- **ब्रांडिंग ऑटोमेशन:** एक बैच रन में सैकड़ों PSD एसेट्स के लोगो पर कॉर्पोरेट रंग लागू करें।  
- **डायनेमिक UI जेनरेशन:** वेब‑आधारित डिज़ाइन टूल में उपयोगकर्ता‑चयनित थीम के आधार पर स्ट्रोक रंग तुरंत बदलें।  
- **प्रि‑फ़्लाइट तैयारी:** फ़ाइलें प्रेस को भेजने से पहले सुनिश्चित करें कि सभी स्ट्रोक रंग प्रिंट स्पेसिफिकेशन्स को पूरा करते हैं।

## सामान्य समस्याएँ और टिप्स

- **Null checks** – कास्ट करने से पहले हमेशा सुनिश्चित करें कि `getEffects()` एक non‑null एरे लौटाता है।  
- **Layer index** – PSD लेयर्स शून्य‑आधारित हैं; सुनिश्चित करें कि आप सही लेयर को टार्गेट कर रहे हैं।  
- **Color format** – `Color.getYellow()` केवल एक उदाहरण है; आप `new Color(r, g, b)` से कस्टम रंग बना सकते हैं।  
- **Opacity range** – अपारदर्शिता एक बाइट (0–255) है; 255 से ऊपर के मान क्लैंप हो जाएंगे।  
- **Resource loading** – यदि आप `loadOptions.setLoadEffectsResource(true)` भूल जाते हैं तो `null` इफ़ेक्ट्स एरे मिलेगा।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.PSD को अन्य Java ग्राफ़िक लाइब्रेरीज़ के साथ उपयोग कर सकता हूँ?**  
A: हाँ, विस्तारित कार्यक्षमता के लिए Aspose.PSD को Apache Commons Imaging या Java2D जैसी लाइब्रेरीज़ के साथ संयोजित किया जा सकता है।

**Q: क्या Aspose.PSD नवीनतम PSD फ़ाइल फ़ॉर्मेट के साथ संगत है?**  
A: बिल्कुल। लाइब्रेरी नियमित रूप से अपडेट की जाती है ताकि नवीनतम Photoshop स्पेसिफिकेशन्स का समर्थन हो सके।

**Q: Aspose.PSD का उपयोग करते समय अपवादों को कैसे संभालूँ?**  
A: विस्तृत ट्रबलशूटिंग और नमूना एरर‑हैंडलिंग कोड के लिए [support forum](https://forum.aspose.com/c/psd/34) देखें।

**Q: क्या मैं खरीदने से पहले Aspose.PSD आज़मा सकता हूँ?**  
A: बिल्कुल! सभी फीचर्स का अन्वेषण करने के लिए एक [free trial](https://releases.aspose.com/) प्राप्त करें।

**Q: Aspose.PSD के लिए अस्थायी लाइसेंस कहाँ प्राप्त कर सकता हूँ?**  
A: अपने विकास वातावरण में लाइब्रेरी का मूल्यांकन करने के लिए एक [temporary license](https://purchase.aspose.com/temporary-license/) प्राप्त करें।

---

**अंतिम अपडेट:** 2026-04-22  
**परीक्षित संस्करण:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}