---
title: Render Text with Different Colors in Text Layer using Aspose.PSD for Java
linktitle: Render Text with Different Colors in Text Layer using Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 13
url: /java/advanced-techniques/render-text-different-colors/
---

## Complete Source Code
```java
package com.aspose.psd.examples.Conversion;

import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;


public class RenderTextWithDifferentColorsInTextLayer {
    public static void main(String[] args) {
        //ExStart:1
        String sourceDir = "Your Document Directory";
        String outputDir = "Your Document Directory";

        String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
        String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

        PsdImage psdImage = null;
        try
        {
            psdImage = (PsdImage) Image.load(targetFilePath);
            TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
            txtLayer.getTextData().updateLayerData();
            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
            psdImage.save(resultFilePath, pngOptions);
        }
        finally
        {
            if (psdImage != null) psdImage.dispose();
        }
        //ExEnd:1

        System.out.println("RenderTextWithDifferentColorsInTextLayer executed successfully");
    }
}

```
