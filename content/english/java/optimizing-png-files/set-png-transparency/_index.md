---
title: Set PNG Transparency in Aspose.PSD for Java
linktitle: Set PNG Transparency in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 15
url: /java/optimizing-png-files/set-png-transparency/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;


public class SpecifyTransparency {
     public static void main(String[] args)
    {
       //ExStart:SpecifyTransparency
       String dataDir = "Your Document Directory";
       
       PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
       
        // Initialize PNG image with psd image pixel data.
        PsdImage pngImage = new PsdImage(psdImage);
        
         // specify the PNG image transparency options and save to file.
                    pngImage.setTransparentColor(Color.getWhite());
                    pngImage.setTransparentColor(true);
                    pngImage.save(dataDir+"Specify_Transparency_result.png");
    //ExEnd:SpecifyTransparency
    }
}

```
