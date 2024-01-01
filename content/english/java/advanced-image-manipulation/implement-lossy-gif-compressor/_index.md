---
title: Implement Lossy GIF Compressor in Aspose.PSD for Java
linktitle: Implement Lossy GIF Compressor in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 13
url: /java/advanced-image-manipulation/implement-lossy-gif-compressor/
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

import com.aspose.psd.imageoptions.GifOptions;

/**
 *
 *  
 */
public class ImplementLossyGIFCompressor {
    
    public static void main(String[] args) throws InterruptedException 
    {
       //ExStart:ImplementLossyGIFCompressor
     String dataDir = "Your Document Directory";
    
      String sourceFile = dataDir + "sample.psd";
      String destName = dataDir + "anim_lossy-200.gif";

      
      // Load an existing image into an instance of RasterImage class       
       Image image = Image.load(sourceFile);
      
       GifOptions gifExport = new GifOptions();
       gifExport.setMaxDiff(80);
      image.save(dataDir + "anim_lossy-80.gif", gifExport);
      
      
      gifExport.setMaxDiff(200);
       image.save(destName, gifExport);
      //ExEnd:ImplementLossyGIFCompressor
    }
}

```