---
title: Render Exposure Adjustment Layer in PSD Files - Java
linktitle: Render Exposure Adjustment Layer in PSD Files - Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 15
url: /java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
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
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;


public class RenderingExposureAdjustmentLayer {
    public static void main(String[] args) 
    {
       //ExStart:RenderingExposureAdjustmentLayer
       String dataDir = "Your Document Directory";
       
       
       // Exposure layer editing
        String sourceFileName = dataDir+"ExposureAdjustmentLayer.psd";
        String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";
        String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";

        
         PsdImage im = (PsdImage)Image.load(sourceFileName);
            
                for(int i=0; i < im.getLayers().length; i++ )
    {
        if (im.getLayers()[i] instanceof ExposureLayer)
                    {
                        ExposureLayer expLayer = (ExposureLayer)im.getLayers()[i];
                        expLayer.setExposure(2);
                        expLayer.setOffset(-0.25f);
                        expLayer.setGammaCorrection(0.5f);
                    }
                }

                // Save PSD
                im.save(psdPathAfterChange);

                // Save PNG
                PngOptions saveOptions = new PngOptions();
                saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
                im.save(pngExportPath, saveOptions);
            
                
                
                 // Exposure layer adding
            sourceFileName = dataDir+"PhotoExample.psd";
            psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";
            pngExportPath = dataDir + "PhotoExampleAddedExposure.png";

              PsdImage img = (PsdImage)Image.load(sourceFileName);
            
                ExposureLayer newlayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);
                
                // Save PSD
                img.save(psdPathAfterChange);

                // Save PNG
                PngOptions options = new PngOptions();
                options.setColorType(PngColorType.TruecolorWithAlpha);
                img.save(pngExportPath, options);
            
       //ExEnd:RenderingExposureAdjustmentLayer
    }
}

```
