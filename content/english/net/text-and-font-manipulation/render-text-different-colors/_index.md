---
title: Rendering Text with Different Colors in Text Layers with Aspose.PSD for .NET
linktitle: Rendering Text with Different Colors in Text Layers with Aspose.PSD for .NET
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 10
url: /net/text-and-font-manipulation/render-text-different-colors/
---

## Complete Source Code
```csharp
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageOptions;
using System;

namespace Aspose.PSD.Examples.Aspose.Conversion
{
    class RenderTextWithDifferentColorsInTextLayer
    {
        public static void Run()
        {
            // The path to the documents directory.
            string SourceDir = "Your Document Directory";
            string OutputDir = RunExamples.GetDataDir_Output();

            //ExStart:1
            string sourceFile = SourceDir + @"text_ethalon_different_colors.psd";
            string destName = OutputDir + @"RenderTextWithDifferentColorsInTextLayer_out.png";

            // Load the noisy image 
            using (var psdImage = (PsdImage)Image.Load(sourceFile))
            {
                var txtLayer = (TextLayer)psdImage.Layers[1];
                txtLayer.TextData.UpdateLayerData();
                PngOptions pngOptions = new PngOptions();
                pngOptions.ColorType = PngColorType.TruecolorWithAlpha;
                psdImage.Save(destName, pngOptions);
            }
            //ExEnd:1

            Console.WriteLine("RenderTextWithDifferentColorsInTextLayer executed successfully");
        }
    }
}

```
