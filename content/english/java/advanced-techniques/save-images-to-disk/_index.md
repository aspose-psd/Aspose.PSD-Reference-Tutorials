---
title: Save Images to Disk with Aspose.PSD for Java
linktitle: Save Images to Disk with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 15
url: /java/advanced-techniques/save-images-to-disk/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.Conversion;

import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;

/**
 *
 *  
 */
public class SavingToDisk
{
    public static void main(String[] args)
    {
       //ExStart:SavingToDisk
       String dataDir = "Your Document Directory";
       String sourceFile = dataDir + "sample.psd";
       String destName = dataDir + "result.png";

        // load PSD image and replace the non found fonts.
        Image image = Image.load(sourceFile);
        
        PsdImage psdImage = (PsdImage)image;
        psdImage.save(destName, new PngOptions());
        
       //ExEnd:SavingToDisk
    }
}

```