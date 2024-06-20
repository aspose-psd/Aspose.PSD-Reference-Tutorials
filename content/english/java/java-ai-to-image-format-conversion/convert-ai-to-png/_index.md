---
title: Convert AI to PNG in Java
linktitle: Convert AI to PNG in Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 13
url: /java/java-ai-to-image-format-conversion/convert-ai-to-png/
---

## Complete Source Code
```java

package com.aspose.psd.examples.ModifyingAndConvertingImages.AI;

import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;


public class AIToPNG {
    
    public static void main(String[] args) 
    {
       //ExStart:AIToPNG
       String dataDir = "Your Document Directory" 
       
       String sourceFileName    = dataDir + "34992OStroke.ai";       
       String outFileName       = dataDir + "34992OStroke.png";
       
       AiImage image = (AiImage)Image.load(sourceFileName);
       
       PngOptions options = new PngOptions();
       options.setColorType(PngColorType.TruecolorWithAlpha);
       
       image.save(outFileName, options);
       //ExEnd:AIToPNG
    }

}

```
