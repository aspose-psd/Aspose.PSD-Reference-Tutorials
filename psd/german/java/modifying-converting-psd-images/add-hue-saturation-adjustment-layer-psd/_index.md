---
title: Fügen Sie der PSD eine Ebene zur Anpassung der Farbtonsättigung hinzu
linktitle: Fügen Sie der PSD eine Ebene zur Anpassung der Farbtonsättigung hinzu
second_title: Aspose.PSD Java API
description: In diesem umfassenden Schritt-für-Schritt-Tutorial erfahren Sie, wie Sie mit Aspose.PSD für Java Anpassungsebenen für Farbton und Sättigung zu PSD hinzufügen. Verbessern Sie Ihren Grafikdesign-Workflow.
weight: 14
url: /de/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Fügen Sie der PSD eine Ebene zur Anpassung der Farbtonsättigung hinzu

## Einführung
Beim Grafikdesign spielt die Farbmanipulation eine entscheidende Rolle – insbesondere das Optimieren von Farbton, Sättigung und Helligkeit kann die Stimmung und Qualität jedes Bildes drastisch verändern. Eine effektive Möglichkeit, dies zu erreichen, ist die Verwendung von Anpassungsebenen in Photoshop (PSD-Dateien). Wenn Sie Ihre PSD-Dateien programmgesteuert mit Java verbessern möchten, hilft Ihnen die Aspose.PSD-Bibliothek! Dieses Tutorial führt Sie durch die Schritte zum Hinzufügen einer Anpassungsebene für Farbton und Sättigung zu Ihren PSD-Dateien, wodurch Ihre Arbeitsabläufe produktiver und effizienter werden.
In diesem Handbuch behandeln wir alles, vom Importieren der erforderlichen Pakete bis hin zu den kleinsten Einzelheiten der Codebeispiele.
## Voraussetzungen
Bevor wir in den Code einsteigen, stellen Sie sicher, dass Sie Folgendes eingerichtet haben:
1.  Java Development Kit (JDK): Stellen Sie sicher, dass auf Ihrem Computer JDK 8 oder höher installiert ist. Sie können es von der[Downloads zum Java SE Development Kit](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD für Java-Bibliothek: Sie benötigen die Aspose.PSD-Bibliothek, die Sie[hier herunterladen](https://releases.aspose.com/psd/java/). 
3. IDE: Eine geeignete integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA oder Eclipse für die Java-Entwicklung.
4. Grundlegende Java-Kenntnisse: Kenntnisse in der Java-Programmierung sind von Vorteil, aber keine Sorge, wir führen Sie Schritt für Schritt durch den Code.
Nachdem wir nun unsere Voraussetzungen geklärt haben, kommen wir zum spaßigen Teil – dem Programmieren!
## Pakete importieren
Um mit der Aspose.PSD-Bibliothek arbeiten zu können, müssen Sie zunächst die erforderlichen Klassen importieren. So können Sie dies in Ihrer Java-Datei tun:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Stellen Sie sicher, dass Sie Ihrem Projekt die entsprechenden Bibliotheken hinzugefügt haben, damit diese Importe reibungslos funktionieren.
## Schritt 1: Richten Sie Ihr Dokumentverzeichnis ein
Jedes Projekt braucht einen Ausgangspunkt, und unser Projekt ist da keine Ausnahme. Sie müssen ein Verzeichnis angeben, in dem Ihre PSD-Dateien gespeichert sind. Dies ist entscheidend, um Bilder ordnungsgemäß laden und speichern zu können.
```java
String dataDir = "Your Document Directory"; // Aktualisieren Sie diesen Pfad zu Ihrem tatsächlichen Verzeichnis
```
## Schritt 2: Laden Sie eine vorhandene PSD-Datei
Um eine vorhandene PSD-Datei zu bearbeiten, müssen wir sie zunächst in unser Programm laden. So können Sie das tun:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Aktualisieren Sie in diesem Code`"HueSaturationAdjustmentLayer.psd"` auf den Namen Ihrer vorhandenen PSD-Datei, die Sie bearbeiten möchten.
## Schritt 3: Bearbeiten Sie die Farbton-/Sättigungsebene
Als Nächstes durchlaufen wir die Ebenen unseres geladenen PSD-Bildes, um vorhandene Farbton-/Sättigungsebenen zu finden und zu bearbeiten. In diesem Schritt ändern wir die Werte für Farbton, Sättigung und Helligkeit.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
In diesem Beispiel:
- Wir stellen den Farbton auf -25, die Sättigung auf -12 und die Helligkeit auf +67 ein.
-  Der`getRange(2)` Methode ermöglicht es uns, bestimmte Farbbereiche nach Wunsch anzupassen.
## Schritt 4: Speichern Sie die geänderte PSD-Datei
Nachdem Sie die Anpassungen vorgenommen haben, besteht der nächste Schritt darin, die Datei zu speichern. Dies ist ein wichtiger Teil unseres Prozesses, um sicherzustellen, dass die vorgenommenen Änderungen nicht verloren gehen.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Schritt 5: Fügen Sie eine neue Farbton-/Sättigungsebene hinzu
Als Nächstes möchten Sie möglicherweise einer anderen PSD-Datei eine neue Einstellungsebene für Farbton/Sättigung hinzufügen. Gehen Sie dazu genauso vor wie zuvor, allerdings mit anderen PSD-Dateien.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Schritt 6: Neue Farbton-/Sättigungswerte für die neue Ebene festlegen
Nachdem Sie diese neue Ebene erstellt haben, wenden Sie wie zuvor die gewünschten Einstellungen für Farbton, Sättigung und Helligkeit an.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Schritt 7: Speichern Sie die aktualisierte PSD-Datei
Speichern Sie abschließend die PSD-Datei mit der hinzugefügten Ebene „Farbton/Sättigung“, damit Sie Ihre Änderungen sehen können.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Herzlichen Glückwunsch! Sie haben PSD-Dateien erfolgreich mit Aspose.PSD für Java bearbeitet. Jetzt können Sie mit verschiedenen Bildern und tieferen Änderungen experimentieren und Ihre Grafikdesignprojekte zum Leben erwecken.
## Abschluss
Das programmgesteuerte Arbeiten mit Grafiken eröffnet eine Welt voller Möglichkeiten. Die Verwendung von Aspose.PSD für Java zum Hinzufügen und Ändern von Farbton-Sättigungs-Anpassungsebenen bietet Flexibilität und Effizienz, die Ihren Design-Workflow optimieren können. Egal, ob Sie Fotos für ein Projekt verbessern oder atemberaubende visuelle Inhalte erstellen, die Beherrschung dieser Tools kann Ihre Ergebnisse erheblich verbessern.
 Entdecken Sie weitere Funktionen von Aspose.PSD, indem Sie eintauchen in[Dokumentation](https://reference.aspose.com/psd/java/) oder erwägen Sie einen[vorläufige Lizenz](https://purchase.aspose.com/temporary-license/) um die volle Leistungsfähigkeit der Bibliothek zu testen.
## Häufig gestellte Fragen
### Was ist eine Farbton-Sättigungs-Anpassungsebene?
Mithilfe einer Einstellungsebene für Farbton und Sättigung können Sie die Farbeigenschaften eines Bildes ändern, ohne die Originalpixel dauerhaft zu verändern.
### Muss Photoshop installiert sein, um Aspose.PSD zu verwenden?
Nein, Aspose.PSD ist eine eigenständige Bibliothek, die unabhängig von Photoshop funktioniert.
### Kann ich Aspose.PSD für die Stapelverarbeitung verwenden?
Ja, Sie können mit Aspose.PSD mehrere PSD-Dateien automatisieren und stapelweise verarbeiten.
### Ist Aspose.PSD kostenlos?
Aspose.PSD bietet eine kostenlose Testversion an, für die langfristige Nutzung ist jedoch eine Lizenz erforderlich. Sie können die Preise anzeigen[Hier](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
