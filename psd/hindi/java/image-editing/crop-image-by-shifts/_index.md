---
date: 2026-07-03
description: Aspose.PSD for Java का उपयोग करके Crop Image Java कैसे करें, सीखें। यह
  step‑by‑step image cropping ट्यूटोरियल PSD फ़ाइलों को लोड करने, शिफ्ट मान सेट करने,
  और saving the result को कवर करता है।
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: शिफ्ट द्वारा Crop Image
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD के साथ शिफ्ट द्वारा Crop Image Java
url: /hi/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# शिफ्ट्स के साथ Aspose.PSD द्वारा जावा में इमेज क्रॉप करें

## परिचय

जावा इमेज प्रोसेसिंग में, **crop image java** ग्राफिक्स, थंबनेल या UI एसेट्स तैयार करने के लिए एक सामान्य आवश्यकता है। Aspose.PSD for Java इस कार्य को सरल बनाता है, क्योंकि यह किसी भी समर्थित रास्टर फ़ॉर्मेट पर काम करने वाला सरल `crop` मेथड प्रदान करता है। इस ट्यूटोरियल में आप सीखेंगे कि PSD फ़ाइल को कैसे लोड करें, बाएँ‑दाएँ‑ऊपर‑नीचे शिफ्ट मान निर्धारित करें, क्रॉप लागू करें, और परिणाम को सहेजें—बिना कस्टम पिक्सेल‑मैनीपुलेशन कोड लिखे।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी क्रॉपिंग को संभालती है?** Aspose.PSD for Java एक बिल्ट‑इन `crop` मेथड प्रदान करती है।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक टेम्पररी लाइसेंस काम करता है; प्रोडक्शन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **समर्थित फ़ॉर्मेट?** 30 से अधिक रास्टर फ़ॉर्मेट, जिसमें PSD, JPEG, PNG, BMP, और TIFF शामिल हैं।  
- **अधिकतम फ़ाइल आकार?** पूरी इमेज को मेमोरी में लोड किए बिना 2 GB तक की फ़ाइलें संभालता है।  
- **कोड की कितनी लाइनों की आवश्यकता?** केवल पाँच तार्किक चरण—लोड, कैश, शिफ्ट निर्धारित करें, क्रॉप, और सहेजें।

## crop image java क्या है?
`crop image java` जावा एप्लिकेशन में बिटमैप को ट्रिम करने की प्रक्रिया को दर्शाता है। Aspose.PSD का उपयोग करके यह ऑपरेशन `crop` मेथड द्वारा किया जाता है, जो इमेज के प्रत्येक पक्ष के लिए शिफ्ट मान लेता है और एक नई इमेज इंस्टेंस लौटाता है।

## इमेज क्रॉपिंग के लिए Aspose.PSD क्यों उपयोग करें?
Aspose.PSD **30+** इमेज फ़ॉर्मेट का समर्थन करता है और कई‑सौ‑पृष्ठों वाले PSD फ़ाइलों को 150 MB से कम RAM में प्रोसेस कर सकता है, इसके लेज़ी‑लोडिंग आर्किटेक्चर के कारण। लाइब्रेरी पिक्सेल‑परफेक्ट परिणाम की गारंटी देती है, लेयर्स, मास्क और कलर प्रोफ़ाइल को संरक्षित रखते हुए—जो कई सामान्य इमेज लाइब्रेरी नहीं कर पातीं।

## आवश्यकताएँ

### जावा डेवलपमेंट किट (JDK)

सुनिश्चित करें कि आपके सिस्टम पर नवीनतम संस्करण का JDK स्थापित है। आप इसे [here](https://www.oracle.com/java/technologies/javase-downloads.html) से डाउनलोड कर सकते हैं।

### Aspose.PSD for Java लाइब्रेरी

शुरू करने के लिए, आपको Aspose.PSD for Java लाइब्रेरी प्राप्त करनी होगी। नवीनतम संस्करण के लिए [download page](https://releases.aspose.com/psd/java/) पर जाएँ।

### इंटीग्रेटेड डेवलपमेंट एनवायरनमेंट (IDE)

एक सुगम कोडिंग अनुभव के लिए अपना पसंदीदा जावा IDE चुनें, जैसे Eclipse या IntelliJ।

## इमेज को जावा में कैसे क्रॉप करें?

अपने स्रोत फ़ाइल को लोड करें, प्रत्येक पक्ष के लिए पिक्सेल शिफ्ट निर्धारित करें, और `crop` मेथड को कॉल करें—यह पूरा वर्कफ़्लो पाँच संक्षिप्त कोड लाइनों में लिखा जा सकता है। `crop` ऑपरेशन एक नई इमेज बनाता है जिसमें केवल निर्दिष्ट क्षेत्र होता है, जबकि मूल फ़ाइल अपरिवर्तित रहती है।

### चरण 1: इमेज लोड करें

`Image` Aspose.PSD में सभी इमेज प्रकारों के लिए बेस क्लास है।  
`RasterImage` रास्टर इमेज को दर्शाता है और क्रॉपिंग क्षमता प्रदान करता है।  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### चरण 2: इमेज डेटा कैश करें

`cacheData()` इमेज डेटा को तेज़ प्रोसेसिंग के लिए मेमोरी में लोड करता है।  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### चरण 3: शिफ्ट मान निर्धारित करें

इमेज के चारों पक्ष (बाएँ, ऊपर, दाएँ, नीचे) के लिए पिक्सेल में शिफ्ट मान निर्दिष्ट करें।  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### चरण 4: क्रॉपिंग लागू करें

`crop(left, right, top, bottom)` प्रत्येक पक्ष पर निर्दिष्ट पिक्सेल शिफ्ट के अनुसार इमेज को ट्रिम करता है।  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### चरण 5: परिणाम सहेजें

`JpegOptions` JPEG एन्कोडिंग सेटिंग्स जैसे क्वालिटी और कलर प्रोफ़ाइल को परिभाषित करता है।  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके सफलतापूर्वक इमेज को क्रॉप कर लिया है।

## सामान्य समस्याएँ और समाधान

- **इमेज अपरिवर्तित दिखती है:** सुनिश्चित करें कि शिफ्ट मान सकारात्मक हैं और मूल आयामों से अधिक नहीं हैं।  
- **बड़ी फ़ाइलों पर OutOfMemoryError:** चरण 2 में दिखाए अनुसार कैशिंग सक्षम करें; इससे Aspose.PSD पूरी इमेज को RAM में रखने के बजाय एक टेम्पररी फ़ाइल का उपयोग करता है।  
- **क्रॉपिंग के बाद कलर शिफ्ट:** यदि आपको सटीक कलर फ़िडेलिटी चाहिए तो `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` कॉल करके कलर प्रोफ़ाइल को संरक्षित रखें।

## अक्सर पूछे जाने वाले प्रश्न

**प्र: क्या Aspose.PSD सभी इमेज फ़ॉर्मेट के साथ संगत है?**  
उ: हाँ, Aspose.PSD 30 से अधिक रास्टर फ़ॉर्मेट का समर्थन करता है, जिसमें PSD, JPEG, PNG, BMP, TIFF, और GIF शामिल हैं, जिससे व्यापक संगतता मिलती है।

**प्र: क्या मैं एक ही इमेज पर कई क्रॉपिंग ऑपरेशन लागू कर सकता हूँ?**  
उ: बिल्कुल। प्रत्येक `crop` कॉल के बाद आपको एक नई इमेज ऑब्जेक्ट मिलता है, जिसे आप आवश्यकता अनुसार फिर से क्रॉप कर सकते हैं।

**प्र: क्या Aspose.PSD समर्थन के लिए कोई कम्युनिटी फ़ोरम है?**  
उ: हाँ, आप [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) पर समर्थन प्राप्त कर सकते हैं और कम्युनिटी के साथ जुड़ सकते हैं।

**प्र: Aspose.PSD के लिए टेम्पररी लाइसेंस कैसे प्राप्त करूँ?**  
उ: टेम्पररी लाइसेंस प्राप्त करने के लिए [here](https://purchase.aspose.com/temporary-license/) पर जाएँ।

**प्र: क्या Aspose.PSD की कार्यक्षमताओं को दर्शाने वाले सैंपल प्रोजेक्ट उपलब्ध हैं?**  
उ: दस्तावेज़ीकरण और उदाहरणों को देखें: [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/)।

---

**अंतिम अपडेट:** 2026-07-03  
**परीक्षित संस्करण:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## संबंधित ट्यूटोरियल

- [Aspose.PSD for Java में आयत द्वारा इमेज क्रॉप करें](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image Java - Aspose.PSD for Java के साथ इमेज को विस्तारित और क्रॉप करें](/psd/java/image-editing/expand-and-crop-images/)
- [Resize Image Java - Aspose.PSD for Java में Resize Type Enumeration का उपयोग](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}