---
title: Export Channel Mixer Adjustment Layer in PSD - Java
linktitle: Export Channel Mixer Adjustment Layer in PSD - Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 14
url: /java/psd-layer-management-effects/export-channel-mixer-adjustment-layer-psd/
---

## Complete Source Code
```java/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CmykChannelMixerLayer;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.RgbChannelMixerLayer;
import com.aspose.psd.imageoptions.PngOptions;


public class RenderingExportOfChannelMixerAdjusmentLyer {
    public static void main(String[] args) 
    {
       //ExStart:RenderingExportOfChannelMixerAdjusmentLyer
       String dataDir = "Your Document Directory";
    
        // Rgb Channel Mixer
        String sourceFileName = dataDir + "ChannelMixerAdjustmentLayerRgb.psd";
        String psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.psd";
        String pngExportPath = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.png";
    
        
        PsdImage im = (PsdImage)Image.load(sourceFileName);
        
        for(int i=0; i < im.getLayers().length; i++ )
                {
                    if (im.getLayers()[i] instanceof RgbChannelMixerLayer)
                    {
                        RgbChannelMixerLayer rgbLayer = (RgbChannelMixerLayer)im.getLayers()[i];
                        rgbLayer.getRedChannel().setBlue((short)100);
                        rgbLayer.getBlueChannel().setGreen((short)-100);
                        rgbLayer.getGreenChannel().setConstant((short)50);
                    }
                }

                // Save PSD
                im.save(psdPathAfterChange);
                
                // Save PNG
                PngOptions saveOptions = new PngOptions();
                saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
                im.save(pngExportPath, saveOptions);
                
                
                
             // Cmyk Channel Mixer
            sourceFileName = dataDir+"ChannelMixerAdjustmentLayerCmyk.psd";
            psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.psd";
            pngExportPath = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.png";
            
           PsdImage img = (PsdImage)Image.load(sourceFileName);
           
                for(int i=0; i < img.getLayers().length; i++ )
                {
                    if (img.getLayers()[i] instanceof CmykChannelMixerLayer)
                    {
                        CmykChannelMixerLayer cmykLayer = (CmykChannelMixerLayer)img.getLayers()[i];
                        cmykLayer.getCyanChannel().setBlack((short)20);
                        cmykLayer.getMagentaChannel().setYellow((short)50);
                        cmykLayer.getYellowChannel().setCyan((short)-25);
                        cmykLayer.getBlackChannel().setYellow((short)25);
                    }
                }

                // Save PSD
                img.save(psdPathAfterChange);

                // Save PNG
                PngOptions options = new PngOptions();
                options.setColorType(PngColorType.TruecolorWithAlpha);
                img.save(pngExportPath, options);
                
    //ExEnd:RenderingExportOfChannelMixerAdjusmentLyer
    }
    
}

```
