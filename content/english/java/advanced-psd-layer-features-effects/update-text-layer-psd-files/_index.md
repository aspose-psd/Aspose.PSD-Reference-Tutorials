---
title: Update Text Layer in PSD Files with Aspose.PSD Java
linktitle: Update Text Layer in PSD Files with Aspose.PSD Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 28
url: /java/advanced-psd-layer-features-effects/update-text-layer-psd-files/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;


public class UpdateTextLayerInPSDFile {
    public static void main(String[] args) 
    {
       //ExStart:UpdateTextLayerInPSDFile
       String dataDir = "Your Document Directory";
       
       // Load a PSD file as an image and cast it into PsdImage
       PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
       
       for(int i=0; i < psdImage.getLayers().length; i++ )
                {
                    if (psdImage.getLayers()[i] instanceof TextLayer)
                    {
                        TextLayer textLayer = (TextLayer)psdImage.getLayers()[i]  ;
                        textLayer.updateText("test update", new Point(0, 0), 15.0f, Color.getPurple());
                    }
                }

                psdImage.save(dataDir + "UpdateTextLayerInPSDFile_out.psd");
       //ExEnd:UpdateTextLayerInPSDFile
    }
}

```
