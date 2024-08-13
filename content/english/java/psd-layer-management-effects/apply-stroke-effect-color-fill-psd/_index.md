---
title: Apply Stroke Effect with Color Fill in PSD - Java
linktitle: Apply Stroke Effect with Color Fill in PSD - Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 21
url: /java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;


public class StrokeEffectWithColorFill {
    
    public static void main(String[] args) 
    {
       //ExStart:StrokeEffectWithColorFill
       String dataDir = "Your Document Directory";
       // Implement rendering of Stroke effect with Color Fill for export
        String sourceFileName = dataDir + "StrokeComplex.psd";
        String exportPath = dataDir + "StrokeComplexRendering.psd";
        String exportPathPng = dataDir+"StrokeComplexRendering.png";
       
        PsdLoadOptions loadOptions = new PsdLoadOptions();
        loadOptions.setLoadEffectsResource(true);
        PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
            
                for (int i = 0; i < im.getLayers().length; i++)
                {
                    StrokeEffect effect = (StrokeEffect)im.getLayers()[i].getBlendingOptions().getEffects()[0];
                    ColorFillSettings settings = (ColorFillSettings)effect.getFillSettings();
                    settings.setColor(Color.getDeepPink());
                }

                // Save psd
                im.save(exportPath, new PsdOptions());

           PngOptions option =  new PngOptions();
           option.setColorType(PngColorType.TruecolorWithAlpha);
                // Save png
                im.save(exportPathPng, option);
             
       //ExEnd:StrokeEffectWithColorFill
    }
}

```
