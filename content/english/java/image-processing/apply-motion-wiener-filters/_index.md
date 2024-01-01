---
title: Apply Motion Wiener Filters using Aspose.PSD for Java
linktitle: Apply Motion Wiener Filters using Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 13
url: /java/image-processing/apply-motion-wiener-filters/
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

import com.aspose.psd.imagefilters.filteroptions.MotionWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;

/**
 *
 *  
 */
public class ApplyMotionWienerFilters {
    public static void main(String[] args) 
    {
       //ExStart:ApplyMotionWienerFilters
       String dataDir = "Your Document Directory";
       
       String sourceFile = dataDir + "sample.psd";
       String destName = dataDir + "motion_filter_out.gif";
       
       Image image = Image.load(sourceFile);
       
       // Cast the image into RasterImage
        RasterImage rasterImage = (RasterImage)image;
        if (rasterImage == null)
        {
            return;
        }
        
         // Create an instance of MotionWienerFilterOptions class and set the length, smooth value and angle.
        MotionWienerFilterOptions options = new MotionWienerFilterOptions(50, 9, 90);
        options.setGrayscale(true);

        // Apply MedianFilterOptions filter to RasterImage object and  Save the resultant image
        rasterImage.filter(image.getBounds(), options);
        image.save(destName, new GifOptions());
       //ExEnd:ApplyMotionWienerFilters
    }
}

```