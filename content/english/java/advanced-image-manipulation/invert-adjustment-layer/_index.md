---
title: Invert Adjustment Layer in Aspose.PSD for Java
linktitle: Invert Adjustment Layer in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 14
url: /java/advanced-image-manipulation/invert-adjustment-layer/
---

## Complete Source Code
```java

package com.aspose.psd.examples.DrawingAndFormattingImages;

import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;


public class InvertAdjustmentLayer {
        
    public static void main(String[] args) 
    {
       //ExStart:InvertAdjustmentLayer
       String dataDir = "Your Document Directory";
       
       String filePath = dataDir + "InvertStripes_before.psd";
       String outputPath = dataDir +  "InvertStripes_after.psd";
       
       PsdImage im = (PsdImage)Image.load(filePath);
       
       im.addInvertAdjustmentLayer();
       im.save(outputPath);
       //ExEnd:InvertAdjustmentLayer
    }

}

```
