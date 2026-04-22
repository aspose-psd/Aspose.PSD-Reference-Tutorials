---
date: 2026-02-07
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में स्ट्रोक रंग कैसे बदलें,
  सीखें। स्ट्रोक लेयर का रंग, अपारदर्शिता और अधिक संशोधित करने के लिए इस चरण‑दर‑चरण
  गाइड का पालन करें।
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java में स्ट्रोक रंग कैसे बदलें
url: /hi/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java में स्ट्रोक रंग कैसे बदलें

## Introduction

यदि आपको प्रोग्रामेटिक रूप से Photoshop दस्तावेज़ में **स्ट्रोक रंग कैसे बदलें** की आवश्यकता है, तो Aspose.PSD for Java इसे सरल बनाता है। इस ट्यूटोरियल में हम स्ट्रोक लेयर जोड़ने, उसके रंग को बदलने, अपारदर्शिता समायोजित करने और परिणाम को सहेजने की प्रक्रिया को चरणबद्ध रूप से देखेंगे। अंत तक आप किसी भी मौजूदा लेयर के स्ट्रोक को संशोधित करना भी सीखेंगे, जिससे आप अपने Java कोड से पूरी रचनात्मक नियंत्रण प्राप्त कर सकते हैं।

## Quick Answers
- **क्या लाइब्रेरी आवश्यक है?** Aspose.PSD for Java (नवीनतम संस्करण)।  
- **क्या मैं स्ट्रोक रंग बदल सकता हूँ?** हाँ – किसी भी `Color` को सेट करने के लिए `ColorFillSettings` का उपयोग करें।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर।  
- **कार्यान्वयन में कितना समय लगता है?** सामान्यतः बुनियादी स्ट्रोक परिवर्तन के लिए 10 मिनट से कम।

## What is a Stroke Layer in a PSD?

स्ट्रोक लेयर एक वेक्टर इफ़ेक्ट है जो लेयर की सामग्री के चारों ओर एक रूपरेखा बनाता है। इसे रंग, मोटाई, अपारदर्शिता और ब्लेंड मोड के साथ अनुकूलित किया जा सकता है। इस इफ़ेक्ट को प्रोग्रामेटिक रूप से संशोधित करने से स्वचालित ब्रांडिंग, बैच प्रोसेसिंग, या डायनेमिक ग्राफ़िक्स जनरेशन संभव हो जाता है।

## Why Use Aspose.PSD to Change Stroke Color?
- **Photoshop की आवश्यकता नहीं** – पूरी तरह से Java में काम करें।  
- **पूर्ण PSD स्पेक अनुपालन** – सभी आधुनिक PSD सुविधाएँ समर्थित हैं।  
- **उच्च प्रदर्शन** – बड़े फ़ाइलों को तेज़ी से प्रोसेस करें।  
- **क्रॉस‑प्लेटफ़ॉर्म** – JVM वाले किसी भी OS पर चलाएँ।

## How to Change Stroke Color Programmatically
नीचे एक संक्षिप्त, चरण‑दर‑चरण मार्गदर्शिका है जो Aspose.PSD for Java का उपयोग करके स्ट्रोक रंग कैसे बदलें, यह ठीक‑ठीक दर्शाती है। प्रत्येक चरण में एक छोटा स्पष्टीकरण और उसके बाद मूल कोड ब्लॉक (अपरिवर्तित) शामिल है।

### Prerequisites

- **Aspose.PSD लाइब्रेरी** – इसे [आधिकारिक दस्तावेज़](https://reference.aspose.com/psd/java/) से डाउनलोड करें।  
- **Java Development Kit (JDK)** – संस्करण 8 या नया।  
- **IDE** – Eclipse, IntelliJ IDEA, या कोई भी Java‑संगत संपादक।

### Import Packages

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

### Step 1: Set Up Your Project

एक नया Java प्रोजेक्ट बनाएं, Aspose.PSD JAR को बिल्ड पाथ में जोड़ें, और सुनिश्चित करें कि लाइब्रेरी बिना त्रुटियों के लोड हो रही है।

### Step 2: Load the PSD File

इफ़ेक्ट संसाधनों को लोड करने को सक्षम करें ताकि स्ट्रोक जानकारी उपलब्ध हो सके।

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Step 3: Access the Stroke Effect Layer

दूसरी लेयर (इंडेक्स 1) से पहला स्ट्रोक इफ़ेक्ट प्राप्त करें।

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### Step 4: Validate Stroke Properties

परिवर्तन करने से पहले मौजूदा प्रॉपर्टीज़ की पुष्टि करें। यह अप्रत्याशित परिणामों से बचने में मदद करता है।

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### Step 5: Set Color and Opacity (How to Change Stroke Color)

यहाँ हम स्ट्रोक रंग को पीले में **बदलते** हैं और अपारदर्शिता को 50 % (127 / 255) तक घटाते हैं।

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### Step 6: Save the Modified PSD

अपडेटेड इमेज को डिस्क पर वापस लिखें। नई फ़ाइल अब संशोधित स्ट्रोक को समाहित करती है।

```java
im.save(exportPath);
```

## Common Use Cases for Changing Stroke Color
- **ब्रांडिंग ऑटोमेशन:** एक ही बैच रन में सैकड़ों PSD एसेट्स के लोगो पर कॉरपोरेट रंग लागू करें।  
- **डायनेमिक UI जनरेशन:** वेब‑आधारित डिज़ाइन टूल में उपयोगकर्ता‑चयनित थीम के आधार पर स्ट्रोक रंग तुरंत बदलें।  
- **प्रि‑फ़्लाइट तैयारी:** फ़ाइलों को प्रिंटिंग प्रेस पर भेजने से पहले सभी स्ट्रोक रंग प्रिंट स्पेसिफिकेशन को पूरा करते हों, यह सुनिश्चित करें।

## Common Pitfalls & Tips

- **Null जांच** – कास्ट करने से पहले हमेशा सुनिश्चित करें कि `getEffects()` एक non‑null एरे लौटाता है।  
- **लेयर इंडेक्स** – PSD लेयर्स शून्य‑आधारित होती हैं; सुनिश्चित करें कि आप सही लेयर को लक्षित कर रहे हैं।  
- **कलर फॉर्मेट** – `Color.getYellow()` केवल एक उदाहरण है; आप `new Color(r, g, b)` से कस्टम रंग बना सकते हैं।  
- **अपारदर्शिता रेंज** – अपारदर्शिता एक बाइट (0–255) है; 255 से ऊपर के मान क्लैंप हो जाएंगे।  
- **रिसोर्स लोडिंग** – `loadOptions.setLoadEffectsResource(true)` को भूलने से `null` इफ़ेक्ट्स एरे मिलेगा।

## Frequently Asked Questions

**प्रश्न: क्या मैं Aspose.PSD को अन्य Java ग्राफ़िक लाइब्रेरीज़ के साथ उपयोग कर सकता हूँ?**  
**उत्तर:** हाँ, Aspose.PSD को Apache Commons Imaging या Java2D जैसी लाइब्रेरीज़ के साथ मिलाकर विस्तारित कार्यक्षमता प्राप्त की जा सकती है।

**प्रश्न: क्या Aspose.PSD नवीनतम PSD फ़ाइल फ़ॉर्मेट के साथ संगत है?**  
**उत्तर:** बिल्कुल। लाइब्रेरी नियमित रूप से अपडेट की जाती है ताकि नवीनतम Photoshop स्पेसिफिकेशन को सपोर्ट किया जा सके।

**प्रश्न: Aspose.PSD का उपयोग करते समय अपवादों को कैसे संभालूँ?**  
**उत्तर:** विस्तृत ट्रबलशूटिंग और नमूना एरर‑हैंडलिंग कोड के लिए [सपोर्ट फ़ोरम](https://forum.aspose.com/c/psd/34) देखें।

**प्रश्न: क्या मैं खरीदने से पहले Aspose.PSD आज़मा सकता हूँ?**  
**उत्तर:** बिल्कुल! सभी सुविधाओं को एक्सप्लोर करने के लिए एक [फ्री ट्रायल](https://releases.aspose.com/) प्राप्त करें।

**प्रश्न: Aspose.PSD के लिए अस्थायी लाइसेंस कहाँ प्राप्त कर सकता हूँ?**  
**उत्तर:** अपने विकास पर्यावरण में लाइब्रेरी का मूल्यांकन करने के लिए एक [अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) प्राप्त करें।

---

**अंतिम अपडेट:** 2026-02-07  
**परीक्षण किया गया:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}