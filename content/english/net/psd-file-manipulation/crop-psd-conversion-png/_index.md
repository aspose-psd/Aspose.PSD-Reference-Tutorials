---
title: Cropping PSD Files when Converting to PNG in Aspose.PSD for .NET
linktitle: Cropping PSD Files when Converting to PNG
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 18
url: /net/psd-file-manipulation/crop-psd-conversion-png/
---

## Complete Source Code
```csharp
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.Conversion
{
    class CroppingPSDWhenConvertingToPNG
    {

        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:CroppingPSDWhenConvertingToPNG

            string srcPath = dataDir + @"sample.psd";
            string destName = dataDir + @"export.png";

            // Load an existing PSD image
            using (RasterImage image = (RasterImage)Image.Load(srcPath))
            {
                // Create an instance of Rectangle class by passing x,y and width,height 
                // Call the crop method of Image class and pass the rectangle class instance
                image.Crop(new Rectangle(0, 0, 350, 450));

                // Create an instance of PngOptions class
                PngOptions pngOptions = new PngOptions();

                // Call the save method, provide output path and PngOptions to convert the PSD file to PNG and save the output
                image.Save(destName, pngOptions);
            }

            //ExEnd:CroppingPSDWhenConvertingToPNG
        }
    }
}

```
