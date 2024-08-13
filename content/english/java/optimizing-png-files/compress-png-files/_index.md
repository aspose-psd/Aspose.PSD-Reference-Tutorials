---
title: Compress PNG Files using Aspose.PSD for Java
linktitle: Compress PNG Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 12
url: /java/optimizing-png-files/compress-png-files/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;

/**
 *
 *  
 */
public class CompressingFiles {
     public static void main(String[] args) 
    {
       //ExStart:CompressingFiles
       String dataDir = "Your Document Directory";
       
       PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
       // Loop over possible CompressionLevel range
                for (int i = 0; i <= 9; i++)
                {
                    // Create an instance of PngOptions for each resultant PNG, Set CompressionLevel and  Save result on disk
                    PngOptions options = new PngOptions();
                    options.setCompressionLevel(i);
                    psdImage.save(dataDir+i + "_out.png", options);
                }
       //ExEnd:CompressingFiles
    }
    
}

```
