---
date: 2026-04-28
description: Aspose.PSD for Java का उपयोग करके कैनवास पर चित्र बनाकर छवि में हस्ताक्षर
  कैसे जोड़ें, सीखें। यह जावा इमेज प्रोसेसिंग ट्यूटोरियल दिखाता है कि छवि को PNG के
  रूप में कैसे सहेजें और ग्राफ़िक्स को ओवरले करें।
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: एक छवि में हस्ताक्षर जोड़ें
second_title: Aspose.PSD Java API
title: इमेज में हस्ताक्षर जोड़ें – Aspose.PSD for Java के साथ कैनवास पर इमेज ड्रॉ
  करें
url: /hi/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# इमेज में सिग्नेचर जोड़ें – Aspose.PSD for Java के साथ कैनवास पर इमेज ड्रॉ करें

## परिचय

हाथ से लिखी या डिजिटल **add signature to image** जोड़ना अनुबंधों, चालानों, या किसी भी दस्तावेज़ के लिए सामान्य आवश्यकता है जिसे प्रामाणिकता का प्रमाण चाहिए। इस ट्यूटोरियल में आप देखेंगे कि Aspose.PSD for Java आपको **draw image on canvas** कैसे करने देता है और सिग्नेचर को एक अतिरिक्त ओवरले लेयर के रूप में मानता है। हम बेस चित्र लोड करने, सिग्नेचर फ़ाइल लोड करने, ग्राफ़िक्स कॉन्टेक्स्ट इनिशियलाइज़ करने, ओवरले ड्रॉ करने, और अंत में **save image as PNG** करने की प्रक्रिया बताएँगे। अंत तक आपके पास किसी भी **java image processing** परिदृश्य के लिए पुन: उपयोग योग्य पैटर्न होगा, चाहे वह सिग्नेचर, वॉटरमार्क, या लोगो हो।

## त्वरित उत्तर
- **draw image on canvas** का क्या मतलब है? यह एक `Graphics` क्लास का उपयोग करके एक इमेज को दूसरे पर रेंडर करने को दर्शाता है।  
- **Java में सिग्नेचर कैसे जोड़ें?** सिग्नेचर फ़ाइल को `Image` के रूप में लोड करें और `Graphics.drawImage` का उपयोग करें।  
- **कौन सा Aspose.PSD संस्करण आवश्यक है?** कोई भी हालिया 24.x रिलीज़; कोड नवीनतम लाइब्रेरी के साथ काम करता है।  
- **क्या मैं कई इमेज ओवरले कर सकता हूँ?** हाँ—विभिन्न स्रोतों के साथ `drawImage` कॉल को दोहराएँ।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।

## “draw image on canvas” क्या है?
Aspose.PSD शब्दावली में, कैनवास पर इमेज ड्रॉ करना मतलब एक `Image` ऑब्जेक्ट को `Graphics` कॉन्टेक्स्ट का उपयोग करके दूसरे पर पेंट करना है। यह ऑपरेशन **overlay images java** तकनीकों की रीढ़ है जैसे वॉटरमार्क, लोगो, या सिग्नेचर जोड़ना।

## सिग्नेचर ओवरले करने के लिए Aspose.PSD क्यों उपयोग करें?
- **पूर्ण PSD समर्थन** – लेयर्स, मास्क, और ट्रांसपैरेंसी के साथ काम करता है।  
- **कोई नेटिव OS निर्भरताएँ नहीं** – शुद्ध Java, सर्वर‑साइड प्रोसेसिंग के लिए उपयुक्त।  
- **उच्च‑प्रदर्शन रेंडरिंग** – बड़े फ़ाइलों और जटिल संयोजनों के लिए अनुकूलित।  

## पूर्वापेक्षाएँ
- Java Development Kit (JDK) 8 या उससे ऊपर।  
- Aspose.PSD for Java JAR को अपने प्रोजेक्ट के classpath में जोड़ें।  
- दो इमेज फ़ाइलें: एक बेस चित्र (जैसे `layers.psd`) और एक सिग्नेचर ग्राफिक (`sample.psd`)।  

## पैकेज आयात करें

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## चरण 1: प्राथमिक और द्वितीयक इमेज लोड करें

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **प्रो टिप:** ड्रॉ करते समय अप्रत्याशित रंग परिवर्तन से बचने के लिए दोनों इमेज को एक ही कलर मोड (RGB) में रखें।

## चरण 2: ग्राफ़िक्स इनिशियलाइज़ करें (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` ऑब्जेक्ट एक पेंटब्रश की तरह कार्य करता है जो आपको **draw image on canvas** करने देता है। इसे प्राथमिक `Image` के साथ इनिशियलाइज़ करने से सभी बाद के ड्रॉइंग कमांड उस कैनवास से जुड़ जाते हैं।

## चरण 3: इमेज में सिग्नेचर जोड़ें (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

इस स्निपेट में हम **overlay images java** करते हैं सिग्नेचर को नीचे‑दाएँ कोने में रखकर। यदि आपको अलग स्थान चाहिए तो `Point` मानों को समायोजित करें।

## सामान्य समस्याएँ और समाधान
| लक्षण | कारण | समाधान |
|---------|-------|-----|
| सिग्नेचर विकृत दिखता है | कैनवास और सिग्नेचर के बीच DPI का मेल नहीं होना | ड्रॉ करने से पहले `signature.resize` उपयोग करें या सुनिश्चित करें कि दोनों फ़ाइलों का DPI समान हो। |
| आउटपुट फ़ाइल बहुत बड़ी है | बिना संपीड़न के सहेजना | `CompressionLevel` को उच्च मान पर सेट करके कॉन्फ़िगर किया गया `PngOptions` पास करें। |
| कुछ भी नहीं ड्रॉ होता | ग्राफ़िक्स डिस्पोज नहीं किया गया | ड्रॉ करने के बाद `graphics.dispose()` कॉल करें (वैकल्पिक, लेकिन अच्छा अभ्यास)। |

## वास्तविक उपयोग के लिए अतिरिक्त टिप्स
- **एकाधिक सिग्नेचर:** विभिन्न `Image` ऑब्जेक्ट और कोऑर्डिनेट्स के साथ `graphics.drawImage` को बार‑बार कॉल करें।  
- **अपारदर्शिता नियंत्रण:** सिग्नेचर को अर्ध‑पारदर्शी बनाने के लिए ड्रॉ करने से पहले `graphics.setOpacity(float opacity)` उपयोग करें।  
- **सिग्नेचर घुमाना:** यदि आपको तिरछा सिग्नेचर चाहिए तो `graphics.rotateTransform(angle)` लागू करें।  
- **अन्य फ़ॉर्मेट में सहेजना:** JPEG, BMP आदि आउटपुट करने के लिए `PngOptions` को `JpegOptions` या `BmpOptions` से बदलें।  

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं इमेज में कई सिग्नेचर जोड़ सकता हूँ?
A1: हाँ, आप विभिन्न सिग्नेचर इमेज के साथ चरणों को दोहराकर कई सिग्नेचर जोड़ सकते हैं।

### Q2: क्या Aspose.PSD अन्य इमेज फ़ॉर्मेट का समर्थन करता है?
A2: हाँ, Aspose.PSD कई इमेज फ़ॉर्मेट का समर्थन करता है, जिससे इमेज प्रोसेसिंग में लचीलापन मिलता है।

### Q3: क्या Java के लिए Aspose.PSD उपयोग करने के लिए लाइसेंस आवश्यक है?
A3: हाँ, Aspose.PSD उपयोग करने के लिए आपको एक वैध लाइसेंस चाहिए। लाइसेंस विवरण के लिए [Purchase Aspose.PSD](https://purchase.aspose.com/buy) देखें।

### Q4: मैं Aspose.PSD के लिए समर्थन कैसे प्राप्त कर सकता हूँ?
A4: सामुदायिक समर्थन और चर्चा के लिए [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) देखें।

### Q5: क्या मैं खरीदने से पहले Aspose.PSD for Java आज़मा सकता हूँ?
A5: हाँ, आप खरीदारी से पहले फीचर देखना चाहते हैं तो एक [free trial](https://releases.aspose.com/) प्राप्त कर सकते हैं।

**अतिरिक्त अक्सर पूछे जाने वाले प्रश्न**

**Q: मैं सिग्नेचर की अपारदर्शिता कैसे बदलूँ?**  
A: `drawImage` कॉल करने से पहले `graphics.setOpacity(float opacity)` उपयोग करें। मान 0.0 (पारदर्शी) से 1.0 (अस्पष्ट) तक होते हैं।

**Q: क्या सिग्नेचर को घुमाना संभव है?**  
A: हाँ—ड्रॉ करने से पहले `graphics.rotateTransform(angle)` के माध्यम से ट्रांसफ़ॉर्मेशन मैट्रिक्स लागू करें।

**Q: क्या मैं PNG के बजाय JPEG पर सिग्नेचर ड्रॉ कर सकता हूँ?**  
A: बिल्कुल। `PngOptions` को `JpegOptions` से बदलें और इच्छित गुणवत्ता स्तर निर्दिष्ट करें।

## निष्कर्ष

इन चरणों का पालन करके आपने Aspose.PSD for Java के साथ **draw image on canvas** करके **add signature to image** करना सीखा। वही पैटर्न वॉटरमार्क, लोगो, या किसी भी ओवरले ग्राफ़िक्स के लिए विस्तारित किया जा सकता है, जिससे आपके Java एप्लिकेशन को शक्तिशाली **java image processing** क्षमताएँ मिलती हैं।

---

**अंतिम अपडेट:** 2026-04-28  
**परीक्षण किया गया:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}