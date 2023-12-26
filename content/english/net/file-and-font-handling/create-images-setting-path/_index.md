---
title: Creating Images by Setting Path in Aspose.PSD for .NET
linktitle: Creating Images by Setting Path
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 11
url: /net/file-and-font-handling/create-images-setting-path/
---

## Complete Source Code
```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
using Aspose.PSD.Sources;

namespace Aspose.PSD.Examples.Aspose.DrawingAndFormattingImages
{
    class CreatingbySettingPath
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:CreatingbySettingPath
            string desName = dataDir + "CreatingAnImageBySettingPath_out.psd";

            // Creates an instance of PsdOptions and set its various properties
            PsdOptions psdOptions = new PsdOptions();
            psdOptions.CompressionMethod = CompressionMethod.RLE;

            // Define the source property for the instance of PsdOptions. Second boolean parameter determines if the file is temporal or not
            psdOptions.Source = new FileCreateSource(desName, false);

            // Creates an instance of Image and call Create method by passing the PsdOptions object
            using (Image image = Image.Create(psdOptions, 500, 500))
            {
                image.Save();
            }

            //ExEnd:CreatingbySettingPath

        }
    }
}

```
