---
title: Render Rotated Text Layer in PSD Files using Java
linktitle: Render Rotated Text Layer in PSD Files using Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 18
url: /java/psd-layer-management-effects/render-rotated-text-layer-psd/
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
import com.aspose.psd.xmp.types.complex.colorant.ColorType;


public class RenderingOfRotatedTextLayer {
    public static void main(String[] args) 
    {
       //ExStart:RenderingOfRotatedTextLayer
       String dataDir = "Your Document Directory";
       
        String sourceFileName = dataDir + "TransformedText.psd";
        String exportPath = dataDir + "TransformedTextExport.psd";
        String exportPathPng = dataDir + "TransformedTextExport.png";
        PsdImage im = (PsdImage)Image.load(sourceFileName);
          
           PngOptions opt =  new PngOptions();
           opt.setColorType(PngColorType.Grayscale);
                im.save(exportPath);
                im.save(exportPathPng,opt);
            
       //ExEnd:RenderingOfRotatedTextLayer
    }
}

```
