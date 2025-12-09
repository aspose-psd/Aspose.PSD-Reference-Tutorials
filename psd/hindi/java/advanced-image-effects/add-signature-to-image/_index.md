---
date: 2025-12-02
description: जावा में Aspose.PSD का उपयोग करके कैनवास पर इमेज कैसे ड्रॉ करें और सिग्नेचर
  ओवरले करें, सीखें। इस चरण-दर-चरण जावा इमेज प्रोसेसिंग ट्यूटोरियल का पालन करें और
  परिणाम को PNG के रूप में सहेजें।
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: कैनवास पर छवि बनाएं – Aspose.PSD for Java के साथ हस्ताक्षर जोड़ें
url: /hi/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# कैनवास पर इमेज ड्रॉ करें – Aspose.PSD for Java के साथ सिग्नेचर जोड़ें

## Introduction

हाथ से लिखी या डिजिटल सिग्नेचर को चित्र में जोड़ना अनुबंधों, चालानों या किसी भी दस्तावेज़ के लिए अक्सर आवश्यक होता है जिसे प्रामाणिकता का प्रमाण चाहिए। **Aspose.PSD for Java** के साथ आप **draw image on canvas** कर सकते हैं और सिग्नेचर को एक अतिरिक्त ओवरले लेयर की तरह मान सकते हैं। इस **java image processing tutorial** में हम पूरे वर्कफ़्लो को समझेंगे—बेस चित्र और सिग्नेचर फ़ाइल को लोड करने से लेकर ग्राफ़िक्स को इनिशियलाइज़ करने, ओवरले ड्रॉ करने, और अंत में **save image png java**‑स्टाइल में सेव करने तक।

## Quick Answers
- **What does “draw image on canvas” mean?** यह `Graphics` क्लास का उपयोग करके एक इमेज को दूसरी इमेज पर रेंडर करने को दर्शाता है।  
- **How to add a signature in Java?** सिग्नेचर फ़ाइल को `Image` के रूप में लोड करें और `Graphics.drawImage` का उपयोग करें।  
- **Which Aspose.PSD version is required?** कोई भी हालिया 24.x रिलीज़; कोड नवीनतम लाइब्रेरी के साथ काम करता है।  
- **Can I overlay multiple images?** हाँ—विभिन्न स्रोतों के साथ `drawImage` कॉल को दोहराएँ।  
- **Do I need a license?** डेवलपमेंट के लिए ट्रायल काम करता है; प्रोडक्शन के लिए कमर्शियल लाइसेंस आवश्यक है।

## What Is “Draw Image on Canvas”?
Aspose.PSD शब्दावली में, कैनवास पर इमेज ड्रॉ करना का मतलब है एक `Image` ऑब्जेक्ट को दूसरे पर `Graphics` कॉन्टेक्स्ट का उपयोग करके पेंट करना। यह ऑपरेशन **overlay images java** तकनीकों जैसे वाटरमार्क, लोगो या सिग्नेचर जोड़ने का मूल आधार है।

## Why Use Aspose.PSD for Overlaying a Signature?
- **Full PSD support** – लेयर्स, मास्क और ट्रांसपैरेंसी के साथ काम करता है।  
- **No native OS dependencies** – शुद्ध Java, सर्वर‑साइड प्रोसेसिंग के लिए उपयुक्त।  
- **High‑performance rendering** – बड़े फ़ाइलों और जटिल कंपोज़िशन के लिए ऑप्टिमाइज़्ड।  

## Prerequisites
- Java Development Kit (JDK) 8 या उससे ऊपर।  
- Aspose.PSD for Java JAR को अपने प्रोजेक्ट की क्लासपाथ में जोड़ें।  
- दो इमेज फ़ाइलें: एक बेस चित्र (जैसे `layers.psd`) और एक सिग्नेचर ग्राफिक (`sample.psd`)।  

## Import Packages

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Load Primary and Secondary Images

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** दोनों इमेज को एक ही कलर मोड (RGB) में रखें ताकि ड्रॉ करते समय अप्रत्याशित रंग परिवर्तन न हों।

## Step 2: Initialize Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` ऑब्जेक्ट एक पेंटब्रश की तरह काम करता है जो आपको **draw image on canvas** करने देता है। इसे प्राइमरी `Image` के साथ इनिशियलाइज़ करने से सभी बाद के ड्रॉ कमांड उस कैनवास से जुड़ जाते हैं।

## Step 3: Add Signature to Image (how to add signature)

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

इस स्निपेट में हम **overlay images java** करके सिग्नेचर को नीचे‑दाएँ कोने में रख रहे हैं। यदि आपको अलग प्लेसमेंट चाहिए तो `Point` वैल्यूज़ को समायोजित करें।

## Common Issues & Solutions
| Symptom | Cause | Fix |
|---------|-------|-----|
| Signature appears distorted | कैनवास और सिग्नेचर के बीच DPI मेल नहीं खाता | ड्रॉ करने से पहले `signature.resize` का उपयोग करें या सुनिश्चित करें कि दोनों फ़ाइलों का DPI समान हो। |
| Output file is huge | बिना कॉम्प्रेशन के सेव किया गया | `CompressionLevel` को उच्च मान पर सेट करने के साथ एक कॉन्फ़िगर किया हुआ `PngOptions` पास करें। |
| Nothing is drawn | Graphics डिस्पोज़ नहीं किया गया | ड्रॉ करने के बाद `graphics.dispose()` कॉल करें (वैकल्पिक, लेकिन अच्छा अभ्यास)। |

## Conclusion

इन चरणों का पालन करके आपने **how to draw image on canvas** सीख लिया और Aspose.PSD for Java का उपयोग करके सहजता से **add a signature** कर ली। इस तकनीक को वाटरमार्क, लोगो या किसी भी ओवरले ग्राफ़िक्स के लिए विस्तारित किया जा सकता है, जिससे आपके Java एप्लिकेशन को शक्तिशाली **java image processing** क्षमताएँ मिलती हैं।

## FAQ's

### Q1: Can I add multiple signatures to an image?

A1: हाँ, आप विभिन्न सिग्नेचर इमेजेज़ के साथ चरणों को दोहराकर कई सिग्नेचर जोड़ सकते हैं।

### Q2: Does Aspose.PSD support other image formats?

A2: हाँ, Aspose.PSD कई इमेज फ़ॉर्मेट्स को सपोर्ट करता है, जिससे इमेज प्रोसेसिंग में लचीलापन मिलता है।

### Q3: Is a license required for using Aspose.PSD for Java?

A3: हाँ, Aspose.PSD के उपयोग के लिए एक वैध लाइसेंस आवश्यक है। लाइसेंसिंग विवरण के लिए [Purchase Aspose.PSD](https://purchase.aspose.com/buy) देखें।

### Q4: How can I get support for Aspose.PSD?

A4: समुदाय समर्थन और चर्चा के लिए [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) पर जाएँ।

### Q5: Can I try Aspose.PSD for Java before purchasing?

A5: हाँ, आप खरीदने से पहले फीचर एक्सप्लोर करने के लिए एक [free trial](https://releases.aspose.com/) ले सकते हैं।

## Additional Frequently Asked Questions

**Q: How do I change the opacity of the signature?**  
A: `drawImage` कॉल करने से पहले `graphics.setOpacity(float opacity)` उपयोग करें। वैल्यू 0.0 (पारदर्शी) से 1.0 (अपारदर्शी) तक हो सकती है।

**Q: Is it possible to rotate the signature?**  
A: हाँ—ड्रॉ करने से पहले `graphics.rotateTransform(angle)` के माध्यम से ट्रांसफ़ॉर्मेशन मैट्रिक्स लागू करें।

**Q: Can I draw the signature onto a JPEG instead of PNG?**  
A: बिल्कुल। `PngOptions` को `JpegOptions` से बदलें और इच्छित क्वालिटी लेवल सेट करें।

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}