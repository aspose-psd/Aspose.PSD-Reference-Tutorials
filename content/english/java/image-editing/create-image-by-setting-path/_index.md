---
title: Create Image by Setting Path in Aspose.PSD for Java
linktitle: Create Image by Setting Path in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 13
url: /java/image-editing/create-image-by-setting-path/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.DrawingAndFormattingImages;

import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;

/**
 *
 *  
 */
public class CreatingBySettingPath
{
    public static void main(String[] args) 
    {
       //ExStart:CreatingBySettingPath
       String dataDir = "Your Document Directory";
       String desName = dataDir + "CreatingAnImageBySettingPath_out.psd";
       // Creates an instance of PsdOptions and set its various properties
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setCompressionMethod(CompressionMethod.RLE);

        // Define the source property for the instance of PsdOptions. Second boolean parameter determines if the file is temporal or not
        psdOptions.setSource(new FileCreateSource(desName, false));
        // Creates an instance of Image and call Create method by passing the PsdOptions object
        Image image = Image.create(psdOptions, 500, 500);
        image.save();
       //ExEnd:CreatingBySettingPath
       
    }
}

```