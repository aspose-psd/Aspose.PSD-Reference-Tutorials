---
title: Loading Images from Stream with Aspose.PSD for Java
linktitle: Loading Images from Stream with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 11
url: /java/advanced-techniques/loading-images-from-stream/
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
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.MemoryStream;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;

/**
 *
 *  
 */
public class LoadingFromStream {
    
    public static void main(String[] args) throws FileNotFoundException
    {
       //ExStart:LoadingFromStream
       String dataDir = "Your Document Directory";
       
        String sourceFile = dataDir + "sample.psd";
        String destName = dataDir + "result.png";
                
         
         FileInputStream inputStream = new FileInputStream(sourceFile);
         Image image = Image.load(inputStream);
         
         PsdImage psdImage = (PsdImage)image;
         FileOutputStream outputStream = new FileOutputStream(destName);
        psdImage.save(outputStream, new PngOptions());
        
       //ExEnd:LoadingFromStream
       
    }
}

```
