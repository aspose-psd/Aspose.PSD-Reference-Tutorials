---
title: Applying Gaussian and Wiener Filters in Aspose.PSD for .NET
linktitle: Applying Gaussian and Wiener Filters in Aspose.PSD for .NET
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 10
url: /net/image-processing/apply-gaussian-wiener-filters/
---

## Complete Source Code
```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.Conversion
{
    class ApplyGausWienerFilters
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir_PSD();

            //ExStart:ApplyGausWienerFilters

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + @"gauss_wiener_out.gif";

            // Load the noisy image 
            using (Image image = Image.Load(sourceFile))
            {
                RasterImage rasterImage = image as RasterImage;
                if (rasterImage == null)
                {
                    return;
                }

                // Create an instance of GaussWienerFilterOptions class and set the radius size and smooth value.
                GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
                options.Grayscale = true;

                // Apply MedianFilterOptions filter to RasterImage object and Save the resultant image
                rasterImage.Filter(image.Bounds, options);
                image.Save(destName, new GifOptions());

            }
            //ExEnd:ApplyGausWienerFilters

        }
    }
}

```
