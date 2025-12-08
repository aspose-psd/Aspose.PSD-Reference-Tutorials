---
date: 2025-12-08
description: Erfahren Sie, wie Sie PSD in PNG konvertieren und Bilder proportional
  in Java mit Aspose.PSD skalieren. Dieses Schritt‑für‑Schritt‑Tutorial behandelt
  das Zwischenspeichern von Bildern, das Skalieren und das Speichern als PNG.
language: de
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Wie man PSD in PNG konvertiert und proportional skaliert mit Aspose.PSD für
  Java
url: /java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man PSD zu PNG konvertiert und proportional skaliert mit Aspose.PSD für Java

## Einleitung

Wenn Sie **PSD zu PNG konvertieren** möchten und dabei das ursprüngliche Seitenverhältnis beibehalten wollen, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie durch ein komplettes **Aspose.PSD‑Tutorial**, das zeigt, **wie man Bilddateien** proportional in Java skaliert, das Bild für optimale Leistung zwischenspeichert und schließlich das Ergebnis als PNG speichert. Am Ende können Sie diesen Workflow in jede Java‑basierte Bildverarbeitungspipeline integrieren.

## Schnelle Antworten
- **Kann Aspose.PSD PSD zu PNG konvertieren?** Ja – einfach das PSD laden und mit `PngOptions` speichern.
- **Unterstützt die Bibliothek proportionale Skalierung?** Absolut; verwenden Sie `resizeWidthProportionally` und `resizeHeightProportionally`.
- **Muss ich das Bild zuerst zwischenspeichern?** Das Caching (`image.cacheData()`) verbessert die Leistung bei großen PSD‑Dateien.
- **Welche Java‑Version ist erforderlich?** Java 8 oder neuer wird vollständig unterstützt.
- **Ist für die Produktion eine Lizenz erforderlich?** Ja, eine kommerzielle Lizenz entfernt Evaluationswasserzeichen.

## Was bedeutet „PSD zu PNG konvertieren“ und warum ist das wichtig?

Das Konvertieren eines Photoshop‑Dokuments (PSD) in eine Portable Network Graphics (PNG)‑Datei ermöglicht es Ihnen, mehrschichtige Designs als leichtes, web‑freundliches Format zu teilen. PNG behält Transparenz und verlustfreie Qualität bei, was es ideal für UI‑Assets, Thumbnails oder jede Situation macht, in der Bildtreue wichtig ist.

## Warum Bild in Java proportional skalieren?

Das **wie man Bild skaliert** ohne Verzerrung des Seitenverhältnisses stellt sicher, dass Grafiken auf verschiedenen Bildschirmen natürlich aussehen. Die `Aspose.PSD`‑API bietet dedizierte Methoden für proportionale Skalierung, die automatisch die passende Höhe oder Breite berechnen und Sie so vor manuellen Rechenfehlern bewahren.

## Voraussetzungen

Bevor wir in den Code eintauchen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java Development Kit (JDK)** – Java 8 oder neuer installiert.
2. **Aspose.PSD for Java** – laden Sie das neueste JAR von der offiziellen Seite [here](https://releases.aspose.com/psd/java/).
3. Eine Beispiel‑PSD‑Datei (`sample.psd`) in einem Verzeichnis, das Sie von Ihrem Projekt aus referenzieren können, platzieren.

## Pakete importieren

Fügen Sie die notwendigen Importe zu Ihrer Java‑Klasse hinzu. Diese Klassen geben Ihnen Zugriff auf das Laden von Bildern, Caching, Skalierung und PNG‑Ausgabeoptionen.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Schritt 1: PSD‑Bild laden

Laden Sie zunächst die Quell‑PSD‑Datei. Wenn die Datei groß ist, reduziert das Caching der Bilddaten den Speicherverbrauch bei nachfolgenden Vorgängen.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Schritt 2: Bild proportional skalieren (Java)

Bestimmen Sie nun die neuen Abmessungen. In diesem Beispiel verkleinern wir das Bild auf **die Hälfte** seiner Originalgröße, wobei das Seitenverhältnis erhalten bleibt. Sie können die Zielbreite oder -höhe nach Bedarf anpassen.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Pro Tipp:** Verwenden Sie entweder `resizeWidthProportionally` *oder* `resizeHeightProportionally` – die Bibliothek berechnet automatisch die andere Dimension, um das Bild proportional zu halten.

## Schritt 3: Das skalierte Bild als PNG speichern

Exportieren Sie schließlich das skalierte Bild im PNG‑Format. Dieser Schritt schließt den **convert PSD to PNG**‑Workflow ab.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Wenn der Code ausgeführt wird, finden Sie eine PNG‑Datei, die halb so groß ist wie das ursprüngliche PSD, mit derselben visuellen Qualität und ohne Verzerrungen.

## Häufige Probleme & Lösungen

| Problem | Ursache | Lösung |
|-------|-------|-----|
| **OutOfMemoryError** | Große PSD nicht zwischengespeichert | Rufen Sie `image.cacheData()` vor dem Skalieren auf |
| **Blank PNG output** | Falscher Dateipfad | Überprüfen Sie `dataDir` und Schreibrechte |
| **Aspect ratio looks off** | Sowohl Breite als auch Höhe manuell verwendet | Verwenden Sie die proportionalen Methoden von Aspose.PSD |

## Häufig gestellte Fragen

**Q: Ist Aspose.PSD mit allen Bildformaten kompatibel?**  
A: Aspose.PSD unterstützt PSD, PNG, JPEG, BMP, GIF und viele weitere. Siehe die vollständige Liste in der [documentation](https://reference.aspose.com/psd/java/).

**Q: Kann ich Aspose.PSD für kommerzielle Projekte verwenden?**  
A: Ja. Kaufen Sie eine kommerzielle Lizenz im [Aspose store](https://purchase.aspose.com/buy).

**Q: Gibt es temporäre Lizenzen für Testzwecke?**  
A: Absolut – fordern Sie eine temporäre Lizenz [here](https://purchase.aspose.com/temporary-license/) für Evaluierungszwecke an.

**Q: Wo finde ich Community‑Support?**  
A: Das [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) ist ein großartiger Ort, um Fragen zu stellen und Lösungen zu teilen.

**Q: Wie greife ich auf die vollständige API‑Referenz zu?**  
A: Detaillierte API‑Dokumentationen sind [here](https://reference.aspose.com/psd/java/) verfügbar.

## Fazit

Sie wissen jetzt, **wie man PSD zu PNG konvertiert**, das Bild proportional skaliert und das Caching effizient nutzt, indem Sie Aspose.PSD für Java einsetzen. Integrieren Sie diese Schritte in Ihre eigenen Anwendungen, um schnelle, hochwertige Bildverarbeitung ohne native Photoshop‑Installation zu ermöglichen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-08  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose