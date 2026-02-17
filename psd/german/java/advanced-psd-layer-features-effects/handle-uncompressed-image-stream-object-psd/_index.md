---
date: 2026-02-17
description: Erfahren Sie, wie Sie PSD in PNG exportieren und unkomprimierte Bildstreams
  mit Aspose.PSD für Java verarbeiten.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: PSD nach PNG exportieren – PSD‑Grafikobjekt erstellen – Unkomprimierter Stream
  in Java
url: /de/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD nach PNG exportieren – PSD‑Grafikobjekt erstellen – Unkomprimierter Stream in Java

## Einführung
Willkommen in der Welt der Bildbearbeitung mit Java! In diesem Tutorial **erstellen Sie ein PSD‑Grafikobjekt**, arbeiten mit unkomprimierten Bild‑Stream‑Objekten und lernen, wie Sie **PSD nach PNG exportieren** mit Aspose.PSD für Java. Egal, ob Sie ein Grafikdesigner sind, der seine Workflows automatisieren möchte, oder ein Softwareentwickler, der leistungsstarke Bildverarbeitungs‑Features in Ihre Anwendungen integrieren will – dieser Leitfaden ist genau für Sie zugeschnitten. Wir führen Sie Schritt für Schritt von den Voraussetzungen bis zum finalen Export und sorgen dafür, dass Sie den gesamten Prozess vollständig verstehen.

## Schnelle Antworten
- **Was bedeutet „PSD‑Grafikobjekt erstellen“?** Es bedeutet, einen Grafik‑Kontext für eine PSD‑Datei zu instanziieren, damit Sie deren Inhalt zeichnen oder bearbeiten können.  
- **Welche Bibliothek verarbeitet unkomprimierte Streams?** Aspose.PSD für Java bietet vollständige Unterstützung für Roh‑ (unkomprimierte) Bilddaten.  
- **Kann ich PSD nach PNG exportieren, nachdem ich es bearbeitet habe?** Ja – sobald Sie ein `Graphics`‑Objekt besitzen, können Sie das PSD rendern und als PNG speichern.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Ist der Export verlustfrei?** Der Export nach PNG bewahrt die Bildqualität, die Dateigröße ist größer als bei JPEG, aber kleiner als bei einer unkomprimierten PSD.  

## So exportieren Sie PSD nach PNG mit Aspose.PSD für Java
Wenn Sie **PSD nach PNG exportieren** möchten, sieht der typische Ablauf folgendermaßen aus:

1. Laden Sie die PSD‑Datei (oder erstellen Sie eine).  
2. Führen Sie Zeichnungen oder Ebenen‑Manipulationen mit einem `Graphics`‑Objekt durch.  
3. Speichern Sie das Ergebnis mit `PngOptions` (die gleiche `Graphics`‑Instanz kann wiederverwendet werden).  

Obwohl sich dieses Tutorial auf die Verarbeitung unkomprimierter Streams konzentriert, kann das von Ihnen erstellte `Graphics`‑Objekt später wiederverwendet werden, um das PSD in eine PNG‑Datei zu rendern.

## Voraussetzungen
Bevor wir zum Code springen, stellen wir sicher, dass Sie alles haben, was Sie für diese Reise benötigen. Hier sind die Voraussetzungen:

### Java Development Kit (JDK)
Stellen Sie sicher, dass JDK auf Ihrem Rechner installiert ist. Sie können es von der Oracle‑Website herunterladen oder OpenJDK verwenden.

### Aspose.PSD for Java
Laden Sie die Aspose.PSD‑Bibliothek herunter und installieren Sie sie. Diese leistungsstarke Bibliothek ermöglicht Ihnen die einfache Manipulation von PSD‑Dateien. Die neueste Version erhalten Sie über [diesen Link](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Es ist empfehlenswert, eine IDE zum Schreiben und Testen Ihres Java‑Codes zu nutzen. Sie können IntelliJ IDEA, Eclipse oder eine andere Ihrer Wahl verwenden.

### Basic Understanding of Java
Grundkenntnisse in Java erleichtern den Prozess. Stellen Sie sicher, dass Sie die Grundlagen wie Klassen, Methoden und Ausnahmebehandlung kennen.

Mit allem bereit, krempeln wir die Ärmel hoch und gehen zum spannenden Teil – dem Coden!

## Pakete importieren
Um loszulegen, müssen wir die notwendigen Pakete für die Arbeit mit Aspose.PSD importieren. Nachfolgend finden Sie die üblichen Imports, die Sie für die Verarbeitung von PSD‑Dateien benötigen.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Jetzt zerlegen wir den Code in leicht verdauliche Schritte, damit Sie problemlos folgen können. Wir richten das Projekt ein, laden eine PSD‑Datei, manipulieren sie und speichern das Ergebnis.

## Schritt 1: Definieren Sie Ihr Dokumentverzeichnis
Bevor Sie mit dem Coden beginnen, sollten Sie festlegen, wo Ihre PSD‑Datei liegt. Das ist im Grunde die Grundvoraussetzung für Ihr Projekt.

```java
String dataDir = "Your Document Directory";
```

Ersetzen Sie `"Your Document Directory"` durch den tatsächlichen Pfad, in dem sich Ihre PSD‑Datei (z. B. layers.psd) befindet. So finden Sie Ihre Dateien ohne Aufwand.

## Schritt 2: Erstellen Sie einen ByteArrayOutputStream
Sie benötigen einen Ort, um das modifizierte Bild zu speichern, bevor Sie etwas damit tun. Ein `ByteArrayOutputStream` hilft Ihnen, die Bilddaten einfach zu erfassen.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Diese Zeile initialisiert ein neues `ByteArrayOutputStream`‑Objekt namens `ms`. Sie verwenden dieses Objekt, um Ihr unkomprimiertes Bild zu speichern.

## Schritt 3: Laden Sie die PSD‑Datei
Jetzt ist es Zeit, die eigentliche PSD‑Datei zu laden. Hier beginnt die Magie!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Diese Zeile lädt Ihre PSD‑Datei in ein `PsdImage`‑Objekt. Stellen Sie sicher, dass der Pfad korrekt ist; sonst erscheint ein Fehler wie ein ungeprüftes Pop‑Quiz.

## Schritt 4: Richten Sie die PsdOptions zum Speichern ein
Sie müssen festlegen, wie das Bild gespeichert werden soll – natürlich unkomprimiert!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Hier erstellen Sie ein `PsdOptions`‑Objekt und setzen die Kompressionsmethode auf `Raw`. Diese Methode sorgt dafür, dass das Bild seine volle Qualität behält und ohne Kompression gespeichert wird.

## Schritt 5: Bild in den Ausgabestream speichern
```java
psdImage.save(ms, saveOptions);
```

Diese Zeile speichert Ihr modifiziertes Bild in den `ByteArrayOutputStream`, den Sie in Schritt 2 erstellt haben, unter Verwendung der in Schritt 4 definierten Optionen. Die `save`‑Methode übernimmt die korrekte Kodierung des Bildes basierend auf Ihren Einstellungen.

## Schritt 6: Ausgabestream zurücksetzen
Nach dem Speichern befindet sich Ihr Ausgabestream am Ende. Sie müssen ihn zurücksetzen, um wieder von Anfang an lesen zu können.

```java
ms.reset();
```

Die `reset`‑Methode bereitet Ihren `ByteArrayOutputStream` darauf vor, wieder von Anfang an gelesen zu werden. Denken Sie daran wie das Zurückspulen eines Kassettenrekorders, bevor Sie Ihren Lieblingssong hören!

## Schritt 7: Laden Sie das neu erstellte Bild
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Hier laden wir das Bild aus dem `ByteArrayOutputStream` in ein neues `PsdImage`‑Objekt. Jetzt können Sie die Ergebnisse Ihrer vorherigen Arbeit überprüfen.

## Schritt 8: Grafikobjekt erstellen
Um das Bild weiter zu modifizieren oder zu rendern, benötigen Sie ein Grafikobjekt.

```java
Graphics graphics = new Graphics(psdImage);
```

Diese Zeile initialisiert ein `Graphics`‑Objekt mit Ihrem `psdImage`. Sie können nun dieses Grafikobjekt verwenden, um das Bild nach Bedarf zu zeichnen oder zu manipulieren. Es ist, als hätten Sie einen Pinsel in der Hand!

## PSD‑Ebenen mit dem Grafikobjekt manipulieren
Jetzt, wo Sie eine **Graphics**‑Instanz besitzen, können Sie **PSD‑Ebenen manipulieren** – zum Beispiel Formen zeichnen, Text hinzufügen oder Filter auf eine bestimmte Ebene anwenden. Der Grafik‑Kontext arbeitet direkt auf den zugrunde liegenden Pixeldaten und gibt Ihnen feinkörnige Kontrolle über das Aussehen jeder Ebene.

## Häufige Probleme und Lösungen
- **NullPointerException beim Laden der Datei** – prüfen Sie den `dataDir`‑Pfad und stellen Sie sicher, dass der Dateiname korrekt ist.  
- **Komprimierte Ausgabe trotz Raw** – vergewissern Sie sich, dass `saveOptions.setCompressionMethod(CompressionMethod.Raw);` vor dem Aufruf von `save` gesetzt wird.  
- **Graphics‑Objekt erscheint leer** – stellen Sie sicher, dass Sie auf die richtige `PsdImage`‑Instanz zeichnen (verwenden Sie die geladene, nicht die neu erstellte, sofern nicht beabsichtigt).

## FAQ

### Was ist Aspose.PSD?
Aspose.PSD ist eine .NET‑Bibliothek, die Entwicklern ermöglicht, Photoshop‑PSD‑Dateien und zugehörige Bildformate programmgesteuert zu erstellen, zu bearbeiten und zu manipulieren.

### Wie kann ich Aspose.PSD für Java herunterladen?
Sie können es von der [Release‑Seite](https://releases.aspose.com/psd/java/) herunterladen.

### Gibt es eine kostenlose Testversion für Aspose.PSD?
Ja, Sie können eine kostenlose Testversion von [hier](https://releases.aspose.com/) erhalten.

### Kann ich Support für Aspose.PSD erhalten?
Absolut! Hilfe finden Sie im [Aspose‑Support‑Forum](https://forum.aspose.com/c/psd/34).

### Wie erhalte ich eine temporäre Lizenz für Aspose.PSD?
Besuchen Sie einfach die [Seite für temporäre Lizenzen](https://purchase.aspose.com/temporary-license/), um loszulegen.

## Häufig gestellte Fragen

**F: Kann ich das Grafikobjekt verwenden, um nur eine bestimmte Ebene zu bearbeiten?**  
A: Ja. Nachdem Sie das PSD geladen haben, wählen Sie die gewünschte Ebene über `psdImage.getLayers().get_Item(index)` aus und übergeben sie dem `Graphics`‑Konstruktor.

**F: Hat die Raw‑Kompressionsmethode Einfluss auf die Dateigröße?**  
A: Raw speichert Pixeldaten ohne Kompression, daher wird die Dateigröße größer sein als bei komprimierten PSDs, aber die Bildqualität bleibt unverändert.

**F: Ist es möglich, das bearbeitete PSD in ein anderes Format (z. B. PNG) zu exportieren?**  
A: Auf jeden Fall. Verwenden Sie nach der Bearbeitung die passende `Image.save`‑Überladung mit `PngOptions` – das ist der Standardweg, um **PSD nach PNG zu exportieren**.

**F: Welche Java‑Version wird benötigt?**  
A: Aspose.PSD für Java unterstützt JDK 8 und höher.

**F: Wie gebe ich Ressourcen nach der Verarbeitung frei?**  
A: Rufen Sie `psdImage.dispose()` auf und schließen Sie alle Streams, um native Ressourcen freizugeben.

---

**Zuletzt aktualisiert:** 2026-02-17  
**Getestet mit:** Aspose.PSD für Java (neueste Version)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}