---
title: Fügen Sie die Farbe der Strichebene in Aspose.PSD für Java hinzu
linktitle: Fügen Sie die Farbe der Strichebene hinzu
second_title: Aspose.PSD Java-API
description: Entdecken Sie die Leistungsfähigkeit von Aspose.PSD für Java mit unserer Schritt-für-Schritt-Anleitung zum Hinzufügen von Strichebenenfarbe. Werten Sie Ihre Grafikdesigns mühelos auf.
type: docs
weight: 14
url: /de/java/advanced-image-effects/add-stroke-layer-color/
---
## Einführung

Nutzen Sie das Potenzial des Grafikdesigns Ihrer Java-Anwendung mit Aspose.PSD. In diesem Tutorial tauchen wir in die faszinierende Welt des Hinzufügens von Strichebenenfarbe mit Aspose.PSD für Java ein. Werten Sie Ihre Grafiken mit auffälligen Strichen auf und erstellen Sie mühelos optisch ansprechende Designs.

## Voraussetzungen

Bevor Sie sich auf diese kreative Reise begeben, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD-Bibliothek: Laden Sie die Aspose.PSD-Bibliothek herunter und richten Sie sie ein, indem Sie den Anweisungen folgen[Dokumentation](https://reference.aspose.com/psd/java/).

- Java Development Kit (JDK): Stellen Sie sicher, dass Java auf Ihrem System installiert ist.

- Integrierte Entwicklungsumgebung (IDE): Wählen Sie eine IDE Ihrer Wahl; Eclipse oder IntelliJ sind beliebte Optionen.

## Pakete importieren

Beginnen wir mit dem Importieren der notwendigen Pakete, um die Magie von Aspose.PSD zu verwirklichen.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Schritt 1: Richten Sie Ihr Projekt ein

Beginnen Sie mit der Erstellung eines neuen Java-Projekts in Ihrer bevorzugten IDE. Stellen Sie sicher, dass die Aspose.PSD-Bibliothek zu Ihrem Projekt hinzugefügt wird.

## Schritt 2: PSD-Datei laden

Laden Sie die PSD-Datei mit Aspose.PSD, um das Laden von Effektressourcen zu ermöglichen.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Schritt 3: Greifen Sie auf die Strichebene zu

Greifen Sie auf die Stricheffektebene in der PSD-Datei zu.

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Schritt 4: Stricheigenschaften validieren

Stellen Sie sicher, dass die Stricheigenschaften den Erwartungen entsprechen.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Schritt 5: Farbe und Deckkraft festlegen

Ändern Sie die Farbe und Deckkraft der Strichebene.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Schritt 6: Speichern Sie die geänderte PSD

Speichern Sie die geänderte PSD-Datei mit der neu hinzugefügten Strichebenenfarbe.

```java
im.save(exportPath);
```

## Abschluss

Glückwunsch! Sie haben mit Aspose.PSD für Java erfolgreich die Farbe der Strichebene zu Ihrer PSD-Datei hinzugefügt. Experimentieren Sie mit verschiedenen Farben und Einstellungen, um Ihren Grafikdesigns Leben einzuhauchen.

## FAQs

### F1: Kann ich Aspose.PSD mit anderen Java-Grafikbibliotheken verwenden?

A1: Ja, Aspose.PSD kann für erweiterte Funktionalität in andere Java-Grafikbibliotheken integriert werden.

### F2: Ist Aspose.PSD mit dem neuesten PSD-Dateiformat kompatibel?

A2: Auf jeden Fall! Aspose.PSD hält mit den neuesten PSD-Dateiformatspezifikationen Schritt und gewährleistet so die Kompatibilität.

### F3: Wie gehe ich mit Ausnahmen um, während ich Aspose.PSD verwende?

 A3: Siehe[Hilfeforum](https://forum.aspose.com/c/psd/34) für Unterstützung bei der Behandlung von Ausnahmen und der Fehlerbehebung.

### F4: Kann ich Aspose.PSD vor dem Kauf testen?

 A4: Auf jeden Fall! Schnapp dir ein[Kostenlose Testphase](https://releases.aspose.com/) um die Funktionen von Aspose.PSD zu erkunden, bevor Sie eine Verpflichtung eingehen.

### F5: Wo kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

 A5: Erhalten Sie a[temporäre Lizenz](https://purchase.aspose.com/temporary-license/) damit Aspose.PSD seine Fähigkeiten in Ihren Projekten bewerten kann.