---
title: Force Font Cache with Aspose.PSD for Java
linktitle: Force Font Cache with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 11
url: /java/advanced-image-manipulation/force-font-cache/
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
import com.aspose.psd.OpenTypeFontsCache;

import com.aspose.psd.fileformats.psd.PsdImage;
import java.io.Console;
import java.util.concurrent.TimeUnit;

/**
 *
 *  
 */
public class ForceFontCache {
    public static void main(String[] args) throws InterruptedException 
    {
       //ExStart:ForceFontCache
     String dataDir = "Your Document Directory";
     
     PsdImage image = (PsdImage)Image.load(dataDir+"sample.psd");
     image.save(dataDir+"NoFont.psd");
     
     
       System.out.println("You have 2 minutes to install the font");
        Thread.sleep(2 * 60 * 1000);
        OpenTypeFontsCache.updateCache();
        
        PsdImage image1 = (PsdImage)Image.load(dataDir+ "sample.psd");
        image1.save(dataDir+"HasFont.psd");
     
     //ExEnd:ForceFontCache
     
    }
}

```
