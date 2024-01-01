---
title: Perform Simple Resizing with Aspose.PSD for Java
linktitle: Perform Simple Resizing with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 11
url: /java/basic-image-operations/simple-resizing/
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

import com.aspose.psd.imageoptions.JpegOptions;

/**
 *
 *  
 */
public class SimpleResizing {
    
    public static void main(String[] args)  
    {
       //ExStart:SimpleResizing
       String dataDir = "Your Document Directory";
       
       String sourceFile = dataDir + "sample.psd";
       String destName = dataDir + "SimpleResizing_out.jpg";

        // Load an existing image into an instance of RasterImage class
        Image image = Image.load(sourceFile);
        
        image.resize(300, 300);
        image.save(destName, new JpegOptions());
       //ExEnd:SimpleResizing
    }
}

```