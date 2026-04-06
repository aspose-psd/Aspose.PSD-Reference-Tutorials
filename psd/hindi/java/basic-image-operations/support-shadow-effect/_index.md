---
date: 2025-12-30
description: Aspose.PSD for Java का उपयोग करके शैडो रंग बदलना और शैडो इफ़ेक्ट को कस्टमाइज़
  करना सीखें। इस चरण‑दर‑चरण शैडो इफ़ेक्ट ट्यूटोरियल का पालन करें।
linktitle: Support Shadow Effect
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ छाया का रंग कैसे बदलें
url: /hi/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ शैडो रंग बदलें

## परिचय

अपने ग्राफिक्स में गहराई जोड़ने का अक्सर मतलब **शैडो रंग बदलना** होता है ताकि डिज़ाइन के मूड से मेल खाए। Aspose.PSD for Java के साथ आप आसानी से ड्रॉप शैडो इफ़ेक्ट जोड़ या संशोधित कर सकते हैं, अपारदर्शिता नियंत्रित कर सकते हैं, और अन्य पैरामीटर को बारीकी से समायोजित कर सकते हैं—सभी Java कोड से। इस **शैडो इफ़ेक्ट ट्यूटोरियल** में हम एक PSD लोड करने, मौजूदा शैडो पढ़ने, उसके रंग, अपारदर्शिता, दूरी को कस्टमाइज़ करने, और अंत में अपडेटेड फ़ाइल को सहेजने की प्रक्रिया दिखाएंगे।

## त्वरित उत्तर
- **“शैडो रंग बदलें” का क्या अर्थ है?** यह PSD लेयर पर लागू DropShadowEffect की color प्रॉपर्टी को अपडेट करता है।  
- **कौन सी लाइब्रेरी इसे सपोर्ट करती है?** Aspose.PSD for Java शैडो इफ़ेक्ट्स के लिए पूर्ण समर्थन प्रदान करती है।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं शैडो अपारदर्शिता सेट कर सकता हूँ?** हाँ – `setOpacity(byte)` का उपयोग करके पारदर्शिता (0‑255) निर्धारित करें।  
- **क्या कोड Java 8+ के साथ संगत है?** बिल्कुल, API Java 8 और उसके बाद के संस्करणों को लक्षित करती है।

## PSD फ़ाइलों में “शैडो रंग बदलें” क्या है?

शैडो रंग बदलने से लेयर के पीछे दिखाई देने वाले ड्रॉप शैडो का दृश्य रंग बदलता है। यह वास्तविक प्रकाश बनाना, ब्रांड रंगों से मेल खाना, या बस कलात्मक आकर्षण जोड़ने के लिए उपयोगी है।

## शैडो इफ़ेक्ट्स को कस्टमाइज़ करने के लिए Aspose.PSD for Java क्यों उपयोग करें?

- **पूर्ण PSD सटीकता** – सभी लेयर इफ़ेक्ट्स, शैडो सहित, संरक्षित रहते हैं।  
- **Photoshop की आवश्यकता नहीं** – किसी भी सर्वर पर प्रोग्रामेटिक रूप से फ़ाइलों को बदलें।  
- **सूक्ष्म नियंत्रण** – रंग, अपारदर्शिता, दूरी, कोण, फैलाव, और शोर को समायोजित करें।  
- **क्रॉस‑प्लेटफ़ॉर्म** – Windows, Linux, और macOS JVMs पर काम करता है।

## पूर्वापेक्षाएँ

- Java प्रोग्रामिंग का बुनियादी ज्ञान।  
- Aspose.PSD for Java स्थापित है। आप इसे [यहाँ](https://releases.aspose.com/psd/java/) डाउनलोड कर सकते हैं।

## पैकेज आयात करें

शुरू करने से पहले, आवश्यक क्लासेस आयात करें ताकि आप इमेज और शैडो इफ़ेक्ट्स के साथ काम कर सकें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## कदम‑दर‑कदम गाइड

### चरण 1: PSD इमेज लोड करें

पहले, इफ़ेक्ट संसाधनों को लोड करने की सुविधा के साथ स्रोत PSD लोड करें:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### चरण 2: मौजूदा ड्रॉप शैडो इफ़ेक्ट प्राप्त करें

इच्छित लेयर पर शैडो इफ़ेक्ट खोजें (इस उदाहरण में, दूसरी लेयर):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### चरण 3: डिफ़ॉल्ट सेटिंग्स सत्यापित करें (वैकल्पिक)

इन असर्शन को चलाने से आपको संशोधित करने से पहले मूल मान समझने में मदद मिलती है:

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

### चरण 4: **शैडो रंग बदलें** और अन्य गुण कस्टमाइज़ करें

अब हम वास्तव में **शैडो रंग को हरा** बदलते हैं, अपारदर्शिता, दूरी, आकार, और अन्य गुण समायोजित करते हैं। यह Aspose.PSD की **शैडो इफ़ेक्ट कस्टमाइज़** क्षमताओं को दर्शाता है:

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### चरण 5: संशोधित इमेज सहेजें

अंत में, अपडेटेड PSD को डिस्क पर लिखें:

```java
im.save(psdPathAfterChange);
```

## सामान्य समस्याएँ और सुझाव

- **इफ़ेक्ट्स प्राप्त करते समय NullPointerException** – सुनिश्चित करें कि `setLoadEffectsResource(true)` कॉल किया गया है; अन्यथा इफ़ेक्ट्स लोड नहीं होते।  
- **रंग नहीं बदल रहा** – पुष्टि करें कि आप सही लेयर इंडेक्स (`im.getLayers()[1]` इस उदाहरण में) को संपादित कर रहे हैं।  
- **अपारदर्शिता अपरिवर्तित लग रही है** – याद रखें कि अपारदर्शिता एक बाइट (0‑255) है। `(byte)` में कास्ट करना आवश्यक है।  

## निष्कर्ष

इन चरणों का पालन करके आप Aspose.PSD for Java का उपयोग करके किसी भी PSD फ़ाइल में **शैडो रंग बदल सकते हैं**, **शैडो अपारदर्शिता सेट कर सकते हैं**, और पूरी तरह से **शैडो इफ़ेक्ट** पैरामीटर कस्टमाइज़ कर सकते हैं। यह आपको मैन्युअल Photoshop कार्य के बिना प्रोग्रामेटिक रूप से अधिक समृद्ध ग्राफिक्स बनाने में सक्षम बनाता है।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या Aspose.PSD for Java पेशेवर ग्राफिक डिज़ाइन प्रोजेक्ट्स के लिए उपयुक्त है?**  
**उत्तर:** बिल्कुल! Aspose.PSD for Java एक शक्तिशाली लाइब्रेरी है जो पेशेवर ग्राफिक डिज़ाइन कार्यों के लिए डिज़ाइन की गई है।

**प्रश्न: क्या मैं Aspose.PSD for Java को व्यावसायिक एप्लिकेशन्स में उपयोग कर सकता हूँ?**  
**उत्तर:** हाँ, Aspose.PSD for Java एक व्यावसायिक उत्पाद है। आप इसे [यहाँ](https://purchase.aspose.com/buy) खरीद सकते हैं।

**प्रश्न: क्या कोई मुफ्त ट्रायल उपलब्ध है?**  
**उत्तर:** हाँ, आप एक मुफ्त ट्रायल संस्करण [यहाँ](https://releases.aspose.com/) देख सकते हैं।

**प्रश्न: विस्तृत दस्तावेज़ीकरण कहाँ मिल सकता है?**  
**उत्तर:** व्यापक दस्तावेज़ीकरण के लिए [यहाँ](https://reference.aspose.com/psd/java/) देखें।

**प्रश्न: Aspose.PSD for Java के लिए समर्थन कैसे प्राप्त करूँ?**  
**उत्तर:** किसी भी समर्थन प्रश्न के लिए समुदाय फ़ोरम [यहाँ](https://forum.aspose.com/c/psd/34) में शामिल हों।

---

**अंतिम अपडेट:** 2025-12-30  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.10  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}