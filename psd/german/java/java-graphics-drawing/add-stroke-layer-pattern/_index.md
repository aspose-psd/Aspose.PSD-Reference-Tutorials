---
date: 2026-01-17
description: Erfahren Sie, wie Sie ein Strichmuster in Java mit Aspose.PSD für Java
  hinzufügen. Folgen Sie dieser Schritt‑für‑Schritt‑Anleitung, um Ihre PSD‑Bilder
  schnell zu verbessern.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Wie man ein Strichmuster in Java mit Aspose.PSD hinzufügt
url: /de/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Stroke Pattern Java mit Aspose.PSD hinzufügt

## Einführung
Wenn Sie **add stroke pattern java** zu einer Photoshop‑Datei hinzufügen müssen, macht Aspose.PSD für Java das überraschend einfach. Egal, ob Sie ein Grafik‑Design‑Tool entwickeln, Stapel‑Bearbeitungen automatisieren oder einfach nur mit Ebeneneffekten experimentieren – dieses Tutorial führt Sie Schritt für Schritt durch den gesamten Prozess – vom Laden der PSD bis zur Überprüfung des neuen Musters. Lassen Sie uns eintauchen und sehen, wie schnell Sie Ihre Bilder verbessern können.

## Schnellantworten
- **Welche Bibliothek benötige ich?** Aspose.PSD für Java  
- **Welche Java‑Version wird unterstützt?** JDK 8 oder neuer  
- **Benötige ich eine Lizenz für Tests?** Eine kostenlose Testversion reicht für die Entwicklung; für die Produktion ist eine Lizenz erforderlich  
- **Wie lange dauert die Implementierung?** Ungefähr 10‑15 Minuten für einen einfachen Muster‑Strich  
- **Kann ich das Muster auf mehreren Ebenen wiederverwenden?** Ja, weisen Sie einfach dieselbe `PattResource` anderen Ebenen zu  

## Was ist add stroke pattern java?
Ein Stroke‑Muster in Java hinzuzufügen bedeutet, einer Ebenen‑Strich‑Effekt‑Füllung ein benutzerdefiniertes Muster (oft ein wiederholendes Bitmap) zuzuweisen. Diese Technik ermöglicht stilisierte Konturen – denken Sie an eine gestrichelte Linie, eine Ziegel‑Textur oder einen benutzerdefinierten Grafikrahmen – direkt innerhalb einer PSD‑Datei, ohne Photoshop zu öffnen.

## Warum Aspose.PSD für add stroke pattern java verwenden?
- **Vollständige PSD‑Treue** – Alle Ebeneneffekte, Ressourcen und Mischmodi bleiben erhalten.  
- **Kein natives Photoshop nötig** – Läuft auf jedem Betriebssystem mit JDK.  
- **Programmgesteuerte Kontrolle** – Automatisieren Sie Stapelverarbeitungen oder integrieren Sie sie in serverseitige Dienste.  
- **Umfangreiche API** – Zugriff auf globale Ressourcen, Muster‑Füllungen und Mischmodi in einer einzigen flüssigen Schnittstelle.

## Voraussetzungen
- **Java Development Kit (JDK)** – Stellen Sie sicher, dass JDK 8 oder neuer installiert ist.  
- **Aspose.PSD für Java** – Laden Sie die Bibliothek von [hier](https://releases.aspose.com/psd/java/) herunter und fügen Sie das JAR Ihrem Projekt‑Classpath hinzu.  
- **IDE** – IntelliJ IDEA, Eclipse oder ein beliebiger Editor Ihrer Wahl.

## Pakete importieren
Importieren Sie zunächst die Klassen, die Sie für die Verarbeitung von PSD‑Dateien, Farben, Rechtecken und Strich‑Effekten benötigen.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```

## Schritt 1: PSD‑Datei laden
Laden Sie die Quell‑PSD, damit Sie mit ihren Ebenen und Ressourcen arbeiten können.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Schritt 2: Neue Musterdaten vorbereiten
Erstellen Sie ein einfaches 4 × 4 Pixel‑Muster, das für den Strich verwendet wird.

```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```

## Schritt 3: Auf den Strich‑Effekt zugreifen
Suchen Sie den Strich‑Effekt auf der Ziel‑Ebene (in diesem Beispiel die vierte Ebene).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Schritt 4: Strich‑Effekt ändern
### Strich‑Effekt‑Eigenschaften aktualisieren
Passen Sie Deckkraft und Mischmodus an, um die visuelle Wirkung des neuen Musters zu sehen.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Muster‑Ressource aktualisieren
Ersetzen Sie die vorhandene globale Muster‑Ressource durch die gerade erstellte.

```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```

## Schritt 5: Neues Muster anwenden
Binden Sie die aktualisierte Muster‑Ressource an den Strich‑Effekt und speichern Sie die PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Schritt 6: Änderungen überprüfen
Laden Sie die Datei erneut und bestätigen Sie, dass das neue Muster, die Deckkraft und der Mischmodus korrekt angewendet wurden.

```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```

## Häufige Probleme und Lösungen
| Problem | Ursache | Lösung |
|-------|-------|-----|
| Muster wird nicht angezeigt | Falsche `PatternId`‑Referenz | Stellen Sie sicher, dass die `PatternId` auf `PattResource` mit der in `PatternFillSettings` verwendeten übereinstimmt. |
| Strich verschwindet nach dem Speichern | Deckkraft auf 0 gesetzt oder Effekt ausgeblendet | Überprüfen Sie, dass `setOpacity` zwischen 0‑255 liegt und `isVisible()` `true` zurückgibt. |
| Unerwartete Farben | Mischmodus stimmt nicht überein | Verwenden Sie `BlendMode.Color` (oder einen anderen Modus), der Ihrer Design‑Absicht entspricht. |

## FAQ's
### Was ist Aspose.PSD für Java?
Aspose.PSD für Java ist eine Bibliothek, die Entwicklern ermöglicht, PSD‑ (Photoshop Document) Dateien programmgesteuert zu erstellen, zu bearbeiten und zu konvertieren.

### Kann ich Aspose.PSD für Java in einem kommerziellen Projekt verwenden?
Ja, Sie können es in kommerziellen Projekten einsetzen. Sie können eine Lizenz [hier](https://purchase.aspose.com/buy) erwerben.

### Gibt es eine kostenlose Testversion von Aspose.PSD für Java?
Ja, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) herunterladen.

### Wie erhalte ich Support für Aspose.PSD für Java?
Sie erhalten Support über die Aspose‑Community‑Foren [hier](https://forum.aspose.com/c/psd/34).

### Was sind die Systemanforderungen für Aspose.PSD für Java?
Sie benötigen ein installiertes JDK und eine IDE für die Entwicklung. Die Bibliothek unterstützt mehrere Betriebssysteme, darunter Windows, Linux und macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-01-17  
**Getestet mit:** Aspose.PSD für Java 24.12 (zum Zeitpunkt des Schreibens die neueste Version)  
**Autor:** Aspose