---
title: Verify Image Transparency with Aspose.PSD for Java
linktitle: Verify Image Transparency with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 14
url: /java/basic-image-operations/verify-image-transparency/
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
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;

/**
 *
 *  
 */
public class VerifyImageTransparency {
    
    public static void main(String[] args)  
    {
       //ExStart:VerifyImageTransparency
       String dataDir = Utils.getDataDir(VerifyImageTransparency.class) + "DrawingAndFormattingImages/";
       
       String sourceFile = dataDir +"sample.psd";
       String destName = dataDir + "AdjustBrightness_out.tiff";
       
       // Load an existing image into an instance of RasterImage class
       PsdImage image = (PsdImage)Image.load(sourceFile);
        
       float opacity = image.getImageOpacity();
        System.out.println(opacity);
        if (opacity == 0)
        {
            // The image is fully transparent.
        }
       //ExEnd:VerifyImageTransparency
    }
}

```
