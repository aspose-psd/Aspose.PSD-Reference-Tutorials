---
date: 2025-12-02
description: Erfahren Sie, wie Sie die Bildverarbeitungs‑Java‑Bibliothek Aspose.PSD
  verwenden, um mehrere Einstellungsebenen, einschließlich der Invertierung‑Einstellungsebene,
  für nahtlose PSD‑Manipulation anzuwenden.
language: de
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Java-Bibliothek zur Bildverarbeitung: Ebene invertieren mit Aspose.PSD'
url: /java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Invert-Anpassungsebene in Aspose.PSD für Java

## Einleitung

Wenn Sie nach einer robusten **image processing java library** suchen, ist Aspose.PSD für Java eine der vielseitigsten Optionen auf dem Markt. In diesem Tutorial zeigen wir, wie man eine **Invert Adjustment Layer** zu einer PSD‑Datei hinzufügt, eine Technik, die Sie mit anderen Anpassungsebenen kombinieren können, um anspruchsvolle visuelle Effekte zu erzielen. Egal, ob Sie ein Batch‑Verarbeitungstool oder einen Einzelbild‑Editor erstellen, bietet Ihnen dieser Leitfaden einen klaren, Schritt‑für‑Schritt‑Pfad, um die Aufgabe schnell zu erledigen.

## Schnelle Antworten
- **Was macht die Invert Adjustment Layer?** Sie kehrt alle Farbwerte im ausgewählten Bereich um und erzeugt einen Negativ‑Bildeffekt.  
- **Welche Bibliothek stellt diese Funktion bereit?** Aspose.PSD, eine führende image processing java library.  
- **Kann ich sie mit anderen Anpassungen kombinieren?** Ja – Sie können **apply multiple adjustment layers** wie Brightness/Contrast, Hue/Saturation und mehr.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion ist verfügbar; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Wie lange dauert die Implementierung?** In der Regel weniger als 10 Minuten für einen einfachen Anwendungsfall.

## Was ist die Invert Adjustment Layer?

Die Invert Adjustment Layer ist eine nicht‑destruktive Bearbeitung, die die RGB‑Werte jedes betroffenen Pixels umkehrt. Da sie oben im Ebenen‑Stack liegt, können Sie ihre Sichtbarkeit umschalten oder sie neu anordnen, ohne die ursprünglichen Bilddaten dauerhaft zu verändern.

## Warum Aspose.PSD als Ihre Image Processing Java Library verwenden?

- **Full PSD support** – lesen, bearbeiten und schreiben von Photoshop‑Dateien ohne installierte Photoshop‑Software.  
- **Cross‑platform** – funktioniert auf jeder Java‑Laufzeit (Java 6+).  
- **Rich adjustment features** – enthält integrierte Methoden für viele gängige Bearbeitungen, wodurch es einfach wird, **apply multiple adjustment layers** in einem einzigen Workflow zu verwenden.  
- **Performance‑optimized** – verarbeitet große Dateien effizient, was für die Batch‑Verarbeitung unerlässlich ist.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Aspose.PSD Library** – laden Sie sie von der offiziellen Seite [here](https://releases.aspose.com/psd/java/) herunter.  
2. **Java Development Environment** – JDK 6.0 oder höher installiert und konfiguriert.

Jetzt tauchen wir in den Code ein.

## Pakete importieren

Beginnen Sie mit dem Import der erforderlichen Klassen. Diese Importe geben Ihnen Zugriff auf die Kern‑APIs für die Bildverarbeitung und die PSD‑spezifische Funktionalität.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Schritt 1: Dokumentverzeichnis einrichten

Definieren Sie den Ordner, der Ihre Quell‑PSD‑Datei enthält und in dem die Ausgabe gespeichert wird.

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: PSD‑Datei laden

Laden Sie die Quelldatei in ein `PsdImage`‑Objekt. Dieses Objekt repräsentiert das gesamte PSD‑Dokument im Speicher.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Schritt 3: Invert Adjustment Layer hinzufügen

Rufen Sie die integrierte Methode auf, um eine Invert Adjustment Layer oben auf dem aktuellen Ebenen‑Stack einzufügen. Sie können später weitere Ebenen (z. B. Helligkeit, Farbton) hinzufügen, um **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## Schritt 4: Ausgabe speichern

Speichern Sie das modifizierte PSD auf dem Datenträger. Die gespeicherte Datei enthält nun die Invert Adjustment Layer und kann in Photoshop oder jedem PSD‑kompatiblen Betrachter geöffnet werden.

```java
im.save(outputPath);
```

### Was ist gerade passiert?

- Das PSD wurde in den Speicher geladen.  
- Eine Invert Adjustment Layer wurde als oberste Ebene hinzugefügt.  
- Das Bild wurde gespeichert, wobei die nicht‑destruktive Bearbeitung erhalten blieb.

Sie haben nun erfolgreich Aspose.PSD, eine **image processing java library**, verwendet, um eine PSD‑Datei zu manipulieren.

## Häufige Probleme & Tipps

| Problem | Ursache | Lösung |
|-------|-------|----------|
| **NullPointerException bei `Image.load`** | Falscher Dateipfad oder fehlende Datei | Überprüfen Sie `dataDir` und den Dateinamen; verwenden Sie absolute Pfade für Tests |
| **Layer-Reihenfolge nicht wie erwartet** | Das Hinzufügen von Ebenen nach bestehenden ändert die Stapelung | Verwenden Sie `im.addInvertAdjustmentLayer()` bevor Sie andere Anpassungen hinzufügen, oder ordnen Sie Ebenen über `im.getLayers()` neu. |
| **Leistungsverlust bei großen PSDs** | Laden sehr großer Dateien in den Speicher | Erwägen Sie die Verarbeitung von Seiten in Teilen oder erhöhen Sie die JVM‑Heap‑Größe (`-Xmx2g`). |

## Häufig gestellte Fragen

**F: Ist Aspose.PSD mit allen Java‑Versionen kompatibel?**  
A: Aspose.PSD unterstützt Java 6.0 und spätere Versionen.

**F: Kann ich mehrere Anpassungsebenen in einem einzigen Vorgang anwenden?**  
A: Ja, Sie können mehrere adjustment layers stapeln – wie Invert, Brightness und Hue/Saturation – um komplexe Effekte zu erzielen.

**F: Wo finde ich zusätzliche Dokumentation für Aspose.PSD?**  
A: Siehe die Dokumentation [here](https://reference.aspose.com/psd/java/) für umfassende Anleitungen und API‑Referenzen.

**F: Gibt es eine kostenlose Testversion für Aspose.PSD?**  
A: Ja, Sie können die kostenlose Testversion [here](https://releases.aspose.com/) erkunden.

**F: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?**  
A: Sie können eine temporäre Lizenz [here](https://purchase.aspose.com/temporary-license/) erhalten.

---

**Zuletzt aktualisiert:** 2025-12-02  
**Getestet mit:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}