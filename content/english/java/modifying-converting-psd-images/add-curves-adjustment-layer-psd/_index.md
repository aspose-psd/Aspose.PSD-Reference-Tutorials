---
title: Add Curves Adjustment Layer in PSD using Java
linktitle: Add Curves Adjustment Layer in PSD using Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 11
url: /java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;

/**
 *
 *  
 */
public class AddCurvesAdjustmentLayer {
    public static void main(String[] args) 
    {
       //ExStart:AddCurvesAdjustmentLayer
       String dataDir = "Your Document Directory";
       
       // Curves layer editing
            String sourceFileName = dataDir+"CurvesAdjustmentLayer";
            String psdPathAfterChange = dataDir+ "CurvesAdjustmentLayerChanged";
            
             for (int j = 1; j < 2; j++)
            {
                String fileName = sourceFileName  + ".psd";
                PsdImage im = (PsdImage)Image.load(fileName);
               
                    
                    for(int k =0; k < im.getLayers().length; k++)
                    {
                        if (im.getLayers()[k] instanceof CurvesLayer)
                        {
                            CurvesLayer curvesLayer = (CurvesLayer)im.getLayers()[k];
                            if (curvesLayer.isDiscreteManagerUsed())
                            {
                                CurvesDiscreteManager manager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

                                for (int i = 10; i < 50; i++)
                                {
                                    manager.setValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));
                                }
                            }
                            else
                            {
                                CurvesContinuousManager manager = (CurvesContinuousManager)curvesLayer.getCurvesManager();
                                manager.addCurvePoint((byte)0, (byte)50, (byte)100);
                                manager.addCurvePoint((byte)0, (byte)150, (byte)130);
                            }
                        }
                    }
                    // Save PSD
                    im.save(psdPathAfterChange + Integer.toString(j) + ".psd");
            

            }
            
            //ExEnd:AddCurvesAdjustmentLayer
    }
}

```
