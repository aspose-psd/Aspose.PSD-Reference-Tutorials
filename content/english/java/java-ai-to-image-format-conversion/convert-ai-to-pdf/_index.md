---
title: Convert AI to PDF in Java
linktitle: Convert AI to PDF in Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 12
url: /java/java-ai-to-image-format-conversion/convert-ai-to-pdf/
---

## Complete Source Code
```java

package com.aspose.psd.examples.ModifyingAndConvertingImages.AI;

import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.PdfOptions;


public class AIToPDF {
    
    public static void main(String[] args) 
    {
        //ExStart:AIToPDF
        String dataDir = "Your Document Directory" 
       
        String sourceFileName    = dataDir + "34992OStroke.ai";       
        String outFileName       = dataDir + "34992OStroke.pdf";
       
        AiImage image = (AiImage)Image.load(sourceFileName);
       
        PdfOptions options = new PdfOptions();
             
        image.save(outFileName, options);
        //ExEnd:AIToPDF
    }
}
```
