---
title: Unterstützt Schatteneffekte in Aspose.PSD für Java
linktitle: Unterstützt Schatteneffekte
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java faszinierende Schatteneffekte zu Bildern hinzufügen. Verbessern Sie Ihr Grafikdesign mit diesem Schritt-für-Schritt-Tutorial.
weight: 13
url: /de/java/basic-image-operations/support-shadow-effect/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unterstützt Schatteneffekte in Aspose.PSD für Java

## Einführung

Das Verbessern von Bildern mit Schatteneffekten ist im Grafikdesign eine gängige Praxis, um Tiefe und Realismus zu verleihen. Aspose.PSD für Java bietet robuste Unterstützung für Schatteneffekte, sodass Entwickler diese Effekte mühelos in ihre Java-Anwendungen integrieren können. In diesem Tutorial erfahren Sie Schritt für Schritt, wie Sie Schatteneffekte mit Aspose.PSD unterstützen.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Grundkenntnisse der Java-Programmierung.
-  Aspose.PSD für Java installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/psd/java/).

## Pakete importieren

Stellen Sie sicher, dass Sie die erforderlichen Pakete importiert haben, um die Aspose.PSD-Funktionen in Ihrer Java-Anwendung nutzen zu können. Verwenden Sie den folgenden Codeausschnitt als Leitfaden:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Schritt 1: Laden Sie das PSD-Bild

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Schritt 2: Schatteneffekt abrufen

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Schritt 3: Standardeinstellungen überprüfen

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

## Schritt 4: Schatteneffekt anpassen

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## Schritt 5: Speichern Sie das geänderte Bild

```java
im.save(psdPathAfterChange);
```

## Abschluss

Mit diesen einfachen Schritten können Sie mühelos Schatteneffekte in Aspose.PSD für Java unterstützen und so die visuelle Attraktivität Ihrer Bilder verbessern.

## Häufig gestellte Fragen

### F1: Ist Aspose.PSD für Java für professionelle Grafikdesignprojekte geeignet?

A1: Auf jeden Fall! Aspose.PSD für Java ist eine leistungsstarke Bibliothek für professionelle Grafikdesignaufgaben.

### F2: Kann ich Aspose.PSD für Java in kommerziellen Anwendungen verwenden?

 A2: Ja, Aspose.PSD für Java ist ein kommerzielles Produkt. Sie können es kaufen[Hier](https://purchase.aspose.com/buy).

### F3: Gibt es eine kostenlose Testversion?

 A3: Ja, Sie können eine kostenlose Testversion ausprobieren[Hier](https://releases.aspose.com/).

### F4: Wo finde ich ausführliche Dokumentation?

 A4: Lesen Sie die ausführliche Dokumentation[Hier](https://reference.aspose.com/psd/java/).

### F5: Wie kann ich Support für Aspose.PSD für Java erhalten?

 A5: Treten Sie dem Community-Forum bei[Hier](https://forum.aspose.com/c/psd/34) für Supportanfragen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
