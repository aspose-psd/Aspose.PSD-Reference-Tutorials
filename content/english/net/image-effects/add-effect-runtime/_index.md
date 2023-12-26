---
title: Adding Effects at Runtime in Aspose.PSD for .NET
linktitle: Adding Effects at Runtime
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 10
url: /net/image-effects/add-effect-runtime/
---

## Complete Source Code
```csharp
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageLoadOptions;

namespace Aspose.PSD.Examples.Aspose.DrawingAndFormattingImages
{
    class AddEffectAtRunTime
    {
        public static void Run()
        {
            string dataDir = "Your Document Directory";
            //ExStart:AddEffectAtRunTime

            // Add color overlay layer effect at runtime
            string sourceFileName = dataDir + "ThreeRegularLayers.psd";
            string exportPath = dataDir + "ThreeRegularLayersChanged.psd";

            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
            {
                var effect = im.Layers[1].BlendingOptions.AddColorOverlay();
                effect.Color = Color.Green;
                effect.Opacity = 128;
                effect.BlendMode = BlendMode.Normal;

                im.Save(exportPath);
            }
            //ExEnd:AddEffectAtRunTime
        }
    }
}
```