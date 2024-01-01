---
title: Bradley Thresholding in Aspose.PSD for Java
linktitle: Bradley Thresholding in Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 16
url: /java/image-processing/bradley-thresholding/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.Conversion;

import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;

/**
 *
 *  
 */
public class BradleyThreshold
{
     public static void main(String[] args) 
    {
       //ExStart:BradleyThreshold
       String dataDir = "Your Document Directory";
       String sourceFile = dataDir + "sample.psd";
       String destName = dataDir + "binarized_out.png";
       
       // Load an image
       PsdImage image = (PsdImage)Image.load(sourceFile);
       
       // Define threshold value, Call BinarizeBradley method and pass the threshold value as parameter and Save the output image
        double threshold = 0.15;
        image.binarizeBradley(threshold);
        image.save(destName, new PngOptions());
       //ExEnd:BradleyThreshold
       
    }
}

```