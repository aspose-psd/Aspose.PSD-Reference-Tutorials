---
title: Belichtungsanpassungsebene in PSD-Dateien rendern – Java
linktitle: Belichtungsanpassungsebene in PSD-Dateien rendern – Java
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie Belichtungsebenen in PSD-Dateien mit Aspose.PSD für Java rendern und anpassen. Schritt-für-Schritt-Anleitung mit Codebeispielen zum Ändern und Hinzufügen von Belichtungsebenen.
weight: 15
url: /de/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Belichtungsanpassungsebene in PSD-Dateien rendern – Java

## Einführung

Arbeiten Sie mit Photoshop-PSD-Dateien und müssen die Belichtung anpassen oder programmgesteuert eine Ebene zur Belichtungsanpassung hinzufügen? Egal, ob Sie vorhandene Ebenen optimieren oder neue hinzufügen, Aspose.PSD für Java bietet eine leistungsstarke und intuitive Möglichkeit, diese Aufgaben zu erledigen. In dieser Anleitung erfahren Sie, wie Sie Aspose.PSD für Java verwenden, um Ebenen zur Belichtungsanpassung in PSD-Dateien zu rendern und zu ändern. Am Ende dieses Tutorials wissen Sie, wie Sie Belichtungseinstellungen in vorhandenen Ebenen anpassen und Ihren PSD-Dateien neue Ebenen zur Belichtungsanpassung hinzufügen. Lassen Sie uns eintauchen!

## Voraussetzungen

Bevor wir mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. Java Development Kit (JDK): Sie müssen JDK auf Ihrem Computer installiert haben. Diese Anleitung setzt voraus, dass Sie mindestens JDK 8 haben.
2.  Aspose.PSD für Java: Sie benötigen die Aspose.PSD-Bibliothek, um mit PSD-Dateien arbeiten zu können. Sie können sie hier herunterladen:[Hier](https://releases.aspose.com/psd/java/).
3. Grundkenntnisse in Java: Wenn Sie mit der Java-Programmierung vertraut sind, können Sie den Anweisungen problemlos folgen.
4. IDE oder Texteditor: Verwenden Sie eine beliebige IDE wie IntelliJ IDEA, Eclipse oder einen Texteditor Ihrer Wahl, um Java-Code zu schreiben und auszuführen.

## Pakete importieren

Zunächst importieren wir die erforderlichen Pakete aus Aspose.PSD für Java. Dieser Schritt stellt sicher, dass unser Code die Funktionen der Bibliothek zum Bearbeiten von PSD-Dateien nutzen kann.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Schritt 1: Laden Sie die PSD-Datei

Zunächst müssen Sie Ihre PSD-Datei in die Anwendung laden. So geht's:

```java
String dataDir = "Your Document Directory";  // Definieren Sie Ihr Dokumentverzeichnis
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Quell-PSD-Dateipfad

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Laden Sie die PSD-Datei
```

 Ersetzen Sie in diesem Codeausschnitt`"Your Document Directory"` mit dem Pfad, in dem sich Ihre PSD-Dateien befinden.`Image.load()` Methode lädt die PSD-Datei in eine Instanz von`PsdImage`, wodurch Sie die Ebenen bearbeiten können.

## Schritt 2: Vorhandene Belichtungsanpassungsebene bearbeiten

Sobald die PSD-Datei geladen ist, können Sie auf vorhandene Ebenen zugreifen und diese ändern. Wenn die Datei eine Ebene zur Belichtungsanpassung enthält, können Sie deren Eigenschaften anpassen:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Passen Sie die Belichtungsstufe an
        expLayer.setOffset(-0.25f);  // Einstellen des Offsets
        expLayer.setGammaCorrection(0.5f);  // Passen Sie die Gammakorrektur an
    }
}
```

In dieser Schleife iterieren wir über alle Ebenen der PSD-Datei. Wenn wir eine`ExposureLayer` modifizieren wir seine`Exposure`, `Offset` , Und`GammaCorrection` Eigenschaften. Dadurch können Sie die visuelle Ausgabe der Belichtungsanpassungsebene feinabstimmen.

## Schritt 3: Speichern Sie die geänderte PSD-Datei

Nachdem Sie Änderungen vorgenommen haben, müssen Sie die aktualisierte PSD-Datei speichern:

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Pfad zum Speichern der geänderten PSD-Datei

im.save(psdPathAfterChange);  // Speichern Sie die Änderungen an der PSD-Datei
```

Diese Zeile speichert die geänderte PSD-Datei im angegebenen Pfad und behält Ihre Belichtungsanpassungen bei.

## Schritt 4: Als PNG exportieren

Um die aktualisierte PSD-Datei als PNG zu exportieren, führen Sie diese Schritte aus:

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Pfad zum Speichern der PNG-Datei

PngOptions saveOptions = new PngOptions();  // PNG-Optionen erstellen
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Stellen Sie den Farbtyp auf Truecolor mit Alpha ein.

im.save(pngExportPath, saveOptions);  // Als PNG speichern
```

 Hier,`PngOptions` wird verwendet, um die PNG-Exporteinstellungen zu konfigurieren.`PngColorType.TruecolorWithAlpha` stellt sicher, dass die PNG-Datei Farbtiefe und Transparenz behält.

## Schritt 5: Fügen Sie eine neue Ebene zur Belichtungsanpassung hinzu

Wenn Sie einer vorhandenen PSD-Datei eine neue Ebene zur Belichtungsanpassung hinzufügen möchten, können Sie dies mit dem folgenden Code tun:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Quell-PSD-Dateipfad

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Laden Sie die PSD-Datei

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Neue Belichtungsanpassungsebene hinzufügen

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Pfad zum Speichern der geänderten PSD-Datei
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Pfad zum Speichern der PNG-Datei

img.save(psdPathAfterChange);  // Speichern Sie die Änderungen an der PSD-Datei

PngOptions options = new PngOptions();  // PNG-Optionen erstellen
options.setColorType(PngColorType.TruecolorWithAlpha);  // Stellen Sie den Farbtyp auf Truecolor mit Alpha ein.

img.save(pngExportPath, options);  // Als PNG speichern
```

In diesem Schritt wird der PSD-Datei eine neue Belichtungsanpassungsebene mit angegebenen Belichtungs-, Offset- und Gammakorrekturwerten hinzugefügt. Anschließend werden die aktualisierten PSD- und PNG-Dateien gespeichert.

## Abschluss

Und da haben Sie es! Sie haben gelernt, wie Sie Belichtungsebenen in PSD-Dateien mit Aspose.PSD für Java rendern und anpassen. Wir haben erläutert, wie Sie vorhandene Belichtungsebenen ändern, neue hinzufügen und Ihre Arbeit als PNG-Dateien exportieren. Egal, ob Sie Fotos optimieren oder Design-Assets vorbereiten, diese Fähigkeiten verbessern Ihre Fähigkeit, PSD-Dateien programmgesteuert zu verwalten. Viel Spaß beim Programmieren!

## Häufig gestellte Fragen

### Was ist Aspose.PSD für Java?

Aspose.PSD für Java ist eine Bibliothek, mit der Sie PSD-Dateien programmgesteuert mit Java erstellen, bearbeiten und konvertieren können. Es bietet umfassende Funktionen für die Arbeit mit Photoshop-Dokumenten.

### Kann ich Aspose.PSD für Java verwenden, um andere Ebenentypen zu bearbeiten?

Ja, Aspose.PSD für Java unterstützt verschiedene Arten von Ebenen, darunter Textebenen, Anpassungsebenen und Bildebenen, und ermöglicht so eine umfassende Bearbeitung von PSD-Dateien.

### Wie beginne ich mit Aspose.PSD für Java?

 Sie können mit dem Herunterladen der Bibliothek von der[Webseite](https://releases.aspose.com/psd/java/) und unter Bezugnahme auf die[Dokumentation](https://reference.aspose.com/psd/java/) für detaillierte Anleitungen und Beispiele.

### Gibt es eine kostenlose Testversion für Aspose.PSD für Java?

 Ja, eine kostenlose Testversion ist verfügbar. Sie können sie herunterladen[Hier](https://releases.aspose.com/).

### Wie erhalte ich Support für Aspose.PSD für Java?

 Für Unterstützung besuchen Sie bitte die[Aspose-Supportforum](https://forum.aspose.com/c/psd/34) wo Sie Fragen stellen und Hilfe von der Community erhalten können.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
