---
date: 2026-06-18
description: Aspose.PSD for Java का उपयोग करके शैडो रंग को बदलना और शैडो इफ़ेक्ट को
  कस्टमाइज़ करना सीखें। इस step‑by‑step शैडो इफ़ेक्ट ट्यूटोरियल का पालन करें।
keywords:
- change shadow color java
- Aspose.PSD shadow effect
- Java PSD manipulation
linktitle: Shadow Effect का समर्थन
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  headline: Change Shadow Color Java with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  name: Change Shadow Color Java with Aspose.PSD for Java
  steps:
  - name: Load the PSD Image
    text: 'First, load the source PSD while enabling the loading of effect resources:'
  - name: Retrieve the Existing Drop Shadow Effect
    text: 'Locate the shadow effect on the desired layer (in this example, the second
      layer):'
  - name: Verify the Default Settings (Optional)
    text: 'Running these assertions helps you understand the original values before
      you modify them:'
  - name: '**Change Shadow Color** and Customize Other Properties'
    text: Now we actually **change shadow color** to green, adjust opacity, distance,
      size, and other attributes. This demonstrates the **customize shadow effect**
      capabilities of Aspose.PSD. The `setOpacity(byte)` method sets the shadow's
      opacity level (0‑255).
  - name: Save the Modified Image
    text: 'Finally, write the updated PSD back to disk using the `save` method of
      `PsdImage`:'
  type: HowTo
- questions:
  - answer: Absolutely! Aspose.PSD for Java is a powerful library designed for professional
      graphic design tasks.
    question: Is Aspose.PSD for Java suitable for professional graphic design projects?
  - answer: Yes, Aspose.PSD for Java is a commercial product. You can purchase it
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial applications?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Refer to the comprehensive documentation [here](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Join the community forum [here](https://forum.aspose.com/c/psd/34) for
      any support queries.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ Java में शैडो रंग बदलें
url: /hi/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में शैडो रंग बदलें Aspose.PSD for Java के साथ

## परिचय

अपने ग्राफिक्स में गहराई जोड़ने के लिए अक्सर **शैडो रंग बदलना** आवश्यक होता है ताकि डिज़ाइन के मूड से मेल खाए। Aspose.PSD for Java के साथ आप आसानी से ड्रॉप‑शैडो इफ़ेक्ट जोड़ या संशोधित कर सकते हैं, अपारदर्शिता नियंत्रित कर सकते हैं, और अन्य पैरामीटर को बारीकी से समायोजित कर सकते हैं—सभी Java कोड से। इस **शैडो इफ़ेक्ट ट्यूटोरियल** में हम PSD लोड करने, मौजूदा शैडो पढ़ने, उसके रंग, अपारदर्शिता, दूरी को कस्टमाइज़ करने, और अंत में अपडेटेड फ़ाइल को सहेजने की प्रक्रिया दिखाएंगे। यह गाइड बिल्कुल बताता है कि **change shadow color java** को पुनरुत्पादक तरीके से कैसे किया जाए।

## त्वरित उत्तर
- **“change shadow color” क्या दर्शाता है?** यह PSD लेयर पर लागू DropShadowEffect की color प्रॉपर्टी को अपडेट करता है।  
- **कौन‑सी लाइब्रेरी इसे सपोर्ट करती है?** Aspose.PSD for Java शैडो इफ़ेक्ट्स के लिए पूर्ण समर्थन प्रदान करती है।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं शैडो अपारदर्शिता सेट कर सकता हूँ?** हाँ – पारदर्शिता (0‑255) निर्धारित करने के लिए `setOpacity(byte)` का उपयोग करें।  
- **क्या कोड Java 8+ के साथ संगत है?** बिल्कुल, API Java 8 और बाद के संस्करणों को लक्षित करती है।

## PSD फ़ाइलों में “change shadow color” क्या है?

शैडो रंग बदलने से लेयर के पीछे दिखाई देने वाले ड्रॉप शैडो की दृश्य रंगत बदलती है। यह समायोजन डिज़ाइनरों को विभिन्न प्रकाश स्थितियों का सिमुलेशन करने, शैडो को ब्रांड के रंग पैलेट के साथ संरेखित करने, और रचनाओं में कलात्मक आकर्षण जोड़ने की अनुमति देता है। रंगत बदलकर आप शैडो को गर्म, ठंडा या किसी विशिष्ट रंग योजना के साथ पूरी तरह मेल करवा सकते हैं, जिससे समग्र दृश्य प्रभाव बढ़ता है।

## शैडो इफ़ेक्ट्स को कस्टमाइज़ करने के लिए Aspose.PSD for Java क्यों उपयोग करें?

Aspose.PSD for Java **100+ इमेज फ़ॉर्मैट्स** को संरक्षित करता है और **2 GB** तक की PSD फ़ाइलों को पूरी दस्तावेज़ को मेमोरी में लोड किए बिना प्रोसेस कर सकता है, जिससे एंटरप्राइज़‑ग्रेड प्रदर्शन मिलता है। यह लाइब्रेरी आपको प्रत्येक शैडो एट्रिब्यूट—color, opacity, distance, angle, spread, और noise—पर पूर्ण नियंत्रण देती है, बिना Photoshop स्थापित किए। यह Windows, Linux, और macOS JVMs पर चलता है, जिससे यह स्वचालित ग्राफिक पाइपलाइन के लिए सबसे भरोसेमंद विकल्प बनता है।

## पूर्वापेक्षाएँ

- Java प्रोग्रामिंग का बुनियादी ज्ञान।  
- Aspose.PSD for Java स्थापित है। आप इसे [यहाँ](https://releases.aspose.com/psd/java/) डाउनलोड कर सकते हैं।  

## पैकेज इम्पोर्ट करें

शुरू करने से पहले, आवश्यक क्लासेस इम्पोर्ट करें ताकि आप इमेज और शैडो इफ़ेक्ट्स के साथ काम कर सकें:

`Color` क्लास API में उपयोग किए जाने वाले रंग मान को दर्शाती है।  
`Image` क्लास सभी इमेज ऑब्जेक्ट्स का बेस टाइप है।  
`PsdImage` क्लास PSD फ़ाइलों के लिए विशिष्ट कार्यक्षमता प्रदान करती है।  
`PsdLoadOptions` क्लास आपको PSD फ़ाइलों को लोड करने के विकल्प निर्दिष्ट करने देता है, जैसे इफ़ेक्ट रिसोर्सेज को सक्षम करना।  
`DropShadowEffect` क्लास PSD लेयर पर लागू ड्रॉप‑शैडो फ़िल्टर को दर्शाती है और आपको उसकी सभी समायोज्य प्रॉपर्टीज़ तक पहुंच देती है।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## चरण‑दर‑चरण गाइड

### चरण 1: PSD इमेज लोड करें

पहले, इफ़ेक्ट रिसोर्सेज को लोड करने की सुविधा के साथ स्रोत PSD लोड करें:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### चरण 2: मौजूदा ड्रॉप शैडो इफ़ेक्ट प्राप्त करें

वांछित लेयर पर शैडो इफ़ेक्ट खोजें (इस उदाहरण में, दूसरी लेयर):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### चरण 3: डिफ़ॉल्ट सेटिंग्स सत्यापित करें (वैकल्पिक)

इन एसेर्शन को चलाने से आप संशोधित करने से पहले मूल मानों को समझ सकते हैं:

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

### चरण 4: **शैडो रंग बदलें** और अन्य प्रॉपर्टीज़ को कस्टमाइज़ करें

अब हम वास्तव में **शैडो रंग बदलते** हैं, इसे हरे रंग में बदलते हैं, अपारदर्शिता, दूरी, आकार और अन्य गुणों को समायोजित करते हैं। यह Aspose.PSD की **शैडो इफ़ेक्ट कस्टमाइज़** करने की क्षमता को दर्शाता है। `setOpacity(byte)` मेथड शैडो की अपारदर्शिता स्तर (0‑255) सेट करता है।  

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

अंत में, `PsdImage` के `save` मेथड का उपयोग करके अपडेटेड PSD को डिस्क पर लिखें:

```java
im.save(psdPathAfterChange);
```

## सामान्य समस्याएँ और सुझाव

- **इफ़ेक्ट्स प्राप्त करते समय NullPointerException** – सुनिश्चित करें कि `setLoadEffectsResource(true)` कॉल किया गया है; अन्यथा इफ़ेक्ट्स लोड नहीं होते।  
- **रंग नहीं बदल रहा** – जाँचें कि आप सही लेयर इंडेक्स (`im.getLayers()[1]` इस उदाहरण में) को संपादित कर रहे हैं।  
- **अपारदर्शिता अपरिवर्तित दिख रही है** – याद रखें कि अपारदर्शिता एक बाइट (0‑255) है। `(byte)` में कास्ट करना आवश्यक है।  

## निष्कर्ष

इन चरणों का पालन करके आप **शैडो रंग बदल सकते** हैं, **शैडो अपारदर्शिता सेट कर सकते** हैं, और किसी भी PSD फ़ाइल में पूरी तरह से **शैडो इफ़ेक्ट** पैरामीटर कस्टमाइज़ कर सकते हैं Aspose.PSD for Java का उपयोग करके। यह आपको मैन्युअल Photoshop कार्य के बिना प्रोग्रामेटिक रूप से समृद्ध ग्राफिक्स बनाने की शक्ति देता है, जो स्वचालित डिज़ाइन पाइपलाइन और बैच प्रोसेसिंग के लिए आदर्श है।

## अक्सर पूछे जाने वाले प्रश्न

**प्र: क्या Aspose.PSD for Java पेशेवर ग्राफिक डिज़ाइन प्रोजेक्ट्स के लिए उपयुक्त है?**  
उ: बिल्कुल! Aspose.PSD for Java एक शक्तिशाली लाइब्रेरी है जो पेशेवर ग्राफिक डिज़ाइन कार्यों के लिए डिज़ाइन की गई है।

**प्र: क्या मैं Aspose.PSD for Java को व्यावसायिक एप्लिकेशन में उपयोग कर सकता हूँ?**  
उ: हाँ, Aspose.PSD for Java एक व्यावसायिक उत्पाद है। आप इसे [यहाँ](https://purchase.aspose.com/buy) खरीद सकते हैं।

**प्र: क्या कोई मुफ्त ट्रायल उपलब्ध है?**  
उ: हाँ, आप एक मुफ्त ट्रायल संस्करण [यहाँ](https://releases.aspose.com/) देख सकते हैं।

**प्र: विस्तृत दस्तावेज़ीकरण कहाँ मिल सकता है?**  
उ: व्यापक दस्तावेज़ीकरण के लिए [यहाँ](https://reference.aspose.com/psd/java/) देखें।

**प्र: Aspose.PSD for Java के लिए समर्थन कैसे प्राप्त करूँ?**  
उ: किसी भी समर्थन प्रश्न के लिए कम्युनिटी फ़ोरम [यहाँ](https://forum.aspose.com/c/psd/34) में शामिल हों।

---

**अंतिम अपडेट:** 2026-06-18  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.10  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Java इमेज मैनिपुलेशन - रनटाइम में इफ़ेक्ट्स जोड़ें Aspose.PSD for Java के साथ](/psd/java/advanced-techniques/add-effects-runtime/)
- [PSD को PNG के रूप में सहेजें और Aspose.PSD for Java में रेंडरिंग ड्रॉप शैडो लागू करें](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Java में इमेज ब्लर करें Aspose.PSD – ब्लर इफ़ेक्ट जोड़ें](/psd/java/advanced-techniques/blur-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}