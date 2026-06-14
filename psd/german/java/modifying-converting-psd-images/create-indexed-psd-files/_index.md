---
date: 2026-03-15
description: Erfahren Sie, wie Sie PSD‑Dateien erstellen, eine PSD‑Farbpalette generieren
  und den PSD‑Farbmodus mit Aspose.PSD für Java in dieser Schritt‑für‑Schritt‑Anleitung
  festlegen.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Wie man PSD-Dateien mit Aspose.PSD für Java erstellt
url: /de/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man PSD-Dateien mit Aspose.PSD für Java erstellt

## Einleitung
Wenn Sie sich jemals gefragt haben **wie man PSD**-Dateien programmgesteuert erstellt, sind Sie hier genau richtig. Aspose.PSD für Java gibt Ihnen die volle Kontrolle über Photoshop‑Dokumente und ermöglicht das Erzeugen, Bearbeiten und Speichern von PSD‑Dateien, ohne Photoshop zu öffnen. In diesem Tutorial führen wir Sie Schritt für Schritt durch das Erstellen einer **indexed PSD**‑Datei, das Festlegen des PSD‑Farbmodus und das Generieren einer benutzerdefinierten Farbpalette – alles mit klaren Java‑Code‑Beispielen. Egal, ob Sie eine Grafik‑Pipeline aufbauen, die Asset‑Erstellung automatisieren oder einfach nur experimentieren möchten, die hier vorgestellten Konzepte helfen Ihnen, Ihre visuellen Ideen zum Leben zu erwecken.

## Schnelle Antworten
- **Welche Bibliothek benötige ich?** Aspose.PSD für Java
- **Kann ich ein indiziertes PSD erstellen?** Ja, indem der Farbmodus auf `Indexed` gesetzt wird
- **Benötige ich Photoshop installiert?** Nein, Aspose.PSD arbeitet eigenständig
- **Welche Java-Version wird benötigt?** JDK 8 oder höher
- **Wie groß kann die Leinwand sein?** Beliebige Größe; dieses Beispiel verwendet 500 × 500 px

## Was ist eine indizierte PSD-Datei?
Eine indizierte PSD speichert Farben in einer Palette anstatt voller Farbwerte für jedes Pixel. Das reduziert die Dateigröße und ist ideal für Grafiken mit begrenzten Farben, wie Icons oder UI‑Assets. Durch das Erzeugen einer benutzerdefinierten Palette bestimmen Sie exakt, welche Farben im Endbild vorkommen.

## Warum eine PSD‑Farbpalette generieren?
Das Erstellen einer **PSD‑Farbpalette** ermöglicht Ihnen:
- Kleine Dateigrößen für Web‑ oder Mobile‑Einsatz beizubehalten  
- Konsistentes Branding sicherzustellen, indem Sie die Farben auf Ihre Unternehmenspalette beschränken  
- Schnellere Rendering‑Leistung in Anwendungen, die indizierte Bilder unterstützen  

## Voraussetzungen
Bevor wir zum Code kommen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Grundkenntnisse in Java** – Sie sollten mit Klassen, Methoden und der Objekterstellung vertraut sein.  
2. **Java Development Kit (JDK) 8+** – installiert und in Ihrer IDE konfiguriert.  
3. **IDE (IntelliJ IDEA, Eclipse usw.)** – optional, aber stark empfohlen für einfacheres Debugging.  
4. **Aspose.PSD for Java Bibliothek** – laden Sie sie **[hier](https://releases.aspose.com/psd/java/)** herunter und fügen Sie die JAR‑Datei dem Klassenpfad Ihres Projekts hinzu.  
5. **Grundlegende Konzepte des Grafikdesigns** – das Verständnis von Farbmodi, Paletten und Grundformen hilft Ihnen beim Folgen.  

## Pakete importieren
Bevor wir mit dem Code fortfahren, stellen wir sicher, dass alle notwendigen Pakete in Ihre Java‑Anwendung importiert wurden. Das benötigen Sie:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Diese Importe ermöglichen Ihnen die Arbeit mit PSD‑Optionen, Farben und Grafikmanipulation über Aspose.PSD.

Nun zerlegen wir den Code Schritt für Schritt, um **wie man PSD**‑Dateien mit einem indizierten Farbmodus erstellt.

## Schritt 1: Dokumentverzeichnis einrichten
Zuerst definieren Sie, wo das erzeugte PSD gespeichert werden soll.

```java
String dataDir = "Your Document Directory";
```

Ersetzen Sie `"Your Document Directory"` durch einen absoluten oder relativen Pfad, z. B. `"/Users/YourName/Documents/"`.

## Schritt 2: Instanz von PsdOptions erstellen
`PsdOptions` enthält alle Einstellungen für die Datei, die Sie erzeugen möchten.

```java
PsdOptions createOptions = new PsdOptions();
```

## Schritt 3: Kern‑Eigenschaften von PsdOptions festlegen
Hier geben wir den Ausgabepfad, den **set psd color mode** auf `Indexed` und die PSD‑Version an.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – der vollständige Pfad der neuen Datei.  
- **Color Mode** – `Indexed` weist Aspose.PSD an, ein palettenbasiertes Bild zu verwenden.  
- **Version** – PSD‑Formatversion (5 funktioniert für die meisten modernen Photoshop‑Versionen).  

## Schritt 4: Farbpalette erstellen (PSD‑Farbpalette generieren)
Definieren Sie die Farben, die im indizierten Bild verfügbar sein sollen.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- Das `palette`‑Array enthält bis zu 256 `Color`‑Objekte.  
- `CompressionMethod.RLE` bietet eine effiziente verlustfreie Kompression für indizierte Bilder.  

## Schritt 5: PSD‑Bildleinwand erstellen
Jetzt erstellen wir ein leeres PSD mit den gewünschten Abmessungen.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Dies erzeugt eine 500 × 500 Pixel‑Leinwand, die die zuvor definierte Palette verwendet.

## Schritt 6: Grafiken auf dem PSD zeichnen
Fügen Sie visuelle Inhalte hinzu – hier zeichnen wir eine einfache rote Ellipse auf einem weißen Hintergrund.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` füllt den Hintergrund mit Weiß.  
- `drawEllipse` rendert eine rote Ellipse mit einer 6‑Pixel‑Strichstärke.  

## Schritt 7: PSD‑Datei speichern
Abschließend speichern wir das Bild auf der Festplatte.

```java
psd.save();
```

Die Datei `Newsample_out.psd` erscheint in dem Verzeichnis, das Sie zuvor angegeben haben.

## Häufige Probleme & Tipps
- **Palette Size** – Wenn Sie mehr als 4 Farben benötigen, fügen Sie sie einfach dem `palette`‑Array hinzu (bis zu 256).  
- **File Permissions** – Stellen Sie sicher, dass der Java‑Prozess Schreibzugriff auf `dataDir` hat.  
- **Incorrect Color Mode** – Das Vergessen von `createOptions.setColorMode(ColorModes.Indexed)` erzeugt ein RGB‑PSD anstelle eines indizierten.  

## Häufig gestellte Fragen

**Q: Was ist Aspose.PSD für Java?**  
A: Aspose.PSD für Java ist eine Bibliothek, die die programmgesteuerte Manipulation von PSD (Photoshop)-Dateien mit Java ermöglicht.

**Q: Kann ich Aspose.PSD kostenlos nutzen?**  
A: Ja, Sie können eine kostenlose Testversion von Aspose.PSD **[hier](https://releases.aspose.com/)** erhalten.

**Q: Muss ich Photoshop installiert haben, um mit Aspose.PSD zu arbeiten?**  
A: Nein, Sie können PSD‑Dateien ohne Photoshop erstellen und manipulieren, da Aspose.PSD alle Vorgänge eigenständig ausführt.

**Q: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD?**  
A: Sie können eine temporäre Lizenz **[hier](https://purchase.aspose.com/temporary-license/)** anfordern.

**Q: Wo kann ich Support für Aspose.PSD erhalten?**  
A: Sie können Support im Aspose‑Forum **[hier](https://forum.aspose.com/c/psd/34)** erhalten.

## Fazit
Sie haben gerade **wie man PSD**‑Dateien mit einem indizierten Farbmodus erstellt, eine benutzerdefinierte Palette generiert und einfache Grafiken hinzugefügt – alles mit Aspose.PSD für Java. Mit diesen Bausteinen können Sie zu komplexeren Zeichnungen, Ebenenverwaltung und Batch‑Verarbeitung übergehen. Für weiterführende Informationen schauen Sie sich die offizielle API‑Referenz **[hier](https://reference.aspose.com/psd/java/)** an und experimentieren Sie weiter mit verschiedenen Paletten und Zeichen‑Primitiven.

---

**Zuletzt aktualisiert:** 2026-03-15  
**Getestet mit:** Aspose.PSD für Java 24.12 (neueste)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}