---
title: Crop PSD File using Aspose.PSD for Java
linktitle: Crop PSD File using Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 17
url: /java/image-processing/crop-psd-file/
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
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;

/**
 *
 *  
 */
public class CropPSDFile {
    
     public static void main(String[] args) 
    {
       //ExStart:CropPSDFile
       String dataDir = "Your Document Directory";
       
       // Implement correct Crop method for PSD files.
        String sourceFileName = dataDir + "1.psd";
        String exportPathPsd = dataDir +"CropTest.psd";
        String exportPathPng = dataDir +"CropTest.png";
        
        RasterImage image = (RasterImage)Image.load(sourceFileName);
        image.crop(new Rectangle(10, 30, 100, 100));
        image.save(exportPathPsd, new PsdOptions());
        
        PngOptions options = new PngOptions();
        options.setColorType(PngColorType.TruecolorWithAlpha);
        image.save(exportPathPng, options);
       //ExEnd:CropPSDFile
    }
}

```