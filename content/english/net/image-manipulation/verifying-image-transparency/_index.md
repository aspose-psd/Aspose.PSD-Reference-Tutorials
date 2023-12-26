---
title: Verifying Image Transparency in Aspose.PSD for .NET
linktitle: Verifying Image Transparency
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 10
url: /net/image-manipulation/verifying-image-transparency/
---

## Complete Source Code
```csharp
using Aspose.PSD.FileFormats.Psd;
using System;

namespace Aspose.PSD.Examples.Aspose.DrawingAndFormattingImages
{
    class VerifyImageTransparency
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:VerifyImageTransparency

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + @"AdjustBrightness_out.tiff";

            // Load an existing image into an instance of RasterImage class
            using (PsdImage image = (PsdImage)Image.Load(sourceFile))
            {
                float opacity = image.ImageOpacity;
                Console.WriteLine(opacity);
                if (opacity == 0)
                {
                    // The image is fully transparent.
                }
            }

            //ExEnd:VerifyImageTransparency

        }

    }
}

```
