---
date: 2026-04-03
description: Aspose.PSD for Java का उपयोग करके स्ट्रोक इफ़ेक्ट और रंग भराव के साथ
  PSD को PNG के रूप में कैसे सहेजें, सीखें। यह चरण‑दर‑चरण गाइड तेज़ी से PSD को PNG
  में निर्यात करना दिखाता है।
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: स्टोक इफ़ेक्ट के साथ PSD को PNG के रूप में सहेजें – जावा
second_title: Aspose.PSD Java API
title: स्ट्रोक इफ़ेक्ट के साथ PSD को PNG के रूप में सहेजें – जावा
url: /hi/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD को PNG के रूप में सहेजें स्ट्रोक इफ़ेक्ट और रंग भराव के साथ – Java

## परिचय

इस मार्गदर्शिका में, आप सीखेंगे कि Aspose.PSD for Java का उपयोग करके स्ट्रोक इफ़ेक्ट और रंग भराव के साथ **PSD को PNG के रूप में सहेजना** कैसे है। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, यह चरण‑दर‑चरण ट्यूटोरियल काम को आसान बना देगा। हम आपके पर्यावरण की सेटअप से लेकर अंतिम छवि को निर्यात करने तक सब कुछ कवर करेंगे, ताकि आप अपने प्रोजेक्ट में जल्दी से **PSD को PNG में निर्यात** कर सकें।

## त्वरित उत्तर

- **यह ट्यूटोरियल क्या हासिल करता है?** यह दिखाता है कि कैसे एक कस्टमाइज़ेबल स्ट्रोक इफ़ेक्ट लागू करने के बाद PSD फ़ाइल को PNG के रूप में सहेजा जाए।  
- **कौन सी लाइब्रेरी उपयोग की गई है?** Aspose.PSD for Java।  
- **क्या मुझे लाइसेंस चाहिए?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **क्या मैं स्ट्रोक का रंग बदल सकता हूँ?** हाँ – आप `ColorFillSettings` के माध्यम से कोई भी रंग सेट कर सकते हैं।  
- **क्या बैच प्रोसेसिंग संभव है?** बिल्कुल – कई PSD फ़ाइलों को प्रोसेस करने के लिए कोड को लूप में रैप करें।

## “PSD को PNG के रूप में सहेजना” क्या है?

PSD को PNG के रूप में सहेजना मतलब Photoshop की मूल लेयर्ड फ़ाइल को एक फ्लैट, वेब‑फ्रेंडली इमेज फ़ॉर्मेट में बदलना है, जबकि दृश्य गुणवत्ता को बनाए रखा जाता है। यह तब उपयोगी होता है जब आपको वेबसाइटों, मोबाइल ऐप्स, या किसी भी प्लेटफ़ॉर्म पर PSD सामग्री दिखानी हो जो सीधे PSD फ़ाइलों का समर्थन नहीं करता।

## रंग भराव के साथ स्ट्रोक इफ़ेक्ट क्यों लागू करें?

स्ट्रोक लेयर सामग्री के चारों ओर एक स्पष्ट आउटलाइन जोड़ता है, जिससे ग्राफ़िक्स जटिल पृष्ठभूमियों के खिलाफ उभरे होते हैं। इसे कस्टम फ़िल रंग के साथ मिलाकर आप इमेज को ब्रांड कर सकते हैं, UI तत्वों को हाइलाइट कर सकते हैं, या फ़ोटोशॉप छोड़े बिना आकर्षक थंबनेल बना सकते हैं।

## पूर्वापेक्षाएँ

1. **Java Development Kit (JDK) 8+** – सुनिश्चित करें कि `java` आपके PATH में है।  
2. **Aspose.PSD for Java** – [website](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी एडिटर जो आप पसंद करते हैं।  
4. **Sample PSD** – एक फ़ाइल जिसमें पहले से ही स्ट्रोक इफ़ेक्ट हो (या फ़ोटोशॉप में जोड़ें)।  
5. **Basic Java knowledge** – आप कुछ लाइनों का कोड लिखेंगे, लेकिन कुछ भी उन्नत नहीं।  

इन सबको तैयार करने के बाद, हम कोडिंग शुरू कर सकते हैं।

## पैकेज आयात करें

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

ये इम्पोर्ट्स उन सभी क्लासों को लाते हैं जो PSD को लोड करने, उसके स्ट्रोक को संशोधित करने, और PSD तथा PNG दोनों आउटपुट को सहेजने के लिए आवश्यक हैं।

## स्ट्रोक इफ़ेक्ट के साथ PSD को PNG के रूप में कैसे सहेजें

### चरण 1: PSD फ़ाइल लोड करें

पहले, उस फ़ोल्डर की ओर इशारा करें जिसमें आपका स्रोत PSD है।

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` को अपने मशीन पर वास्तविक पथ से बदलें।

अब फ़ाइल को लोड करें जबकि किसी भी मौजूदा इफ़ेक्ट संसाधनों को संरक्षित रखें:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### चरण 2: स्ट्रोक रंग सेट करें (और वैकल्पिक रूप से चौड़ाई अनुकूलित करें)

नीचे दिया गया लूप प्रत्येक लेयर के माध्यम से चलता है, पहला `StrokeEffect` लेता है, और उसके फ़िल रंग को बदलता है। यदि आपको **स्ट्रोक की चौड़ाई अनुकूलित** करनी है तो आप `StrokeEffect` ऑब्जेक्ट पर `setWidth` या `setPosition` भी समायोजित कर सकते हैं।

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **प्रो टिप:** `Color.getDeepPink()` सिर्फ एक उदाहरण है। कस्टम RGB मानों के लिए `new Color(r, g, b)` का उपयोग करें।

### चरण 3: संशोधित PSD सहेजें (वैकल्पिक)

यदि आप अपडेटेड स्ट्रोक के साथ PSD संस्करण रखना चाहते हैं, तो इसे इस तरह सहेजें:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### चरण 4: इमेज को PNG के रूप में निर्यात करें (मुख्य “PSD को PNG के रूप में सहेजना” चरण)

अंत में, संपादित PSD को एक PNG फ़ाइल में बदलें जो वेब उपयोग के लिए तैयार हो:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

PNG में वह डीप‑पिंक स्ट्रोक बना रहता है जो आपने पहले सेट किया था, और `TruecolorWithAlpha` विकल्प सुनिश्चित करता है कि ट्रांसपैरेंसी संरक्षित रहे।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|-----|
| **`ArrayIndexOutOfBoundsException`** | लेयर में कोई इफ़ेक्ट नहीं है या पहला इफ़ेक्ट `StrokeEffect` नहीं है। | जाँचें कि लेयर में वास्तव में स्ट्रोक है या सही प्रकार खोजने के लिए `getEffects()` के माध्यम से इटरेट करें। |
| **रंग नहीं बदल रहा** | आप मूल सेटिंग्स की बजाय सेटिंग्स की कॉपी को संपादित कर रहे हो सकते हैं। | सुनिश्चित करें कि आप `effect.getFillSettings()` से सीधे `ColorFillSettings` को कास्ट कर रहे हैं। |
| **PNG खाली दिख रहा है** | PSD को लेयर को रास्टराइज़ किए बिना लोड किया गया था। | सभी संशोधनों के बाद `im.save(..., new PngOptions())` कॉल करें; बदलावों से पहले मूल `im` को सहेजने से बचें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.PSD for Java का उपयोग करके एक ही लेयर पर कई इफ़ेक्ट लागू कर सकता हूँ?**  
A: हाँ, आप लेयर के ब्लेंडिंग विकल्पों तक पहुँच सकते हैं और आवश्यकतानुसार कई इफ़ेक्ट जोड़ सकते हैं, जिसमें शैडोज़, ग्लो, और स्ट्रोक शामिल हैं।

**Q: क्या PSD फ़ाइलों के बैच के लिए प्रक्रिया को स्वचालित करना संभव है?**  
A: बिल्कुल। लोडिंग, इफ़ेक्ट‑आवेदन, और सहेजने की लॉजिक को एक `for‑each` लूप में रैप करें जो डायरेक्टरी में फ़ाइलों पर इटरेट करता है।

**Q: मैं PSD फ़ाइल में किए गए बदलावों को कैसे वापस ले सकता हूँ?**  
A: किसी भी संशोधन को सहेजने से पहले मूल फ़ाइल को पुनः लोड करें; Aspose.PSD अनडू स्टैक प्रदान नहीं करता।

**Q: क्या मैं स्ट्रोक की चौड़ाई और स्थिति को कस्टमाइज़ कर सकता हूँ?**  
A: हाँ। मोटाई और प्लेसमेंट (भीतर, बाहर, या केंद्रित) को नियंत्रित करने के लिए `effect.setWidth(float)` और `effect.setPosition(StrokeEffect.Position)` का उपयोग करें।

**Q: क्या Aspose.PSD for Java लाइब्रेरी मुफ्त में उपयोग की जा सकती है?**  
A: मूल्यांकन के लिए एक मुफ्त ट्रायल उपलब्ध है। पूरी कार्यक्षमता के लिए खरीदा गया लाइसेंस आवश्यक है। विवरण के लिए [buy options](https://purchase.aspose.com/buy) देखें।

---

**अंतिम अपडेट:** 2026-04-03  
**परीक्षित संस्करण:** Aspose.PSD 24.12 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}