---
date: 2026-06-28
description: जावा में overlay opacity सेट करना, color overlay लागू करना, और Aspose.PSD
  for Java का उपयोग करके overlay color को customize करना सीखें। ready‑to‑run examples
  के साथ Step‑by‑run guide।
keywords:
- set overlay opacity java
- Aspose.PSD overlay effect
- Java PSD color overlay
linktitle: Color Overlay इफ़ेक्ट लागू करें
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to set overlay opacity java, apply a color overlay, and customize
    overlay color using Aspose.PSD for Java. Step‑by‑run guide with ready‑to‑run examples.
  headline: How to Set Overlay Opacity Java with Aspose.PSD
  type: TechArticle
- description: Learn how to set overlay opacity java, apply a color overlay, and customize
    overlay color using Aspose.PSD for Java. Step‑by‑run guide with ready‑to‑run examples.
  name: How to Set Overlay Opacity Java with Aspose.PSD
  steps:
  - name: Set Your Document Directory
    text: The `File` class represents a file system path. Replace **Your Document
      Directory** with the absolute path where your PSD files reside.
  - name: Load PSD File with Effects
    text: '`LoadOptions` tells Aspose.PSD how to read the file. Setting `setLoadEffectsResource(true)`
      ensures existing layer effects, including any colour overlay, are loaded and
      become accessible.'
  - name: Access Color Overlay Effect
    text: '`Layer` is Aspose.PSD’s representation of a PSD layer. `ColorOverlayEffect`
      is the specific effect object that controls colour overlay properties. Here
      we retrieve the first effect of the second layer (index 1). Adjust the indices
      if your PSD structure differs.'
  - name: Customize Overlay Color and Set Overlay Opacity
    text: The `ColorOverlayEffect` class represents a color overlay effect applied
      to a PSD layer. - **Colour** – Use any static colour from `java.awt.Color` or
      create a custom one with `new Color(r, g, b)`. - **Opacity** – The opacity byte
      ranges from 0 (fully transparent) to 255 (fully opaque). In this exam
  - name: Save the Modified PSD File
    text: '`save` writes the updated document back to disk. The edited file, *ColorOverlayChanged.psd*,
      now contains the new overlay colour and opacity.'
  type: HowTo
- questions:
  - answer: No, a layer can have only one `ColorOverlayEffect`. To simulate multiple
      colours, duplicate the layer and apply separate overlays.
    question: Can I apply multiple overlays to a single layer?
  - answer: Yes, it works with Eclipse, IntelliJ IDEA, NetBeans, and any IDE that
      supports Maven or Gradle.
    question: Is Aspose.PSD compatible with different Java IDEs?
  - answer: Yes, you can use it in both personal and commercial applications. Visit
      [here](https://purchase.aspose.com/buy) for licensing details.
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) for community
      help or purchase a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority support.
    question: How can I get support for Aspose.PSD?
  - answer: Yes, explore the [free trial](https://releases.aspose.com/) version before
      deciding.
    question: Are there free trial options available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD के साथ जावा में overlay opacity कैसे सेट करें
url: /hi/java/image-editing/color-overlay-effect/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD के साथ Java में Overlay Opacity सेट करना

## परिचय

Aspose.PSD for Java का उपयोग करके ग्राफिक डिज़ाइन और इमेज मैनिपुलेशन की दुनिया में आपका स्वागत है! इस ट्यूटोरियल में आप **how to set overlay opacity java** सीखेंगे, PSD लेयर पर एक कलर ओवरले लागू करेंगे, और ओवरले रंग को कस्टमाइज़ करेंगे। चाहे आप बैच‑प्रोसेसिंग टूल बना रहे हों या डिज़ाइन में ब्रांड रंग की एक झलक जोड़ रहे हों, नीचे दिए गए चरण आपको आवश्यक सभी चीज़ों के माध्यम से मार्गदर्शन करेंगे, प्रीरेक्विज़िट्स से लेकर अंतिम फ़ाइल को सेव करने तक।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी उपयोग की गई है?** Aspose.PSD for Java  
- **मुख्य लक्ष्य?** Set overlay opacity java, apply a colour overlay, and save the edited PSD  
- **पूर्वापेक्षाएँ?** Java 8+, Aspose.PSD for Java, a PSD file with at least one layer  
- **आम कार्यान्वयन समय?** 10‑15 minutes for a basic overlay  
- **क्या मैं बाद में ओवरले रंग बदल सकता हूँ?** Yes – modify the `ColorOverlayEffect` properties and re‑save  

## set overlay opacity java क्या है?
`setOpacity(byte)` मेथड ओवरले की ट्रांसपेरेंसी लेवल सेट करता है। “set overlay opacity java” वाक्यांश PSD लेयर पर कलर‑ओवरले इफ़ेक्ट की अपारदर्शिता मान (0‑255) को Java कोड के माध्यम से समायोजित करने को दर्शाता है। Aspose.PSD में आप `ColorOverlayEffect.setOpacity(byte)` मेथड के ज़रिए अपारदर्शिता को नियंत्रित करते हैं, जो सीधे ओवरले की पारदर्शिता या ठोसता को प्रभावित करता है।

## ओवरले ऑपरेशन्स के लिए Aspose.PSD क्यों उपयोग करें?
Aspose.PSD **100 % PSD fidelity** को बनाए रखता है और **50+ इनपुट और आउटपुट फॉर्मेट** (जैसे PSD, PNG, JPEG, TIFF, और BMP) को सपोर्ट करता है। यह **500 MB** तक की फ़ाइलों को पूरी डॉक्यूमेंट को मेमोरी में लोड किए बिना प्रोसेस करता है, जिससे यह सर्वर‑साइड ऑटोमेशन के लिए आदर्श बनता है। Adobe Photoshop की कोई इंस्टॉलेशन आवश्यक नहीं है, और वही Java कोड Windows, Linux, और macOS पर चलता है।

## पूर्वापेक्षाएँ

- **Java Development Environment** – JDK 8 या उससे ऊपर इंस्टॉल हो।  
- **Aspose.PSD Library** – Aspose.PSD लाइब्रेरी for Java को [here](https://releases.aspose.com/psd/java/) से डाउनलोड और इंस्टॉल करें।  
- **PSD Document** – एक PSD फ़ाइल (जैसे *ColorOverlay.psd*) जिसमें कम से कम एक लेयर हो जहाँ आप ओवरले जोड़ना चाहते हैं।  

## पैकेज इम्पोर्ट करें

अपने Java प्रोजेक्ट में आवश्यक पैकेज इम्पोर्ट करें। इससे कंपाइलर उन क्लासेज़ को ढूँढ़ सकेगा जिनका आप उपयोग करेंगे।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## चरण‑दर‑चरण गाइड

### चरण 1: अपना डॉक्यूमेंट डायरेक्टरी सेट करें

`File` क्लास फ़ाइल सिस्टम पाथ को दर्शाती है।  
**Your Document Directory** को उस एब्सोल्यूट पाथ से बदलें जहाँ आपकी PSD फ़ाइलें स्थित हैं।

```java
String dataDir = "Your Document Directory";
```

### चरण 2: इफ़ेक्ट्स के साथ PSD फ़ाइल लोड करें

`LoadOptions` Aspose.PSD को फ़ाइल पढ़ने का तरीका बताता है। `setLoadEffectsResource(true)` सेट करने से मौजूदा लेयर इफ़ेक्ट्स, जिसमें कोई भी colour overlay शामिल है, लोड हो जाते हैं और एक्सेसिबल बन जाते हैं।

```java
String sourceFileName = dataDir + "ColorOverlay.psd";
String psdPathAfterChange = dataDir + "ColorOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### चरण 3: कलर ओवरले इफ़ेक्ट तक पहुँचें

`Layer` Aspose.PSD की PSD लेयर का प्रतिनिधित्व करता है। `ColorOverlayEffect` वह विशेष इफ़ेक्ट ऑब्जेक्ट है जो colour overlay प्रॉपर्टीज़ को नियंत्रित करता है।  
यहाँ हम दूसरे लेयर (इंडेक्स 1) के पहले इफ़ेक्ट को प्राप्त करते हैं। यदि आपका PSD स्ट्रक्चर अलग है तो इंडेक्स को समायोजित करें।

```java
com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect colorOverlay = (com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect)
        (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### चरण 4: ओवरले रंग को कस्टमाइज़ करें और ओवरले अपारदर्शिता सेट करें

`ColorOverlayEffect` क्लास PSD लेयर पर लागू एक color overlay इफ़ेक्ट को दर्शाती है।  
- **Colour** – `java.awt.Color` से कोई भी स्थिर रंग उपयोग करें या `new Color(r, g, b)` से कस्टम बनाएं।  
- **Opacity** – अपारदर्शिता बाइट 0 (पूरी तरह पारदर्शी) से 255 (पूरी तरह अपारदर्शी) तक होती है। इस उदाहरण में हमने इसे 50 % (`128`) पर सेट किया है।  

> **Pro tip:** **change PSD overlay colour** को डायनामिक रूप से करने के लिए, कॉन्फ़िगरेशन फ़ाइल से इच्छित हेक्स वैल्यू पढ़ें और `Color.fromArgb()` से कनवर्ट करें।

```java
colorOverlay.setColor(Color.getGreen());
colorOverlay.setOpacity((byte) 128);
```

### चरण 5: संशोधित PSD फ़ाइल को सेव करें

`save` अपडेटेड डॉक्यूमेंट को डिस्क पर लिखता है। संपादित फ़ाइल, *ColorOverlayChanged.psd*, अब नया ओवरले रंग और अपारदर्शिता रखती है।

```java
im.save(psdPathAfterChange);
```

## कैसे सेट करें overlay opacity java

`ColorOverlayEffect` क्लास PSD लेयर पर लागू एक color overlay इफ़ेक्ट को दर्शाती है। लक्ष्य PSD को लोड करें, इच्छित लेयर से `ColorOverlayEffect` प्राप्त करें, `setOpacity((byte)128)` (या 0‑255 के बीच कोई भी मान) कॉल करें, और फिर डॉक्यूमेंट को सेव करें। यह एक‑लाइन परिवर्तन ओवरले की ट्रांसपेरेंसी को तुरंत समायोजित करता है, बिना अन्य लेयर एट्रिब्यूट्स को प्रभावित किए।

## सामान्य उपयोग केस

- **Branding** – मार्केटिंग एसेट्स पर बड़े पैमाने पर कॉरपोरेट colour overlay लागू करें।  
- **Theming** – UI मॉकअप्स को लाइट और डार्क थीम्स के बीच डायनामिक रूप से स्विच करें।  
- **Proofing** – जाँचें कि विभिन्न ओवरले अपारदर्शिताएँ जटिल बैकग्राउंड पर टेक्स्ट की पठनीयता को कैसे प्रभावित करती हैं।  

## सामान्य समस्याएँ और समाधान

| Issue | Solution |
|-------|----------|
| **Overlay not visible** | Ensure `loadOptions.setLoadEffectsResource(true)` is set and that the target layer actually has a `ColorOverlayEffect`. |
| **Wrong layer index** | Use `psdImage.getLayers()` to inspect layer names and pick the correct index. |
| **Opacity appears too light/dark** | Adjust the byte value (0‑255). Remember that 255 is fully opaque. |
| **Colour not applied** | Verify you are using `colorOverlay.setColor()` with a valid `java.awt.Color` instance. |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं एक ही लेयर पर कई ओवरले लागू कर सकता हूँ?**  
A: नहीं, एक लेयर में केवल एक `ColorOverlayEffect` हो सकता है। कई रंगों का सिमुलेशन करने के लिए लेयर को डुप्लिकेट करें और अलग‑अलग ओवरले लागू करें।

**Q: क्या Aspose.PSD विभिन्न Java IDEs के साथ संगत है?**  
A: हाँ, यह Eclipse, IntelliJ IDEA, NetBeans, और किसी भी IDE के साथ काम करता है जो Maven या Gradle को सपोर्ट करता है।

**Q: क्या मैं Aspose.PSD को व्यावसायिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?**  
A: हाँ, आप इसे व्यक्तिगत और व्यावसायिक दोनों एप्लिकेशन में उपयोग कर सकते हैं। लाइसेंसिंग विवरण के लिए [here](https://purchase.aspose.com/buy) देखें।

**Q: Aspose.PSD के लिए सपोर्ट कैसे प्राप्त करूँ?**  
A: समुदाय सहायता के लिए [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) पर जाएँ या प्रायोरिटी सपोर्ट के लिए एक [temporary license](https://purchase.aspose.com/temporary-license/) खरीदें।

**Q: क्या मुफ्त ट्रायल विकल्प उपलब्ध हैं?**  
A: हाँ, निर्णय लेने से पहले [free trial](https://releases.aspose.com/) संस्करण को एक्सप्लोर करें।

---

**Last Updated:** 2026-06-28  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## संबंधित ट्यूटोरियल

- [Set Layer Opacity and Support Blend Modes in Aspose.PSD for Java](/psd/java/basic-image-operations/support-blend-modes/)
- [Set Fill Opacity for PSD Layers with Aspose.PSD Java](/psd/java/psd-image-modification-conversion/set-fill-opacity-psd-layers/)
- [Add Pattern Overlay Effects in Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}