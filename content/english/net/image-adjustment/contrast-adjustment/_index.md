---
title: Implementing Contrast Adjustment in Aspose.PSD for .NET
linktitle: Implementing Contrast Adjustment
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 11
url: /net/image-adjustment/contrast-adjustment/
---

## Complete Source Code
```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.DrawingAndFormattingImages
{
    class AdjustingContrast
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:AdjustingContrast

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + @"AdjustContrast_out.tiff";

            // Load an existing image into an instance of RasterImage class
            using (var image = Image.Load(sourceFile))
            {
                // Cast object of Image to RasterImage
                RasterImage rasterImage = (RasterImage)image;
                // Check if RasterImage is cached and Cache RasterImage for better performance
                if (!rasterImage.IsCached)
                {
                    rasterImage.CacheData();
                }

                // Adjust the contrast
                rasterImage.AdjustContrast(50);

                // Create an instance of TiffOptions for the resultant image, Set various properties for the object of TiffOptions and Save the resultant image to TIFF format
                TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
                tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
                tiffOptions.Photometric = TiffPhotometrics.Rgb;
                rasterImage.Save(destName, tiffOptions);
            }


            //ExEnd:AdjustingContrast

        }

    }
}

```
