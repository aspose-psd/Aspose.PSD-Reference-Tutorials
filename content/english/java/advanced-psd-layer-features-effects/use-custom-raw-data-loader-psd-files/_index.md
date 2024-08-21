---
title: Use Custom Raw Data Loader in PSD Files - Java
linktitle: Use Custom Raw Data Loader in PSD Files - Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 29
url: /java/advanced-psd-layer-features-effects/use-custom-raw-data-loader-psd-files/
---

## Complete Source Code
```java

import com.aspose.psd.*;

public class UseCustomRawDataLoader
{
    public static void main(String[] args)
    {
        //ExStart:UseCustomRawDataLoader
        class RawDataTester implements IPartialRawDataLoader
        {
            public void process(Rectangle rectangle, byte[] pixels, Point start, Point end)
            {
            }

            public void process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions)
            {
            }
        }

        String sourceDir = "Your Source Directory";
        String inFilePath = sourceDir + "CmykWithAlpha.psd";

        RasterImage image = (RasterImage)Image.load(inFilePath);
        try
        {
            RawDataSettings rawDataSettings = image.getRawDataSettings();
            RawDataTester loader = new RawDataTester();
            image.loadRawData(image.getBounds(), rawDataSettings, loader);
        }
        finally
        {
            image.dispose();
        }
        //ExEnd:UseCustomRawDataLoader
    }
}

```