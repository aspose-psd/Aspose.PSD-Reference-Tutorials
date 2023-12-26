---
title: Saving Images to Stream with Aspose.PSD for .NET
linktitle: Saving Images to Stream with Aspose.PSD for .NET
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 11
url: /net/file-saving-and-exporting/save-images-to-stream/
---

## Complete Source Code
```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
using System.IO;

namespace Aspose.PSD.Examples.Aspose.Conversion
{
    class SavingtoStream
    {
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir_PSD();

            //ExStart:SavingtoStream

            string sourceFile = dataDir + @"sample.psd";
            string destName = dataDir + "result.png";

            // load PSD image and replace the non found fonts.
            using (Image image = Image.Load(sourceFile))
            {
                PsdImage psdImage = (PsdImage)image;
                MemoryStream stream = new MemoryStream();
                psdImage.Save(stream, new PngOptions());
            }

            //ExEnd:SavingtoStream

        }
    }
}

```
