---
date: 2026-03-18
description: Erfahren Sie, wie Sie PSD in PNG konvertieren und dabei die PNG‑Bit‑Tiefe
  mit Aspose.PSD für Java ändern – Schritt‑für‑Schritt‑Anleitung mit Codebeispielen.
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Wie man PSD in PNG mit festgelegter Bit‑Tiefe mit Aspose.PSD für Java konvertiert
url: /de/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD in PNG mit angegebener Bittiefe konvertieren mit Aspose.PSD für Java

## Einführung
Wenn Sie **psd to png** konvertieren und die genaue PNG‑Bittiefe steuern müssen, sind Sie hier genau richtig. In diesem Tutorial zeigen wir, wie Sie die PNG‑Bittiefe ändern, während Sie eine PSD‑Datei als PNG‑Bild mit Aspose.PSD für Java speichern. Egal, ob Sie ein Batch‑Verarbeitungstool, einen Web‑Service oder ein Desktop‑Utility bauen – das **save png with options**‑Feature, z. B. Graustufen‑Farbtyp und benutzerdefinierte Bittiefe, gibt Ihnen feinkörnige Kontrolle über Bildqualität und Dateigröße.

## Schnelle Antworten
- **Kann ich die PNG‑Bittiefe ändern?** Ja – verwenden Sie `PngOptions.setBitDepth()`, um 1, 2, 4, 8 oder 16 Bits anzugeben.  
- **Welche Farbtypen werden unterstützt?** Grayscale, TrueColor, Indexed und weitere über `PngColorType`.  
- **Benötige ich eine Lizenz für Aspose.PSD?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Welche Java‑Version wird benötigt?** Java 8+ (die Bibliothek ist mit neueren JDKs kompatibel).  
- **Ist der Code sofort ausführbar?** Ja – ersetzen Sie einfach den Platzhalter‑Pfad durch Ihren eigenen Ordner.

## Was bedeutet „convert psd to png“ mit benutzerdefinierter Bittiefe?
Das Konvertieren einer Photoshop‑PSD‑Datei in ein PNG‑Bild ist eine gängige Aufgabe, wenn Sie ein web‑freundliches Format benötigen. Die Möglichkeit, die **png‑Qualität** durch Festlegen der Bittiefe anzupassen, ermöglicht es Ihnen, die visuelle Treue gegen die Dateigröße abzuwägen, was besonders nützlich für Thumbnails, Icons oder bei begrenzter Bandbreite ist.

## Warum Aspose.PSD für Java verwenden?
Aspose.PSD für Java bietet eine High‑Level‑API, die die Komplexität des PSD‑Formats abstrahiert. Sie ermöglicht es Ihnen, **grayscale png zu erstellen**, **png mit Optionen zu speichern** und Farbprofile zu handhaben, ohne sich mit Low‑Level‑Byte‑Manipulation befassen zu müssen. Die Bibliothek ist vollständig verwaltet, plattformübergreifend und erhält regelmäßige Updates.

## Voraussetzungen
1. **Java Development Kit (JDK)** – laden Sie es von [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunter.  
2. **Aspose.PSD for Java** – erhalten Sie das neueste JAR über [this link](https://releases.aspose.com/psd/java/).  
3. **Grundlegende Java‑Kenntnisse** – Sie sollten mit Klassen, Methoden und Ausnahmebehandlung vertraut sein.  
4. **Eine IDE** wie IntelliJ IDEA oder Eclipse (optional, aber empfohlen).  
5. **Eine Beispiel‑PSD‑Datei** – legen Sie sie in einen Ordner, auf den Sie im Code verweisen.

Alles bereit? Großartig – lassen Sie uns die erforderlichen Pakete importieren.

## Pakete importieren
Da wir nun die Voraussetzungen abgedeckt haben, ist es Zeit, unsere Umgebung einzurichten, indem wir die relevanten Pakete in unserer Java‑Anwendung importieren. Starten Sie Ihre Entwicklungsumgebung und fügen Sie die folgenden Import‑Anweisungen am Anfang Ihrer Java‑Datei hinzu:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Diese Anweisungen importieren die Klassen, die wir im gesamten Tutorial verwenden werden, sodass wir PSD‑Dateien laden und sie als PNG‑Bilder mit der angegebenen Bittiefe speichern können.

## Schritt 1: Dokumentverzeichnis einrichten
Bevor wir mit der Bildverarbeitung beginnen, definieren wir ein Verzeichnis, in dem unsere Bilder gespeichert werden. Das ist, als würden Sie einen Ordner für Ihre Bastelmaterialien anlegen, bevor Sie ein Projekt starten.

```java
String dataDir = "Your Document Directory";
```

## Schritt 2: PSD‑Bild laden
Als Nächstes müssen wir die PSD‑Bilddatei laden, die Sie konvertieren möchten. Stellen Sie sich das vor wie das Öffnen einer Leinwand, auf der Sie Ihre Arbeit verrichten.

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Hier verwenden wir die Methode `Image.load()`, um unsere Beispiel‑PSD‑Datei zu lesen und sie in `PsdImage` zu casten, um PSD‑spezifische Eigenschaften zuzugreifen.

## Schritt 3: PNG‑Optionen erstellen
Sobald wir unsere Leinwand geöffnet haben, benötigen wir ein Set von Optionen, wie wir unser Bild speichern wollen. Das entspricht im Wesentlichen der Auswahl Ihrer Farben und Pinselstile, bevor Sie mit dem Malen beginnen.

```java
PngOptions options = new PngOptions();
```

In diesem Schritt initialisieren wir eine Instanz von `PngOptions`, die es uns ermöglicht, die Parameter für unsere PNG‑Ausgabe festzulegen.

## Schritt 4: Gewünschten Farbtyp festlegen
Jetzt entscheiden wir, welche Art von Farben wir in unserem endgültigen PNG‑Bild haben wollen. Streben Sie eine bunte Palette oder einen monochromen Stil an? Lassen Sie uns diese Entscheidung treffen!

```java
options.setColorType(PngColorType.Grayscale);
```

In diesem Beispiel setzen wir den Farbtyp auf grayscale. Sie könnten auch `PngColorType.TrueColor` wählen, wenn Sie ein Vollfarbbild möchten. Das ist der Teil, in dem wir **create grayscale png**.

## Schritt 5: Bittiefe festlegen
Als Nächstes legen wir die Bittiefe fest. Das ist ähnlich, wie Ihrem Drucker mitzuteilen, wie fein er Ihr Bild drucken soll – je mehr Bits, desto mehr Details!

```java
options.setBitDepth((byte)1);
```

Hier setzen wir die Bittiefe auf **1 Bit**, was für einfache Graustufen‑Bilder geeignet ist. Sie können den Wert je nach Qualitätsanforderungen auf 2, 4, 8 oder 16 ändern – ein klassisches Beispiel dafür, wie man **change png bit depth**.

## Schritt 6: PNG‑Bild speichern
Schließlich ist es Zeit, Ihr Meisterwerk zu speichern! Dieser Schritt schließt unser Projekt ab, indem wir unser Kunstwerk von der Bearbeitungs‑Leinwand in eine Galerie‑Wand übertragen.

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

Mit der `save()`‑Methode von `PsdImage` speichern wir die konvertierte Datei und wenden die definierten Optionen an. Voilà! Unser Bild ist nun mit der benutzerdefinierten Bittiefe gespeichert.

## Häufige Probleme und Lösungen
- **`NullPointerException` beim Laden der PSD** – prüfen Sie, ob `dataDir` auf den richtigen Ordner zeigt und `sample.psd` existiert.  
- **Nicht unterstützte Bittiefe** – Aspose.PSD unterstützt 1, 2, 4, 8 und 16 Bits für PNG. Die Verwendung eines anderen Werts löst eine `IllegalArgumentException` aus.  
- **Farbtyp‑Mismatch** – wenn Sie eine Bittiefe setzen, die nicht mit dem gewählten `PngColorType` kompatibel ist, passt die Bibliothek automatisch die nächstgelegene unterstützte Einstellung an.

## Häufig gestellte Fragen

**Q: Was ist Aspose.PSD für Java?**  
A: Aspose.PSD für Java ist eine Bibliothek zum Arbeiten mit PSD‑Dateien in Java‑Anwendungen, die es Ihnen ermöglicht, Bilder zu manipulieren und zu konvertieren.

**Q: Wie lege ich verschiedene Bittiefen fest?**  
A: Sie können die Bittiefe mit der Methode `options.setBitDepth((byte)n)` festlegen, wobei Sie `n` durch die gewünschte Tiefe ersetzen.

**Q: Kann ich Aspose.PSD kostenlos nutzen?**  
A: Ja, Sie können die Bibliothek mit einer kostenlosen Testversion ausprobieren, die Sie [hier](https://releases.aspose.com/) finden.

**Q: Wo kann ich eine Support‑Lizenz für Aspose erhalten?**  
A: Für eine temporäre Lizenz können Sie sich [hier](https://purchase.aspose.com/temporary-license/) bewerben.

**Q: Welche Bildtypen kann ich konvertieren?**  
A: Aspose.PSD arbeitet hauptsächlich mit PSD‑Dateien, unterstützt jedoch die Konvertierung in verschiedene Formate wie PNG, JPEG und TIFF.

## Fazit
Sie haben nun gelernt, wie Sie **convert psd to png** durchführen und dabei die PNG‑Bittiefe mit Aspose.PSD für Java steuern. Durch Anpassen der `PngOptions` können Sie **adjust png quality** ändern, **grayscale png** erstellen und die Dateigröße für jedes Szenario feinjustieren. Experimentieren Sie mit verschiedenen Farbtypen und Bittiefen, um das optimale Gleichgewicht für Ihre Anwendung zu finden.

---

**Zuletzt aktualisiert:** 2026-03-18  
**Getestet mit:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}