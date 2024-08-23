---
title: जावा में स्ट्रोक लेयर पैटर्न कैसे जोड़ें
linktitle: जावा में स्ट्रोक लेयर पैटर्न कैसे जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में स्ट्रोक लेयर पैटर्न जोड़ने का तरीका जानें। अपनी छवियों को आसानी से बेहतर बनाने के लिए इस चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## परिचय
जावा में किसी छवि में स्ट्रोक लेयर पैटर्न जोड़ना एक कठिन काम लग सकता है, लेकिन जावा के लिए Aspose.PSD के साथ, यह आपके विचार से कहीं ज़्यादा आसान है। चाहे आप ग्राफ़िक्स डिज़ाइन कर रहे हों या फ़ोटो संपादन एप्लिकेशन पर काम कर रहे हों, यह गाइड आपको चरण-दर-चरण प्रक्रिया से गुज़ारेगी। शुरू करने के लिए तैयार हैं? चलिए शुरू करते हैं!
## आवश्यक शर्तें
शुरू करने से पहले आपको कुछ चीजों की आवश्यकता होगी:
- जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके सिस्टम पर JDK स्थापित है।
-  Aspose.PSD for Java: लाइब्रेरी को यहाँ से डाउनलोड करें[यहाँ](https://releases.aspose.com/psd/java/) और इसे अपने प्रोजेक्ट में शामिल करें.
- IDE: अपने पसंदीदा एकीकृत विकास वातावरण (IDE) जैसे कि IntelliJ IDEA या Eclipse का उपयोग करें।
## पैकेज आयात करें
सबसे पहले, आपको अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने की आवश्यकता है। ये पैकेज Aspose.PSD के साथ काम करने के लिए आवश्यक हैं।
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## चरण 1: PSD फ़ाइल लोड करें
स्ट्रोक लेयर पैटर्न जोड़ने में पहला चरण उस PSD फ़ाइल को लोड करना है जिसे आप संपादित करना चाहते हैं।
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
PSD फ़ाइल लोड करके, अब आप इसकी परतों और प्रभावों तक पहुंच सकते हैं और उनमें हेरफेर कर सकते हैं।
## चरण 2: नया पैटर्न डेटा तैयार करें
इसके बाद, आपको नया पैटर्न डेटा तैयार करना होगा जिसे आप स्ट्रोक परत पर लागू करेंगे।
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
इस पैटर्न डेटा का उपयोग नया स्ट्रोक प्रभाव बनाने के लिए किया जाएगा।
## चरण 3: स्ट्रोक प्रभाव तक पहुंचें
स्ट्रोक प्रभाव को संशोधित करने के लिए, आपको विशिष्ट परत और उसके सम्मिश्रण विकल्पों तक पहुंचने की आवश्यकता है।
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
यह सुनिश्चित करता है कि आप सही परत और प्रभाव के साथ काम कर रहे हैं।
## चरण 4: स्ट्रोक प्रभाव को संशोधित करें
अब, आइए नए पैटर्न डेटा के साथ स्ट्रोक प्रभाव को संशोधित करें।
### स्ट्रोक प्रभाव गुण अद्यतन करें
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### पैटर्न संसाधन को अपडेट करें
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
यह कोड स्निपेट नए पैटर्न डेटा के साथ पैटर्न संसाधन को अद्यतन करता है।
## चरण 5: नया पैटर्न लागू करें
अंत में, स्ट्रोक प्रभाव पर नया पैटर्न लागू करें और परिवर्तनों को सहेजें।
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
इससे यह सुनिश्चित होता है कि नया पैटर्न सही ढंग से लागू हो और फ़ाइल परिवर्तनों के साथ सहेजी गई हो।
## चरण 6: परिवर्तनों को सत्यापित करें
यह सुनिश्चित करने के लिए कि सब कुछ सही ढंग से काम कर रहा है, फ़ाइल को पुनः लोड करें और परिवर्तनों को सत्यापित करें।
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
यह चरण सत्यापित करता है कि पैटर्न डेटा स्ट्रोक प्रभाव पर सही ढंग से लागू किया गया है।
## निष्कर्ष
और अब यह हो गया! आपने Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में स्ट्रोक लेयर पैटर्न सफलतापूर्वक जोड़ लिया है। इन चरणों का पालन करके, आप अपनी छवियों को आसानी से अनुकूलित और बेहतर बना सकते हैं। हैप्पी कोडिंग!
## अक्सर पूछे जाने वाले प्रश्न
### Java के लिए Aspose.PSD क्या है?
Aspose.PSD for Java एक लाइब्रेरी है जो डेवलपर्स को प्रोग्रामेटिक रूप से PSD (फ़ोटोशॉप दस्तावेज़) फ़ाइलों को बनाने, संपादित करने और परिवर्तित करने की अनुमति देती है।
### क्या मैं किसी व्यावसायिक परियोजना में Java के लिए Aspose.PSD का उपयोग कर सकता हूँ?
 हां, आप इसे व्यावसायिक परियोजनाओं में उपयोग कर सकते हैं। आप यहां से लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).
### क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?
 हां, आप यहां से निःशुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).
### मैं Java के लिए Aspose.PSD का समर्थन कैसे प्राप्त कर सकता हूं?
 आप Aspose समुदाय मंचों से सहायता प्राप्त कर सकते हैं[यहाँ](https://forum.aspose.com/c/psd/34).
### Java के लिए Aspose.PSD हेतु सिस्टम आवश्यकताएँ क्या हैं?
आपको विकास के लिए JDK इंस्टॉल और एक IDE की आवश्यकता है। लाइब्रेरी विंडोज, लिनक्स और मैकओएस सहित कई ऑपरेटिंग सिस्टम का समर्थन करती है।