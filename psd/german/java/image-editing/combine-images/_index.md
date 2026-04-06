---
date: 2025-12-30
description: Erfahren Sie, wie Sie mit Aspose.PSD in Java eine PSD‑Datei erstellen,
  indem Sie zwei Bilder kombinieren. Folgen Sie unserer Schritt‑für‑Schritt‑Anleitung,
  um Bilder schnell zu einer PSD‑Datei zusammenzuführen.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Wie man eine PSD-Datei in Java erstellt – Bilder mit Aspose.PSD kombinieren
url: /de/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD-Datei in Java erstellen – Bilder mit Aspose.PSD kombinieren

## Einführung

Wenn Sie **eine PSD-Datei in Java** erstellen möchten, indem Sie mehrere Bilder zusammenführen, macht Aspose.PSD die Aufgabe unkompliziert. In diesem Tutorial führen wir Sie Schritt für Schritt durch das Kombinieren von zwei Bildern zu einer einzigen PSD‑Leinwand, erklären, warum dieser Ansatz nützlich ist, und stellen Ihnen sofort ausführbaren Code zur Verfügung. Am Ende können Sie **zwei Bilder in Java** kombinieren und eine professionell aussehende, mehrschichtige Datei erzeugen.

## Schnellantworten
- **Welche Bibliothek ist am besten zum Zusammenführen von Bildern in eine PSD?** Aspose.PSD für Java.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für ein einfaches Kombinieren.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich mehr als zwei Bilder hinzufügen?** Ja – wiederholen Sie die `drawImage`‑Aufrufe für jede weitere Ebene.  
- **Welche Java‑Version wird unterstützt?** Java 8 und neuer.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Aspose.PSD Bibliothek** – laden Sie sie von [hier](https://releases.aspose.com/psd/java/) herunter.  
2. **Java Development Kit (JDK)** – Java 8+ wird empfohlen.  
3. **Dokumentverzeichnis** – ein Ordner auf Ihrem Rechner, in dem die Quellbilder und die resultierende PSD gespeichert werden.

## Pakete importieren

Importieren Sie die benötigten Aspose.PSD‑Klassen in Ihr Projekt:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: PSD‑Optionen erstellen (Datei vorbereiten)

Zuerst erstellen wir eine Instanz von `PsdOptions`, die die Ausgabeeinstellungen enthält.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Schritt 2: FileCreateSource festlegen (Zielort der PSD definieren)

Weisen Sie den Optionen ein `FileCreateSource` zu, das auf die gewünschte Zieldatei zeigt.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Schritt 3: Image‑Instanz erstellen (Leinwandgröße initialisieren)

Erzeugen Sie ein `Image`‑Objekt mit den Optionen und geben Sie eine Leinwand von 600 × 600 Pixel an.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Schritt 4: Graphics initialisieren und das erste Bild zeichnen

Ein `Graphics`‑Objekt ermöglicht das Malen auf der Leinwand. Wir löschen den Hintergrund zu Weiß und zeichnen das erste Quellbild auf die linke Hälfte.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Schritt 5: Das zweite Bild zeichnen (Kombination abschließen)

Jetzt platzieren wir das zweite Bild auf der rechten Hälfte derselben Leinwand.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Schritt 6: Die resultierende PSD‑Datei speichern

Abschließend speichern wir die kombinierte Leinwand auf dem Datenträger.

```java
image.save();
```

Herzlichen Glückwunsch! Sie haben **Bilder erfolgreich in eine PSD zusammengeführt** und eine PSD‑Datei in Java erstellt.

## Warum Bilder mit Aspose.PSD kombinieren?

- **Layer‑aware** – jeder `drawImage`‑Aufruf fügt eine separate Ebene hinzu, die Sie später bearbeiten können.  
- **Formatflexibilität** – unterstützt PSD, PNG, JPEG, BMP und mehr.  
- **Keine nativen Abhängigkeiten** – reines Java, funktioniert auf jedem Betriebssystem, das das JDK ausführt.  

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|---------|---------|--------|
| `File not found`‑Fehler beim Laden der Quellbilder | Falscher `dataDir`‑Pfad | Stellen Sie sicher, dass `dataDir` auf den Ordner zeigt, der `example1.psd` und `example2.psd` enthält. |
| Ausgabedatei ist leer | `graphics.clear` nach dem Zeichnen aufgerufen | Stellen Sie sicher, dass `graphics.clear(Color.getWhite())` **vor** allen `drawImage`‑Aufrufen ausgeführt wird. |
| Lizenz‑Ausnahme zur Laufzeit | Fehlende oder abgelaufene Aspose.PSD‑Lizenz | Laden Sie eine gültige Lizenz mit `License license = new License(); license.setLicense("Aspose.PSD.lic");` bevor Sie irgendeinen API‑Aufruf tätigen. |

## Häufig gestellte Fragen

### Q1: Ist Aspose.PSD mit allen Bildformaten kompatibel?
A1: Aspose.PSD konzentriert sich hauptsächlich auf das PSD‑Dateiformat. Es unterstützt jedoch verschiedene andere Formate für Ein- und Ausgabe.

### Q2: Kann ich weitere Änderungen am kombinierten Bild vornehmen?
A2: Absolut! Nach dem Kombinieren der Bilder können Sie das resultierende PSD mit den umfangreichen Funktionen von Aspose.PSD weiter bearbeiten.

### Q3: Gibt es Lizenzanforderungen für die Nutzung von Aspose.PSD?
A3: Ja, für die kommerzielle Nutzung ist eine gültige Lizenz erforderlich. Diese erhalten Sie [hier](https://purchase.aspose.com/buy).

### Q4: Gibt es eine kostenlose Testversion von Aspose.PSD?
A4: Ja, Sie können Aspose.PSD mit einer kostenlosen Testversion [hier](https://releases.aspose.com/) ausprobieren.

### Q5: Wo finde ich Support für Fragen zu Aspose.PSD?
A5: Besuchen Sie das [Aspose.PSD‑Forum](https://forum.aspose.com/c/psd/34) für Community‑Support und Diskussionen.

---

**Zuletzt aktualisiert:** 2025-12-30  
**Getestet mit:** Aspose.PSD 24.11 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}