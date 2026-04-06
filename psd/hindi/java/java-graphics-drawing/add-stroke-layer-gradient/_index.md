---
date: 2026-01-14
description: Aspose.PSD for Java का उपयोग करके इस चरण‑दर‑चरण ट्यूटोरियल के साथ PSD
  फ़ाइलों में ग्रेडिएंट स्ट्रोक लेयर बनाना और स्ट्रोक ग्रेडिएंट को कस्टमाइज़ करना
  सीखें।
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: जावा में ग्रेडिएंट स्ट्रोक लेयर कैसे बनाएं
url: /hi/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में Gradient Stroke Layer कैसे बनाएं

## परिचय
क्या आपने कभी सोचा है कि **gradient stroke layer** को अपने PSD फ़ाइलों में Java का उपयोग करके कैसे बनाएं? आप सही जगह पर हैं! आज हम Aspose.PSD for Java में डुबकी लगाएंगे—एक शक्तिशाली लाइब्रेरी जो आपको PSD फ़ाइलों को आसानी से मैनिपुलेट करने देती है। चाहे आप ग्राफ़िक्स प्रोग्रामिंग में नए हों या मौजूदा डिज़ाइनों को फाइन‑ट्यून करना चाहते हों, यह गाइड आपको स्टेप‑बाय‑स्टेप स्ट्रोक ग्रेडिएंट जोड़ने और कस्टमाइज़ करने के माध्यम से ले जाएगा।

## त्वरित उत्तर
- **मुख्य लक्ष्य क्या है?** PSD फ़ाइल पर एक gradient stroke layer बनाना।  
- **कौन सी लाइब्रेरी आवश्यक है?** Aspose.PSD for Java।  
- **क्या मुझे लाइसेंस चाहिए?** हाँ, उत्पादन के लिए एक वैध (या अस्थायी) लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण काम करता है?** Java 8 या उससे ऊपर।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बुनियादी gradient stroke के लिए लगभग 10‑15 मिनट।

## ग्रेडिएंट स्ट्रोक लेयर क्या है?
एक ग्रेडिएंट स्ट्रोक लेयर एक वेक्टर आउटलाइन है जो किसी आकार या टेक्स्ट के चारों ओर होती है और रंगों के बीच सुगमता से ट्रांज़िशन करती है। Aspose.PSD का उपयोग करके आप प्रोग्रामेटिकली स्ट्रोक के रंग, अपारदर्शिता, कोण, और प्रकार (linear, radial, आदि) को परिभाषित कर सकते हैं।

## क्यों उपयोग करें Aspose.PSD for Java?
- **पूर्ण PSD समर्थन** – Photoshop के बिना PSD फ़ाइलें पढ़ें, संपादित करें और लिखें।  
- **समृद्ध इफ़ेक्ट API** – स्ट्रोक, शैडो, ग्लो और कई अन्य लेयर इफ़ेक्ट्स तक पहुंच।  
- **क्रॉस‑प्लेटफ़ॉर्म** – किसी भी OS पर काम करता है जो Java सपोर्ट करता है।  
- **कोई नेटिव डिपेंडेंसी नहीं** – शुद्ध Java, CI पाइपलाइनों में आसानी से इंटीग्रेट।  

## पूर्वापेक्षाएँ
1. **Java Development Kit (JDK)** – नवीनतम JDK को [Oracle की वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html) से इंस्टॉल करें।  
2. **Aspose.PSD for Java** – लाइब्रेरी को [Aspose.PSD डाउनलोड पेज](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
3. **IDE** – IntelliJ IDEA, Eclipse, या NetBeans।  
4. **लाइसेंस** – यदि आपके पास पूर्ण लाइसेंस नहीं है तो एक [अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) प्राप्त करें।

## पैकेज इम्पोर्ट करें
पहले, उन क्लासेज़ को इम्पोर्ट करें जिनकी हमें PSD लोड करने, इफ़ेक्ट्स एक्सेस करने, और ग्रेडिएंट फ़िल सेट करने के लिए आवश्यकता होगी।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

अब प्रक्रिया को स्पष्ट चरणों में विभाजित करते हैं।

## चरण 1: PSD फ़ाइल लोड करें
हम स्रोत PSD को लोड करते हैं और इफ़ेक्ट रिसोर्सेज़ को सक्षम करते हैं ताकि स्ट्रोक इफ़ेक्ट उपलब्ध हो।

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## चरण 2: स्ट्रोक इफ़ेक्ट एक्सेस करें
मान लेते हैं कि वह स्ट्रोक जिसे हम संशोधित करना चाहते हैं, तीसरी लेयर (इंडेक्स 2) से संबंधित है, हम उसका `StrokeEffect` प्राप्त करते हैं।

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## चरण 3: स्ट्रोक इफ़ेक्ट प्रॉपर्टीज़ की जाँच करें
परिवर्तन करने से पहले, हम मौजूदा सेटिंग्स की पुष्टि करते हैं ताकि हमें ठीक‑ठीक पता हो कि हम क्या अपडेट कर रहे हैं।

```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```

## चरण 4: ग्रेडिएंट फ़िल सेटिंग्स संशोधित करें
यहाँ हम रंग, अपारदर्शिता, ब्लेंड मोड, और अन्य प्रॉपर्टीज़ को बदलते हैं ताकि इच्छित लुक प्राप्त हो सके।

```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```

## चरण 5: रंग और ट्रांसपेरेंसी पॉइंट्स जोड़ें और संशोधित करें
हम नए रंग और ट्रांसपेरेंसी पॉइंट्स जोड़ते हैं, फिर मौजूदा पॉइंट्स को समायोजित करके ग्रेडिएंट को आकार देते हैं।

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## चरण 6: संशोधित PSD फ़ाइल सहेजें
सभी समायोजन के बाद, हम अपडेटेड फ़ाइल को डिस्क पर वापस लिखते हैं।

```java
im.save(exportPath);
```

## चरण 7: संशोधनों की पुष्टि करें
सहेजी गई फ़ाइल को लोड करें और यह सुनिश्चित करें कि हर प्रॉपर्टी हमारे द्वारा किए गए बदलावों को दर्शाती है।

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## निष्कर्ष
अब आप जानते हैं कि Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में **gradient stroke layer** इफ़ेक्ट्स कैसे बनाएं। एक PSD लोड करके, स्ट्रोक इफ़ेक्ट एक्सेस करके, ग्रेडिएंट फ़िल सेटिंग्स को ट्यून करके, और परिणाम को सहेजकर, आप बिना Photoshop खोले ही प्रोग्रामेटिकली प्रोफेशनल‑ग्रेड ग्राफ़िक्स बना सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न
### Aspose.PSD for Java क्या है?
Aspose.PSD for Java एक लाइब्रेरी है जो डेवलपर्स को Java एप्लिकेशन्स में PSD फ़ाइलों के साथ काम करने की सुविधा देती है, जिससे PSD फ़ाइलें बनाने, मैनिपुलेट करने और कनवर्ट करने की क्षमताएँ मिलती हैं।

### क्या मुझे Aspose.PSD for Java उपयोग करने के लिए लाइसेंस चाहिए?
हाँ, Aspose.PSD for Java उपयोग करने के लिए एक वैध लाइसेंस आवश्यक है। आप मूल्यांकन के लिए एक [अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

### क्या मैं Aspose.PSD for Java से शून्य से PSD फ़ाइलें बना सकता हूँ?
बिल्कुल! Aspose.PSD for Java व्यापक APIs प्रदान करता है जिससे आप प्रोग्रामेटिकली PSD फ़ाइलें बना और मैनिपुलेट कर सकते हैं।

### क्या Aspose.PSD for Java के साथ अन्य इफ़ेक्ट्स लागू करना संभव है?
हाँ, आप Aspose.PSD for Java का उपयोग करके शैडो, ग्लो और कई अन्य इफ़ेक्ट्स लागू कर सकते हैं।

### Aspose.PSD for Java की डॉक्यूमेंटेशन कहाँ मिल सकती है?
आप डॉक्यूमेंटेशन [यहाँ](https://reference.aspose.com/psd/java/) पा सकते हैं।

---

**अंतिम अपडेट:** 2026-01-14  
**परीक्षण किया गया:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
