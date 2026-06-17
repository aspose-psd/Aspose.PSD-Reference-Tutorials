---
date: 2026-02-20
description: Aspose.PSD for Java का उपयोग करके PSD को PNG में बदलना सीखें, साथ ही
  PSD का कलर मोड 16‑बिट ग्रेस्केल सेट करना। कोड उदाहरणों के साथ चरण‑दर‑चरण मार्गदर्शिका।
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Java में 16‑बिट ग्रेस्केल कलर मोड के साथ PSD को PNG में कैसे बदलें
url: /hi/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

Let's craft translation.

Be careful with markdown formatting.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD को PNG में 16‑बिट ग्रेस्केल कलर मोड के साथ जावा में परिवर्तित करें

## परिचय
जब आप ग्राफिक डिज़ाइन और इमेज मैनिपुलेशन की दुनिया में गहराई से उतर रहे होते हैं, **how to convert PSD to PNG** जानना एक गुप्त हथियार जैसा होता है। 16‑बिट ग्रेस्केल मोड का उपयोग करने से अविश्वसनीय गहराई और टोनल समृद्धि मिलती है, जिससे आपकी छवियां अलग दिखती हैं। इस ट्यूटोरियल में हम **set PSD color mode** को 16‑बिट ग्रेस्केल पर सेट करने और फिर **export PSD as PNG** को Aspose.PSD for Java का उपयोग करके करने की प्रक्रिया देखेंगे। क्या आप अपनी इमेज वर्कफ़्लो को अगले स्तर पर ले जाना चाहते हैं? चलिए शुरू करते हैं।

## त्वरित उत्तर
- **What does “convert PSD to PNG” involve?** PSD को लोड करना, वैकल्पिक रूप से उसका कलर मोड बदलना, और उसे PNG फ़ाइल के रूप में सेव करना।  
- **Which Aspose class handles the conversion?** लोड करने के लिए `PsdImage` और सेव करने के लिए `PngOptions`।  
- **Do I need a special license?** परीक्षण के लिए ट्रायल चल सकता है; प्रोडक्शन के लिए पेड लाइसेंस आवश्यक है।  
- **Can I keep the 16‑bit depth in PNG?** हाँ, `PngColorType.GrayscaleWithAlpha` का उपयोग करके।  
- **What IDEs are supported?** कोई भी जावा IDE – IntelliJ IDEA, Eclipse, VS Code, आदि।

## क्यों PSD को PNG में 16‑बिट ग्रेस्केल के साथ परिवर्तित करें?
* **Preserve tonal detail:** 16‑बिट ग्रेस्केल 65 536 शेड्स ऑफ ग्रे स्टोर करता है, जो 8‑बिट (256 शेड्स) से बहुत अधिक है।  
* **Broad compatibility:** PNG ब्राउज़रों, मोबाइल ऐप्स और डेस्कटॉप टूल्स में व्यापक रूप से समर्थित है, जबकि उच्च‑गुणवत्ता डेटा को बरकरार रखता है।  
* **Lossless workflow:** Aspose.PSD के साथ परिवर्तित करने से कोई अनचाहा कम्प्रेशन आर्टिफैक्ट नहीं बनता, जो आर्काइविंग या आगे की प्रोसेसिंग के लिए आदर्श है।

## आवश्यकताएँ
शुरू करने से पहले, सुनिश्चित करें कि आपके पास इस ट्यूटोरियल को सर्वोत्तम रूप से उपयोग करने के लिए सभी चीज़ें सेट हैं। आपको ये चाहिए:

1. **Java Development Kit (JDK)** – सुनिश्चित करें कि आपके पास नवीनतम संस्करण स्थापित है। आप इसे [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड कर सकते हैं।  
2. **Aspose.PSD for Java Library** – यह वह इंजन है जो हमें PSD फ़ाइलों को मैनीपुलेट करने देगा। इसे [Aspose download page](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
3. **एक IDE** – IntelliJ IDEA, Eclipse, या Visual Studio Code ठीक रहेगा।  
4. **बुनियादी Java ज्ञान** – Java सिंटैक्स की परिचितता चरणों को सुगम बनाएगी।  
5. **एक सैंपल PSD फ़ाइल** – या तो Adobe Photoshop में बनाएं या ऑनलाइन एक मुफ्त सैंपल डाउनलोड करें।

तैयार हैं? बढ़िया! अब आवश्यक पैकेज इम्पोर्ट करें और कोडिंग शुरू करें।

## पैकेज इम्पोर्ट करें
शुरू करने के लिए, अपने Java फ़ाइल में आवश्यक Aspose.PSD इम्पोर्ट जोड़ें:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

ये इम्पोर्ट आपको PSD फ़ाइलों को मैनीपुलेट करने, कलर मोड सेट करने, और परिणाम को PNG के रूप में एक्सपोर्ट करने की सुविधाएँ देंगे।

## चरण 1: अपने डायरेक्टरीज़ को परिभाषित करें
सबसे पहले, स्रोत और आउटपुट फ़ोल्डर सेट करें। यह प्रोग्राम को बताता है कि मूल PSD कहाँ पढ़ना है और परिवर्तित फ़ाइलें कहाँ लिखनी हैं।

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

प्लेसहोल्डर स्ट्रिंग्स को अपने मशीन पर वास्तविक पाथ्स से बदलें।

## चरण 2: इमेज प्रोसेसिंग को संभालने के लिए मेथड बनाएं
हम परिवर्तन लॉजिक को एक पुन: उपयोग योग्य मेथड में एन्कैप्सुलेट करेंगे। यह सभी पैरामीटर लेता है जिन्हें आप ट्यून कर सकते हैं, जैसे कलर मोड, बिट डेप्थ, और कम्प्रेशन।

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

यह मेथड आपको **set PSD color mode** करने और फिर **export PSD as PNG** करने की अनुमति देता है, एक ही फ्लो में।

## चरण 3: फ़ाइल पाथ्स निर्धारित करें और PSD लोड करें
मेथड के अंदर, पूर्ण फ़ाइल पाथ बनाएं और मूल 16‑बिट ग्रेस्केल PSD लोड करें:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` आपको प्रत्येक एक्सपोर्टेड फ़ाइल के लिए उपयोग किए गए सेटिंग्स को ट्रैक करने में मदद करता है।

## चरण 4: लेयर या पूरी इमेज प्रोसेस करें
अब हम या तो किसी विशेष लेयर पर या पूरी इमेज पर ड्रॉ करेंगे। इस उदाहरण में हम परिणाम को अधिक स्पष्ट बनाने के लिए एक हल्की ग्रे बॉर्डर जोड़ते हैं।

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

आयत को डायनामिक रूप से गणना किया जाता है ताकि वह इमेज साइज चाहे जो भी हो, केंद्र में रहे।

## चरण 5: संशोधित PSD फ़ाइल को सेव करें
ड्रॉ करने के बाद, हम PSD को ठीक उसी कलर मोड और बिट डेप्थ के साथ सेव करते हैं जो आपने निर्दिष्ट किया था। यह **setting PSD color mode** का मूल भाग है, परिवर्तन से पहले।

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## चरण 6: PSD को PNG में परिवर्तित करें
अंत में, हम नए सेव किए गए PSD को लोड करते हैं और उसे PNG के रूप में एक्सपोर्ट करते हैं। `PngColorType.GrayscaleWithAlpha` का उपयोग करके हम PNG फ़ाइल में 16‑बिट डेप्थ को बरकरार रखते हैं।

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

अब आपने सफलतापूर्वक **converted PSD to PNG** किया है, जबकि उच्च‑गुणवत्ता 16‑बिट ग्रेस्केल डेटा को बनाए रखा है।

## सामान्य समस्याएँ और समाधान
| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| **“Unsupported color type” exception** | असमर्थित चैनल कॉन्फ़िगरेशन के साथ PSD को सेव करने की कोशिश। | सुनिश्चित करें कि `channelBitsCount` वास्तविक बिट डेप्थ (16) से मेल खाता हो और `channelsCount` ग्रेस्केल (1) के लिए सही हो। |
| **File not found** | स्रोत डायरेक्टरी पाथ गलत है। | `sourceDir` स्ट्रिंग को दोबारा जांचें और पुष्टि करें कि PSD फ़ाइल मौजूद है। |
| **Output PNG appears black** | PNG को अल्फा चैनल हैंडलिंग के बिना सेव किया गया। | ऊपर दिखाए अनुसार `PngColorType.GrayscaleWithAlpha` का उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: 16‑बिट ग्रेस्केल कलर मोड क्या है?**  
उत्तर: यह 65 536 शेड्स ऑफ ग्रे प्रदान करता है, जो मानक 8‑बिट (256 शेड्स) की तुलना में बहुत अधिक टोनल डिटेल देता है।

**प्रश्न: क्या मैं Aspose.PSD को नॉन‑ग्रेस्केल इमेजेज़ के लिए उपयोग कर सकता हूँ?**  
उत्तर: बिल्कुल! Aspose.PSD RGB, CMYK, Lab, और कई अन्य कलर मोड्स को सपोर्ट करता है।

**प्रश्न: क्या Aspose.PSD का ट्रायल संस्करण उपलब्ध है?**  
उत्तर: हाँ, आप Aspose.PSD का फ्री ट्रायल संस्करण आज़मा सकते हैं। बस [Aspose download page](https://releases.aspose.com/) पर जाएँ।

**प्रश्न: मैं Aspose.PSD के और उदाहरण कहाँ पा सकता हूँ?**  
उत्तर: अधिक विस्तृत उदाहरण और ट्यूटोरियल के लिए आप [documentation](https://reference.aspose.com/psd/java/) देख सकते हैं।

**प्रश्न: Aspose.PSD का लाइसेंस कैसे खरीदूँ?**  
उत्तर: आप लाइसेंस खरीदने के लिए [Aspose purchase page](https://purchase.aspose.com/buy) पर जा सकते हैं।

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}