---
title: Convert CMYK PSD to CMYK TIFF using Aspose.PSD for Java
linktitle: Convert CMYK PSD to CMYK TIFF using Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 10
url: /java/psd-conversion/cmyk-psd-to-cmyk-tiff/
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

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.imageoptions.TiffOptions;

/**
 *
 *  
 */
public class CMYKPSDtoCMYKTiff {
    
    public static void main(String[] args) 
    {
       //ExStart:CMYKPSDtoCMYKTiff
       String dataDir = "Your Document Directory";
       
       String sourceFile = dataDir + "sample.psd";
       String destName = dataDir + "output.tiff";
       
       Image image = Image.load(sourceFile);
       image.save(destName, new TiffOptions(TiffExpectedFormat.TiffLzwCmyk));
       //ExEnd:CMYKPSDtoCMYKTiff
    }
}

```
