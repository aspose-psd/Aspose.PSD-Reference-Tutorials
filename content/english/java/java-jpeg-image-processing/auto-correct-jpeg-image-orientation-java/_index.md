---
title: Auto Correct JPEG Image Orientation in Java
linktitle: Auto Correct JPEG Image Orientation in Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 12
url: /java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.ModifyingAndConvertingImages.JPEG;

import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;


public class AutoCorrectOrientationOfJPEGImages {
    
    
    public static void main(String[] args) 
    {
       //ExStart:AutoCorrectOrientationOfJPEGImages
       String dataDir = "Your Document Directory"
      
       PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
       
        // Iterate over resources.
                
                for(int i =0; i < image.getImageResources().length; i++)
                {
                    // Find thumbnail resource. Typically they are in the Jpeg file format.
                    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource)
                    {
                        // Adjust thumbnail data.
                        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
                        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
                        if (exifData != null && exifData.getThumbnail() != null)
                        {
                            // If there is thumbnail stored then auto-rotate it.
                            PsdImage jpegImage =(PsdImage)exifData.getThumbnail();
                            if (jpegImage != null)
                            {
                                //jpegImage.autoRotate();
                            }
                        }
                    }
                }

                // Save image.
                image.save();
       
       //ExEnd:AutoCorrectOrientationOfJPEGImages
    }
}

```
