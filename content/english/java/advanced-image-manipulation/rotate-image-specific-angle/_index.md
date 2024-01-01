---
title: Rotate an Image on a Specific Angle with Aspose.PSD for Java
linktitle: Rotate an Image on a Specific Angle with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 20
url: /java/advanced-image-manipulation/rotate-image-specific-angle/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.DrawingAndFormattingImages;

import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;

/**
 *
 *  
 */
public class RotatingAnImageOnASpecificAngle
{
    public static void main(String[] args)  
    {
       //ExStart:RotatingAnImageOnASpecificAngle
       String dataDir = "Your Document Directory";
       
       String sourceFile = dataDir + "sample.psd";
       String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
       
       RasterImage image = (RasterImage)Image.load(sourceFile);
       // Before rotation, the image should be cached for better performance
        if (!image.isCached())
        {
            image.cacheData();
        }
        // Perform the rotation on 20 degree while keeping the image size proportional with red background color and Save the result to a new file
        image.rotate(20f, true, Color.getRed());
        image.save(destName, new JpegOptions());
       //ExEnd:RotatingAnImageOnASpecificAngle
    }
}

```