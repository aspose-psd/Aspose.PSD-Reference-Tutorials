---
title: Merge PSD Layers with Aspose.PSD for Java
linktitle: Merge PSD Layers with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 11
url: /java/psd-layer-management-effects/merge-psd-layers/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;


public class MergePSDLayers {

 public static void main(String[] args) 
    {
       //ExStart:MergePSDLayers
       String dataDir = "Your Document Directory";
       
       // Load a PSD file as an image and cast it into PsdImage
       PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
       
       // Create JPEG option class object, Set its properties and save image
        JpegOptions jpgOptions = new JpegOptions();
        psdImage.save(dataDir + "MergePSDlayers_output.jpg", jpgOptions);
       //ExEnd:MergePSDLayers
    }
}

```
