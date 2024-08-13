---
title: Support Clipping Mask in PSD Files with Aspose.PSD Java
linktitle: Support Clipping Mask in PSD Files with Aspose.PSD Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 16
url: /java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
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


public class SupportOfClippingMask {
    
    public static void main(String[] args) 
    {
       //ExStart:SupportOfClippingMask
       String dataDir = "Your Document Directory";
       
       // Exposure layer editing
            // Export of the psd with complex clipping mask
            String sourceFileName = dataDir+"ClippingMaskComplex.psd";
            String exportPath = dataDir+ "ClippingMaskComplex.png";

            PsdImage im = (PsdImage)Image.load(sourceFileName);
            
                // Export to PNG
                PngOptions saveOptions = new PngOptions();
                saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
                im.save(exportPath, saveOptions);
            
       //ExEnd:SupportOfClippingMask
    }
}

```
