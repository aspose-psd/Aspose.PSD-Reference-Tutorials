---
title: So fügen Sie in Java einen Strichebenenverlauf hinzu
linktitle: So fügen Sie in Java einen Strichebenenverlauf hinzu
second_title: Aspose.PSD Java API
description: Erfahren Sie in diesem umfassenden Schritt-für-Schritt-Tutorial, wie Sie mit Aspose.PSD für Java Strichebenenverläufe in PSD-Dateien hinzufügen und anpassen.
type: docs
weight: 10
url: /de/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## Einführung
Haben Sie sich schon einmal gefragt, wie Sie mit Java einen Strichebenenverlauf zu Ihren Bildern hinzufügen können? Dann sind Sie hier richtig! Heute tauchen wir in die Welt von Aspose.PSD für Java ein, einer leistungsstarken Bibliothek, mit der Sie PSD-Dateien mühelos bearbeiten können. Egal, ob Sie Anfänger oder erfahrener Entwickler sind, diese Schritt-für-Schritt-Anleitung führt Sie durch den Prozess des Hinzufügens eines Strichebenenverlaufs zu Ihren PSD-Dateien. Also schnallen Sie sich an und machen Sie sich bereit, Ihre Fähigkeiten zur Grafikbearbeitung zu verbessern!
## Voraussetzungen
Bevor wir beginnen, müssen Sie einige Dinge vorbereitet haben. Stellen Sie sicher, dass Sie über Folgendes verfügen:
1.  Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem System installiert ist. Sie können es hier herunterladen:[Website von Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD für Java-Bibliothek: Sie können es herunterladen von der[Aspose.PSD-Downloadseite](https://releases.aspose.com/psd/java/).
3. Eine integrierte Entwicklungsumgebung (IDE): Jede IDE wie IntelliJ IDEA, Eclipse oder NetBeans funktioniert.
4.  Eine gültige Lizenz: Sie erhalten eine[vorläufige Lizenz](https://purchase.aspose.com/temporary-license/) wenn Sie kein volles haben.
## Pakete importieren
Zunächst importieren wir die erforderlichen Pakete. Diese ermöglichen uns die Verwendung der Klassen und Methoden, die zur Bearbeitung der PSD-Datei erforderlich sind.
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
Lassen Sie uns das Beispiel zum besseren Verständnis nun in mehrere Schritte aufteilen.
## Schritt 1: Laden Sie die PSD-Datei
 Zuerst müssen wir die PSD-Datei laden, die wir ändern möchten. Wir verwenden die`PsdLoadOptions` um anzugeben, dass wir die Effektressourcen laden möchten.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Schritt 2: Zugriff auf den Stricheffekt
Als nächstes müssen wir auf den Stricheffekt der Ebene zugreifen, die uns interessiert. Hier nehmen wir an, dass es sich um die dritte Ebene (Index 2) in der PSD-Datei handelt.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Schritt 3: Überprüfen Sie die Eigenschaften des Stricheffekts
Bevor wir Änderungen vornehmen, überprüfen wir die Eigenschaften des Stricheffekts, um sicherzustellen, dass wir die richtigen Einstellungen ändern.
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
## Schritt 4: Ändern Sie die Einstellungen für die Verlaufsfüllung
Jetzt ist es an der Zeit, die Einstellungen für die Verlaufsfüllung entsprechend unseren Anforderungen zu ändern. Wir ändern Farbe, Deckkraft, Mischmodus und andere Eigenschaften.
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
## Schritt 5: Farb- und Transparenzpunkte hinzufügen und ändern
Fügen wir neue Farb- und Transparenzpunkte hinzu und ändern die vorhandenen, um den gewünschten Verlaufseffekt zu erzielen.
```java
// Neuen Farbpunkt hinzufügen
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Position des vorherigen Punktes ändern
fillSettings.getColorPoints()[1].setLocation(1899);
// Neuen Transparenzpunkt hinzufügen
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Position des vorherigen Transparenzpunkts ändern
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Schritt 6: Speichern Sie die geänderte PSD-Datei
Nachdem wir alle notwendigen Änderungen vorgenommen haben, müssen wir die PSD-Datei speichern.
```java
im.save(exportPath);
```
## Schritt 7: Überprüfen der Änderungen
Laden wir abschließend die gespeicherte PSD-Datei und überprüfen, ob unsere Änderungen korrekt angewendet wurden.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Farbpunkte prüfen
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
// Transparenzpunkte prüfen
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
## Abschluss
Und da haben Sie es! Sie wissen jetzt, wie Sie mit Aspose.PSD für Java Strichebenenverläufe in PSD-Dateien hinzufügen und bearbeiten. In diesem Tutorial wurde das Laden der PSD-Datei, der Zugriff auf und die Änderung von Stricheffekten sowie das Speichern der Änderungen behandelt. Mit diesen Fähigkeiten können Sie optisch ansprechende Verläufe erstellen und Ihre PSD-Dateien an Ihre Bedürfnisse anpassen.
## Häufig gestellte Fragen
### Was ist Aspose.PSD für Java?
Aspose.PSD für Java ist eine Bibliothek, die Entwicklern die Arbeit mit PSD-Dateien in Java-Anwendungen ermöglicht und Funktionen zum Erstellen, Bearbeiten und Konvertieren von PSD-Dateien bietet.
### Benötige ich eine Lizenz, um Aspose.PSD für Java zu verwenden?
 Ja, Sie benötigen eine gültige Lizenz, um Aspose.PSD für Java zu verwenden. Sie erhalten eine[vorläufige Lizenz](https://purchase.aspose.com/temporary-license/) zu Auswertungszwecken.
### Kann ich Aspose.PSD für Java verwenden, um PSD-Dateien von Grund auf neu zu erstellen?
Auf jeden Fall! Aspose.PSD für Java bietet umfassende APIs zum programmgesteuerten Erstellen und Bearbeiten von PSD-Dateien.
### Ist es möglich, mit Aspose.PSD für Java andere Effekte anzuwenden?
Ja, Sie können mit Aspose.PSD für Java verschiedene Effekte wie Schatten, Glanz und mehr anwenden.
### Wo finde ich die Dokumentation für Aspose.PSD für Java?
 Die Dokumentation finden Sie[Hier](https://reference.aspose.com/psd/java/).