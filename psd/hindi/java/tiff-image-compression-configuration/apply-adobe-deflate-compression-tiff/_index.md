---
title: TIFF में Adobe Deflate Compression लागू करें - Java
linktitle: TIFF में Adobe Deflate Compression लागू करें - Java
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java का उपयोग करके TIFF छवियों पर Adobe Deflate संपीड़न लागू करना सीखें। कुशल छवि प्रसंस्करण के लिए चरण-दर-चरण मार्गदर्शिका।
weight: 12
url: /hi/java/tiff-image-compression-configuration/apply-adobe-deflate-compression-tiff/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# TIFF में Adobe Deflate Compression लागू करें - Java

## परिचय

क्या आपने कभी सोचा है कि गुणवत्ता से समझौता किए बिना अपनी TIFF छवियों को कुशलतापूर्वक कैसे संपीड़ित किया जाए? यदि आप बड़ी छवि फ़ाइलों से निपट रहे हैं, तो आप शायद धीमी लोडिंग समय और भंडारण समस्याओं के दर्द को जानते होंगे। यहीं पर Adobe Deflate संपीड़न काम आता है, और Aspose.PSD for Java के साथ, आप इसे आसानी से अपनी परियोजनाओं में लागू कर सकते हैं। यह ट्यूटोरियल आपको TIFF छवि पर Adobe Deflate संपीड़न को चरण दर चरण लागू करने के बारे में बताएगा। शुरू करने के लिए तैयार हैं? चलिए शुरू करते हैं!

## आवश्यक शर्तें

इससे पहले कि हम वास्तविक कोड में कूदें, आइए सुनिश्चित करें कि आपने सब कुछ सेट कर लिया है। आपको ये चाहिए:

1. जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके मशीन पर JDK का नवीनतम संस्करण स्थापित है।
2.  Aspose.PSD for Java: Aspose.PSD for Java लाइब्रेरी को अपने प्रोजेक्ट में डाउनलोड और एकीकृत करें। आप इसे यहाँ से प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
3. विकास पर्यावरण: एक IDE जैसे IntelliJ IDEA, Eclipse, या NetBeans.
4.  अस्थायी लाइसेंस (वैकल्पिक): यदि आप खरीदने के लिए तैयार नहीं हैं, तो आप प्राप्त कर सकते हैं[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) सुविधाओं को आज़माने के लिए.

## पैकेज आयात करें

आइए अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करके शुरू करें। ये आयात महत्वपूर्ण हैं क्योंकि वे आपको Aspose.PSD लाइब्रेरी और जावा उपयोगिताओं के साथ काम करने की अनुमति देते हैं।

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.TiffRational;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.fileformats.tiff.enums.TiffPlanarConfigs;
import com.aspose.psd.fileformats.tiff.enums.TiffResolutionUnits;
import com.aspose.psd.imageoptions.TiffOptions;
```

अब जबकि हमने मूल बातें जान ली हैं, तो आइए इस प्रक्रिया को आसान चरणों में विभाजित करें।

## चरण 1: TIFF विकल्प सेट करें

 सबसे पहली बात, आपको इसका एक उदाहरण बनाना होगा`TiffOptions` और इसे अपनी ज़रूरतों के हिसाब से कॉन्फ़िगर करें। ये विकल्प परिभाषित करते हैं कि TIFF फ़ाइल को कैसे प्रोसेस किया जाएगा, जिसमें इसका रिज़ॉल्यूशन, रंग योजना और संपीड़न शामिल है।

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
```

यहाँ, हम एक बना रहे हैं`TiffOptions` ऑब्जेक्ट को डिफ़ॉल्ट प्रारूप में बदलें। लेकिन यह तो बस शुरुआत है! 

## चरण 2: छवि गुण कॉन्फ़िगर करें

 इसके बाद, आपको TIFF छवि के विभिन्न गुण सेट करने होंगे, जैसे`BitsPerSample`, `Photometric`, `Resolution` , और`PlanarConfiguration`ये सेटिंग्स यह निर्धारित करती हैं कि छवि डेटा कैसे संग्रहीत और प्रदर्शित किया जाए।

```java
int[] ushort = { 8, 8, 8 };
options.setBitsPerSample(ushort);
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
```

प्रत्येक संपत्ति क्या करती है, यहां बताया गया है:
- बिट्सपरसैंपल: प्रत्येक रंग चैनल के लिए प्रति सैंपल बिट्स की संख्या निर्धारित करता है।
- फोटोमेट्रिक: रंग मॉडल को परिभाषित करता है (इस मामले में, RGB).
- रिज़ॉल्यूशन: छवि के क्षैतिज और ऊर्ध्वाधर रिज़ॉल्यूशन को निर्दिष्ट करता है।
- प्लानर कॉन्फ़िगरेशन: यह निर्धारित करता है कि पिक्सेल डेटा कैसे संग्रहीत किया जाता है।

## चरण 3: एडोब डिफ्लेट कम्प्रेशन लागू करें

अब जादू की बारी है! आप अपनी TIFF इमेज पर Adobe Deflate कम्प्रेशन लागू करेंगे, जो इमेज की गुणवत्ता खोए बिना फ़ाइल का आकार कम करने में मदद करता है।

```java
options.setCompression(TiffCompressions.AdobeDeflate);
```

एडोब डिफ्लेट एक दोषरहित संपीड़न विधि है जो उन छवियों के लिए एकदम उपयुक्त है जहां आपको फ़ाइल आकार को कम करते हुए उच्च गुणवत्ता बनाए रखने की आवश्यकता होती है।

## चरण 4: TIFF छवि बनाएं और संपादित करें

विकल्प सेट होने के बाद, अब एक नई TIFF छवि बनाने और उसमें बदलाव करने का समय है। इस चरण में, हम एक सरल 100x100 छवि बनाएंगे और इसे लाल पिक्सेल से भरेंगे।

```java
PsdImage tiffImage = new PsdImage(100, 100);

for (int j = 0; j < tiffImage.getHeight(); j++) {
    for (int i = 0; i < tiffImage.getWidth(); i++) {
        tiffImage.setPixel(i, j, Color.getRed());
    }
}
```

यहाँ, हम छवि के प्रत्येक पिक्सेल को लूप कर रहे हैं और उसका रंग लाल पर सेट कर रहे हैं। बेशक, आप अधिक जटिल छवियाँ बनाने के लिए इस भाग को कस्टमाइज़ कर सकते हैं।

## चरण 5: संपीड़ित TIFF छवि सहेजें

अंत में, छवि को कॉन्फ़िगर करने और बनाने के बाद, अंतिम चरण इसे लागू संपीड़न के साथ सहेजना है। सुनिश्चित करें कि आपने सही निर्देशिका पथ निर्दिष्ट किया है।

```java
String dataDir = "Your Document Directory";
tiffImage.save(dataDir + "TIFFwithAdobeDeflateCompression_output.tif");
```

बस! आपने Aspose.PSD for Java का उपयोग करके TIFF छवि पर Adobe Deflate संपीड़न सफलतापूर्वक लागू कर दिया है।

## निष्कर्ष

और अब यह हो गया! Aspose.PSD for Java के साथ TIFF इमेज पर Adobe Deflate कम्प्रेशन लागू करना एक सीधी प्रक्रिया है। चाहे आप अपनी वेबसाइट, डिजिटल मीडिया या किसी अन्य प्रोजेक्ट के लिए बड़ी इमेज के साथ काम कर रहे हों, यह विधि सुनिश्चित करती है कि आपकी फ़ाइलें उच्च-गुणवत्ता वाली बनी रहें और आकार में अधिक प्रबंधनीय हों। Aspose.PSD for Java की शक्ति इसकी सरलता और दक्षता में निहित है, जो इसे जटिल छवि प्रारूपों के साथ काम करने वाले डेवलपर्स के लिए एक उपयोगी उपकरण बनाती है।

## अक्सर पूछे जाने वाले प्रश्न

### एडोब डिफ्लेट संपीड़न क्या है?
एडोब डिफ्लेट एक दोषरहित संपीड़न विधि है जिसका उपयोग गुणवत्ता खोए बिना TIFF छवियों के आकार को कम करने के लिए किया जाता है।

### क्या मैं Java के लिए Aspose.PSD के साथ अन्य संपीड़न विधियों का उपयोग कर सकता हूँ?
हां, Aspose.PSD LZW, CCITT, और JPEG जैसे विभिन्न संपीड़न विधियों का समर्थन करता है।

### क्या Aspose.PSD लाइब्रेरी निःशुल्क है?
 Aspose.PSD एक निःशुल्क परीक्षण प्रदान करता है, लेकिन पूर्ण कार्यक्षमता के लिए लाइसेंस की आवश्यकता होती है। आप एक प्राप्त कर सकते हैं[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) इसे आज़माने के लिए.

### रिज़ॉल्यूशन सेटिंग TIFF छवि को कैसे प्रभावित करती है?
रिज़ॉल्यूशन, प्रिंट या डिस्प्ले के समय छवि की स्पष्टता निर्धारित करता है। उच्च रिज़ॉल्यूशन बेहतर गुणवत्ता प्रदान करते हैं, लेकिन इसके परिणामस्वरूप फ़ाइल का आकार बड़ा हो जाता है।

### क्या मैं Java के लिए Aspose.PSD के साथ अन्य छवि प्रारूपों में हेरफेर कर सकता हूं?
बिल्कुल! Aspose.PSD PSD, PNG, JPEG, आदि जैसे विभिन्न प्रारूपों का समर्थन करता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
