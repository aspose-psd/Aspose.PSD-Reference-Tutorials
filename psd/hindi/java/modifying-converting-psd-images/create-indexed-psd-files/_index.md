---
date: 2026-03-15
description: Aspose.PSD for Java का उपयोग करके इस चरण‑दर‑चरण गाइड में PSD फ़ाइलें
  बनाना, PSD रंग पैलेट उत्पन्न करना और PSD रंग मोड सेट करना सीखें।
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलें कैसे बनाएं
url: /hi/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

 headings (#, ##, ###). Keep code block placeholders unchanged.

Also note there is a note: "For Hindi, ensure proper RTL formatting if needed" but Hindi is LTR, okay.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java का उपयोग करके PSD फ़ाइलें कैसे बनाएं

## Introduction
यदि आप कभी प्रोग्रामेटिक रूप से **PSD फ़ाइलें कैसे बनाएं** इस बारे में सोचते रहे हैं, तो आप सही जगह पर हैं। Aspose.PSD for Java आपको Photoshop दस्तावेज़ों पर पूर्ण नियंत्रण देता है, जिससे आप Photoshop को कभी खोले बिना PSD फ़ाइलें उत्पन्न, संपादित और सहेज सकते हैं। इस ट्यूटोरियल में हम **indexed PSD** फ़ाइल बनाने, PSD कलर मोड सेट करने, और एक कस्टम कलर पैलेट जेनरेट करने की प्रक्रिया को स्पष्ट, चरण‑दर‑चरण Java कोड के साथ दिखाएंगे। चाहे आप ग्राफ़िक्स पाइपलाइन बना रहे हों, एसेट निर्माण को स्वचालित कर रहे हों, या सिर्फ प्रयोग कर रहे हों, यहाँ के सिद्धांत आपके विज़ुअल विचारों को जीवन में लाने में मदद करेंगे।

## Quick Answers
- **मुझे कौनसी लाइब्रेरी चाहिए?** Aspose.PSD for Java
- **क्या मैं एक indexed PSD बना सकता हूँ?** हाँ, कलर मोड को `Indexed` सेट करके
- **क्या मुझे Photoshop इंस्टॉल करना आवश्यक है?** नहीं, Aspose.PSD स्वतंत्र रूप से काम करता है
- **कौनसा Java संस्करण आवश्यक है?** JDK 8 या बाद का
- **कैनवास कितना बड़ा हो सकता है?** कोई भी आकार; इस उदाहरण में 500 × 500 px उपयोग किया गया है

## What is an Indexed PSD File?
एक indexed PSD प्रत्येक पिक्सेल के पूर्ण‑रंग मानों के बजाय रंगों को एक पैलेट में संग्रहीत करता है। इससे फ़ाइल आकार कम होता है और सीमित रंगों वाले ग्राफ़िक्स, जैसे आइकॉन या UI एसेट्स, के लिए आदर्श है। एक कस्टम पैलेट जेनरेट करके आप यह नियंत्रित कर सकते हैं कि अंतिम छवि में कौन‑से रंग दिखाई देंगे।

## Why Generate a PSD Color Palette?
- वेब या मोबाइल उपयोग के लिए फ़ाइल आकार छोटा रखें  
- अपने कॉर्पोरेट पैलेट तक रंग सीमित करके सुसंगत ब्रांडिंग सुनिश्चित करें  
- उन अनुप्रयोगों में रेंडरिंग गति बढ़ाएँ जो indexed इमेजेस को सपोर्ट करते हैं  

## Prerequisites
कोड में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java का बुनियादी ज्ञान** – आपको क्लासेज़, मेथड्स, और ऑब्जेक्ट निर्माण में सहज होना चाहिए।  
2. **Java Development Kit (JDK) 8+** – आपके IDE में इंस्टॉल और कॉन्फ़िगर किया हुआ।  
3. **IDE (IntelliJ IDEA, Eclipse, आदि)** – वैकल्पिक लेकिन आसान डिबगिंग के लिए अत्यधिक अनुशंसित।  
4. **Aspose.PSD for Java लाइब्रेरी** – इसे **[here](https://releases.aspose.com/psd/java/)** से डाउनलोड करें और JAR को अपने प्रोजेक्ट के क्लासपाथ में जोड़ें।  
5. **ग्राफ़िक डिज़ाइन के मूल सिद्धांत** – कलर मोड्स, पैलेट्स, और बेसिक शेप्स की समझ आपको ट्यूटोरियल को बेहतर समझने में मदद करेगी।

## Import Packages
कोड आगे बढ़ाने से पहले, सुनिश्चित करें कि आपके Java एप्लिकेशन में सभी आवश्यक पैकेज इम्पोर्ट किए गए हैं। आपको यह चाहिए:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

ये इम्पोर्ट्स आपको Aspose.PSD के माध्यम से PSD विकल्प, रंग, और ग्राफ़िक्स मैनिपुलेशन के साथ काम करने में सक्षम करेंगे।

अब, चलिए कोड को चरण‑दर‑चरण तोड़ते हैं ताकि **PSD फ़ाइलें कैसे बनाएं** को indexed कलर मोड के साथ समझा सकें।

## Step 1: Set Up Your Document Directory
पहले, यह निर्धारित करें कि जेनरेट किया गया PSD कहाँ सहेजा जाएगा।

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` को एक absolute या relative पाथ से बदलें, उदाहरण के लिए, `"/Users/YourName/Documents/"`।

## Step 2: Create an Instance of PsdOptions
`PsdOptions` वह सभी सेटिंग्स रखता है जो आप जनरेट करने वाले फ़ाइल के लिए आवश्यक हैं।

```java
PsdOptions createOptions = new PsdOptions();
```

## Step 3: Set Core Properties of PsdOptions
यहाँ हम आउटपुट लोकेशन, **set psd color mode** को `Indexed` सेट करते हैं, और PSD संस्करण निर्दिष्ट करते हैं।

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – नई फ़ाइल का पूर्ण पाथ।  
- **Color Mode** – `Indexed` Aspose.PSD को बताता है कि वह पैलेट‑आधारित इमेज उपयोग करे।  
- **Version** – PSD फ़ॉर्मेट संस्करण (5 अधिकांश आधुनिक Photoshop संस्करणों के लिए काम करता है)।

## Step 4: Create a Color Palette (Generate PSD Color Palette)
इंडेक्स्ड इमेज में उपलब्ध रंगों को परिभाषित करें।

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- `palette` एरे में अधिकतम 256 `Color` ऑब्जेक्ट्स रखे जा सकते हैं।  
- `CompressionMethod.RLE` इंडेक्स्ड इमेजेस के लिए प्रभावी लॉसलेस कंप्रेशन प्रदान करता है।

## Step 5: Create the PSD Image Canvas
अब हम इच्छित आयामों के साथ एक खाली PSD बनाते हैं।

```java
Image psd = Image.create(createOptions, 500, 500);
```

यह 500 × 500 पिक्सेल का कैनवास बनाता है जो पहले परिभाषित पैलेट का उपयोग करता है।

## Step 6: Draw Graphics on the PSD
विज़ुअल कंटेंट जोड़ें—यहाँ हम सफ़ेद बैकग्राउंड पर एक साधारण लाल अंडाकार ड्रॉ करते हैं।

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` बैकग्राउंड को सफ़ेद से भरता है।  
- `drawEllipse` 6‑पिक्सेल स्ट्रोक के साथ एक लाल अंडाकार रेंडर करता है।

## Step 7: Save the PSD File
अंत में, इमेज को डिस्क पर सहेजें।

```java
psd.save();
```

फ़ाइल `Newsample_out.psd` उस डायरेक्टरी में दिखाई देगी जिसे आपने पहले निर्दिष्ट किया था।

## Common Issues & Tips
- **Palette Size** – यदि आपको 4 से अधिक रंगों की आवश्यकता है, तो बस उन्हें `palette` एरे में जोड़ें (अधिकतम 256)।  
- **File Permissions** – सुनिश्चित करें कि Java प्रोसेस को `dataDir` पर लिखने की अनुमति है।  
- **Incorrect Color Mode** – यदि आप `createOptions.setColorMode(ColorModes.Indexed)` को भूल जाते हैं तो यह एक RGB PSD बनाएगा, न कि indexed।  

## Frequently Asked Questions

**Q: Aspose.PSD for Java क्या है?**  
A: Aspose.PSD for Java एक लाइब्रेरी है जो Java का उपयोग करके प्रोग्रामेटिक रूप से PSD (Photoshop) फ़ाइलों को मैनीपुलेट करने में सक्षम बनाती है।

**Q: क्या मैं Aspose.PSD को मुफ्त में उपयोग कर सकता हूँ?**  
A: हाँ, आप Aspose.PSD का फ्री ट्रायल संस्करण **[here](https://releases.aspose.com/)** से एक्सेस कर सकते हैं।

**Q: क्या Aspose.PSD के साथ काम करने के लिए मुझे Photoshop इंस्टॉल करना आवश्यक है?**  
A: नहीं, आप Photoshop के बिना भी PSD फ़ाइलें बना और मैनीपुलेट कर सकते हैं, क्योंकि Aspose.PSD सभी ऑपरेशन्स स्वतंत्र रूप से संभालता है।

**Q: Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त करें?**  
A: आप अस्थायी लाइसेंस **[here](https://purchase.aspose.com/temporary-license/)** से अनुरोध कर सकते हैं।

**Q: Aspose.PSD के लिए समर्थन कहाँ प्राप्त कर सकते हैं?**  
A: आप Aspose फ़ोरम **[here](https://forum.aspose.com/c/psd/34)** से समर्थन प्राप्त कर सकते हैं।

## Conclusion
आपने अभी-अभी **PSD फ़ाइलें कैसे बनाएं** को indexed कलर मोड के साथ सीखा, एक कस्टम पैलेट जेनरेट किया, और सरल ग्राफ़िक्स जोड़े—सब कुछ Aspose.PSD for Java का उपयोग करके। इन बिल्डिंग ब्लॉक्स के साथ आप अधिक जटिल ड्रॉइंग्स, लेयर मैनेजमेंट, और बैच प्रोसेसिंग की ओर विस्तार कर सकते हैं। गहरी खोज के लिए, आधिकारिक API रेफ़रेंस **[here](https://reference.aspose.com/psd/java/)** देखें और विभिन्न पैलेट्स और ड्रॉइंग प्रिमिटिव्स के साथ प्रयोग करते रहें।

---

**अंतिम अपडेट:** 2026-03-15  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.12 (latest)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}