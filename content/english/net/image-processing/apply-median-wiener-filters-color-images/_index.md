---
title: Applying Median and Wiener Filters in Color Images with Aspose.PSD for .NET
linktitle: Applying Median and Wiener Filters in Color Images with Aspose.PSD for .NET
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 11
url: /net/image-processing/apply-median-wiener-filters-color-images/
---

## Complete Source Code
```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.Conversion
{
    class ApplyMedianAndWienerFilters
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:ApplyMedianAndWienerFilters

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + @"median_test_denoise_out.gif";

            // Load the noisy image 
            using (Image image = Image.Load(sourceFile))
            {
                // Cast the image into RasterImage
                RasterImage rasterImage = image as RasterImage;
                if (rasterImage == null)
                {
                    return;
                }

                // Create an instance of MedianFilterOptions class and set the size, Apply MedianFilterOptions filter to RasterImage object and Save the resultant image
                MedianFilterOptions options = new MedianFilterOptions(4);
                rasterImage.Filter(image.Bounds, options);
                image.Save(destName, new GifOptions());
            }
            //ExEnd:ApplyMedianAndWienerFilters

        }
    }
}

```
