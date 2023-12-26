---
title: Supporting Outer Glow Effect in Aspose.PSD for .NET
linktitle: Supporting Outer Glow Effect in Aspose.PSD for .NET
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 16
url: /net/image-manipulation/supporting-outer-glow-effect/
---

## Complete Source Code
```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.DrawingAndFormattingImages
{
    public class SupportOfOuterGlowEffect
    {
        public static void Run()
        {
            // The path to the documents directory.
            string baseDir = "Your Document Directory";
            string outputDir = "Your Output Directory";
            
            //ExStart:SupportOfOuterGlowEffect
            //ExSummary:The following code demonstrates the OuterGlowEffect support.

            string src = Path.Combine(baseDir, "GreenLayer.psd");
            string outputPng = Path.Combine(outputDir, "output261.png");

            using (var image = (PsdImage)Image.Load(src))
            {
                OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
                effect.Range = 10;
                effect.Spread = 10;
                ((IColorFillSettings)effect.FillColor).Color = Color.Red;
                effect.Opacity = 128;
                effect.BlendMode = BlendMode.Normal;

                image.Save(outputPng, new PngOptions());
            }

            //ExEnd:SupportOfOuterGlowEffect
            
            File.Delete(outputPng);
            
            Console.WriteLine("SupportOfOuterGlowEffect executed successfully");
        }
        
    }
}
```
