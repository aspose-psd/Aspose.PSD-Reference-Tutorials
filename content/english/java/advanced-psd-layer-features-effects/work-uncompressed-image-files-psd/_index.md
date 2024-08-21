---
title: Work with Uncompressed Image Files in PSD using Java
linktitle: Work with Uncompressed Image Files in PSD using Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 27
url: /java/advanced-psd-layer-features-effects/work-uncompressed-image-files-psd/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;


public class UncompressedImageUsingFile {
    
    public static void main(String[] args) 
    {
       //ExStart:UncompressedImageUsingFile
       String dataDir = "Your Document Directory";
       
        // Load a PSD file as an image and cast it into PsdImage
     PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
            
    PsdOptions saveOptions = new PsdOptions();
    saveOptions.setCompressionMethod(CompressionMethod.Raw);
    psdImage.save(dataDir+"uncompressed_out.psd", saveOptions);
         
    // Now reopen the newly created image.
            PsdImage img = (PsdImage)Image.load(dataDir+"uncompressed_out.psd");
            
                Graphics graphics = new Graphics(img);
                // Perform graphics operations.
            
       //ExEnd:UncompressedImageUsingFile
    }
}

```