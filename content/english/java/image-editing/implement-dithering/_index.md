---
title: Implement Dithering for Raster Images in Aspose.PSD for Java
linktitle: Implement Dithering for Raster Images in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 17
url: /java/image-editing/implement-dithering/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.DrawingAndFormattingImages;

import com.aspose.psd.DitheringMethod;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;


public class DitheringForRasterImages
{
    public static void main(String[] args) 
    {
       //ExStart:DitheringForRasterImages
     String dataDir = "Your Document Directory";
     String sourceFile = dataDir + "sample.psd";
     String destName = dataDir + "SampleImage_out.bmp";

            // Load an existing image into an instance of RasterImage class
            PsdImage image = (PsdImage)Image.load(sourceFile);
            
                // Peform Floyd Steinberg dithering on the current image and Save the resultant image
                image.dither(DitheringMethod.ThresholdDithering, 4);
                image.save(destName, new BmpOptions());
            
     
     //ExEnd:DitheringForRasterImages
    }
    
}

```