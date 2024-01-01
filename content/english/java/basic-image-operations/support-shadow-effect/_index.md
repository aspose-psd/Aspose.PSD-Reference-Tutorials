---
title: Support Shadow Effect in Aspose.PSD for Java
linktitle: Support Shadow Effect in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 13
url: /java/basic-image-operations/support-shadow-effect/
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
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

/**
 *
 *  
 */
public class SupportShadowEffect {
    public static void main(String[] args)  
    {
       //ExStart:SupportShadowEffect
       String dataDir = "Your Document Directory";
       
       String sourceFileName = dataDir+"Shadow.psd";
        String psdPathAfterChange = dataDir+"ShadowChanged.psd";
        
         PsdLoadOptions loadOptions = new PsdLoadOptions();
         loadOptions.setLoadEffectsResource(true);
         
         PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
         
         DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);

        Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
        Assert.areEqual(255, shadowEffect.getOpacity());
        Assert.areEqual(3, shadowEffect.getDistance());
        Assert.areEqual(7, shadowEffect.getSize());
        Assert.areEqual(true, shadowEffect.getUseGlobalLight());
        Assert.areEqual(90, shadowEffect.getAngle());
        Assert.areEqual(0, shadowEffect.getSpread());
        Assert.areEqual(0, shadowEffect.getNoise());

        shadowEffect.setColor( Color.getGreen());
        shadowEffect.setOpacity((byte)128);
        shadowEffect.setDistance(11);
        shadowEffect.setUseGlobalLight(false);
        shadowEffect.setSize(9);
        shadowEffect.setAngle(45);
        shadowEffect.setSpread(3);
        shadowEffect.setNoise(50);

        im.save(psdPathAfterChange);
       //ExEnd:SupportShadowEffect
    }
}

```