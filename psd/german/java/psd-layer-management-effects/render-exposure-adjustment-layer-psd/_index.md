---
date: 2026-04-05
description: Erfahren Sie, wie Sie den Belichtungsanpassungseffekt in PSD-Dateien
  mit Aspose.PSD für Java rendern. Schritt-für-Schritt-Anleitung mit Codebeispielen
  zum Ändern und Hinzufügen von Belichtungsebenen.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: Render‑Belichtungsanpassungsebene in PSD‑Dateien – Java
second_title: Aspose.PSD Java API
title: Render‑Exposure‑Anpassungsebene in PSD‑Dateien – Java
url: /de/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Render-Expositionsanpassungsebene in PSD-Dateien – Java

## Einführung

Arbeiten Sie mit Photoshop‑PSD‑Dateien und müssen **Expositionsanpassungsebene rendern** programmatisch? Egal, ob Sie vorhandene Ebenen anpassen oder neue hinzufügen, Aspose.PSD für Java bietet eine leistungsstarke und intuitive Möglichkeit, diese Aufgaben zu erledigen. In diesem Leitfaden zeigen wir, wie Sie Aspose.PSD für Java verwenden, um Expositionsanpassungsebenen in PSD‑Dateien zu rendern und zu bearbeiten. Am Ende dieses Tutorials wissen Sie, wie Sie Belichtungseinstellungen in bestehenden Ebenen anpassen und neue Expositionsanpassungsebenen zu Ihren PSD‑Dateien hinzufügen können. Lassen Sie uns loslegen!

## Schnelle Antworten
- **Welche Bibliothek wird benötigt?** Aspose.PSD for Java
- **Kann ich eine vorhandene Expositions‑Ebene bearbeiten?** Ja, Sie können Belichtung, Offset und Gamma‑Korrektur ändern.
- **Wie füge ich eine neue Expositionsanpassungsebene hinzu?** Verwenden Sie `addExposureAdjustmentLayer()` auf einer `PsdImage`‑Instanz.
- **Wird der PNG‑Export unterstützt?** Absolut – verwenden Sie `PngOptions`, um das Ergebnis als PNG zu speichern.
- **Benötige ich eine Lizenz für die Produktion?** Für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich; eine kostenlose Testversion ist verfügbar.

## Was ist eine gerenderte Expositionsanpassungsebene?

Eine Expositionsanpassungsebene ist eine nicht‑destruktive Photoshop‑Ebene, die Helligkeit, Offset und Gamma des zugrunde liegenden Bildes ändert. Das Rendern bedeutet, diese Einstellungen anzuwenden, sodass das visuelle Ergebnis die Anpassungen widerspiegelt, das Sie anschließend in Formate wie PNG exportieren können.

## Warum Aspose.PSD für Java zum Rendern einer Expositionsanpassungsebene verwenden?

- **Vollständige Kontrolle** – Ebeneneigenschaften manipulieren, ohne Photoshop zu öffnen.
- **Stapelverarbeitung** – Anpassungen über viele Dateien hinweg automatisieren.
- **Plattformübergreifend** – auf jedem System mit einem JDK ausführen.
- **Erhält PSD‑Struktur** – Ebenen editierbar halten für zukünftige Änderungen.

## Voraussetzungen

1. **Java Development Kit (JDK)** – mindestens JDK 8.
2. **Aspose.PSD for Java** – laden Sie es von [hier](https://releases.aspose.com/psd/java/) herunter.
3. **Grundlegende Java‑Kenntnisse** – Sie sollten mit der Standard‑Java‑Syntax vertraut sein.
4. **IDE oder Texteditor** – IntelliJ IDEA, Eclipse, VS Code oder ein beliebiger Editor Ihrer Wahl.

## Pakete importieren

Zuerst importieren Sie die erforderlichen Aspose.PSD‑Klassen:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## So rendern Sie eine Expositionsanpassungsebene – Schritt‑für‑Schritt‑Anleitung

### Schritt 1: PSD-Datei laden

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

Ersetzen Sie `"Your Document Directory"` durch den Ordner, der Ihre PSD‑Dateien enthält. Die Methode `Image.load()` gibt ein `PsdImage`‑Objekt zurück, das Ihnen vollen Zugriff auf die Ebenen des Dokuments gewährt.

### Schritt 2: Vorhandene Expositionsanpassungsebene bearbeiten

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

Die Schleife durchläuft jede Ebene, findet jede `ExposureLayer` und aktualisiert deren drei Schlüsselparameter. Dies ist der Kern des **Renderns der Expositionsanpassungsebene** mit Ihren benutzerdefinierten Werten.

### Schritt 3: Modifizierte PSD-Datei speichern

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

Die modifizierte PSD behält alle ursprünglichen Ebenen unverändert bei, aber die Expositionsanpassung spiegelt nun die neuen Einstellungen wider.

### Schritt 4: Ergebnis als PNG exportieren

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

Die Verwendung von `PngOptions` mit `TruecolorWithAlpha` stellt sicher, dass das exportierte PNG die volle Farbtiefe und etwaige Transparenz aus der PSD beibehält.

### Schritt 5: Neue Expositionsanpassungsebene hinzufügen

Wenn Sie einer bestehenden Datei **eine neue Expositionsanpassungsebene hinzufügen** müssen, verwenden Sie den folgenden Code:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

## Häufige Probleme & Tipps

- **Ebene nicht gefunden** – Stellen Sie sicher, dass die PSD tatsächlich eine `ExposureLayer` enthält. Verwenden Sie `instanceof ExposureLayer` wie gezeigt, um `ClassCastException` zu vermeiden.
- **Dateipfad‑Fehler** – Verwenden Sie absolute Pfade oder prüfen Sie, dass `dataDir` mit einem Dateiseparator endet (`/` oder `\`).
- **Lizenz‑Ausnahme** – Das Ausführen ohne gültige Lizenz fügt dem Ergebnis ein Wasserzeichen hinzu. Registrieren Sie Ihre Lizenz früh im Code (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## FAQ

### Was ist Aspose.PSD für Java?

Aspose.PSD für Java ist eine Bibliothek, die es Ihnen ermöglicht, PSD‑Dateien programmgesteuert mit Java zu erstellen, zu bearbeiten und zu konvertieren. Sie bietet umfassende Funktionalität für die Arbeit mit Photoshop‑Dokumenten.

### Kann ich Aspose.PSD für Java verwenden, um andere Ebenentypen zu manipulieren?

Ja, Aspose.PSD für Java unterstützt verschiedene Ebenentypen, einschließlich Textebenen, Anpassungsebenen und Bildebenen, und ermöglicht umfangreiche Manipulationen von PSD‑Dateien.

### Wie beginne ich mit Aspose.PSD für Java?

Sie können beginnen, indem Sie die Bibliothek von der [Website](https://releases.aspose.com/psd/java/) herunterladen und die [Dokumentation](https://reference.aspose.com/psd/java/) für detaillierte Anleitungen und Beispiele konsultieren.

### Gibt es eine kostenlose Testversion von Aspose.PSD für Java?

Ja, eine kostenlose Testversion ist verfügbar. Sie können sie [hier](https://releases.aspose.com/) herunterladen.

### Wie erhalte ich Support für Aspose.PSD für Java?

Für Support können Sie das [Aspose‑Support‑Forum](https://forum.aspose.com/c/psd/34) besuchen, wo Sie Fragen stellen und Hilfe von der Community erhalten können.

**Zusätzliche Fragen**

**F: Kann ich mehrere PSD‑Dateien stapelweise verarbeiten?**  
A: Absolut. Packen Sie die Lade-, Bearbeitungs‑ und Speicherlogik in eine Schleife, die über eine Liste von Dateipfaden iteriert.

**F: Bewahrt die Bibliothek die Ebenenhierarchie, wenn ich eine neue Expositions‑Ebene hinzufüge?**  
A: Ja. Die neue Ebene wird über den bestehenden Ebenen eingefügt und behält die ursprüngliche Hierarchie bei.

**F: In welche Bildformate kann ich neben PNG exportieren?**  
A: Aspose.PSD unterstützt JPEG, BMP, TIFF und mehrere weitere Formate über die entsprechenden `*Options`‑Klassen.

**Zuletzt aktualisiert:** 2026-04-05  
**Getestet mit:** Aspose.PSD für Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}