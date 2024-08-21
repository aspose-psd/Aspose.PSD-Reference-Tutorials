---
title: Apply Adjustment Layers in PSD Files using Java
linktitle: Apply Adjustment Layers in PSD Files using Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 15
url: /java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;



public class SupportOfAdjusmentLayers {
    public static void main(String[] args) 
    {
       //ExStart:SupportOfAdjusmentLayers
       String dataDir = "Your Document Directory";
       
       // Channel Mixer Adjustment Layer
        String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
        String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
        
        PsdImage im = (PsdImage)Image.load(sourceFileName1);
            
                for (int i = 0; i < im.getLayers().length; i++)
                {
                   if(im.getLayers()[i] instanceof AdjustmentLayer){ 
                    AdjustmentLayer adjustmentLayer = (AdjustmentLayer)im.getLayers()[i];

                    if (adjustmentLayer != null)
                    {
                        adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
                    }
                    
                    }
                }

                // Save PSD
                im.save(exportPath1);
            
                
                // Levels adjustment layer
            String sourceFileName2 =dataDir+ "LevelsAdjustmentLayerRgb.psd";
            String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";

            PsdImage img = (PsdImage)Image.load(sourceFileName2);
            
                for (int i = 0; i < img.getLayers().length; i++)
                {
                    if(img.getLayers()[i] instanceof AdjustmentLayer){ 
                    AdjustmentLayer adjustmentLayer = (AdjustmentLayer)img.getLayers()[i];

                    if (adjustmentLayer != null)
                    {
                        adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
                    }
                    
                    }
                }

                // Save PSD
                img.save(exportPath2);
            
       //ExEnd:SupportOfAdjusmentLayers
       
    }
}

```