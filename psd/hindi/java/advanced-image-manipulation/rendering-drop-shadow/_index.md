---
date: 2025-12-04
description: Aspose.PSD for Java का उपयोग करके PSD को PNG के रूप में सहेजना और रेंडरिंग
  ड्रॉप शैडो लागू करना सीखें। यह गाइड शैडो जोड़ने, PSD को PNG में बदलने, और Java में
  ड्रॉप शैडो लागू करने के बारे में बताता है।
language: hi
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Aspose.PSD Java के साथ PSD को PNG के रूप में सहेजें और ड्रॉप शैडो जोड़ें
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java के साथ PSD को PNG के रूप में सहेजें और ड्रॉप शैडो जोड़ें

## परिचय

यदि आप Java में Photoshop फ़ाइलों के साथ काम कर रहे हैं, तो **PSD को PNG के रूप में सहेजना** और साथ ही एक पेशेवर‑दिखावट वाला ड्रॉप शैडो जोड़ना एक सामान्य आवश्यकता है। Aspose.PSD इस कार्य को सरल बनाता है, जिससे आप **PSD को PNG में बदल सकते हैं** और **ड्रॉप शैडो Java** को कुछ ही पंक्तियों के कोड में लागू कर सकते हैं। इस ट्यूटोरियल में हम पूरी प्रक्रिया को समझेंगे, PSD फ़ाइल को लोड करने से लेकर अंतिम PNG को रेंडर किए गए शैडो इफ़ेक्ट के साथ एक्सपोर्ट करने तक।

## त्वरित उत्तर
- **“PSD को PNG के रूप में सहेजना” का क्या मतलब है?** यह एक लेयर्ड Photoshop फ़ाइल को एक फ्लैट PNG इमेज में बदल देता है, जिसमें ट्रांसपेरेंसी बनी रहती है।  
- **क्या मैं कन्वर्ज़न के दौरान ड्रॉप शैडो जोड़ सकता हूँ?** हाँ—Aspose.PSD आपको एक्सपोर्ट से पहले लेयर इफ़ेक्ट्स को संशोधित करने की अनुमति देता है।  
- **क्या कोड चलाने के लिए लाइसेंस चाहिए?** मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है; प्रोडक्शन के लिए लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर।  
- **क्या ड्रॉप‑शैडो इफ़ेक्ट को कस्टमाइज़ किया जा सकता है?** बिल्कुल—आप रंग, अपारदर्शिता, दूरी, आकार, कोण, और अधिक समायोजित कर सकते हैं।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास ये हैं:

- **Java विकास वातावरण** – JDK 8 या नया स्थापित हो।  
- **Aspose.PSD लाइब्रेरी** – आधिकारिक साइट [here](https://releases.aspose.com/psd/java/) से नवीनतम JAR डाउनलोड करें।  
- **एक PSD फ़ाइल** – ऐसी फ़ाइल जिसमें कम से कम एक लेयर हो जिसे आप शैडो के साथ बढ़ाना चाहते हैं।  

## Java में ड्रॉप शैडो के साथ PSD को PNG के रूप में कैसे सहेजें?

नीचे चरण‑दर‑चरण गाइड दिया गया है। प्रत्येक चरण में संक्षिप्त व्याख्या और आवश्यक कोड स्निपेट शामिल है जिसे आप कॉपी कर सकते हैं।

### चरण 1: आवश्यक पैकेज आयात करें

हम उन क्लासों को आयात करके शुरू करते हैं जो इमेज लोडिंग, इफ़ेक्ट हैंडलिंग, और PNG एक्सपोर्ट क्षमताएँ प्रदान करती हैं।

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### चरण 2: दस्तावेज़ निर्देशिका निर्धारित करें

उस फ़ोल्डर को सेट करें जहाँ आपका स्रोत PSD और परिणामी PNG स्थित होंगे।

```java
String dataDir = "Your Document Directory";
```

### चरण 3: PSD और PNG फ़ाइल पथ सेट करें

इनपुट PSD और आउटपुट PNG के पूर्ण पथ निर्दिष्ट करें।

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### चरण 4: इफ़ेक्ट सक्षम करके PSD फ़ाइल लोड करें

**loadEffectsResource** को सक्षम करने से लेयर इफ़ेक्ट्स (जैसे शैडो) को संशोधित करने के लिए उपलब्ध कराया जाता है।

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### चरण 5: ड्रॉप शैडो इफ़ेक्ट तक पहुँचें

यहाँ हम दूसरे लेयर (इंडेक्स 1) पर लागू पहले इफ़ेक्ट को प्राप्त करते हैं। यही वह जगह है जहाँ हम शैडो पैरामीटर पढ़ेंगे या बदलेंगे।

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### चरण 6: शैडो इफ़ेक्ट प्रॉपर्टीज़ को वैध करें (वैकल्पिक लेकिन उपयोगी)

मौजूदा प्रॉपर्टीज़ की जाँच करने से आपको यह तय करने में मदद मिलती है कि आपको कुछ बदलने की आवश्यकता है या नहीं। नीचे दिए गए असर्शन डिफ़ॉल्ट मानों की पुष्टि करते हैं।

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **प्रो टिप:** यदि आप **how to add shadow** को कस्टम सेटिंग्स के साथ लागू करना चाहते हैं, तो `shadowEffect` की प्रॉपर्टीज़ को सहेजने से पहले संशोधित करें (जैसे, `shadowEffect.setColor(Color.getRed());`)।

### चरण 7: संशोधित इमेज को PNG के रूप में सहेजें

अंत में, हम PSD (रेंडर किए गए शैडो के साथ) को PNG फ़ाइल में एक्सपोर्ट करते हैं। `TruecolorWithAlpha` विकल्प ट्रांसपेरेंसी को संरक्षित रखता है।

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

और इस प्रकार—एक पूर्ण **convert PSD to PNG** वर्कफ़्लो तैयार है जो एक ही पास में **apply drop shadow java** भी करता है।

## इस कार्य के लिए Aspose.PSD क्यों उपयोग करें?

- **कोई नेटिव Photoshop आवश्यक नहीं** – Java को सपोर्ट करने वाले किसी भी प्लेटफ़ॉर्म पर काम करता है।  
- **पूर्ण PSD फिडेलिटी** – सभी लेयर जानकारी, मास्क, और इफ़ेक्ट्स संरक्षित रहते हैं।  
- **सूक्ष्म नियंत्रण** – एक्सपोर्ट से पहले ड्रॉप शैडो के हर पैरामीटर को समायोजित करें।  
- **उच्च प्रदर्शन** – बड़े फ़ाइलों और बैच प्रोसेसिंग के लिए अनुकूलित।

## सामान्य समस्याएँ एवं ट्रबलशूटिंग

| लक्षण | संभावित कारण | समाधान |
|---------|--------------|-----|
| `NullPointerException` on `shadowEffect` | लक्ष्य लेयर में कोई इफ़ेक्ट नहीं है या इंडेक्स गलत है। | लेयर इंडेक्स (`im.getLayers()[i]`) की जाँच करें और सुनिश्चित करें कि इफ़ेक्ट मौजूद है। |
| एक्सपोर्ट किया गया PNG खाली है | PNG विकल्प सही से सेट नहीं हैं या इमेज सहेजी नहीं गई। | `PngColorType.TruecolorWithAlpha` का उपयोग करें और `im.save()` पथ लिखने योग्य है यह पुष्टि करें। |
| शैडो रंग दिखाई नहीं दे रहा | शैडो अपारदर्शिता 0 पर सेट है या रंग पृष्ठभूमि के समान है। | `shadowEffect.setOpacity(255);` सेट करें और कंट्रास्टिंग रंग चुनें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं एक साथ कई लेयर्स पर ड्रॉप शैडो लागू कर सकता हूँ?**  
उत्तर: हाँ। `im.getLayers()` पर लूप चलाएँ और प्रत्येक लेयर के `DropShadowEffect` को आवश्यकतानुसार संशोधित करें।

**प्रश्न: ‘Spread’ पैरामीटर क्या करता है?**  
उत्तर: यह नियंत्रित करता है कि शैडो पूरी तरह अपारदर्शी से पारदर्शी तक कितनी तेज़ी से बदलता है। उच्च स्प्रेड से कठोर किनारा बनता है।

**प्रश्न: क्या Aspose.PSD सभी Photoshop संस्करणों के साथ संगत है?**  
उत्तर: यह कई PSD संस्करणों को सपोर्ट करता है, शुरुआती रिलीज़ से लेकर नवीनतम Photoshop CC फ़ाइलों तक।

**प्रश्न: यदि मुझे समस्याएँ आती हैं तो मदद कैसे प्राप्त करूँ?**  
उत्तर: समुदाय समर्थन और आधिकारिक सहायता के लिए [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) देखें।

**प्रश्न: क्या मैं Aspose.PSD को खरीदने से पहले आज़मा सकता हूँ?**  
उत्तर: बिल्कुल। मुफ्त ट्रायल के लिए [Aspose वेबसाइट](https://releases.aspose.com/) से डाउनलोड करें।

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**अंतिम अपडेट:** 2025-12-04  
**टेस्टेड विद:** Aspose.PSD 24.12 for Java  
**लेखक:** Aspose  

---