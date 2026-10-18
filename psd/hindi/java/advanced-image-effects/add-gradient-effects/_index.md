---
date: 2026-10-18
description: Aspose.PSD का उपयोग करके Java इमेज में radial gradient इफ़ेक्ट बनाना
  सीखें। सहज एकीकरण के लिए इस step‑by‑step गाइड का पालन करें।
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: ग्रेडिएंट इफ़ेक्ट जोड़ें
og_description: Aspose.PSD का उपयोग करके radial gradient java इफ़ेक्ट बनाना सीखें।
  यह ट्यूटोरियल दिखाता है कि कैसे gradient ओवरले जोड़ें, अनुकूलित करें और मिनटों में
  सहेजें।
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Aspose.PSD के साथ radial gradient java बनाएं – step‑by‑step गाइड
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Aspose.PSD for Java में radial gradient इफ़ेक्ट कैसे बनाएं
url: /hi/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java में रेडियल ग्रेडिएंट इफ़ेक्ट कैसे बनाएं

## परिचय

इस गाइड में आप Aspose.PSD लाइब्रेरी का उपयोग करके **create radial gradient java** इफ़ेक्ट बनाना सीखेंगे। रेडियल ग्रेडिएंट आपके PSD लेयर्स में गहराई, फोकस या हल्की चमक जोड़ने के लिए आदर्श हैं, बिना Photoshop खोले। ट्यूटोरियल के अंत तक आप PSD लोड कर सकेंगे, ग्रेडिएंट ओवरले लागू कर सकेंगे, उसकी प्रॉपर्टीज़ को समायोजित कर सकेंगे, और परिणाम को सहेज सकेंगे — सभी Java कोड से।

## त्वरित उत्तर

- **मैं क्या हासिल कर सकता हूँ?** PSD लेयर्स पर रेडियल ग्रेडिएंट ओवरले को जोड़ना, संपादित करना और मिश्रित करना।  
- **कौन सी लाइब्रेरी आवश्यक है?** Aspose.PSD for Java (latest version)।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **कार्यान्वयन में कितना समय लगेगा?** बुनियादी रेडियल ग्रेडिएंट ओवरले के लिए लगभग 10‑15 मिनट।  
- **क्या यह Java 8+ के साथ संगत है?** हां, API Java 8 और नए रनटाइम्स को सपोर्ट करता है।

## पूर्वापेक्षाएँ

ट्यूटोरियल में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1. **Aspose.PSD for Java लाइब्रेरी** – सुनिश्चित करें कि आपने Aspose.PSD for Java लाइब्रेरी डाउनलोड और इंस्टॉल की है। आप लाइब्रेरी और उसकी दस्तावेज़ीकरण [Aspose.PSD Java दस्तावेज़ पृष्ठ](https://reference.aspose.com/psd/java/) पर पा सकते हैं।  
2. **Java विकास पर्यावरण** – अपने मशीन पर Java विकास पर्यावरण सेट करें (JDK 8 या उच्चतर, आपका पसंदीदा IDE)।  
3. **नवीनतम Aspose.PSD रिलीज़** – नवीनतम संस्करण [Aspose रिलीज़ पृष्ठ](https://releases.aspose.com/) से डाउनलोड करें।  
4. **समर्थन संसाधन** – यदि आपको समस्याएँ आती हैं, तो [Aspose.PSD सपोर्ट फ़ोरम](https://forum.aspose.com/c/psd/34) देखें।  
5. **लाइसेंस खरीद** – जब आप उत्पादन के लिए तैयार हों, तो [खरीद पृष्ठ](https://purchase.aspose.com/buy) से लाइसेंस प्राप्त करें।

अब जब आपके पास सब कुछ सेट हो गया है, चलिए चरण‑दर‑चरण गाइड के साथ आगे बढ़ते हैं।

## ग्रेडिएंट ओवरले इफ़ेक्ट क्या है?

एक ग्रेडिएंट ओवरले इफ़ेक्ट लेयर के चयनित क्षेत्र में दो या अधिक रंगों के बीच एक सुगम परिवर्तन पेंट करता है। Photoshop में यह इफ़ेक्ट मिश्रित, रंगित और स्थित किया जा सकता है ताकि परिष्कृत दृश्य डिज़ाइन बन सकें। `GradientOverlayEffect` क्लास Aspose.PSD का उस लेयर‑स्टाइल का प्रतिनिधित्व है, जो रंग स्टॉप्स, अपारदर्शिता, ब्लेंड मोड, और ग्रेडिएंट शैली जैसी प्रॉपर्टीज़ को उजागर करता है।

## रेडियल ग्रेडिएंट इफ़ेक्ट कैसे बनाएं

PSD लोड करें, लक्ष्य लेयर खोजें, `GradientOverlayEffect` प्रॉपर्टीज़ को समायोजित करें, और अंत में फ़ाइल सहेजें। एक बार इमेज लोड हो जाने पर पूरा वर्कफ़्लो चार संक्षिप्त Java कोड लाइनों में फिट हो जाता है।

### चरण 1: PSD फ़ाइल लोड करें और ग्रेडिएंट ओवरले तक पहुँचें

`PsdLoadOptions` यह निर्धारित करता है कि PSD फ़ाइल कैसे लोड की जाती है, जिससे आप इफ़ेक्ट रिसोर्सेज़ को लोड करने को सक्षम कर सकते हैं। `Image.load` फ़ाइल को एक `Image` ऑब्जेक्ट में पढ़ता है।

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

इस चरण में, हम एक PSD फ़ाइल लोड करते हैं और दूसरे लेयर (इंडेक्स 1) से पहला `GradientOverlayEffect` प्राप्त करते हैं। `loadOptions.setLoadEffectsResource(true)` कॉल यह सुनिश्चित करती है कि इफ़ेक्ट रिसोर्सेज़ संपादन के लिए उपलब्ध हों।

### चरण 2: प्रारंभिक सेटिंग्स की जाँच करें

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

परिवर्तन करने से पहले, वर्तमान ब्लेंड मोड, अपारदर्शिता, और दृश्यता की पुष्टि करना एक अच्छी प्रथा है। यह आपको ग्रेडिएंट ओवरले की बेसलाइन स्थिति समझने में मदद करता है।

### चरण 3: ग्रेडिएंट सेटिंग्स संशोधित करें

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

यहाँ आप ग्रेडिएंट का रंग, अपारदर्शिता, और ब्लेंड मोड कस्टमाइज़ कर सकते हैं। उदाहरण में रंग को हरे में बदलता है, अपारदर्शिता को 193 (255 में से) तक घटाता है, और ब्लेंड मोड को **Lighten** में बदलता है। आप `BlendMode` के अन्य मानों जैसे `Multiply`, `Screen`, या `Overlay` के साथ प्रयोग कर सकते हैं।

### चरण 4: संपादित इमेज सहेजें

```java
// Save the edited image
im.save(exportPath);
```

अपनी संशोधनों को लागू करने के बाद, PSD को नई फ़ाइल में सहेजकर बदलावों को स्थायी बनाएं। यह चरण सुनिश्चित करता है कि मूल फ़ाइल अपरिवर्तित रहे।

### चरण 5: बदलावों की जाँच करें

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

ऊपर दिया गया स्निपेट दर्शाता है कि कैसे एक PSD खोलें, दूसरे लेयर के पहले इफ़ेक्ट (मान लिया गया है कि यह ग्रेडिएंट ओवरले है) को प्राप्त करें, और उसे संशोधन के लिए तैयार करें।

### चरण 2: मूल सेटिंग्स की जाँच करें (वैकल्पिक लेकिन अनुशंसित)

किसी भी चीज़ को बदलने से पहले, मौजूदा ब्लेंड मोड, अपारदर्शिता, और दृश्यता की जाँच करना आपको बेसलाइन समझने में मदद करता है। कोड में `Assert` कॉल यह पुष्टि करते हैं कि इफ़ेक्ट वर्तमान में **Normal** ब्लेंड मोड, पूरी तरह अपारदर्शी, और दृश्यमान है।

### चरण 3: रेडियल शैली प्राप्त करने के लिए ग्रेडिएंट प्रॉपर्टीज़ समायोजित करें

आप ग्रेडिएंट का रंग, अपारदर्शिता, और ब्लेंड मोड बदल सकते हैं। एक वास्तविक रेडियल इफ़ेक्ट के लिए, ग्रेडिएंट शैली सेट करें:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Pro tip:* प्रारंभिक रंग को परिभाषित करने के लिए `Color.getGreen()` या कोई भी `java.awt.Color` इंस्टेंस उपयोग करें, और अंत रंग के लिए `gradientOverlay.setColor2(Color.getBlue())` का प्रयोग करें।

### चरण 4: संपादित PSD सहेजें

`im.save(exportPath);` को कॉल करने से संशोधित इमेज डिस्क पर लिखी जाती है। सहेजी गई फ़ाइल रेडियल ग्रेडिएंट ओवरले को बरकरार रखती है और Photoshop में खोली जा सकती है, ब्राउज़र में प्रीव्यू की जा सकती है, या अन्य फ़ॉर्मैट में परिवर्तित की जा सकती है।

## रेडियल ग्रेडिएंट ओवरले क्यों बनाएं?

रेडियल ग्रेडिएंट डिज़ाइनों में गहराई और फोकस जोड़ते हैं, जिससे तत्व त्रि‑आयामी या स्पॉटलाइटेड दिखते हैं। ये निम्नलिखित के लिए आदर्श हैं:

- **बैकग्राउंड फिल्स** जो केंद्रीय विषय की ओर नजर आकर्षित करते हैं।  
- **बटन या आइकन हाइलाइट्स** जहाँ हल्की चमक आवश्यक होती है।  
- **क्रिएटिव फोटो इफ़ेक्ट्स** जैसे विगनेट या लाइट बर्स्ट।  

Aspose.PSD **50+ इनपुट और आउटपुट फ़ॉर्मैट्स** को प्रोसेस करता है और पूरी डॉक्यूमेंट को मेमोरी में लोड किए बिना कई‑सौ‑पेज़ PSD फ़ाइलों को संभाल सकता है, जिससे आप बड़े एसेट लाइब्रेरीज़ में ग्रेडिएंट निर्माण को स्वचालित कर सकते हैं।

## सामान्य समस्याएँ और टिप्स

- **इफ़ेक्ट दिखाई नहीं दे रहा:** सुनिश्चित करें कि `gradientOverlay.isVisible()` `true` लौटाता है। कुछ PSD फ़ाइलें डिफ़ॉल्ट रूप से इफ़ेक्ट्स को छिपाती हैं।  
- **गलत लेयर इंडेक्स:** लेयर्स शून्य‑आधारित होते हैं; दोबारा जांचें कि आप सही लेयर को टार्गेट कर रहे हैं (`im.getLayers()[1]` दूसरे लेयर को दर्शाता है)।  
- **अपारदर्शिता कास्टिंग:** `setOpacity` मेथड एक `byte` की अपेक्षा करता है। `int` पास करने से कंपाइलेशन एरर होगा; जैसा दिखाया गया है वैसा स्पष्ट रूप से कास्ट करें।  
- **रिसोर्स लोडिंग:** यदि इफ़ेक्ट्स तक पहुँचते समय `null` मिलता है, तो इमेज लोड करने से पहले `loadOptions.setLoadEffectsResource(true)` सेट है या नहीं, जांचें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं एक ही इमेज पर कई ग्रेडिएंट इफ़ेक्ट्स लागू कर सकता हूँ?**  
A: हाँ। लेयर की `BlendingOptions` प्राप्त करें, `Effects` कलेक्शन पर इटररेट करें, और आपको आवश्यक प्रत्येक ग्रेडिएंट के लिए एक नया `GradientOverlayEffect` जोड़ें।

**Q: मैं ग्रेडिएंट ओवरले के साथ कौन से अन्य इफ़ेक्ट्स को संयोजित कर सकता हूँ?**  
A: Aspose.PSD शैडोज़, ग्लो, बीवेल और अधिक प्रदान करता है। प्रत्येक इफ़ेक्ट `Effects` एरे में दिखाई देता है और स्वतंत्र रूप से कॉन्फ़िगर किया जा सकता है।

**Q: यदि इफ़ेक्ट्स सही ढंग से रेंडर नहीं हो रहे हैं तो मैं कैसे ट्रबलशूट करूँ?**  
A: सुनिश्चित करें कि PSD को `setLoadEffectsResource(true)` के साथ लोड किया गया है, लेयर की दृश्यता जांचें, और पुष्टि करें कि आप सही इफ़ेक्ट इंडेक्स को संशोधित कर रहे हैं।

**Q: क्या Aspose.PSD for Java के लिए कोई ट्रायल संस्करण उपलब्ध है?**  
A: हाँ, आप एक मुफ्त ट्रायल [यहाँ](https://releases.aspose.com/) प्राप्त कर सकते हैं।

**Q: मैं Aspose.PSD for Java के लिए लाइसेंस कहाँ खरीद सकता हूँ?**  
A: लाइसेंसिंग जानकारी के लिए [खरीद पृष्ठ](https://purchase.aspose.com/buy) देखें।

## अतिरिक्त अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं प्रोग्रामेटिकली ग्रेडिएंट दिशा बदल सकता हूँ?**  
A: हाँ। ग्रेडिएंट एंगल को डिग्री में सेट करने के लिए `GradientOverlayEffect.setAngle(float angle)` मेथड का उपयोग करें। रेडियल ग्रेडिएंट्स के लिए एंगल को अनदेखा किया जाता है, लेकिन मेथड को अभी भी कॉल करना आवश्यक है।

**Q: क्या Aspose.PSD रेडियल ग्रेडिएंट्स को सपोर्ट करता है?**  
A: बिल्कुल। `GradientOverlayEffect` प्रॉपर्टीज़ के माध्यम से ग्रेडिएंट शैली को `GradientStyle.Radial` सेट करें।

**Q: क्या PSD को अन्य फ़ॉर्मैट्स (जैसे PNG) में कनवर्ट करने पर ग्रेडिएंट ओवरले बरकरार रहता है?**  
A: जब आप PSD को रास्टराइज़ करते हैं (जैसे PNG के रूप में सहेजते हैं), तो ग्रेडिएंट ओवरले का दृश्य परिणाम बरकरार रहता है, लेकिन इफ़ेक्ट स्वयं पिक्सेल डेटा का हिस्सा बन जाता है।

**Q: मैं लेयर से ग्रेडिएंट ओवरले कैसे हटाऊँ?**  
A: लेयर की `BlendingOptions` प्राप्त करें, `Effects` कलेक्शन में `GradientOverlayEffect` खोजें, और `remove(effect)` का उपयोग करके उसे हटाएँ।

**Q: क्या ग्रेडिएंट बदलावों को एनीमेट करना संभव है?**  
A: जबकि Aspose.PSD सीधे एनीमेशन को संभालता नहीं है, आप विभिन्न ग्रेडिएंट पैरामीटर्स के साथ PSD फ़ाइलों की एक श्रृंखला बना सकते हैं और फिर उन्हें किसी अन्य लाइब्रेरी का उपयोग करके वीडियो या GIF में संयोजित कर सकते हैं।

## निष्कर्ष

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके अपनी इमेजेज़ में **how to create radial gradient java** इफ़ेक्ट बनाना सीख लिया है। ऊपर दिए गए चरणों का पालन करके आप प्रोग्रामेटिकली ग्रेडिएंट ओवरले जोड़, संशोधित, और सहेज सकते हैं, जिससे आपको PSD एसेट्स पर पूर्ण रचनात्मक नियंत्रण मिलता है। विभिन्न रंगों, ब्लेंड मोड्स, और अपारदर्शिता मानों के साथ प्रयोग करें ताकि आप आवश्यक दृश्य प्रभाव प्राप्त कर सकें।

---

**अंतिम अपडेट:** 2026-10-18  
**परीक्षण किया गया:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**लेखक:** Aspose  

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## संबंधित ट्यूटोरियल

- [Aspose.PSD का उपयोग करके Java में ग्रेडिएंट फ़िल PSD बनाएं – ग्रेडिएंट फ़िल लेयर जोड़ें](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [पैटर्न ओवरले PSD: Aspose.PSD for Java के साथ इफ़ेक्ट्स जोड़ें](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Aspose.PSD के साथ Java में कलर ओवरले लागू करें और अपारदर्शिता सेट करें](/psd/java/image-editing/color-overlay-effect/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}