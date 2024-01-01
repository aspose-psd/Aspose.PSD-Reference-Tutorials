---
title: Synchronize Root using Aspose.PSD for Java
linktitle: Synchronize Root using Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: 
type: docs
weight: 19
url: /java/advanced-techniques/synchronize-root/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.aspose.psd.examples.Conversion;

import com.aspose.psd.StreamContainer;

import com.aspose.psd.system.io.MemoryStream;



public class SyncRoot {
   
    public static void main(String[] args)
    {
       //ExStart:SyncRoot
       String dataDir = "Your Document Directory";
       
       
        // Create an instance of Stream container class and assign memory stream object.
       StreamContainer streamContainer = new StreamContainer(new java.io.ByteArrayInputStream(new byte[0]));
       
            try
        {
            // check if the access to the stream source is synchronized.
            synchronized (streamContainer.getSyncRoot())
            {
                    // do work
                    // now access to streamContainer is synchronized
            }
        }
        finally
        {
                streamContainer.dispose();
        }
       //ExEnd:SyncRoot
       
    }
}

```