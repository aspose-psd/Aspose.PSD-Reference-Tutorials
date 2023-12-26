---
title: Grayscaling Images with Aspose.PSD for .NET
linktitle: Grayscaling Images with Aspose.PSD for .NET
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 14
url: /net/image-processing/grayscaling-images/
---

## Complete Source Code
```csharp
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.Conversion
{
    class Grayscaling
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:Garysacling

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + @"Grayscaling_out.jpg";

            // Load an image in an instance of Image
            using (Image image = Image.Load(sourceFile))
            {
                // Cast the image to RasterCachedImage and Check if image is cached
                RasterCachedImage rasterCachedImage = (RasterCachedImage)image;
                if (!rasterCachedImage.IsCached)
                {
                    // Cache image if not already cached
                    rasterCachedImage.CacheData();
                }

                // Transform image to its grayscale representation and Save the resultant image
                rasterCachedImage.Grayscale();
                rasterCachedImage.Save(destName, new JpegOptions());
            }


            //ExEnd:Garysacling

        }
    }
}

```
