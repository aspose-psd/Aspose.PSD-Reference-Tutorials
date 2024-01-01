---
title: Binarization with Otsu Threshold in Aspose.PSD for Java
linktitle: Binarization with Otsu Threshold in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 15
url: /java/image-processing/binarization-otsu-threshold/
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
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;

/**
 *
 *  
 */
public class BinarizationWithOtsuThreshold {
    public static void main(String[] args) 
    {
       //ExStart:BinarizationWithOtsuThreshold
       String dataDir = "Your Document Directory";
       
       String sourceFile = dataDir + "sample.psd";
       String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
       
       Image image = Image.load(sourceFile);
       // Cast the image to RasterCachedImage and Check if image is cached
        RasterCachedImage rasterCachedImage = (RasterCachedImage)image;
        if (!rasterCachedImage.isCached())
        {
            // Cache image if not already cached
            rasterCachedImage.cacheData();
        }
        // Binarize image with Otsu Thresholding and Save the resultant image                
        rasterCachedImage.binarizeOtsu();

        rasterCachedImage.save(destName, new JpegOptions());
       //ExEnd:BinarizationWithOtsuThreshold
    }
}

```