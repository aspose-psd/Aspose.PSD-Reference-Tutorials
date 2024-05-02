---
title: .NET के लिए Aspose.PSD में MLST संसाधन प्रबंधन में महारत हासिल करना
linktitle: एमएलएसटी संसाधनों को संभालना
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD के साथ फ़ोटोशॉप फ़ाइलों में परत स्थिति में हेरफेर करना सीखें। कुशल एमएलएसटी संसाधन प्रबंधन के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 14
url: /hi/net/psd-file-manipulation/mlst-resources/
---
## परिचय
.NET के लिए Aspose.PSD में MLST (मल्टीपल लेयर स्टेट्स) संसाधनों को संभालने पर गहन ट्यूटोरियल में आपका स्वागत है। .NET के लिए Aspose.PSD एक शक्तिशाली लाइब्रेरी है जो फ़ोटोशॉप फ़ाइलों के साथ काम करने के लिए व्यापक क्षमताएं प्रदान करती है। इस ट्यूटोरियल में, हम एमएलएसटी संसाधनों के समर्थन पर ध्यान केंद्रित करेंगे, जो परत की स्थिति में कुशलतापूर्वक हेरफेर करने के लिए एक निम्न-स्तरीय तंत्र की पेशकश करते हैं।
## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में गहराई से जाएँ, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:
-  .NET लाइब्रेरी के लिए Aspose.PSD: सुनिश्चित करें कि आपके पास लाइब्रेरी स्थापित है। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[.NET डाउनलोड पेज के लिए Aspose.PSD](https://releases.aspose.com/psd/net/).
- दस्तावेज़ और आउटपुट निर्देशिकाएँ: अपनी दस्तावेज़ निर्देशिका सेट करें (`baseDir`) और आउटपुट निर्देशिका (`outputDir`) दिए गए कोड में।
## नामस्थान आयात करें
अपने .NET प्रोजेक्ट में, Aspose.PSD के साथ काम करने के लिए आवश्यक नेमस्पेस शामिल करें:
```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures;
```
## चरण 1: निर्देशिका पथ सेट करें
```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```
अपने प्रोजेक्ट में "आपकी दस्तावेज़ निर्देशिका" और "आपकी आउटपुट निर्देशिका" को वास्तविक पथों से बदलना सुनिश्चित करें।
## चरण 2: PSD छवि लोड करें
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
string outputPsd = Path.Combine(outputDir, "output_image1219.psd");
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    // हेरफेर के लिए कोड अगले चरणों में जोड़ा जाएगा।
}
```
## चरण 3: एमएलएसटी संसाधन तक पहुंचें
```csharp
Layer layer1 = image.Layers[1];
ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];
```
## चरण 4: परत स्थिति में हेरफेर करें
```csharp
ListStructure layerStatesList = (ListStructure)mlstResource.Items[1];
DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Types[1];
BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Structures[0];
// फ़्रेम 1 पर परत 1 को अक्षम करें
layerEnabled.Value = false;
```
## चरण 5: संशोधित छवि सहेजें
```csharp
image.Save(outputPsd);
```
## चरण 6: साफ़ करें
```csharp
File.Delete(outputPsd);
Console.WriteLine("SupportOfMlstResource executed successfully");
```
## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.PSD में MLST संसाधनों को कैसे संभालना है। यह सुविधा फ़ोटोशॉप फ़ाइलों में परत स्थिति को प्रोग्रामेटिक रूप से हेरफेर करने के लिए एक मजबूत तंत्र प्रदान करती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं विभिन्न फ़ोटोशॉप संस्करणों में बनाई गई PSD फ़ाइलों के साथ काम करने के लिए .NET के लिए Aspose.PSD का उपयोग कर सकता हूँ?

A1: हां, .NET के लिए Aspose.PSD विभिन्न फ़ोटोशॉप संस्करणों में बनाई गई PSD फ़ाइलों का समर्थन करता है।

### Q2: क्या .NET के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 उ2: हां, आप यहां से नि:शुल्क परीक्षण डाउनलोड कर सकते हैं[पृष्ठ जारी करता है](https://releases.aspose.com/).

### Q3: मुझे .NET के लिए Aspose.PSD के लिए विस्तृत दस्तावेज़ कहां मिल सकते हैं?

A3: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/psd/net/).

### Q4: मैं .NET के लिए Aspose.PSD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A4: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन के लिए.

### Q5: मैं .NET के लिए Aspose.PSD का लाइसेंस कैसे खरीदूं?

 A5: आप लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).