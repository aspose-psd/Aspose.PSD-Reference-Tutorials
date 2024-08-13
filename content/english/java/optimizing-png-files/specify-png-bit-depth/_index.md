---
title: Specify PNG Bit Depth in Aspose.PSD for Java
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 14
url: /java/optimizing-png-files/specify-png-bit-depth/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;

/**
 *
 *  
 */
public class SpecifyBitDepth {
     public static void main(String[] args) 
    {
       //ExStart:SpecifyBitDepth
       String dataDir = "Your Document Directory";
       
       PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
       // Create an instance of PngOptions, Set the desired ColorType, BitDepth according to the specified ColorType and save image
                PngOptions options = new PngOptions();
                options.setColorType(PngColorType.Grayscale);
                options.setBitDepth((byte)1);
                psdImage.save(dataDir+"SpecifyBitDepth_out.png", options);
       //ExEnd:SpecifyBitDepth
    }
}

```
