---
title: Support RGB Color in PSD Files with Aspose.PSD Java
linktitle: Support RGB Color in PSD Files with Aspose.PSD Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 20
url: /java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.JpegOptions;
import com.aspose.psd.imageoptions.PsdOptions;


public class SupportOfRGBColor {
    public static void main(String[] args) 
    {
       //ExStart:SupportOfRGBColor
       String dataDir = "Your Document Directory";
       
        // Support of RGB Color mode with 16bits/channel (64 bits per color)
        String sourceFileName = dataDir + "inRgb16.psd";
        String outputFilePathJpg = dataDir+ "outRgb16.jpg";
        String outputFilePathPsd = dataDir + "outRgb16.psd";
        
        
         PsdLoadOptions options = new PsdLoadOptions();
         
         PsdImage image = (PsdImage)Image.load(sourceFileName, options);
            
                image.save(outputFilePathPsd, new PsdOptions(image));
                JpegOptions saveOptions = new JpegOptions();
                saveOptions.setQuality(100);
                image.save(outputFilePathJpg, saveOptions);
            
       //ExEnd:SupportOfRGBColor
       
    }
}

```