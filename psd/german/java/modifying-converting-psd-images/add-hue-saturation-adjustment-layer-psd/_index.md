---
date: 2026-03-13
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java eine Farbton‑Sättigungs‑Ebene
  zu PSD‑Dateien hinzufügen. Dieser Leitfaden zeigt außerdem, wie Sie PSD‑Dateien
  stapelweise verarbeiten und programmgesteuert eine Farbton‑Anpassungsebene erstellen.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Farbton‑Sättigungs‑Ebene zu PSD hinzufügen mit Aspose.PSD für Java
url: /de/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

 unchanged.

Also the line "---" stays.

Now produce final output with all translations.

Be careful to preserve markdown formatting, shortcodes, code block placeholders.

Let's construct final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Farbton‑Sättigungsebene zu PSD hinzufügen

## Einleitung
Wenn es um Grafikdesign geht, spielt die Farbmanipulation eine entscheidende Rolle – insbesondere das Anpassen von Farbton, Sättigung und Helligkeit kann die Stimmung und Qualität eines Bildes drastisch verändern. Eine effektive Methode, dies zu erreichen, ist die Verwendung von Einstellungsebenen in Photoshop (PSD‑Dateien). Wenn Sie programmgesteuert mit Java **add hue saturation layer** möchten, hilft Ihnen die Aspose.PSD‑Bibliothek! Dieses Tutorial führt Sie Schritt für Schritt durch das Hinzufügen einer Hue Saturation Adjustment Layer zu Ihren PSD‑Dateien und macht Ihren Workflow produktiver und effizienter.

## Schnelle Antworten
- **Welche Bibliothek ermöglicht das Hinzufügen einer hue saturation layer in Java?** Aspose.PSD for Java.  
- **Muss Photoshop installiert sein?** Nein, die Bibliothek funktioniert unabhängig von Photoshop.  
- **Kann ich PSD‑Dateien mit diesem Ansatz stapelweise verarbeiten?** Ja – sobald Sie die Schritte automatisiert haben, können Sie sie auf viele Dateien anwenden.  
- **Welche Java‑Version wird benötigt?** JDK 8 oder höher.  
- **Ist für den Produktionseinsatz eine Lizenz erforderlich?** Ja, nach der Testphase ist eine kommerzielle Lizenz erforderlich.

## Was ist eine „add hue saturation layer“-Operation?
Eine **add hue saturation layer**‑Operation erstellt eine nicht‑destruktive Einstellungsebene, mit der Sie Farbton-, Sättigungs‑ und Helligkeitswerte ändern können, ohne die ursprünglichen Pixeldaten zu verändern. Das ist ideal, um Farben in einer gesamten Komposition oder in bestimmten Farbbereichen fein abzustimmen.

## Warum Aspose.PSD für Java verwenden?
- **Keine Photoshop‑Abhängigkeit** – funktioniert auf jeder Plattform, die Java ausführt.  
- **Vollständige PSD‑Treue** – bewahrt alle Ebeneninformationen, Masken und Effekte.  
- **Batch‑bereit** – Sie können Ordner durchlaufen und dieselbe Anpassung auf Dutzende von Dateien anwenden.  
- **Leistungsorientiert** – optimiert für große Dokumente und serverseitige Automatisierung.

## Voraussetzungen
Bevor wir zum Code kommen, stellen Sie sicher, dass Sie Folgendes bereit haben:

1. **Java Development Kit (JDK):** Stellen Sie sicher, dass JDK 8 oder höher auf Ihrem Rechner installiert ist. Sie können es von den [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html) herunterladen.  
2. **Aspose.PSD for Java Library:** Sie benötigen die Aspose.PSD‑Bibliothek, die Sie [hier herunterladen](https://releases.aspose.com/psd/java/) können.  
3. **IDE:** Eine geeignete integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA oder Eclipse für die Java‑Entwicklung.  
4. **Grundkenntnisse in Java:** Vertrautheit mit Java‑Programmierung ist von Vorteil, aber keine Sorge – wir führen Sie durch jede Zeile.

Jetzt, wo die Voraussetzungen geklärt sind, gehen wir zum spaßigen Teil über – dem Coden!

## Pakete importieren
Um mit der Aspose.PSD‑Bibliothek zu arbeiten, ist der erste Schritt, die notwendigen Klassen zu importieren. So geht's in Ihrer Java‑Datei:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

Stellen Sie sicher, dass die entsprechenden Bibliotheken Ihrem Projekt hinzugefügt wurden, damit diese Importe reibungslos funktionieren.

## Schritt 1: Dokumentverzeichnis einrichten
Jedes Projekt braucht einen Ausgangspunkt, und unseres ist keine Ausnahme. Sie müssen ein Verzeichnis angeben, in dem Ihre PSD‑Dateien gespeichert sind. Das ist entscheidend, um Bilder korrekt zu laden und zu speichern.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Schritt 2: Vorhandene PSD‑Datei laden
Um eine vorhandene PSD‑Datei zu bearbeiten, müssen wir sie zuerst in unser Programm laden. So geht's:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

In diesem Code passen Sie `"HueSaturationAdjustmentLayer.psd"` an den Namen Ihrer vorhandenen PSD‑Datei an, die Sie bearbeiten möchten.

## Schritt 3: Hue/Saturation‑Ebene bearbeiten
Als nächstes durchlaufen wir die Ebenen unseres geladenen PSD‑Bildes, um vorhandene Hue/Saturation‑Ebenen zu finden und zu bearbeiten. Dieser Schritt beinhaltet das Anpassen von Farbton, Sättigung und Helligkeit.

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
- Wir stellen den Farbton auf **-25**, die Sättigung auf **-12** und die Helligkeit auf **+67** ein.  
- Die Methode `getRange(2)` ermöglicht es, bestimmte Farbbereiche nach Wunsch zu justieren.

## Schritt 4: Modifizierte PSD‑Datei speichern
Nachdem die Anpassungen vorgenommen wurden, ist der nächste Schritt, die Datei zu speichern. Das ist ein wesentlicher Teil unseres Prozesses, damit die Änderungen nicht verloren gehen.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Schritt 5: Neue Hue/Saturation‑Ebene hinzufügen
Wenn Sie **create hue adjustment layer** von Grund auf neu erstellen möchten, können Sie einer anderen PSD‑Datei eine brandneue Hue/Saturation‑Einstellungsebene hinzufügen. Verwenden Sie dafür das gleiche Lade‑Muster, aber rufen Sie die Methode `addHueSaturationAdjustmentLayer()` auf.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Schritt 6: Neue Hue/Saturation‑Werte für die neue Ebene festlegen
Jetzt, wo Sie diese neue Ebene erstellt haben, wenden Sie die gewünschten Farbton‑, Sättigungs‑ und Helligkeitseinstellungen wie zuvor an.

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

## Schritt 7: Aktualisierte PSD‑Datei speichern
Zum Schluss speichern Sie die PSD‑Datei mit der hinzugefügten Hue/Saturation‑Ebene, damit Sie Ihre Änderungen sehen können.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

Herzlichen Glückwunsch! Sie haben erfolgreich PSD‑Dateien mit Aspose.PSD für Java manipuliert. Jetzt können Sie mit verschiedenen Bildern und tieferen Änderungen experimentieren und Ihre Grafikdesign‑Projekte zum Leben erwecken.

## Wie man PSD‑Dateien stapelweise mit Farbton‑Anpassungen verarbeitet
Da der obige Code vollständig skriptfähig ist, können Sie die gesamte Sequenz in einer Schleife verpacken, die über jede `.psd`‑Datei in einem Ordner iteriert. Das ermöglicht Ihnen, **batch process psd files** zu durchführen und dieselben Farbton‑, Sättigungs‑ und Helligkeitsanpassungen in einem Durchlauf anzuwenden – perfekt für groß angelegte Marken‑Updates.

## Häufige Probleme und Lösungen
- **NullPointerException beim Laden einer Datei:** Stellen Sie sicher, dass `dataDir` mit dem passenden Dateiseparator (`/` oder `\`) endet und der Dateiname korrekt ist.  
- **Anpassungswerte außerhalb des Bereichs:** Farbton, Sättigung und Helligkeit akzeptieren Werte von -255 bis 255. Halten Sie Ihre Zahlen innerhalb dieses Bereichs.  
- **Ebene nicht gefunden:** Wenn die PSD keine Hue/Saturation‑Ebene enthält, überspringt die `instanceof`‑Prüfung den Block. Verwenden Sie `addHueSaturationAdjustmentLayer()`, um zuerst eine zu erstellen.

## Häufig gestellte Fragen

**Q: Was ist eine Hue Saturation Adjustment Layer?**  
A: Sie ermöglicht es, die Farbeigenschaften eines Bildes zu ändern, ohne die ursprünglichen Pixel dauerhaft zu verändern.

**Q: Muss Photoshop installiert sein, um Aspose.PSD zu nutzen?**  
A: Nein, Aspose.PSD ist eine eigenständige Bibliothek, die unabhängig von Photoshop funktioniert.

**Q: Kann ich Aspose.PSD für die Stapelverarbeitung nutzen?**  
A: Ja, Sie können mehrere PSD‑Dateien mit Aspose.PSD automatisieren und stapelweise verarbeiten.

**Q: Ist Aspose.PSD kostenlos?**  
A: Aspose.PSD bietet eine kostenlose Testversion an, aber für den langfristigen Einsatz ist eine Lizenz erforderlich. Die Preise können Sie [hier](https://purchase.aspose.com/buy) einsehen.

## Fazit
Die programmgesteuerte Arbeit mit Grafiken eröffnet ein breites Spektrum an Möglichkeiten. Mit Aspose.PSD für Java **add hue saturation layer** und **create hue adjustment layer** zu nutzen, bietet Flexibilität und Effizienz, die Ihren Design‑Workflow straffen können. Egal, ob Sie Fotos für ein Projekt optimieren oder beeindruckende visuelle Inhalte erstellen – das Beherrschen dieser Werkzeuge kann Ihre Ergebnisse erheblich verbessern.

Entdecken Sie gerne weitere Funktionen von Aspose.PSD, indem Sie in die [documentation](https://reference.aspose.com/psd/java/) eintauchen, oder erwägen Sie, eine [temporary license](https://purchase.aspose.com/temporary-license/) zu erwerben, um die volle Leistungsfähigkeit der Bibliothek zu testen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-03-13  
**Getestet mit:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

---