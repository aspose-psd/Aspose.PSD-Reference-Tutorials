---
date: 2026-01-14
description: Erfahren Sie, wie Sie eine Verlauf‑Kontur‑Ebene erstellen und Konturverläufe
  in PSD‑Dateien mit Aspose.PSD für Java in diesem Schritt‑für‑Schritt‑Tutorial anpassen.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Wie man eine Verlaufs‑Strich‑Ebene in Java erstellt
url: /de/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man einen Gradient‑Stroke‑Layer in Java erstellt

## Einführung
Haben Sie sich jemals gefragt, wie Sie **create gradient stroke layer** in Ihren PSD-Dateien mit Java erstellen können? Sie sind hier genau richtig! Heute tauchen wir in Aspose.PSD für Java ein – eine leistungsstarke Bibliothek, die es Ihnen ermöglicht, PSD-Dateien mühelos zu manipulieren. Egal, ob Sie neu in der Grafikprogrammierung sind oder bestehende Designs feinabstimmen möchten, führt Sie diese Anleitung Schritt für Schritt durch das Hinzufügen und Anpassen von Stroke‑Gradients.

## Schnelle Antworten
- **Was ist das Hauptziel?** Erstellen Sie einen **gradient stroke layer** in einer PSD-Datei.  
- **Welche Bibliothek wird benötigt?** Aspose.PSD für Java.  
- **Benötige ich eine Lizenz?** Ja, für den produktiven Einsatz ist eine gültige (oder temporäre) Lizenz erforderlich.  
- **Welche Java-Version wird unterstützt?** Java 8 oder höher.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für einen einfachen **gradient stroke**.

## Was ist ein Gradient Stroke Layer?
Ein Gradient Stroke Layer ist eine Vektor‑Umrandung um eine Form oder einen Text, die sanft zwischen Farben übergeht. Mit Aspose.PSD können Sie programmgesteuert die Farben, Deckkraft, den Winkel und den Typ (linear, radial usw.) des Strokes festlegen.

## Warum Aspose.PSD für Java verwenden?
- **Vollständige PSD‑Unterstützung** – PSD-Dateien lesen, bearbeiten und schreiben ohne Photoshop.  
- **Umfangreiche Effekt‑API** – Zugriff auf Stroke, Schatten, Leuchten und viele andere Ebeneneffekte.  
- **Plattformübergreifend** – funktioniert auf jedem Betriebssystem, das Java unterstützt.  
- **Keine nativen Abhängigkeiten** – reines Java, einfach in CI‑Pipelines zu integrieren.

## Voraussetzungen
1. **Java Development Kit (JDK)** – Installieren Sie das neueste JDK von [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD für Java** – Laden Sie die Bibliothek von der [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse oder NetBeans.  
4. **Lizenz** – Holen Sie sich eine [temporary license](https://purchase.aspose.com/temporary-license/), falls Sie keine Vollversion besitzen.

## Pakete importieren
Zuerst importieren Sie die Klassen, die wir zum Laden der PSD, zum Zugriff auf Effekte und zur Konfiguration von Gradient‑Füllungen benötigen.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

Jetzt teilen wir den Prozess in klare Schritte auf.

## Schritt 1: PSD-Datei laden
Wir laden die Quell‑PSD und aktivieren die Effekt‑Ressourcen, sodass der Stroke‑Effekt verfügbar ist.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Schritt 2: Auf den Stroke‑Effekt zugreifen
Angenommen, der zu ändernde Stroke gehört zur dritten Ebene (Index 2), dann rufen wir dessen `StrokeEffect` ab.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Schritt 3: Stroke‑Effekteigenschaften überprüfen
Bevor Änderungen vorgenommen werden, prüfen wir die bestehenden Einstellungen, um genau zu wissen, was wir aktualisieren.

```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```

## Schritt 4: Gradient‑Füllungseinstellungen ändern
Hier ändern wir Farbe, Deckkraft, Mischmodus und weitere Eigenschaften, um das gewünschte Aussehen zu erzielen.

```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```

## Schritt 5: Farb‑ und Transparenzpunkte hinzufügen und ändern
Wir fügen neue Farb‑ und Transparenzpunkte hinzu und passen anschließend die bestehenden an, um den Gradient zu formen.

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## Schritt 6: Modifizierte PSD-Datei speichern
Nach allen Anpassungen schreiben wir die aktualisierte Datei zurück auf die Festplatte.

```java
im.save(exportPath);
```

## Schritt 7: Änderungen überprüfen
Laden Sie die gespeicherte Datei und prüfen Sie, dass jede Eigenschaft die vorgenommenen Änderungen widerspiegelt.

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## Fazit
Sie wissen jetzt, wie Sie **create gradient stroke layer**‑Effekte in PSD-Dateien mit Aspose.PSD für Java **erstellen**. Durch das Laden einer PSD, den Zugriff auf den Stroke‑Effekt, das Anpassen der Gradient‑Füllungseinstellungen und das Speichern des Ergebnisses können Sie programmgesteuert professionelle Grafiken erzeugen, ohne Photoshop zu öffnen.

## FAQ

### Was ist Aspose.PSD für Java?
Aspose.PSD für Java ist eine Bibliothek, die Entwicklern ermöglicht, in Java‑Anwendungen mit PSD‑Dateien zu arbeiten und Funktionen zum Erstellen, Manipulieren und Konvertieren von PSD‑Dateien bereitstellt.

### Benötige ich eine Lizenz für die Nutzung von Aspose.PSD für Java?
Ja, Sie benötigen eine gültige Lizenz, um Aspose.PSD für Java zu verwenden. Sie können eine [temporary license](https://purchase.aspose.com/temporary-license/) für Evaluierungszwecke erhalten.

### Kann ich mit Aspose.PSD für Java PSD‑Dateien von Grund auf neu erstellen?
Absolut! Aspose.PSD für Java bietet umfassende APIs, um PSD‑Dateien programmgesteuert zu erstellen und zu manipulieren.

### Ist es möglich, weitere Effekte mit Aspose.PSD für Java anzuwenden?
Ja, Sie können verschiedene Effekte wie Schatten, Leuchten und weitere mit Aspose.PSD für Java anwenden.

### Wo finde ich die Dokumentation für Aspose.PSD für Java?
Die Dokumentation finden Sie [hier](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-01-14  
**Getestet mit:** Aspose.PSD für Java 24.11  
**Autor:** Aspose