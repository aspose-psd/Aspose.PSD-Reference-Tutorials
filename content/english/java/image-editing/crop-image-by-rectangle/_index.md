---
title: Crop Image by Rectangle in Aspose.PSD for Java
linktitle: Crop Image by Rectangle in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 15
url: /java/image-editing/crop-image-by-rectangle/
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
public class CroppingByRectangle
{
    public static void main(String[] args) 
    {
       //ExStart:CroppingByRectangle
     String dataDir = "Your Document Directory";
     
     String sourceFile = dataDir + "sample.psd";
    String destName = dataDir + "CroppingByRectangle_out.jpg";

    // Load an existing image into an instance of RasterImage class
    RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
    
     if (!rasterImage.isCached())
    {
        rasterImage.cacheData();
    }

    // Create an instance of Rectangle class with desired size, 
    //Perform the crop operation on object of Rectangle class and Save the results to disk
    Rectangle rectangle = new Rectangle(20, 20, 20, 20);

    rasterImage.crop(rectangle);
    rasterImage.save(destName, new JpegOptions());
    
     //ExEnd:CroppingByRectangle
    }
}

```
