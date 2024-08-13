---
title: Add Text Layer on Runtime in PSD Files using Java
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 17
url: /java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
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
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;

/**
 *
 *  
 */
public class AddTextLayerOnRuntime {
  
    public static void main(String[] args) 
    {
       //ExStart:AddTextLayerOnRuntime
       String dataDir = Utils.getDataDir(AddTextLayerOnRuntime.class) + "PSD/";
       
       
       String sourceFileName = dataDir+"OneLayer.psd";
       String psdPath = dataDir + "ImageWithTextLayer.psd";
       
       Image img = Image.load(sourceFileName);
       
       PsdImage im = (PsdImage)img;
                Rectangle rect = new Rectangle(
                    (int)(im.getWidth() * 0.25),
                    (int)(im.getHeight() * 0.25),
                    (int)(im.getWidth() * 0.5),
                    (int)(im.getHeight() * 0.5));

                TextLayer layer = im.addTextLayer("Added text", rect);

                im.save(psdPath);
       
       //ExEnd:AddTextLayerOnRuntime
    }
}

```
