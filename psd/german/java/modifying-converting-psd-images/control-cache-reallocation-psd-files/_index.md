---
date: 2026-03-13
description: Erfahren Sie, wie Sie PSD‑Bild‑Java‑Projekte erstellen und dabei die
  Cache‑Umverteilung mit Aspose.PSD für Java verwalten. Optimieren Sie Speicher- und
  Festplattenverbrauch effizient.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: PSD-Bild mit Java erstellen – Cache-Neuzuweisung steuern
url: /de/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cache-Neuzuweisung in PSD-Dateien steuern

## Introduction
If you need to **create PSD image java** projects efficiently, controlling cache reallocation is essential. When working with images and Photoshop files programmatically, efficiency is a key factor. Aspose.PSD for Java offers robust features to manage and manipulate PSD files seamlessly. One of the fundamental aspects of optimizing performance is controlling cache reallocation. Cache management helps in maintaining the balance between memory and disk usage, ensuring your application runs smoothly, without unexpected crashes or slowdowns.  

## Quick Answers
- **Was bewirkt die Cache-Neuzuweisung?** Sie balanciert Speicher- und Plattenverbrauch bei der Verarbeitung großer PSD-Dateien.  
- **Welcher Cache-Typ ist am besten für große Bilder?** `CacheOnDiskOnly` hält den Speicher frei, indem der Cache auf der Festplatte gespeichert wird.  
- **Wie viel Festplattenspeicher kann ich zuweisen?** Bis zu 1 GB (oder jede Größe, die Sie mit `setMaxDiskSpaceForCache` festlegen).  
- **Benötige ich eine Lizenz, um diese Funktionen zu nutzen?** Eine Lizenz entfernt die Trial‑Beschränkungen; siehe die Aspose‑Kaufseite.  
- **Kann ich die Cache‑Nutzung zur Laufzeit überwachen?** Ja, verwenden Sie `Cache.getAllocatedDiskBytesCount()` und `Cache.getAllocatedMemoryBytesCount()`.

## Why Control Cache Reallocation?
Managing cache is crucial when you **create PSD image java** applications that handle high‑resolution or multi‑layer files. Proper cache settings prevent out‑of‑memory errors, reduce GC pauses, and give you predictable performance on servers or desktop apps.

## Prerequisites
Before we jump into the coding part, there are a few things you need to ensure so that everything runs smoothly:
1. Java Development Kit (JDK): Stellen Sie sicher, dass das JDK auf Ihrem Rechner installiert ist. Sie können es von [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunterladen.  
2. Aspose.PSD for Java: Sie müssen die Aspose.PSD‑Bibliothek herunterladen. Die neueste Version finden Sie [here](https://releases.aspose.com/psd/java/).  
3. IDE Setup: Eine integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA oder Eclipse erleichtert die Verwaltung Ihres Codes.  
4. Basic Understanding of Java: Grundlegendes Verständnis von Java: Vertrautheit mit Java‑Programmierung hilft, die Konzepte und Code‑Snippets besser zu verstehen.  
5. Aspose License (Optional): Wenn Sie Wasserzeichen entfernen und die volle Funktionalität erhalten möchten, erwägen Sie den Kauf einer Lizenz [here](https://purchase.aspose.com/buy) oder testen Sie die kostenlose Testversion [here](https://releases.aspose.com/).

## Import Packages
Before we start writing the code, let’s make sure we have the necessary packages imported. Below is a brief list of what to include at the beginning of your Java file:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## How to Create PSD Image Java with Cache Control
Im Folgenden finden Sie eine Schritt‑für‑Schritt‑Anleitung, die die Cache‑Konfiguration direkt mit dem Prozess der Erstellung eines PSD‑Bildes in Java verknüpft.

### Step 1: Setting Up Your Data Directory
Zunächst müssen Sie ein Verzeichnis einrichten, in dem die Cache‑Dateien gespeichert werden sollen. Dies ist für eine effektive Cache‑Verwaltung unerlässlich.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Definiert das Verzeichnis für Ihren Dokument‑Cache.  
- `Cache.setCacheFolder(dataDir)`: Diese Methode legt den Cache‑Ordner auf das angegebene Verzeichnis fest. Jeder von Aspose erstellte Cache wird nun hier statt im Standard‑Temp‑Verzeichnis gespeichert.

### Step 2: Configuring Cache To Disk
Als Nächstes geben wir an, dass der Cache ausschließlich auf der Festplatte gespeichert werden soll. Das ist besonders nützlich, wenn Ihre Anwendung große Dateien verwendet und Sie sicherstellen möchten, dass der Speicher frei bleibt.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Diese Option stellt sicher, dass der Cache nicht im Speicher gehalten wird, was bei der Verarbeitung großer PSD‑Dateien ohne übermäßigen RAM‑Verbrauch vorteilhaft ist.

### Step 3: Setting Maximum Disk and Memory Cache Size
Jetzt beschränken wir die Cache‑Größen. Das ist entscheidend, da ein unbegrenzter Cache zu Leistungsproblemen führen kann.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Legt ein Limit von 1 GB für den Cache auf der Festplatte fest. Sie können diese Größe je nach Bedarf anpassen.  
- `Cache.setMaxMemoryForCache(1073741824)`: Beschränkt ebenfalls den In‑Memory‑Cache und stellt sicher, dass Ihre Anwendung nicht zu viel Speicher verbraucht.

### Step 4: Manage Cache Reallocation Strategy
Die Verwaltung, wie der Cache neu zugewiesen wird, ist entscheidend für die Aufrechterhaltung der Leistung. So können Sie ihn konfigurieren.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Wenn auf `false` gesetzt, erlaubt dies Aspose, die Cache‑Neuzuweisung flexibler zu verwalten, was zu besserer Leistung führen kann.

### Step 5: Check Allocated Cache Size
Dieser Schritt dient der Überwachung, wie viele Bytes derzeit für den Cache im Speicher oder auf der Festplatte zugewiesen sind. Implementieren wir das:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Speichert die Anzahl der auf der Festplatte zugewiesenen Bytes.  
- `long l2`: Speichert die Anzahl der im Speicher zugewiesenen Bytes.  
Sie können diese Werte jederzeit prüfen, um sicherzustellen, dass Ihre Anwendung Speicher- und Plattenverbrauch wie erwartet verwaltet.

### Step 6: Creating a PSD Image
Nachdem wir die Cache‑Konfigurationen festgelegt haben, erstellen wir ein einfaches PSD‑Bild.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Dieses Objekt ermöglicht das Festlegen von Optionen beim Erstellen eines Photoshop‑Bildes.  
- `Color[] color`: Ein Array, das die Farben enthält, die in der Bildpalette verwendet werden.

### Step 7: Saving Pixel Data to the Image
Jetzt füllen wir unser Bild mit Pixeldaten und speichern es.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Dies ist ein Array von Farbobjekten. Hier füllen wir es mit weißen Pixeln.  
- `image.savePixels(image.getBounds(), pixels)`: Diese Methode speichert die Pixeldaten im Bild. Sie aktualisiert das Bild mit den definierten Farben.

### Step 8: Monitoring Allocated Cache After Image Creation
Nach der Erstellung des Bildes ist es sinnvoll, erneut zu prüfen, wie viele Bytes für den Cache zugewiesen sind.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Erfasst die aktuelle Zuweisung auf der Festplatte nach der Bild‑Erstellung.  
- `long memoryBytes`: Erfasst die aktuelle Zuweisung im Speicher.  
Dieser Schritt hilft Ihnen zu bestimmen, wie viel Cache nach Ihren Vorgängen verbraucht wird.

### Step 9: Check for Proper Disposal
Abschließend ist es entscheidend, sicherzustellen, dass alle Aspose.PSD‑Objekte ordnungsgemäß freigegeben wurden, um Speicherlecks zu vermeiden.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` und `l2`: Diese Variablen helfen Ihnen, die endgültige Zuweisung zu prüfen. Wenn sie nicht null sind, deutet das darauf hin, dass einige Objekte nicht ordnungsgemäß freigegeben wurden.

## Common Issues and Solutions
- **Cache‑Ordner nicht erstellt** – Stellen Sie sicher, dass die Anwendung Schreibrechte für den Pfad hat, den Sie `Cache.setCacheFolder` übergeben haben.  
- **Out‑of‑Memory‑Fehler** – Überprüfen Sie, dass `Cache.setCacheType(CacheType.CacheOnDiskOnly)` vor dem Laden großer PSD‑Dateien angewendet wird.  
- **Unerwartete Cache‑Größe** – Verwenden Sie die Methoden `Cache.getAllocated*BytesCount()` nach jeder größeren Operation, um das Wachstum zu verfolgen.

## Frequently Asked Questions

**Q: Was ist Aspose.PSD?**  
A: Aspose.PSD ist eine Bibliothek für .NET‑ und Java‑Entwickler, um Photoshop (PSD)-Dateien programmgesteuert zu erstellen, zu manipulieren und zu konvertieren.

**Q: Wie prüfe ich die zugewiesene Cache‑Größe?**  
A: Verwenden Sie Methoden wie `Cache.getAllocatedDiskBytesCount()` und `Cache.getAllocatedMemoryBytesCount()`, um die aktuelle Cache‑Nutzung zu überwachen.

**Q: Kann ich ein benutzerdefiniertes Verzeichnis für den Cache festlegen?**  
A: Ja, Sie können ein anderes Verzeichnis angeben, indem Sie `Cache.setCacheFolder("Your Directory Path")` verwenden.

**Q: Ist Aspose.PSD kostenlos nutzbar?**  
A: Aspose.PSD ist eine kostenpflichtige Bibliothek, aber Sie können mit einer kostenlosen Testversion beginnen, die auf ihrer [website](https://releases.aspose.com/) verfügbar ist.

**Q: Was passiert, wenn ich Objekte nicht freigebe?**  
A: Das Nicht‑Freigeben von Objekten kann zu Speicherlecks führen, wodurch Ihre Anwendung mehr Ressourcen verbraucht als nötig.

## Conclusion
Controlling cache reallocation while you **create PSD image java** applications can make a significant difference in performance. By following the steps above, you’ll efficiently manage cache, minimize memory consumption, and generate high‑quality PSD files with Aspose.PSD for Java. Apply these techniques, and your projects will run smoother and scale better.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}