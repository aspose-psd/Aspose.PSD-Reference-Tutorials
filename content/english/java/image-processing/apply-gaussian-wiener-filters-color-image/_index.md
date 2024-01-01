---
title: Apply Gaussian and Wiener Filters for Color Images with Aspose.PSD for Java
linktitle: Apply Gaussian and Wiener Filters for Color Images with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 11
url: /java/image-processing/apply-gaussian-wiener-filters-color-image/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.Conversion;

import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;

/**
 *
 *  
 */
public class ApplyGausWienerFiltersForColorImage {
    public static void main(String[] args) 
    {
       //ExStart:ApplyGausWienerFiltersForColorImage
       String dataDir = "Your Document Directory";
       String sourceFile = dataDir + "sample.psd";
       String destName = dataDir + "gauss_wiener_color_out.gif";
       
       Image image = Image.load(sourceFile);
       
        // Cast the image into RasterImage
                RasterImage rasterImage = (RasterImage)image;
                if (rasterImage == null)
                {
                    return;
                }
                
                // Create an instance of GaussWienerFilterOptions class and set the radius size and smooth value.
                GaussWienerFilterOptions options = new GaussWienerFilterOptions(5, 1.5);
                options.setBrightness(1);

                // Apply MedianFilterOptions filter to RasterImage object and Save the resultant image
                rasterImage.filter(image.getBounds(), options);
                image.save(destName, new GifOptions());
       //ExEnd:ApplyGausWienerFiltersForColorImage
    }
}

```
