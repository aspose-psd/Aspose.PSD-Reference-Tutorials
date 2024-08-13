---
title: Add Level Adjustment Layer in PSD
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 16
url: /java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;

/**
 *
 *  
 */
public class AddLevelAdjustmentLayer {
    
    public static void main(String[] args) 
    {
       //ExStart:AddLevelAdjustmentLayer
       String dataDir = "Your Document Directory";
    
       String sourceFileName = dataDir +"LevelsAdjustmentLayer.psd";
       String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
       
       PsdImage im = (PsdImage)Image.load(sourceFileName);
       
        
        for (int i =0; i <im.getLayers().length; i++)
                {
                    
                    if (im.getLayers()[i] instanceof LevelsLayer)
                    {
                        LevelsLayer levelsLayer = (LevelsLayer)im.getLayers()[i];
                        LevelChannel channel = levelsLayer.getChannel(0);
                        channel.setInputMidtoneLevel(2.0f);
                        channel.setInputShadowLevel((short)10);
                        channel.setInputHighlightLevel((short)230);
                        channel.setOutputShadowLevel((short)20);
                        channel.setOutputHighlightLevel((short)200);
                    }
                }
        
        // Save PSD
       im.save(psdPathAfterChange);
    //ExEnd:AddLevelAdjustmentLayer
    }
}

```
