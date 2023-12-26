---
title: Setting for Replacing Missing Fonts in Aspose.PSD for .NET
linktitle: Setting for Replacing Missing Fonts
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 11
url: /net/text-and-font-manipulation/replace-missing-fonts/
---

## Complete Source Code
```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.Conversion
{
    class SettingforReplacingMissingFonts
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string outputFolder = "Your Output Directory"; ;

            //ExStart:SettingforReplacingMissingFonts

            string sourceFileName = Path.Combine(dataDir, "sample_konstanting.psd");

            string[] outputs = new string[]
            {
                "replacedfont0.tiff",
                "replacedfont1.png",
                "replacedfont2.jpg"
            };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
            {
                // This way you can use different fonts for different outputs 
                image.Save(Path.Combine(outputFolder, outputs[0]), new TiffOptions(TiffExpectedFormat.TiffJpegRgb) { DefaultReplacementFont = "Arial" });
                image.Save(Path.Combine(outputFolder, outputs[1]), new PngOptions { DefaultReplacementFont = "Verdana" });
                image.Save(Path.Combine(outputFolder, outputs[2]), new JpegOptions { DefaultReplacementFont = "Times New Roman" });
            }
            //ExEnd:SettingforReplacingMissingFonts

            Console.WriteLine("SettingforReplacingMissingFonts executed successfully");
        }
    }
}

```
