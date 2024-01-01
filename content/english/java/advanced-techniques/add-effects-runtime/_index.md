---
title: Add Effects at Runtime with Aspose.PSD for Java
linktitle: Add Effects at Runtime with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 20
url: /java/advanced-techniques/add-effects-runtime/
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

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

/**
 *
 *  
 */
public class AddEffectAtRunTime {
    
    public static void main(String[] args) 
    {
       //ExStart:AddEffectAtRunTime
       String dataDir = "Your Document Directory";
       
        String sourceFileName =dataDir+"ThreeRegularLayers.psd";
        String exportPath = dataDir+"ThreeRegularLayersChanged.psd";

        PsdLoadOptions loadOptions = new PsdLoadOptions();
        loadOptions.setLoadEffectsResource(true);
        
        PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
        
                ColorOverlayEffect effect = im.getLayers()[1].getBlendingOptions().addColorOverlay();
                effect.setColor(Color.getGreen()) ;
                effect.setOpacity((byte)128);
                effect.setBlendMode(BlendMode.Normal) ;

                im.save(exportPath);
        
       
       //ExEnd:AddEffectAtRunTime
    }
    
}

```
