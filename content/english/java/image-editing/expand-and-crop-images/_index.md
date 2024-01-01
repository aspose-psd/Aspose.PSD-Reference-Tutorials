---
title: Expand and Crop Images with Aspose.PSD for Java
linktitle: Expand and Crop Images with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 18
url: /java/image-editing/expand-and-crop-images/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.DrawingAndFormattingImages;

import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;

/**
 *
 *  
 */
public class ExpandAndCropImages {
    
    public static void main(String[] args) 
    {
       //ExStart:ExpandAndCropImages
     String dataDir = "Your Document Directory";
     
     String sourceFile = dataDir + "example1.psd";
     String destName = dataDir + "jpeg_out.jpg";
     
     RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
     rasterImage.cacheData();
    // Create an instance of Rectangle class and define X,Y and Width, height of the rectangle, and Save output image
    Rectangle destRect = new Rectangle(-200, -200, 300, 300);
    rasterImage.save(destName, new JpegOptions(), destRect);
     //ExEnd:ExpandAndCropImages 
    }
}

```
