---
title: Working with Blend Modes in Aspose.PSD for .NET
linktitle: Working with Blend Modes
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 16
url: /net/layer-effects/working-with-blend-modes/
---

## Complete Source Code
```csharp
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;

namespace Aspose.PSD.Examples.Aspose.DrawingAndFormattingImages
{
    class SupportBlendModes
    {

        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //ExStart:SupportBlendModes
            var files = new string[]
      {
           "Normal",
           "Dissolve",
           "Darken",
           "Multiply",
           "ColorBurn",
           "LinearBurn",
           "DarkerColor",
           "Lighten",
           "Screen",
           "ColorDodge",
           "LinearDodgeAdd",
           "LightenColor",
           "Overlay",
           "SoftLight",
           "HardLight",
           "VividLight",
           "LinearLight",
           "PinLight",
           "HardMix",
           "Difference",
           "Exclusion",
           "Subtract",
           "Divide",
            "Hue",
           "Saturation",
            "Color",
           "Luminosity",
            };

            foreach (var fileName in files)
            {

                using (var im = (PsdImage)Image.Load(dataDir + fileName + ".psd"))
                {
                    // Export to PNG
                    var saveOptions = new PngOptions();
                    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;
                    var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";
                    im.Save(pngExportPath100, saveOptions);

                    // Set opacity 50%
                    im.Layers[1].Opacity = 127;
                    var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";
                    im.Save(pngExportPath50, saveOptions);
                }
            }
        }
        //ExEnd:SupportBlendModes

    }
}
```