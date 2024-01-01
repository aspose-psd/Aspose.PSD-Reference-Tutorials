---
title: Resizing with Resize Type Enumeration in Aspose.PSD for Java
linktitle: Resizing with Resize Type Enumeration in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 18
url: /java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
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
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;

/**
 *
 *  
 */
public class ResizingWithResizeTypeEnumeration
{
    public static void main(String[] args)  
    {
       //ExStart:ResizingWithResizeTypeEnumeration
     String dataDir = "Your Document Directory";
     
      String sourceFile = dataDir + "sample.psd";
      String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
      
      // Load an existing image into an instance of RasterImage class
      Image image = Image.load(sourceFile);
      image.resize(300, 300, ResizeType.LanczosResample);
      image.save(destName, new JpegOptions());
      //ExEnd:ResizingWithResizeTypeEnumeration
    }
    
}

```
