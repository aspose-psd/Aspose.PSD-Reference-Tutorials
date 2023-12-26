---
title: Handling MLST Resources in Aspose.PSD for .NET
linktitle: Handling MLST Resources
second_title: Aspose.PSD .NET API
description: 
type: docs
weight: 14
url: /net/psd-file-manipulation/mlst-resources/
---

## Complete Source Code
```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures;

namespace Aspose.PSD.Examples.Aspose.Animation
{
    public class SupportOfMlstResource
    {
        public static void Run()
        {
            // The path to the documents directory.
            string baseDir = "Your Document Directory";
            string outputDir = "Your Output Directory";
            
            //ExStart:SupportOfMlstResource
            //ExSummary:The following code demonstrates support of MlstResource resource that gives a low-level mechanism to manipulate the layer states.
            
            string sourceFile = Path.Combine(baseDir, "image1219.psd");
            string outputPsd = Path.Combine(outputDir, "output_image1219.psd");

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))
            {
                Layer layer1 = image.Layers[1];
                ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
                MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];
            
                ListStructure layerStatesList = (ListStructure)mlstResource.Items[1];
                DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Types[1];
                BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Structures[0];
            
                // Disable layer 1 on frame 1
                layerEnabled.Value = false;
            
                image.Save(outputPsd);
            }
            
            //ExEnd:SupportOfMlstResource
            
            File.Delete(outputPsd);
            
            Console.WriteLine("SupportOfMlstResource executed successfully");
        }
    }
}
```