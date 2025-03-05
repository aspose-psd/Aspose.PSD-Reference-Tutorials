---
title: जावा में स्ट्रोक लेयर ग्रेडिएंट कैसे जोड़ें
linktitle: जावा में स्ट्रोक लेयर ग्रेडिएंट कैसे जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: इस व्यापक चरण-दर-चरण ट्यूटोरियल के साथ Java के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में स्ट्रोक लेयर ग्रेडिएंट को जोड़ने और अनुकूलित करने का तरीका जानें।
type: docs
weight: 10
url: /hi/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## परिचय
क्या आपने कभी सोचा है कि Java का उपयोग करके अपनी छवियों में स्ट्रोक लेयर ग्रेडिएंट कैसे जोड़ा जाए? खैर, आप सही जगह पर हैं! आज, हम Aspose.PSD for Java की दुनिया में गोता लगा रहे हैं, एक शक्तिशाली लाइब्रेरी जो आपको PSD फ़ाइलों को आसानी से हेरफेर करने में मदद करती है। चाहे आप शुरुआती हों या अनुभवी डेवलपर, यह चरण-दर-चरण मार्गदर्शिका आपको अपनी PSD फ़ाइलों में स्ट्रोक लेयर ग्रेडिएंट जोड़ने की प्रक्रिया से गुज़ारेगी। तो, तैयार हो जाइए और अपने ग्राफ़िक संपादन कौशल को बढ़ाने के लिए तैयार हो जाइए!
## आवश्यक शर्तें
शुरू करने से पहले, कुछ चीजें हैं जो आपको तैयार रखनी होंगी। सुनिश्चित करें कि आपके पास निम्नलिखित चीजें हैं:
1.  जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके सिस्टम पर JDK इंस्टॉल है। आप इसे यहाँ से डाउनलोड कर सकते हैं[ओरेकल की वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java लाइब्रेरी: आप इसे यहाँ से डाउनलोड कर सकते हैं[Aspose.PSD डाउनलोड पृष्ठ](https://releases.aspose.com/psd/java/).
3. एकीकृत विकास परिवेश (आईडीई): कोई भी आईडीई जैसे इंटेलीज आईडीईए, एक्लिप्स या नेटबीन्स काम करेगा।
4.  वैध लाइसेंस: आप प्राप्त कर सकते हैं[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) यदि आपके पास पूरा नहीं है।
## पैकेज आयात करें
सबसे पहले, आइए आवश्यक पैकेज आयात करें। ये हमें PSD फ़ाइल में हेरफेर करने के लिए आवश्यक क्लासेस और विधियों का उपयोग करने में सक्षम करेंगे।
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
अब, बेहतर समझ के लिए आइए इस उदाहरण को कई चरणों में विभाजित करें।
## चरण 1: PSD फ़ाइल लोड करें
 सबसे पहले, हमें उस PSD फ़ाइल को लोड करना होगा जिसे हम संशोधित करना चाहते हैं।`PsdLoadOptions` यह निर्दिष्ट करने के लिए कि हम प्रभाव संसाधन लोड करना चाहते हैं।
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## चरण 2: स्ट्रोक प्रभाव तक पहुंचें
इसके बाद, हमें उस परत के स्ट्रोक प्रभाव तक पहुंचने की आवश्यकता है जिसमें हम रुचि रखते हैं। यहां, हम मानते हैं कि यह PSD फ़ाइल में तीसरी परत (सूचकांक 2) है।
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## चरण 3: स्ट्रोक प्रभाव गुणों को सत्यापित करें
कोई भी परिवर्तन करने से पहले, आइए स्ट्रोक प्रभाव के गुणों को सत्यापित करें ताकि यह सुनिश्चित हो सके कि हम सही सेटिंग्स संशोधित कर रहे हैं।
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
## चरण 4: ग्रेडिएंट भरण सेटिंग संशोधित करें
अब, अपनी आवश्यकताओं के अनुसार ग्रेडिएंट फिल सेटिंग्स को संशोधित करने का समय आ गया है। हम रंग, अपारदर्शिता, ब्लेंड मोड और अन्य गुण बदलेंगे।
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
## चरण 5: रंग और पारदर्शिता बिंदु जोड़ें और संशोधित करें
आइए, वांछित ग्रेडिएंट प्रभाव प्राप्त करने के लिए नए रंग और पारदर्शिता बिंदु जोड़ें तथा मौजूदा बिंदुओं को संशोधित करें।
```java
// नया रंग बिंदु जोड़ें
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// पिछले बिंदु का स्थान बदलें
fillSettings.getColorPoints()[1].setLocation(1899);
// नया पारदर्शिता बिंदु जोड़ें
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// पिछले पारदर्शिता बिंदु का स्थान बदलें
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## चरण 6: संशोधित PSD फ़ाइल सहेजें
सभी आवश्यक संशोधन करने के बाद, हमें PSD फ़ाइल को सेव करना होगा।
```java
im.save(exportPath);
```
## चरण 7: संशोधनों को सत्यापित करें
अंत में, आइए सहेजी गई PSD फ़ाइल को लोड करें और सत्यापित करें कि हमारे परिवर्तन सही ढंग से लागू किए गए हैं।
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// रंग बिन्दुओं की जाँच करें
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
// पारदर्शिता बिंदुओं की जाँच करें
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
और अब यह हो गया! अब आप जानते हैं कि Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में स्ट्रोक लेयर ग्रेडिएंट कैसे जोड़ें और उसमें हेरफेर करें। इस ट्यूटोरियल में PSD फ़ाइल लोड करना, स्ट्रोक इफ़ेक्ट को एक्सेस करना और संशोधित करना, और परिवर्तनों को सहेजना शामिल है। इन कौशलों के साथ, आप दिखने में आकर्षक ग्रेडिएंट बना सकते हैं और अपनी PSD फ़ाइलों को अपनी ज़रूरतों के हिसाब से कस्टमाइज़ कर सकते हैं।
## अक्सर पूछे जाने वाले प्रश्न
### Java के लिए Aspose.PSD क्या है?
Aspose.PSD for Java एक लाइब्रेरी है जो डेवलपर्स को जावा अनुप्रयोगों में PSD फाइलों के साथ काम करने की अनुमति देती है, PSD फाइलों को बनाने, हेरफेर करने और परिवर्तित करने की सुविधाएँ प्रदान करती है।
### क्या मुझे Java के लिए Aspose.PSD का उपयोग करने के लिए लाइसेंस की आवश्यकता है?
 हां, आपको Java के लिए Aspose.PSD का उपयोग करने के लिए एक वैध लाइसेंस की आवश्यकता है। आप एक प्राप्त कर सकते हैं[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) मूल्यांकन प्रयोजनों के लिए।
### क्या मैं स्क्रैच से PSD फ़ाइलें बनाने के लिए Aspose.PSD for Java का उपयोग कर सकता हूँ?
बिल्कुल! Aspose.PSD for Java PSD फ़ाइलों को प्रोग्रामेटिक रूप से बनाने और उनमें हेरफेर करने के लिए व्यापक API प्रदान करता है।
### क्या Java के लिए Aspose.PSD का उपयोग करके अन्य प्रभाव लागू करना संभव है?
हां, आप Java के लिए Aspose.PSD का उपयोग करके छाया, चमक और अधिक जैसे विभिन्न प्रभाव लागू कर सकते हैं।
### मैं Java के लिए Aspose.PSD का दस्तावेज़ कहां पा सकता हूं?
 आप दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/psd/java/).