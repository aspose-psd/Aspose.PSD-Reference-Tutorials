---
title: Resize Image Proportionally with Aspose.PSD for Java
linktitle: Resize Image Proportionally with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 17
url: /java/advanced-image-manipulation/resize-image-proportionally/
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
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.imageoptions.PngOptions;

/**
 *
 *  
 */
public class ResizeImageProportionally {
    
    public static void main(String[] args)  
    {
       //ExStart:ResizeImageProportionally
     String dataDir = Utils.getDataDir(ResizeImageProportionally.class) + "DrawingAndFormattingImages/";
     
     String sourceFile = dataDir + "sample.psd";
     String destName = dataDir + "SimpleResizeImageProportionally_out.png";
     
     Image image = Image.load(sourceFile);
     
     if (!image.isCached())
        {
            image.cacheData();
        }
        // Specifying width and height
        int newWidth = image.getWidth() / 2;
        image.resizeWidthProportionally(newWidth);
        int newHeight = image.getHeight() / 2;
        image.resizeHeightProportionally(newHeight);
        image.save(destName, new PngOptions());
     //ExEnd:ResizeImageProportionally
    }
}

```
