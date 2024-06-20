---
title: Convert PSB to JPG in Java
linktitle: Convert PSB to JPG in Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 10
url: /java/java-psb-to-image-format-conversion/convert-psb-to-jpg-java/
---

## Complete Source Code
```java

package com.aspose.psd.examples.ModifyingAndConvertingImages.PSB;

import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.JpegOptions;


public class PSBToJPG {
    
     public static void main(String[] args) 
    {
       //ExStart:PSBToJPG
       String dataDir = "Your Document Directory"
       
       String sourceFileName = dataDir + "Simple.psb";
     
       PsdLoadOptions options = new PsdLoadOptions();
       PsdImage image = (PsdImage)Image.load(sourceFileName, options);
       
       JpegOptions jpgoptions = new JpegOptions();
       jpgoptions.setQuality(95);
       
       // All jpeg and psd files must be readable
        image.save(dataDir + "Simple_output.jpg",jpgoptions);
        image.save(dataDir + "Simple_output.psb");
       //ExEnd:PSBToJPG
       
    }

}

```