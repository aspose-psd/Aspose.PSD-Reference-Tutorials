---
title: Cropping PSD Files with Aspose.PSD for .NET
linktitle: Cropping PSD Files with Aspose.PSD for .NET
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 19
url: /net/psd-file-manipulation/crop-psd-file/
---

## Complete Source Code
```csharp
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.Conversion
{
    class CropPSDFile
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:CropPSDFile
            // Implement correct Crop method for PSD files.
            string sourceFileName = dataDir + "1.psd";
            string exportPathPsd = dataDir + "CropTest.psd";
            string exportPathPng = dataDir + "CropTest.png";
            using (RasterImage image = Image.Load(sourceFileName) as RasterImage)
            {
                image.Crop(new Rectangle(10, 30, 100, 100));
                image.Save(exportPathPsd, new PsdOptions());
                image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }


            //ExEnd:CropPSDFile

        }
    }
}

```