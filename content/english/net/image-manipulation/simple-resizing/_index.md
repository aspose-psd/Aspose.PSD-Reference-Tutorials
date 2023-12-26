---
title: Simple Resizing of Images in Aspose.PSD for .NET
linktitle: Simple Resizing of Images
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 17
url: /net/image-manipulation/simple-resizing/
---

## Complete Source Code
```csharp
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.DrawingAndFormattingImages
{
    class SimpleResizing
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:SimpleResizing

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + @"SimpleResizing_out.jpg";

            // Load an existing image into an instance of RasterImage class
            using (Image image = Image.Load(sourceFile))
            {
                image.Resize(300, 300);
                image.Save(destName, new JpegOptions());
            }

            //ExEnd:SimpleResizing

        }

    }
}

```
