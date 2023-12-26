---
title: Saving Images to Disk with Aspose.PSD for .NET
linktitle: Saving Images to Disk with Aspose.PSD for .NET
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 10
url: /net/file-saving-and-exporting/save-images-to-disk/
---

## Complete Source Code
```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.Conversion
{
    class SavingtoDisk
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:SavingtoDisk

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + "result.png";

            // load PSD image and replace the non found fonts.
            using (Image image = Image.Load(sourceFile))
            {
                PsdImage psdImage = (PsdImage)image;
                psdImage.Save(destName, new PngOptions());
            }

            //ExEnd:SavingtoDisk

        }
    }
}

```