---
title: Export Images to PSD Format with Java
linktitle: Export Images to PSD Format with Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 11
url: /java/psd-image-modification-conversion/export-images-psd-format/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;


public class ExportImageToPSD {
    public static void main(String[] args)
    {
       //ExStart:ExportImageToPSD
       String dataDir = "Your Document Directory";
       
       // Create a new image from scratch.
            PsdImage bmpImage = new PsdImage(300, 300);
            
                // Fill image data.
                Graphics graphics = new Graphics(bmpImage);
                graphics.clear(Color.getWhite());
                Pen pen = new Pen(Color.getBrown());
                graphics.drawRectangle(pen, bmpImage.getBounds());

                // Create an instance of PsdOptions, Set it's various properties Save image to disk in PSD format
                PsdOptions psdOptions = new PsdOptions();
                psdOptions.setColorMode(ColorModes.Rgb);
                psdOptions.setCompressionMethod(CompressionMethod.Raw);
                psdOptions.setVersion(4);
                bmpImage.save(dataDir+"ExportImageToPSD_output.psd", psdOptions);
             
       
       //ExEnd:ExportImageToPSD
    }
}

```
