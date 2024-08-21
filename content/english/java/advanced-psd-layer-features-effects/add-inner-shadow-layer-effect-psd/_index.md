---
title: Add Inner Shadow Layer Effect in PSD with Java
linktitle: Add Inner Shadow Layer Effect in PSD with Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 12
url: /java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
---

## Complete Source Code
```java

import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;

public class SupportInnerShadowLayerEffect
{
    public static void main(String[] args)
    {
        //ExStart:SupportInnerShadowLayerEffect
        String sourceDir = "Your Source Directory";
        String outputDir = "Your Document Directory";

        String sourceFile = sourceDir + "sample.psd";
        String destName = outputDir + "sample_out.psd";

        PsdLoadOptions loadOptions = new PsdLoadOptions();
        loadOptions.setLoadEffectsResource(true);

        // Load an existing image into an instance of PsdImage class
        PsdImage image = (PsdImage)Image.load(sourceFile, loadOptions);
        try
        {
            Layer layer = image.getLayers()[image.getLayers().length - 1];
            IShadowEffect shadowEffect = (IShadowEffect)layer.getBlendingOptions().getEffects()[0];

            shadowEffect.setColor(Color.getGreen());
            shadowEffect.setOpacity((byte)128);
            shadowEffect.setDistance(1);
            shadowEffect.setUseGlobalLight(false);
            shadowEffect.setSize(2);
            shadowEffect.setAngle(45);
            shadowEffect.setSpread(50);
            shadowEffect.setNoise(5);

            image.save(destName, new PsdOptions(image));
        }
        finally
        {
            image.dispose();
        }
        //ExEnd:SupportInnerShadowLayerEffect
    }
}

```