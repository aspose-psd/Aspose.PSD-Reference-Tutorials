---
title: जावा में स्ट्रोक लेयर ग्रेडिएंट कैसे जोड़ें
linktitle: जावा में स्ट्रोक लेयर ग्रेडिएंट कैसे जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: इस व्यापक चरण-दर-चरण ट्यूटोरियल के साथ जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में स्ट्रोक लेयर ग्रेडिएंट्स को जोड़ना और अनुकूलित करना सीखें।
type: docs
weight: 10
url: /hi/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## परिचय
क्या आपने कभी सोचा है कि जावा का उपयोग करके अपनी छवियों में स्ट्रोक लेयर ग्रेडिएंट कैसे जोड़ें? खैर, आप सही जगह पर हैं! आज, हम जावा के लिए Aspose.PSD की दुनिया में गोता लगा रहे हैं, एक शक्तिशाली लाइब्रेरी जो आपको PSD फ़ाइलों को आसानी से प्रबंधित करने में मदद करती है। चाहे आप शुरुआती हों या अनुभवी डेवलपर, यह चरण-दर-चरण मार्गदर्शिका आपको अपनी PSD फ़ाइलों में स्ट्रोक लेयर ग्रेडिएंट जोड़ने की प्रक्रिया के बारे में बताएगी। तो, कमर कस लें और अपने ग्राफिक संपादन कौशल को बढ़ाने के लिए तैयार हो जाएं!
## आवश्यक शर्तें
इससे पहले कि हम शुरुआत करें, कुछ चीजें हैं जिनका आपको ध्यान रखना होगा। सुनिश्चित करें कि आपके पास निम्नलिखित हैं:
1.  जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[ओरेकल की वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  जावा लाइब्रेरी के लिए Aspose.PSD: आप इसे यहां से डाउनलोड कर सकते हैं[Aspose.PSD डाउनलोड पृष्ठ](https://releases.aspose.com/psd/java/).
3. एक एकीकृत विकास पर्यावरण (आईडीई): IntelliJ IDEA, Eclipse, या NetBeans जैसी कोई भी IDE काम करेगी।
4.  एक वैध लाइसेंस: आप प्राप्त कर सकते हैं[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) यदि आपके पास पूरा नहीं है।
## पैकेज आयात करें
सबसे पहले चीज़ें, आइए आवश्यक पैकेज आयात करें। ये हमें PSD फ़ाइल में हेरफेर करने के लिए आवश्यक कक्षाओं और विधियों का उपयोग करने में सक्षम बनाएंगे।
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
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
अब, आइए बेहतर समझ के लिए उदाहरण को कई चरणों में विभाजित करें।
## चरण 1: PSD फ़ाइल लोड करें
 सबसे पहले, हमें PSD फ़ाइल लोड करनी होगी जिसे हम संशोधित करना चाहते हैं। हम उपयोग करेंगे`PsdLoadOptions` यह निर्दिष्ट करने के लिए कि हम प्रभाव संसाधनों को लोड करना चाहते हैं।
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
कोई भी परिवर्तन करने से पहले, आइए यह सुनिश्चित करने के लिए स्ट्रोक प्रभाव के गुणों को सत्यापित करें कि हम सही सेटिंग्स को संशोधित कर रहे हैं।
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
## चरण 4: ग्रेडिएंट भरण सेटिंग्स को संशोधित करें
अब, हमारी आवश्यकताओं के अनुसार ग्रेडिएंट भरण सेटिंग्स को संशोधित करने का समय आ गया है। हम रंग, अपारदर्शिता, मिश्रण मोड और अन्य गुण बदल देंगे।
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
आइए वांछित ग्रेडिएंट प्रभाव प्राप्त करने के लिए नए रंग और पारदर्शिता बिंदु जोड़ें और मौजूदा बिंदुओं को संशोधित करें।
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
सभी आवश्यक संशोधन करने के बाद, हमें PSD फ़ाइल को सहेजना होगा।
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
// रंग बिंदुओं की जाँच करें
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
आखिर तुमने इसे हासिल कर ही लिया है! अब आप जानते हैं कि जावा के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में स्ट्रोक लेयर ग्रेडिएंट्स को कैसे जोड़ा और हेरफेर किया जाए। इस ट्यूटोरियल में PSD फ़ाइल को लोड करना, स्ट्रोक प्रभावों तक पहुंचना और संशोधित करना और परिवर्तनों को सहेजना शामिल है। इन कौशलों के साथ, आप दिखने में आकर्षक ग्रेडिएंट बना सकते हैं और अपनी PSD फ़ाइलों को अपनी आवश्यकताओं के अनुरूप अनुकूलित कर सकते हैं।
## अक्सर पूछे जाने वाले प्रश्न
### जावा के लिए Aspose.PSD क्या है?
जावा के लिए Aspose.PSD एक लाइब्रेरी है जो डेवलपर्स को जावा अनुप्रयोगों में PSD फ़ाइलों के साथ काम करने की अनुमति देती है, PSD फ़ाइलों को बनाने, हेरफेर करने और परिवर्तित करने की सुविधाएँ प्रदान करती है।
### क्या मुझे Java के लिए Aspose.PSD का उपयोग करने के लिए लाइसेंस की आवश्यकता है?
 हां, जावा के लिए Aspose.PSD का उपयोग करने के लिए आपको एक वैध लाइसेंस की आवश्यकता है। आप एक प्राप्त कर सकते हैं[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) मूल्यांकन प्रयोजनों के लिए.
### क्या मैं शुरू से ही PSD फ़ाइलें बनाने के लिए जावा के लिए Aspose.PSD का उपयोग कर सकता हूँ?
बिल्कुल! जावा के लिए Aspose.PSD प्रोग्रामेटिक रूप से PSD फ़ाइलों को बनाने और उनमें हेरफेर करने के लिए व्यापक एपीआई प्रदान करता है।
### क्या जावा के लिए Aspose.PSD का उपयोग करके अन्य प्रभाव लागू करना संभव है?
हां, आप जावा के लिए Aspose.PSD का उपयोग करके छाया, चमक और बहुत कुछ जैसे विभिन्न प्रभाव लागू कर सकते हैं।
### मैं जावा के लिए Aspose.PSD के लिए दस्तावेज़ कहाँ पा सकता हूँ?
 आप दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/psd/java/).