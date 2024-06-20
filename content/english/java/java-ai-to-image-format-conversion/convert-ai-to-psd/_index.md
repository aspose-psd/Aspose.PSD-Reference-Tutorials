---
title: Convert AI to PSD in Java
linktitle: Convert AI to PSD in Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 14
url: /java/java-ai-to-image-format-conversion/convert-ai-to-psd/
---

## Complete Source Code
```java

package com.aspose.psd.examples.ModifyingAndConvertingImages.AI;

import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.PsdOptions;


public class AIToPSD {
    
    public static void main(String[] args) 
    {
       //ExStart:AIToPSD
       String dataDir = "Your Document Directory" 
       
       String sourceFileName    = dataDir + "34992OStroke.ai";       
       String outFileName       = dataDir + "34992OStroke.psd";
       
       AiImage image = (AiImage)Image.load(sourceFileName);
       
       PsdOptions options = new PsdOptions();
             
       image.save(outFileName, options);
       //ExEnd:AIToPSD
    }

}

```
