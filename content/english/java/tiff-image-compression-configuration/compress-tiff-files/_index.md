---
title: Compress TIFF Files using Aspose.PSD for Java
linktitle: Compress TIFF Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 10
url: /java/tiff-image-compression-configuration/compress-tiff-files/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.ColorPaletteHelper;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;

/**
 *
 *  
 */
public class CompressingTiff {
     public static void main(String[] args) 
    {
       //ExStart:CompressingTiff
       String dataDir = "Your Document Directory";
       
       
       // Load a PSD file as an image and cast it into PsdImage
       PsdImage psdImage = (PsdImage)Image.load(dataDir+"layers.psd");
   // Create an instance of TiffOptions for the resultant image
                TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

                // Set BitsPerSample, Compression, Photometric mode and graycale palette
             int[] ushort  =  {4};  
                outputSettings.setBitsPerSample(ushort);
                outputSettings.setCompression(TiffCompressions.Lzw);
                outputSettings.setPhotometric(TiffPhotometrics.Palette);
                outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(true));

                psdImage.save(dataDir+"SampleTiff_out.tiff", outputSettings);
       //ExEnd:CompressingTiff
    }
}

```
