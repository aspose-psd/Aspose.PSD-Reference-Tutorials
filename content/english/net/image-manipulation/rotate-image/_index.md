---
title: Rotating an Image in Aspose.PSD for .NET
linktitle: Rotating an Image
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 15
url: /net/image-manipulation/rotate-image/
---

## Complete Source Code
```csharp
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.DrawingAndFormattingImages
{
    class RotatinganImage
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:RotatinganImage

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + @"RotatingAnImage_out.jpg";

            // Load an existing image into an instance of RasterImage class
            using (Image image = Image.Load(sourceFile))
            {
                image.RotateFlip(RotateFlipType.Rotate270FlipNone);
                image.Save(destName, new JpegOptions());
            }

            //ExEnd:RotatinganImage

        }

    }
}

```
