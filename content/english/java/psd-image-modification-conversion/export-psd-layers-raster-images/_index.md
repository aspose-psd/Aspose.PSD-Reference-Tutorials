---
title: Export PSD Layers to Raster Images using Java
linktitle: Export PSD Layers to Raster Images using Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 12
url: /java/psd-image-modification-conversion/export-psd-layers-raster-images/
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
import com.aspose.psd.imageoptions.PngOptions;

/**
 *
 *  
 */
public class ExportPSDLayerToRasterImage {
    
    public static void main(String[] args) 
    {
       //ExStart:ExportPSDLayerToRasterImage
       String dataDir = "Your Document Directory";
       
       // Load a PSD file as an image and caste it into PsdImage
          PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
            
                // Create an instance of PngOptions class
                PngOptions pngOptions = new PngOptions();
                pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

                // Loop through the list of layers
                for (int i = 0; i < psdImage.getLayers().length; i++)
                {
                    // Convert and save the layer to PNG file format.
                    psdImage.getLayers()[i].save(dataDir + String.format("layer_out%d.png", i + 1), pngOptions);
                }
            
       //ExEnd:ExportPSDLayerToRasterImage
    }
}

```
