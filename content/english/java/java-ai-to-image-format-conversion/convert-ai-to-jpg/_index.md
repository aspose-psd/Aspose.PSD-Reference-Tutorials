---
title: Convert AI to JPG in Java
linktitle: Convert AI to JPG in Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 11
url: /java/java-ai-to-image-format-conversion/convert-ai-to-jpg/
---

## Complete Source Code
```java

package com.aspose.psd.examples.ModifyingAndConvertingImages.AI;

import com.aspose.psd.Image;
import com.aspose.psd.ImageOptionsBase;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.JpegOptions;


public class AIToJPG {

    public static void main(String[] args) 
    {
       //ExStart:AIToJPG
       String dataDir = "Your Document Directory" 
       
       String sourceFileName    = dataDir + "34992OStroke.ai";       
       String outFileName       = dataDir + "34992OStroke.jpg";
       
       AiImage image = (AiImage)Image.load(sourceFileName);
       
       JpegOptions options = new JpegOptions();
       options.setQuality(85);
       
       image.save(outFileName, options);
       //ExEnd:AIToJPG
    }
}

```
