---
title: Apply Rendering Color Effect in Aspose.PSD for Java
linktitle: Apply Rendering Color Effect in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 15
url: /java/advanced-image-manipulation/rendering-color-effect/
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

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;

/**
 *
 *  
 */
public class RenderingColorEffect {
    
    public static void main(String[] args) throws InterruptedException 
    {
       //ExStart:RenderingColorEffect
     String dataDir = "Your Document Directory";
     
     
    String sourceFileName = dataDir+"ColorOverlay.psd";
    String pngExportPath = dataDir+"ColorOverlayresult.png";
    
    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setLoadEffectsResource(true);
    
    PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
    ColorOverlayEffect colorOverlay = (ColorOverlayEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
     
    PngOptions saveOptions = new PngOptions();
    saveOptions.setColorType(PngColorType.TruecolorWithAlpha) ;
    im.save(pngExportPath, saveOptions);
     //ExEnd:RenderingColorEffect
    }
}

```
