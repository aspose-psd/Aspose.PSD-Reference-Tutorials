---
title: Convert PSB to PDF in Java
linktitle: Convert PSB to PDF in Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 11
url: /java/java-psb-to-image-format-conversion/convert-psb-to-pdf-java/
---

## Complete Source Code
```java

package com.aspose.psd.examples.ModifyingAndConvertingImages.PSB;

import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PdfOptions;


public class PSBToPDF {

    public static void main(String[] args) 
    {
       //ExStart:PSBToPDF
       String dataDir = "Your Document Directory"       
       String sourceFileName = dataDir + "Simple.psb";
     
       
       PsdImage image = (PsdImage)Image.load(sourceFileName);          
       
       image.save(dataDir + "Simple_output.pdf",new PdfOptions());
      
       //ExEnd:PSBToPDF
       
    }
}

```
