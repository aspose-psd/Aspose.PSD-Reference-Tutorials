---
title: Support Layer Mask in PSD Files with Java
linktitle: Support Layer Mask in PSD Files with Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 18
url: /java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/
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


public class SupportOfLayerMask {
    public static void main(String[] args) 
    {
       //ExStart:SupportOfLayerMask
       String dataDir = "Your Document Directory";
       // Export of the psd with complex mask
            String sourceFileName = dataDir + "MaskComplex.psd";
            String exportPath = dataDir + "MaskComplex.png";

            PsdImage im = (PsdImage)Image.load(sourceFileName);
            
                // Export to PNG
                PngOptions saveOptions = new PngOptions();
                saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
                im.save(exportPath, saveOptions);
            
       
       //ExEnd:SupportOfLayerMask
       
    }
}

```