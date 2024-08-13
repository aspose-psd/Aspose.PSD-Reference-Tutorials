---
title: Manage Brightness and Contrast in PSD Layers - Java
linktitle: Manage Brightness and Contrast in PSD Layers - Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 21
url: /java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.ModifyingAndConvertingImages.PSD;

import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;

/**
 *
 *  
 */
public class ManageBrightnessContrastAdjustmentLayer {
    
     public static void main(String[] args) 
    {
       //ExStart:ManageBrightnessContrastAdjustmentLayer
       String dataDir = Utils.getDataDir(ManageBrightnessContrastAdjustmentLayer.class) + "PSD/";
       
 // Brightness/Contrast layer editing
    String sourceFileName = dataDir+"BrightnessContrastModern.psd";
    String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd"; 
    
    PsdImage im = (PsdImage)Image.load(sourceFileName);
    
    
    for(int i=0; i < im.getLayers().length; i++ )
    {
        if (im.getLayers()[i] instanceof BrightnessContrastLayer)
        {
            BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
            brightnessContrastLayer.setBrightness(50);
            brightnessContrastLayer.setContrast(50);
        }
    }
    // Save PSD
    im.save(psdPathAfterChange);
       //ExEnd:ManageBrightnessContrastAdjustmentLayer
    }
}

```
