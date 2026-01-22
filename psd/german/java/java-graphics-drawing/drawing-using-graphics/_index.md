---
date: 2026-01-22
description: Erfahren Sie, wie Sie mit Aspose.PSD ein PSD‑Bild in Java erstellen,
  Grafiken zeichnen, ein Polygon füllen und PSD nach BMP exportieren. Ein vollständiges
  Java‑Bildbearbeitungstutorial.
linktitle: Drawing Using Graphics in Java
second_title: Aspose.PSD Java API
title: PSD-Bild in Java erstellen – Zeichnen mit Graphics und Aspose.PSD
url: /de/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Grafiken in Java zeichnen

## Einleitung
In diesem **java image manipulation tutorial** zeigen wir Ihnen, wie Sie programmgesteuert **create PSD image java** mit Aspose.PSD erstellen können. Egal, ob Sie Grafiken on-the-fly erzeugen, Polygone f bis zum## Schnelle Antworten BmpOptions())` auf.
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose temporäre Lizenz ist für die Evaluierung verfügbar.
- **Welche Java‑Version wird benötigt?** JDK 8 oder höher.

## Voraussetzungen
Bevor Sie in dieses Tutorial einsteigen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:
- Grundkenntnisse in der Java‑Programmierung.
- Java Development Kit (JDK) auf Ihrem System installiert.
- Integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA oder Eclipse.
- Aspose.PSD for Java Bibliothek. Sie können sie von [hier](https://releases.aspose.com/psd/java/) herunterladen.

## Grafiken in Java mit Aspose.PSD zeichnen
Um zu beginnen, importieren Sie die erforderlichen Pakete von Aspose.PSD for Java sowie weitere Standard‑Java‑Bibliotheken:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Schritt 1: Bildobjekt erstellen
Zuerst instanziieren Sie ein `PsdImage`‑Objekt mit bestimmten Abmessungen:

```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Schritt 2: Graphics‑Objekt initialisieren
Als Nächstes initialisieren Sie ein `Graphics`‑Objekt mit dem `PsdImage`:

```java
Graphics graphics = new Graphics(image);
```

## Schritt 3: Bildoberfläche löschen
Löschen Sie die Bildoberfläche mit einer angegebenen Farbe (in diesem Beispiel Weiß):

```java
graphics.clear(Color.getWhite());
```

## Schritt 4: Pen‑Objekt erstellen und konfigurieren
Erstellen Sie ein `Pen`‑Objekt, um die Strich‑Eigenschaften (Farbe, Dicke usw.) zu definieren:

```java
Pen pen = new Pen(Color.getBlue());
```

## Schritt 5: Formen zeichnen – Wie man Grafiken in Java zeichnet
Zeichnen Sie eine Ellipse auf das Bild, indem Sie das `Pen`‑Objekt und ein Begrenzungsrechteck verwenden:

```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Polygon in Java‑Grafik füllen
Definieren und verwenden Sie einen `LinearGradientBrush`, um ein Polygon mit einem Farbverlauf zu füllen:

```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## PSD nach BMP exportieren
Speichern Sie schließlich das modifizierte Bild an einem angegebenen Ort und Format (in diesem Beispiel BMP):

```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Fazit
Durch das Befolgen dieses **java image manipulation tutorial** wissen Sie nun, wie Sie **create PSD image java** erstellen, Formen zeichnen, Farbverläufe anwenden, Polygone füllen und **export PSD to BMP** mit Aspose.PSD durchführen. Experimentieren Sie mit verschiedenen Pinseln, Farben und Geometrien, um Ihre Java‑Anwendungen mit leistungsstarken Grafikfunktionen zu bereichern.

## Häufig gestellte Fragen

**Q: Kann Aspose.PSD komplexe Bildmanipulationen verarbeiten?**  
A: Ja, Aspose.PSD unterstützt ein breites Spektrum an Operationen, einschließlich Ebenenbearbeitung, Farbkorrekturen und Textdarstellung.

**Q: Ist Aspose.PSD für Hochleistungs‑Anwendungen geeignet?**  
A: Absolut, Aspose.PSD ist für Leistung und Speicher‑Effizienz optimiert.

**Q: Wo finde ich weitere Beispiele und Dokumentation?**  
A: Besuchen Sie die [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/) für umfassende Anleitungen und API‑Referenzen.

**Q: Unterstützt Aspose.PSD mehrere Bildformate für den Export?**  
A: Ja, Aspose.PSD kann in BMP, PNG, JPEG, TIFF und andere gängige Formate exportieren.

**Q: Wie erhalte ich Support oder Hilfe, wenn ich auf Probleme stoße?**  
A: Wenden Sie sich an die Aspose.PSD‑Community im [support forum](https://forum.aspose.com/c/psd/34) oder erwägen Sie eine [temporary license](https://purchase.aspose.com/temporary-license/) für prioritären Support.

---

**Zuletzt aktualisiert:** 2026-01-22  
**Getestet mit:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}