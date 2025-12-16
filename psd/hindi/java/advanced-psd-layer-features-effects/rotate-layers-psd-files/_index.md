---
date: 2025-12-15
description: Aspose.PSD का उपयोग करके जावा में PSD को PNG में बदलना और PSD लेयर्स
  को घुमाना सीखें। कोड नमूनों के साथ चरण‑दर‑चरण मार्गदर्शिका।
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: जावा का उपयोग करके PSD को PNG में बदलें और PSD फ़ाइलों में लेयर को घुमाएँ
url: /hi/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD को PNG में बदलें और PSD फ़ाइलों में लेयर्स को घुमाएँ Java का उपयोग करके

## परिचय
यदि आपको **PSD को PNG में बदलना** है और साथ ही लेयर्स को घुमाना है, तो यह गाइड आपके लिए है। चाहे आप बैच‑प्रोसेसिंग टूल बना रहे हों या इमेज मैनिपुलेशन को वेब सर्विस में इंटीग्रेट कर रहे हों, प्रोग्रामेटिक रूप से यह करने से समय बचता है और Adobe Photoshop पर निर्भरता समाप्त होती है। इस ट्यूटोरियल में हम आपको **PSD लेयर्स को कैसे घुमाएँ** और परिणाम को PNG के रूप में एक्सपोर्ट करें, यह Aspose.PSD लाइब्रेरी फॉर Java का उपयोग करके दिखाएंगे। चलिए काम शुरू करते हैं और आपके डिज़ाइन वर्कफ़्लो को सुचारू बनाते हैं!

## त्वरित उत्तर
- **मैं कौनसी लाइब्रेरी इस्तेमाल कर सकता हूँ?** Aspose.PSD for Java  
- **क्या मैं एक ही बार में घुमा और बदल सकता हूँ?** हाँ – PSD को घुमाएँ फिर PNG के रूप में सेव करें  
- **क्या मुझे लाइसेंस चाहिए?** परीक्षण के लिए फ्री ट्रायल काम करता है; प्रोडक्शन के लिए पेड लाइसेंस आवश्यक है  
- **कौनसा Java संस्करण समर्थित है?** Java 8 और उसके बाद के संस्करण  
- **क्या PNG आउटपुट ट्रांसपेरेंट है?** हाँ, जब आप `PngColorType.TruecolorWithAlpha` सेट करते हैं  

## “PSD को PNG में बदलना” क्या है?
Photoshop दस्तावेज़ (PSD) को PNG इमेज में बदलना मतलब है दृश्य सामग्री—सभी लेयर्स, मास्क और ट्रांसपेरेंसी सहित—को एक व्यापक रूप से समर्थित रास्टर फ़ॉर्मेट में निकालना। PNG अल्फा चैनल को संरक्षित रखता है, जिससे यह वेब ग्राफ़िक्स, थंबनेल और आगे की इमेज प्रोसेसिंग के लिए आदर्श बनता है।

## PSD को PNG में बदलने और PSD लेयर्स को घुमाने के लिए Aspose.PSD for Java का उपयोग क्यों करें?
- **Photoshop की ज़रूरत नहीं** – किसी भी सर्वर या CI वातावरण में काम करता है  
- **पूरा लेयर समर्थन** – ट्रांसपेरेंसी और लेयर इफ़ेक्ट्स को बरकरार रखता है  
- **सरल API** – कुछ ही मेथड कॉल्स से घुमाएँ, फ़्लिप करें और सेव करें  
- **क्रॉस‑प्लेटफ़ॉर्म** – Windows, Linux और macOS पर चलता है  

## पूर्वापेक्षाएँ
कोड में डुबकी लगाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- **Java Development Kit (JDK)** – [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) से डाउनलोड करें।  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse, या NetBeans सभी ठीक हैं।  
- **Aspose.PSD for Java library** – नवीनतम JAR [release page](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
- **Basic Java knowledge** – क्लासेज़, ऑब्जेक्ट्स और एक्सेप्शन हैंडलिंग की समझ।

## चरण-दर-चरण मार्गदर्शिका

### Step 1: Set Up Your Java Project
अपने IDE में एक नया Java प्रोजेक्ट बनाएं और Aspose.PSD JAR को प्रोजेक्ट के बिल्ड पाथ में जोड़ें।

### Step 2: Import Required Classes
अपने Java सोर्स फ़ाइल के शीर्ष पर निम्नलिखित इम्पोर्ट्स जोड़ें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

ये क्लासेज़ आपको इमेज लोडिंग, रोटेशन और PNG‑स्पेसिफिक ऑप्शन्स तक पहुंच देती हैं।

### Step 3: Define File Paths
निर्दिष्ट करें कि आपका स्रोत PSD कहाँ स्थित है और आउटपुट फ़ाइलें कहाँ लिखी जाएँगी।

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** परीक्षण के दौरान “file not found” त्रुटियों से बचने के लिए एक एब्सोल्यूट पाथ उपयोग करें।

### Step 4: Load the PSD File
PSD को एक मैनिपुलेबल ऑब्जेक्ट में लोड करें।

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

अब `im` पूरे Photoshop दस्तावेज़ को दर्शाता है, जिसमें सभी लेयर्स शामिल हैं।

### Step 5: Rotate the Image (How to rotate PSD)
`RotateFlipType` से एक रोटेशन टाइप चुनें। इस उदाहरण में हम 270° घुमाते हैं और दोनों अक्षों को फ़्लिप करते हैं।

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

`Rotate90FlipNone` या `Rotate180FlipX` जैसे अन्य मानों के साथ प्रयोग करने के लिए स्वतंत्र महसूस करें।

### Step 6: Save the Rotated Image as PNG (convert PSD to PNG)
ट्रांसपेरेंसी बनाए रखने के लिए PNG विकल्प कॉन्फ़िगर करें, फिर सेव करें।

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

परिणामी PNG लेयर ट्रांसपेरेंसी को बरकरार रखता है, जिससे यह वेब उपयोग के लिए तैयार है।

### Step 7: Save the Modified PSD (optional)
यदि आपको घुमाव लागू किए हुए नया PSD भी चाहिए, तो उसे वापस सेव करें।

```java
im.save(psdPath);
```

अब आपके पास PNG प्रीव्यू और एक अपडेटेड PSD फ़ाइल दोनों हैं।

## सामान्य समस्याएँ और समाधान
- **File not found:** सुनिश्चित करें कि `dataDir` अंत में एक पाथ सेपरेटर (`/` या `\`) रखता है।  
- **OutOfMemoryError on large PSDs:** JVM हीप साइज बढ़ाएँ (`-Xmx2g`)।  
- **Transparency lost:** सुनिश्चित करें कि `PngColorType.TruecolorWithAlpha` सेट है; अन्यथा PNG बिना अल्फा के सेव होगा।

## FAQs
### क्या मैं PSD फ़ाइल में किसी विशिष्ट लेयर को घुमा सकता हूँ?
हाँ, आप `im.getLayers()` पर इटरेट करने के बाद व्यक्तिगत लेयर्स पर `Layer.rotateFlip()` उपयोग कर सकते हैं।

### क्या Aspose.PSD for Java में कोई प्रदर्शन सीमा है?
लाइब्रेरी अधिकांश फ़ाइलों को कुशलता से संभालती है, लेकिन बहुत बड़े PSDs (>500 MB) को अतिरिक्त मेमोरी की आवश्यकता हो सकती है।

### क्या Aspose.PSD मुफ्त है?
Aspose एक फ्री ट्रायल प्रदान करता है, लेकिन प्रोडक्शन के लिए पेड लाइसेंस आवश्यक है। परीक्षण के लिए [temporary license](https://purchase.aspose.com/temporary-license/) देखें।

### विस्तृत दस्तावेज़ीकरण कहाँ मिल सकता है?
आप [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) पर व्यापक दस्तावेज़ीकरण पा सकते हैं।

### यदि Aspose.PSD उपयोग करते समय समस्याएँ आती हैं तो क्या करें?
सहायता के लिए [Aspose Support Forum](https://forum.aspose.com/c/psd/34) पर संपर्क करें।

## अतिरिक्त अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या PSD को PNG में बदलने से लेयर इफ़ेक्ट्स संरक्षित रहते हैं?**  
**उत्तर:** हाँ, जब आप `PngColorType.TruecolorWithAlpha` के साथ सेव करते हैं, तो अधिकांश दृश्य इफ़ेक्ट्स PNG में रास्टराइज़ हो जाते हैं।

**प्रश्न: क्या मैं कई PSD फ़ाइलों को बैच‑प्रोसेस कर सकता हूँ?**  
**उत्तर:** बिल्कुल। कोड को एक लूप में रखें जो PSD फ़ाइलों की डायरेक्टरी पर इटरेट करे।

**प्रश्न: क्या PNG कॉम्प्रेशन लेवल सेट करना संभव है?**  
**उत्तर:** `PngOptions` क्लास में `setCompressionLevel(int)` मेथड है जो फाइन‑ट्यूनिंग की अनुमति देता है।

**प्रश्न: क्या मुझे इमेज ऑब्जेक्ट को बंद करना चाहिए?**  
**उत्तर:** `PsdImage` `Closeable` को इम्प्लीमेंट करता है; `im.close()` को `finally` ब्लॉक में कॉल करें या try‑with‑resources उपयोग करें।

**प्रश्न: क्या घुमाया गया PNG मूल के समान आयाम रखेगा?**  
**उत्तर:** 90° या 270° घुमाने से चौड़ाई और ऊँचाई बदल जाती है। PNG नई ओरिएंटेशन को दर्शाएगा।

## निष्कर्ष
Aspose.PSD for Java का उपयोग करके आप **PSD को PNG में बदल सकते हैं** और **PSD लेयर्स को घुमा सकते हैं** केवल कुछ लाइनों के कोड से। यह तरीका Photoshop की आवश्यकता को समाप्त करता है, स्वचालित वर्कफ़्लो को तेज़ बनाता है, और इमेज आउटपुट पर पूर्ण नियंत्रण देता है। इसे अपने प्रोजेक्ट्स में आज़माएँ और देखें कि आप कितना समय बचाते हैं!

---

**अंतिम अपडेट:** 2025-12-15  
**टेस्टेड विथ:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}