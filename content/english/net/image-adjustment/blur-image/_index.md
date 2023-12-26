---
title: Blurring an Image in Aspose.PSD for .NET
linktitle: Blurring an Image
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 13
url: /net/image-adjustment/blur-image/
---

## Complete Source Code
```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.DrawingAndFormattingImages
{
    class BluranImage
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:BluranImage

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + @"BlurAnImage_out.gif";

            // Load an existing image into an instance of RasterImage class
            using (var image = Image.Load(sourceFile))
            {
                // Convert the image into RasterImage, 
                //Pass Bounds[rectangle] of image and GaussianBlurFilterOptions instance to Filter method and Save the results
                RasterImage rasterImage = (RasterImage)image;

                rasterImage.Filter(rasterImage.Bounds, new GaussianBlurFilterOptions(15, 15));

                rasterImage.Save(destName, new GifOptions());
            }
            //ExEnd:BluranImage

        }

    }
}

```