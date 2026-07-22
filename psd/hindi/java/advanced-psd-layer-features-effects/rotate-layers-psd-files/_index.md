---
date: 2026-02-17
description: जानेँ कैसे Aspose.PSD का उपयोग करके जावा में PSD को PNG में बदलें, PNG
  की पारदर्शिता बनाए रखें, और PSD लेयर्स को घुमाएँ। कोड नमूनों के साथ चरण‑दर‑चरण गाइड।
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Java का उपयोग करके PSD को PNG में बदलें और PSD फ़ाइलों में लेयर्स को घुमाएँ
url: /hi/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD को PNG में बदलें और PSD फ़ाइलों में लेयर्स को घुमाएँ Java का उपयोग करके

## परिचय
यदि आपको **PSD को PNG में बदलने** के साथ-साथ लेयर्स को घुमाने की आवश्यकता है, तो यह गाइड आपके लिए है। चाहे आप एक बैच‑प्रोसेसिंग टूल बना रहे हों, एक वेब सेवा जो ऑन‑द‑फ्लाई इमेज मैनिपुलेशन करती हो, या सिर्फ डिज़ाइन वर्कफ़्लो को ऑटोमेट कर रहे हों, प्रोग्रामेटिक रूप से यह करना समय बचाता है और Adobe Photoshop पर निर्भरता को हटाता है। इस ट्यूटोरियल में हम **PSD लेयर्स को कैसे घुमाएँ** और परिणाम को PNG के रूप में निर्यात करें, यह Aspose.PSD लाइब्रेरी फ़ॉर Java का उपयोग करके देखेंगे। चलिए काम शुरू करते हैं और आपका डिज़ाइन वर्कफ़्लो सुचारू रूप से चलाने में मदद करते हैं!

## त्वरित उत्तर
- **कौन सी लाइब्रेरी उपयोग कर सकते हैं?** Aspose.PSD फ़ॉर Java  
- **क्या मैं एक ही बार में घुमा और बदल सकता हूँ?** हाँ – PSD को घुमाएँ फिर PNG के रूप में सहेजें  
- **क्या लाइसेंस की जरूरत है?** परीक्षण के लिए मुफ्त ट्रायल चलती है; प्रोडक्शन के लिए पेड लाइसेंस आवश्यक है  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और उसके बाद के संस्करण  
- **क्या PNG आउटपुट ट्रांसपेरेंट रहेगा?** हाँ, जब आप `PngColorType.TruecolorWithAlpha` सेट करते हैं  

## “PSD को PNG में बदलना” क्या है?
Photoshop दस्तावेज़ (PSD) को PNG इमेज में बदलना का अर्थ है दृश्य सामग्री—सभी लेयर्स, मास्क और ट्रांसपेरेंसी सहित—को एक व्यापक रूप से समर्थित रास्टर फ़ॉर्मेट में निकालना। PNG अल्फा चैनल को संरक्षित रखता है, जिससे यह वेब ग्राफ़िक्स, थंबनेल और आगे की इमेज प्रोसेसिंग के लिए आदर्श बनता है।

## Aspose.PSD फ़ॉर Java का उपयोग करके PSD को PNG में बदलना और PSD लेयर्स को घुमाना क्यों?
- **Photoshop की आवश्यकता नहीं** – किसी भी सर्वर या CI वातावरण में काम करता है  
- **पूर्ण लेयर समर्थन** – ट्रांसपेरेंसी और लेयर इफ़ेक्ट्स को बरकरार रखता है  
- **सरल API** – कुछ मेथड कॉल्स से घुमाएँ, फ्लिप करें और सहेजें  
- **क्रॉस‑प्लेटफ़ॉर्म** – Windows, Linux और macOS पर चलता है  
- **Java इमेज कन्वर्ज़न** को एक ही लाइब्रेरी के साथ आसान बनाता है  

## पूर्वापेक्षाएँ
कोड में डुबकी लगाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- **Java Development Kit (JDK)** – [Oracle वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html) से डाउनलोड करें।  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse, या NetBeans सभी ठीक हैं।  
- **Aspose.PSD फ़ॉर Java लाइब्रेरी** – नवीनतम JAR [रिलीज़ पेज](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
- **बेसिक Java ज्ञान** – क्लासेज, ऑब्जेक्ट्स और एक्सेप्शन हैंडलिंग की परिचितता।  

## चरण‑दर‑चरण गाइड

### चरण 1: अपना Java प्रोजेक्ट सेट अप करें
अपने IDE में एक नया Java प्रोजेक्ट बनाएं और Aspose.PSD JAR को प्रोजेक्ट की बिल्ड पाथ में जोड़ें।

### चरण 2: आवश्यक क्लासेज इम्पोर्ट करें
अपने Java स्रोत फ़ाइल के शीर्ष पर निम्नलिखित इम्पोर्ट जोड़ें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

ये क्लासेज आपको इमेज लोड करने, घुमाने और PNG‑विशिष्ट विकल्पों तक पहुँच देती हैं।

### चरण 3: फ़ाइल पाथ निर्धारित करें
निर्दिष्ट करें कि आपका स्रोत PSD कहाँ स्थित है और आउटपुट फ़ाइलें कहाँ लिखी जाएँगी।

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **प्रो टिप:** परीक्षण के दौरान “फ़ाइल नहीं मिली” त्रुटियों से बचने के लिए पूर्ण (absolute) पाथ उपयोग करें।

### चरण 4: PSD फ़ाइल लोड करें
PSD को एक मैनीपुलेटेबल ऑब्जेक्ट में लोड करें।

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

अब `im` पूरे Photoshop दस्तावेज़ को दर्शाता है, जिसमें सभी लेयर्स शामिल हैं।

### चरण 5: इमेज को घुमाएँ (PSD को कैसे घुमाएँ)
`RotateFlipType` से एक रोटेशन टाइप चुनें। इस उदाहरण में हम 270° घुमाते हैं और दोनों अक्षों को फ्लिप करते हैं।

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

अन्य मानों जैसे `Rotate90FlipNone` या `Rotate180FlipX` के साथ प्रयोग करने के लिए स्वतंत्र रहें। यही ट्यूटोरियल का **PSD को कैसे घुमाएँ** भाग है।

### चरण 6: घुमा हुआ इमेज PNG के रूप में सहेजें (PSD को PNG में बदलें)
ट्रांसपेरेंसी बनाए रखने के लिए PNG विकल्प कॉन्फ़िगर करें, फिर सहेजें।

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

परिणामी PNG लेयर ट्रांसपेरेंसी को बरकरार रखता है, जिससे **PNG ट्रांसपेरेंसी को संरक्षित** किया जा सके।

### चरण 7: संशोधित PSD सहेजें (वैकल्पिक)
यदि आपको घुमाव लागू किए हुए नया PSD भी चाहिए, तो उसे वापस सहेजें।

```java
im.save(psdPath);
```

अब आपके पास एक PNG प्रीव्यू और एक अपडेटेड PSD फ़ाइल दोनों हैं।

## सामान्य समस्याएँ और समाधान
- **फ़ाइल नहीं मिली:** सुनिश्चित करें कि `dataDir` के अंत में पाथ सेपरेटर (`/` या `\`) हो।  
- **बड़े PSD पर OutOfMemoryError:** JVM हीप साइज बढ़ाएँ (`-Xmx2g`)।  
- **ट्रांसपेरेंसी खो गई:** सुनिश्चित करें कि `PngColorType.TruecolorWithAlpha` सेट है; अन्यथा PNG अल्फा के बिना सहेजा जाएगा।  
- **Flip PSD इमेज अपेक्षित रूप से व्यवहार नहीं कर रही:** चुने हुए `RotateFlipType` कॉन्स्टेंट को दोबारा जांचें; कुछ कॉन्स्टेंट एक ही कदम में रोटेशन और फ्लिप को मिलाते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं PSD फ़ाइल में किसी विशिष्ट लेयर को घुमा सकता हूँ?**  
उत्तर: हाँ, आप `im.getLayers()` पर इटररेट करके व्यक्तिगत लेयर्स पर `Layer.rotateFlip()` उपयोग कर सकते हैं।

**प्रश्न: क्या Aspose.PSD फ़ॉर Java में कोई प्रदर्शन सीमा है?**  
उत्तर: लाइब्रेरी अधिकांश फ़ाइलों को कुशलता से संभालती है, लेकिन अत्यधिक बड़े PSD (>500 MB) को अतिरिक्त मेमोरी की आवश्यकता हो सकती है।

**प्रश्न: क्या Aspose.PSD मुफ्त है?**  
उत्तर: Aspose एक मुफ्त ट्रायल प्रदान करता है, लेकिन प्रोडक्शन के लिए पेड लाइसेंस आवश्यक है। परीक्षण के लिए [टेम्पररी लाइसेंस](https://purchase.aspose.com/temporary-license/) देखें।

**प्रश्न: विस्तृत दस्तावेज़ीकरण कहाँ मिल सकता है?**  
उत्तर: आप व्यापक दस्तावेज़ीकरण [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) पर पा सकते हैं।

**प्रश्न: यदि Aspose.PSD उपयोग करते समय समस्याएँ आती हैं तो क्या करें?**  
उत्तर: मदद के लिए [Aspose Support Forum](https://forum.aspose.com/c/psd/34) पर संपर्क करें।

**प्रश्न: क्या PSD को PNG में बदलने से लेयर इफ़ेक्ट्स बरकरार रहते हैं?**  
उत्तर: हाँ, जब आप `PngColorType.TruecolorWithAlpha` के साथ सहेजते हैं, अधिकांश दृश्य इफ़ेक्ट्स PNG में रास्टराइज़ हो जाते हैं।

**प्रश्न: क्या मैं कई PSD फ़ाइलों को बैच‑प्रोसेस कर सकता हूँ?**  
उत्तर: बिल्कुल। कोड को एक लूप में रखें जो PSD फ़ाइलों की डायरेक्टरी पर इटररेट करे।

**प्रश्न: क्या PNG कम्प्रेशन लेवल सेट करना संभव है?**  
उत्तर: `PngOptions` क्लास में `setCompressionLevel(int)` मेथड है जिससे आप फाइन‑ट्यून कर सकते हैं।

**प्रश्न: क्या मुझे इमेज ऑब्जेक्ट को बंद करना चाहिए?**  
उत्तर: `PsdImage` `Closeable` को इम्प्लीमेंट करता है; `im.close()` को `finally` ब्लॉक में कॉल करें या try‑with‑resources उपयोग करें।

**प्रश्न: क्या घुमा हुआ PNG मूल के समान आयाम रखेगा?**  
उत्तर: 90° या 270° घुमाने से चौड़ाई और ऊँचाई बदल जाती है। PNG नई ओरिएंटेशन को दर्शाएगा।

## निष्कर्ष
Aspose.PSD फ़ॉर Java का उपयोग करके आप **PSD को PNG में बदल सकते हैं**, **PNG ट्रांसपेरेंसी को संरक्षित रख सकते हैं**, और **PSD लेयर्स को घुमा सकते हैं** केवल कुछ लाइनों के कोड से। यह तरीका Photoshop की आवश्यकता को समाप्त करता है, ऑटोमेटेड वर्कफ़्लो को तेज़ बनाता है, और इमेज आउटपुट पर पूर्ण नियंत्रण देता है। इसे अपने प्रोजेक्ट्स में आज़माएँ और देखें कितना समय बचता है!

---

**अंतिम अपडेट:** 2026-02-17  
**टेस्टेड विथ:** Aspose.PSD फ़ॉर Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}