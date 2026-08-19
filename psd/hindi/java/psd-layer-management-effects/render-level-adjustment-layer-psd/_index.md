---
date: 2026-04-05
description: Aspose.PSD for Java का उपयोग करके PSD को PNG में निर्यात करना और आसानी
  से छवि कंट्रास्ट बढ़ाना सीखें। इस चरण‑दर‑चरण गाइड के साथ लेवल्स एडजस्टमेंट लेयर्स
  में महारत हासिल करें।
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: PSD को PNG में निर्यात करें और जावा में लेवल एडजस्टमेंट लेयर को रेंडर करें
second_title: Aspose.PSD Java API
title: PSD को PNG में निर्यात करें और Java में लेवल एडजस्टमेंट लेयर को रेंडर करें
url: /hi/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD को PNG में निर्यात करें और Java में लेवल एडजस्टमेंट लेयर रेंडर करें

## परिचय

क्या आपने कभी PSD फ़ाइल खोली और देखा कि रंग सपाट लग रहे हैं या कंट्रास्ट ठीक नहीं है? आप Aspose.PSD for Java का उपयोग करके **export PSD to PNG** को जल्दी से कर सकते हैं और लेवल्स एडजस्टमेंट लेयर के साथ छवि को फाइन‑ट्यून कर सकते हैं। इस ट्यूटोरियल में हम पूरी प्रक्रिया को चरण‑दर‑चरण देखेंगे—PSD लोड करने से, उसके लेवल्स को समायोजित करने से, अंत में PNG के रूप में सहेजने तक—ताकि आप रंगीनता बढ़ा सकें और वेब‑तैयार एसेट्स मिनटों में तैयार कर सकें।

## त्वरित उत्तर
- **export PSD to PNG** का क्या अर्थ है? यह एक Photoshop दस्तावेज़ को बिना नुकसान के PNG छवि में बदलता है जबकि ट्रांसपैरेंसी को संरक्षित रखता है।  
- **क्या निर्यात से पहले लेवल्स समायोजित कर सकता हूँ?** हाँ, Aspose.PSD आपको प्रोग्रामेटिकली इनपुट और आउटपुट लेवल्स को बदलने की सुविधा देता है।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या बैच प्रोसेसिंग संभव है?** बिल्कुल—आप कोड को लूप में रखकर कई PSD फ़ाइलों को संभाल सकते हैं।  
- **कौन सा Java संस्करण आवश्यक है?** Java 8 या उससे नया संस्करण अनुशंसित है।

## “export PSD to PNG” क्या है?
PSD को PNG में निर्यात करना का मतलब है लेयर्ड Photoshop फ़ाइल को एक पोर्टेबल नेटवर्क ग्राफ़िक्स (PNG) छवि में फ्लैटन करना। PNG लॉसलेस कम्प्रेशन और अल्फा चैनल का समर्थन करता है, जिससे यह वेब ग्राफ़िक्स और UI एसेट्स के लिए आदर्श बनता है।

## निर्यात से पहले लेवल्स क्यों समायोजित करें?
लेवल्स को समायोजित करने से आप शैडो, मिडटोन और हाइलाइट्स को नियंत्रित कर सकते हैं, जिससे कुल कंट्रास्ट और रंग संतुलन बेहतर होता है। यह कदम सुनिश्चित करता है कि अंतिम PNG बिना Photoshop में मैन्युअल एडिटिंग के भी पॉलिश दिखे।

## पूर्वापेक्षाएँ

- **Java Development Kit (JDK)** – Oracle वेबसाइट से नवीनतम संस्करण डाउनलोड करें ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html))।  
- **Aspose.PSD for Java Library** – आधिकारिक डाउनलोड पेज से प्राप्त करें ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/))। एक मुफ्त ट्रायल उपलब्ध है ([https://releases.aspose.com/](https://releases.aspose.com/))।  

## पैकेज आयात करें

कोड में डुबकी लगाने से पहले, उन क्लासेज़ को आयात करें जो हमें PSD मैनिपुलेशन और PNG निर्यात तक पहुँच देती हैं:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## चरण‑दर‑चरण मार्गदर्शिका

### चरण 1: फ़ाइल पथ निर्धारित करें (PSD प्रोसेसिंग को स्वचालित कैसे करें)

स्रोत PSD, संशोधित PSD, और अंतिम PNG निर्यात स्थान के लिए स्पष्ट, वर्णनात्मक वेरिएबल्स सेट करें।

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### चरण 2: PSD छवि लोड करें

`Image.load` का उपयोग करके PSD फ़ाइल को `PsdImage` ऑब्जेक्ट में पढ़ें। Aspose.PSD स्वचालित रूप से फ़ॉर्मेट का पता लगाता है।

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### चरण 3: लेयर्स के माध्यम से इटररेट करें (लेवल्स कैसे समायोजित करें)

हर लेयर पर लूप करें ताकि Levels Adjustment Layer को खोजा जा सके।

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### चरण 4: लेवल्स लेयर की पहचान करें

`instanceof LevelsLayer` के साथ प्रत्येक लेयर की जाँच करें। मिलने पर उसे कास्ट करें ताकि हम उसकी प्रॉपर्टीज़ को बदल सकें।

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### चरण 5: लेवल्स को फाइन‑ट्यून करें (लेवल्स कैसे समायोजित करें)

पहले चैनल (आमतौर पर कॉम्पोजिट चैनल) के इनपुट और आउटपुट दोनों लेवल्स को समायोजित करें। ये मान उदाहरण हैं; अपनी आवश्यकता अनुसार प्रयोग करें।

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### चरण 6: संशोधित PSD सहेजें (PSD को स्वचालित कैसे करें)

परिवर्तनों को नई PSD फ़ाइल में सहेजें।

```java
im.save(psdPathAfterChange);
```

### चरण 7: PNG के रूप में निर्यात करें (Export PSD to PNG)

यदि आपको PNG संस्करण चाहिए, तो `PngOptions` को कॉन्फ़िगर करें और छवि को सहेजें।

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## सामान्य उपयोग केस

- **वेब एसेट तैयारी:** डिज़ाइनर‑प्रदान किए गए PSD मॉकअप को ब्राउज़र‑तैयार PNG में बदलें।  
- **बैच प्रोसेसिंग:** CI पाइपलाइन में दर्जनों PSD फ़ाइलों के स्वचालित रूपांतरण को लागू करें।  
- **डायनामिक इमेज जेनरेशन:** निर्यात से पहले उपयोगकर्ता इनपुट के आधार पर लेवल्स को रीयल‑टाइम में समायोजित करें।

## समस्या निवारण और सुझाव

- **लेयर्स तक पहुँचते समय Null pointer:** सुनिश्चित करें कि PSD में वास्तव में एक Levels Adjustment Layer मौजूद है; अन्यथा null‑check जोड़ें।  
- **निर्यात के बाद अप्रत्याशित रंग:** पुष्टि करें कि PNG कलर टाइप `TruecolorWithAlpha` पर सेट है ताकि ट्रांसपैरेंसी बनी रहे।  
- **बहुत सारी फ़ाइलों के साथ प्रदर्शन:** बैच प्रोसेसिंग के दौरान मेमोरी चर्न कम करने के लिए समान `PsdImage` इंस्टेंस को पुन: उपयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं व्यक्तिगत रंग चैनलों (RGB) को अलग‑अलग समायोजित कर सकता हूँ?**  
A: हाँ। `levelsLayer.getChannel(index)` का उपयोग करें जहाँ `index` = 0 (Red), 1 (Green), 2 (Blue) है, ताकि प्रत्येक चैनल को स्वतंत्र रूप से ट्यून किया जा सके।

**Q: एक PSD में कई Levels Adjustment Layers को कैसे संभालूँ?**  
A: लूप प्रत्येक लेयर को प्रोसेस करता है; प्रत्येक मिलने वाला `LevelsLayer` को `if` ब्लॉक के भीतर कोड के अनुसार समायोजित किया जाएगा।

**Q: Levels के अलावा कंट्रास्ट सुधारने के अन्य तरीके हैं क्या?**  
A: Aspose.PSD Curves, Brightness/Contrast, और Histogram Equalization एडजस्टमेंट भी प्रदान करता है।

**Q: क्या मैं इस प्रक्रिया को PSD फ़ाइलों के फ़ोल्डर के लिए स्वचालित कर सकता हूँ?**  
A: पूरे वर्कफ़्लो को `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` लूप में रखें और प्रत्येक फ़ाइल को क्रमशः प्रोसेस करें।

**Q: अधिक दस्तावेज़ीकरण और समर्थन कहाँ मिल सकता है?**  
A: आधिकारिक रेफ़रेंस देखें ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) और कम्युनिटी फ़ोरम पर जाएँ ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34))।

## निष्कर्ष

**export PSD to PNG** वर्कफ़्लो को मास्टर करके और प्रोग्रामेटिकली **लेवल्स कैसे समायोजित करें** सीखकर, आप अपने Java वातावरण से बाहर निकले बिना इमेज क्वालिटी पर पूर्ण नियंत्रण प्राप्त कर लेते हैं। चाहे आप वेब के लिए एसेट्स तैयार कर रहे हों, डिज़ाइन पाइपलाइन को स्वचालित कर रहे हों, या बैच प्रोसेसर बना रहे हों, Aspose.PSD for Java काम को सरल और विश्वसनीय बनाता है।

---

**अंतिम अद्यतन:** 2026-04-05  
**परीक्षित संस्करण:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}