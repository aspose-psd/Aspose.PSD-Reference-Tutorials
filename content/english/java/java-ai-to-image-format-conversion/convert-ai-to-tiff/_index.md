---
title: Convert AI to TIFF in Java
linktitle: Convert AI to TIFF in Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 15
url: /java/java-ai-to-image-format-conversion/convert-ai-to-tiff/
---

## Complete Source Code
```java

package com.aspose.psd.examples.ModifyingAndConvertingImages.AI;

import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.imageoptions.TiffOptions;


public class AIToTIFF {
    
    public static void main(String[] args) 
    {
       //ExStart:AIToTIFF
       String dataDir = "Your Document Directory" 
       
       String sourceFileName    = dataDir + "34992OStroke.ai";       
       String outFileName       = dataDir + "34992OStroke.tiff";
       
       AiImage image = (AiImage)Image.load(sourceFileName);
       
             
       image.save(outFileName, new TiffOptions(TiffExpectedFormat.TiffDeflateRgba));
       //ExEnd:AIToTIFF
    }

}

```
