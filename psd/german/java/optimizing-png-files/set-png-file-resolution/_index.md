---
date: 2026-03-18
description: Erfahren Sie, wie Sie die PNG‑Auflösung in Java ändern und die Bildauflösung
  in Java mit Aspose.PSD für Java festlegen. Folgen Sie dieser Schritt‑für‑Schritt‑Anleitung,
  um Ihre Bilder schnell zu optimieren.
linktitle: Change PNG resolution java using Aspose.PSD
second_title: Aspose.PSD Java API
title: PNG-Auflösung in Java mit Aspose.PSD ändern
url: /de/java/optimizing-png-files/set-png-file-resolution/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG-Auflösung in Java ändern mit Aspose.PSD

## Einführung
Wenn Sie die **PNG-Auflösung in Java** schnell und zuverlässig ändern müssen, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie Schritt für Schritt durch die erforderlichen Schritte, um die PNG-Dateiauflösung mit Aspose.PSD für Java anzupassen. Egal, ob Sie ein Batch‑Verarbeitungstool, einen Web‑Dienst oder einfach nur ein paar Assets verfeinern, derselbe Ansatz funktioniert überall. Öffnen Sie Ihre bevorzugte IDE und legen wir los!

## Schnelle Antworten
- **Welche Bibliothek verarbeitet die PNG‑Auflösung?** Aspose.PSD for Java  
- **Primäre Methode?** `PngOptions.setResolutionSettings`  
- **Typische DPI‑Werte?** 72 × 96 für web‑fertige Bilder  
- **Benötige ich eine Lizenz?** Eine Testversion funktioniert zum Testen; für die Produktion ist eine Lizenz erforderlich  
- **Unterstütztes JDK?** Java 8 oder höher  

## Was bedeutet „PNG-Auflösung in Java ändern“?
Die PNG‑Auflösung in Java zu ändern bedeutet, die DPI‑Metadaten (dots per inch) zu ändern, die Browsern und Druckern mitteilen, wie groß das Bild angezeigt werden soll. Die Pixeldaten bleiben unverändert, aber das Auflösungstag wird aktualisiert, was die Druckgröße und -qualität beeinflussen kann.

## Warum Aspose.PSD für diese Aufgabe verwenden?
Aspose.PSD bietet eine High‑Level‑API, die die Low‑Level‑PNG‑Verarbeitung abstrahiert, sodass Sie sich auf die Geschäftslogik statt auf Dateiformat‑Eigenheiten konzentrieren können. Es unterstützt Hunderte von PSD‑Funktionen, läuft auf jeder Plattform, die Java ausführt, und erfordert keine nativen Bibliotheken.

## Voraussetzungen
1. **Java Development Kit (JDK) 8+** – Der Code läuft auf jedem aktuellen JDK.  
2. **Aspose.PSD for Java** – Laden Sie es über den [download link](https://releases.aspose.com/psd/java/) herunter.  
3. **Eine IDE** – IntelliJ IDEA, Eclipse oder VS Code mit Java‑Unterstützung.  
4. **Eine Beispiel‑PSD‑Datei** – Wir werden sie in PNG konvertieren und die Auflösung ändern.  
5. **Grundlegende Java‑Kenntnisse** – Sie werden die Code‑Snippets ohne weitere Erklärung verstehen.  

## Pakete importieren
Jetzt, wo alles eingerichtet ist, importieren Sie die benötigten Klassen. Diese Importe geben Ihnen Zugriff auf das Laden von Bildern, Auflösungseinstellungen und PNG‑Exportoptionen.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResolutionSetting;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Schritt 1: Ihr Java‑Projekt einrichten
Erstellen Sie ein neues Java‑Projekt (oder ein Maven/Gradle‑Modul) und fügen Sie das Aspose.PSD‑JAR dem Build‑Pfad hinzu. Wenn Sie Maven verwenden, fügen Sie die passende Abhängigkeit aus dem Aspose‑Repository hinzu.

## Schritt 2: Definieren Sie Ihr Dokumentverzeichnis
Geben Sie dem Programm an, wo die Quell‑PSD‑Datei zu finden ist und wo das Ausgabe‑PNG gespeichert werden soll.

```java
String dataDir = "Your Document Directory"; // Update with your folder path
```

Ersetzen Sie `"Your Document Directory"` durch den absoluten oder relativen Pfad, der `sample.psd` enthält.

## Schritt 3: Laden Sie das PSD‑Bild
Verwenden Sie die Klasse `PsdImage`, um die PSD‑Datei von der Festplatte zu lesen.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Stellen Sie sicher, dass der Dateiname mit dem tatsächlichen PSD übereinstimmt, das Sie verarbeiten möchten.

## Schritt 4: PNG‑Optionen erstellen und konfigurieren
Hier ändern wir tatsächlich die **PNG‑Auflösung in Java**. Wir instanziieren `PngOptions` und setzen die horizontalen und vertikalen DPI‑Werte über `ResolutionSetting`.

```java
PngOptions options = new PngOptions();
options.setResolutionSettings(new ResolutionSetting(72, 96)); // 72 DPI horizontal, 96 DPI vertical
```

Ersetzen Sie `72` und `96` gerne durch beliebige Werte, die zu Ihrem Zielgerät passen. Dies ist der Kern der **set image resolution java**‑Operation.

## Schritt 5: Das resultierende PNG speichern
Exportieren Sie schließlich das PSD als PNG mit den neuen Auflösungs‑Metadaten.

```java
psdImage.save(dataDir + "SettingResolution_output.png", options);
```

Die Datei `SettingResolution_output.png` erscheint im selben Ordner und enthält nun die von Ihnen angegebenen DPI‑Werte.

## Häufige Fallstricke & Tipps
- **Falscher Pfad** – Überprüfen Sie, ob `dataDir` mit einem Dateiseparator (`/` oder `\`) endet.  
- **Nicht unterstützte DPI** – Die meisten Browser ignorieren DPI‑Werte über 300; halten Sie sie im vernünftigen Bereich.  
- **Speichernutzung** – Große PSD‑Dateien können viel RAM verbrauchen; erwägen Sie, `psdImage` nach dem Speichern zu entsorgen (`psdImage.dispose()`).  

## Fazit
Sie haben gerade gelernt, wie man die **PNG‑Auflösung in Java** mit Aspose.PSD ändert. Durch Anpassen von `ResolutionSetting` können Sie steuern, wie Ihre PNGs von Druckern und Design‑Tools interpretiert werden, ohne die Pixeldaten zu verändern. Erkunden Sie weitere Optionen wie Kompressionsgrad, Farbtiefe oder Batch‑Verarbeitung, um Ihren Arbeitsablauf weiter zu automatisieren.

Für weiterführende Informationen schauen Sie sich die offizielle [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) an.

## FAQ
### Welche Formate kann ich mit Aspose.PSD für Java aus PSD‑Dateien konvertieren?
Sie können PSD‑Dateien in Formate wie PNG, JPEG, BMP und TIFF konvertieren.  
### Benötige ich eine Lizenz, um Aspose.PSD für Java zu verwenden?
Ja, obwohl eine kostenlose Testversion verfügbar ist, ist für die fortgesetzte Nutzung nach der Evaluierung eine gültige Lizenz erforderlich.  
### Kann ich die Auflösung mehrmals in einem Programm ändern?
Absolut! Sie können verschiedene `PngOptions`‑Instanzen für unterschiedliche Export‑Einstellungen innerhalb derselben Anwendung erstellen.  
### Was ist, wenn meine PSD‑Datei beschädigt ist?
Aspose.PSD behandelt viele gängige Probleme, aber wenn eine Datei stark beschädigt ist, lässt sie sich möglicherweise nicht laden. Bewahren Sie stets ein Backup auf.  
### Ist Aspose.PSD für Hochleistungs‑Anwendungen geeignet?
Ja, es ist darauf ausgelegt, große Dateien effizient zu verarbeiten und eignet sich für performance‑intensive Bildverarbeitungsaufgaben.

## Häufig gestellte Fragen
**Q: Wie kann ich programmgesteuert unterschiedliche DPI für die horizontale und vertikale Achse festlegen?**  
A: Verwenden Sie `new ResolutionSetting(horizontalDpi, verticalDpi)` wie im PNG‑Optionen‑Beispiel gezeigt.  

**Q: Kann ich mehrere PSD‑Dateien in einem Durchlauf batch‑verarbeiten?**  
A: Ja – wickeln Sie die Lade‑, Options‑Konfigurations‑ und Speicher‑Schritte in eine Schleife, die über Ihre Dateisammlung iteriert.  

**Q: Beeinflusst das Ändern der DPI die Dateigröße?**  
A: In der Regel nicht; DPI ist ein Metadatum. Die Dateigröße ändert sich nur, wenn Sie die Kompression oder die Pixeldimensionen ändern.  

**Q: Gibt es eine Möglichkeit, die aktuelle DPI eines bestehenden PNG zu lesen?**  
A: Laden Sie das PNG mit `Image.load()` und prüfen Sie `image.getResolutionSettings()` (für PNG‑Dateien verfügbar).  

**Q: Welche JDK‑Versionen werden offiziell unterstützt?**  
A: Aspose.PSD für Java unterstützt JDK 8 bis JDK 21.  

**Zuletzt aktualisiert:** 2026-03-18  
**Getestet mit:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}