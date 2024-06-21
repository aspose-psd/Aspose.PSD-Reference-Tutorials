---
title: So fügen Sie ein Strichebenenmuster in Java hinzu
linktitle: So fügen Sie ein Strichebenenmuster in Java hinzu
second_title: Aspose.PSD Java-API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java ein Strichebenenmuster zu PSD-Dateien hinzufügen. Befolgen Sie diese Schritt-für-Schritt-Anleitung, um Ihre Bilder ganz einfach zu verbessern.
type: docs
weight: 11
url: /de/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Einführung
Das Hinzufügen eines Strichebenenmusters zu einem Bild in Java mag wie eine entmutigende Aufgabe klingen, aber mit Aspose.PSD für Java ist es einfacher, als Sie denken. Egal, ob Sie Grafiken entwerfen oder an Fotobearbeitungsanwendungen arbeiten, dieser Leitfaden führt Sie Schritt für Schritt durch den Prozess. Bereit anzufangen? Lass uns eintauchen!
## Voraussetzungen
Bevor Sie beginnen, benötigen Sie ein paar Dinge:
- Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem System installiert ist.
-  Aspose.PSD für Java: Laden Sie die Bibliothek herunter von[Hier](https://releases.aspose.com/psd/java/) und integrieren Sie es in Ihr Projekt.
- Eine IDE: Verwenden Sie Ihre bevorzugte integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA oder Eclipse.
## Pakete importieren
Als Erstes müssen Sie die erforderlichen Pakete in Ihr Java-Projekt importieren. Diese Pakete sind für die Arbeit mit Aspose.PSD unerlässlich.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Schritt 1: Laden Sie die PSD-Datei
Der erste Schritt beim Hinzufügen eines Strichebenenmusters besteht darin, die PSD-Datei zu laden, die Sie bearbeiten möchten.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Durch das Laden der PSD-Datei können Sie nun auf deren Ebenen und Effekte zugreifen und diese bearbeiten.
## Schritt 2: Bereiten Sie neue Musterdaten vor
Als Nächstes müssen Sie die neuen Musterdaten vorbereiten, die Sie auf die Strichebene anwenden.
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
Diese Musterdaten werden verwendet, um den neuen Stricheffekt zu erstellen.
## Schritt 3: Greifen Sie auf den Stricheffekt zu
Um den Stricheffekt zu ändern, müssen Sie auf die jeweilige Ebene und ihre Fülloptionen zugreifen.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Dadurch wird sichergestellt, dass Sie mit der richtigen Ebene und dem richtigen Effekt arbeiten.
## Schritt 4: Ändern Sie den Stricheffekt
Jetzt ändern wir den Stricheffekt mit den neuen Musterdaten.
### Aktualisieren Sie die Eigenschaften des Stricheffekts
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Aktualisieren Sie die Musterressource
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
Dieses Code-Snippet aktualisiert die Musterressource mit den neuen Musterdaten.
## Schritt 5: Wenden Sie das neue Muster an
Wenden Sie abschließend das neue Muster auf den Stricheffekt an und speichern Sie die Änderungen.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Dadurch wird sichergestellt, dass das neue Muster korrekt angewendet wird und die Datei mit den Änderungen gespeichert wird.
## Schritt 6: Überprüfen Sie die Änderungen
Um sicherzustellen, dass alles korrekt funktioniert, laden Sie die Datei erneut und überprüfen Sie die Änderungen.
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
In diesem Schritt wird überprüft, ob die Musterdaten korrekt auf den Stricheffekt angewendet wurden.
## Abschluss
Und da haben Sie es! Sie haben mit Aspose.PSD für Java erfolgreich ein Strichebenenmuster zu einer PSD-Datei hinzugefügt. Wenn Sie diese Schritte befolgen, können Sie Ihre Bilder ganz einfach anpassen und verbessern. Viel Spaß beim Codieren!
## FAQs
### Was ist Aspose.PSD für Java?
Aspose.PSD für Java ist eine Bibliothek, die es Entwicklern ermöglicht, PSD-Dateien (Photoshop Document) programmgesteuert zu erstellen, zu bearbeiten und zu konvertieren.
### Kann ich Aspose.PSD für Java in einem kommerziellen Projekt verwenden?
 Ja, Sie können es in kommerziellen Projekten verwenden. Sie können eine Lizenz erwerben bei[Hier](https://purchase.aspose.com/buy).
### Gibt es eine kostenlose Testversion für Aspose.PSD für Java?
 Ja, Sie können eine kostenlose Testversion herunterladen von[Hier](https://releases.aspose.com/).
### Wie erhalte ich Unterstützung für Aspose.PSD für Java?
 Unterstützung erhalten Sie in den Aspose-Community-Foren[Hier](https://forum.aspose.com/c/psd/34).
### Was sind die Systemanforderungen für Aspose.PSD für Java?
Sie benötigen ein installiertes JDK und eine IDE für die Entwicklung. Die Bibliothek unterstützt mehrere Betriebssysteme, darunter Windows, Linux und macOS.