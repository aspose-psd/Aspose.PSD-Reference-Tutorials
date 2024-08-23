---
title: Unterstützen Sie Grenzinformationsressourcen in PSD – Java
linktitle: Unterstützen Sie Grenzinformationsressourcen in PSD – Java
second_title: Aspose.PSD Java API
description: Meistern Sie die Randbearbeitung in PSD-Dateien mit Aspose.PSD für Java. Lernen Sie, Randbreite, Einheiten und mehr in leicht verständlichen Schritten zu ändern. Verbessern Sie Ihre PSD-Designs programmgesteuert.
type: docs
weight: 23
url: /de/java/psd-layer-management-effects/support-border-information-resource-psd/
---
## Einführung

Hatten Sie schon einmal das Bedürfnis, diese lästigen Ränder in Ihren PSD-Dateien programmgesteuert zu optimieren? Nun, keine Sorge mehr! Aspose.PSD für Java kommt zur Rettung und bietet eine leistungsstarke und benutzerfreundliche Möglichkeit, Randinformationsressourcen in Ihren PSD-Dateien zu bearbeiten. Diese umfassende Anleitung führt Sie Schritt für Schritt durch den Prozess und ermöglicht Ihnen, Ihre Ränder wie nie zuvor zu kontrollieren.

## Voraussetzungen:

Stellen Sie vor dem Eintauchen sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Java Development Kit (JDK): Sie müssen eine kompatible JDK-Version auf Ihrem System installiert haben. Spezifische Anforderungen finden Sie in der Dokumentation zu Aspose.PSD für Java. ([https://docs.aspose.com/psd/java/](https://docs.aspose.com/psd/java/))

2. Aspose.PSD für Java-Bibliothek: Laden Sie die Aspose.PSD für Java-Bibliothek von der Website herunter. ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)) Sie können sich je nach Bedarf für eine kostenlose Testversion entscheiden oder eine Lizenz erwerben.

3. Eine PSD-Datei mit Rändern: Suchen Sie eine PSD-Datei, die eine Randinformationsressource enthält. Dies kann eine vorgefertigte Vorlage, ein Bild mit Rändern oder irgendetwas mit einem Rand sein, das Sie ändern möchten.

## Pakete importieren

Sobald Sie die Voraussetzungen erfüllt haben, können wir die Bühne für unsere magische Randmanipulation bereiten. So importieren Sie die erforderlichen Pakete:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.ResourceBlock;
import com.aspose.psd.fileformats.psd.resources.BorderInformationResource;
import com.aspose.psd.fileformats.psd.resources.resolutionenums.PhysicalUnit;
```

Wir importieren wichtige Klassen aus der Aspose.PSD-Bibliothek für Java:

- `Image`: Diese Klasse bietet die Grundlage zum Laden und Bearbeiten von PSD-Bildern.
- `PsdImage`: Diese Klasse stellt das eigentliche PSD-Bildobjekt dar, mit dem wir arbeiten werden.
- `ResourceBlock`: Dies ist die Basisklasse für verschiedene Ressourcen, die in eine PSD-Datei eingebettet sind, einschließlich Ränder.
- `PhysicalUnit`: Mit dieser Klasse können wir Einheiten für Rahmenmaße angeben (z. B. Zoll, Pixel).
- `BorderInformationResource`: Das ist der Star der Show! Es ermöglicht uns, auf Informationen zuzugreifen und diese zu ändern, die für Ränder in der PSD-Datei spezifisch sind.

Nachdem wir nun die Importe geklärt haben, begeben wir uns auf eine schrittweise Reise der Grenzmanipulation:

## Schritt 1: Dateipfade definieren

Legen Sie zunächst die Speicherorte Ihrer Quell- und Ausgabe-PSD-Dateien fest. Ersetzen Sie einfach die Platzhalter durch Ihre tatsächlichen Dateipfade:

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
```

Stellen Sie sich das Quellverzeichnis als den Speicherort Ihrer ursprünglichen PSD-Datei mit den Rändern vor, die Sie anpassen möchten. Das Ausgabeverzeichnis enthält die geänderte PSD-Datei, nachdem wir unsere Änderungen angewendet haben.

## Schritt 2: Laden Sie das PSD-Bild

Es ist Zeit, die PSD-Datei mit den Randinformationen zu laden. So geht's:

```java
String inPsdFilePath = sourceDir + "/SupportBorderInformationResource.psd";
String outPsdFilePath = outputDir + "/SupportBorderInformationResource_output.psd";

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

 Wir erstellen Zeichenfolgen für die Eingabe- und Ausgabedateipfade basierend auf den zuvor definierten Verzeichnissen und dem spezifischen PSD-Dateinamen. Dann verwenden wir die`Image.load()` Methode zum Laden des PSD-Bildes und zum Konvertieren in eine`PsdImage` Objekt zur weiteren Manipulation.

## Schritt 3: Zugriff auf die Grenzinformationsressource

Jetzt kommt der spannende Teil – der Zugriff auf die Grenzinformationsressource! So finden Sie sie im geladenen PSD-Bild:

```java
ResourceBlock[] imageResources = psdImage.getImageResources();

BorderInformationResource borderInfoResource = null;
for (ResourceBlock imageResource : imageResources) {
  if (imageResource instanceof BorderInformationResource) {
    borderInfoResource = (BorderInformationResource) imageResource;
    break;
  }
}
```

Wir erhalten zunächst ein Array aller Bildressourcen innerhalb der PSD-Datei mithilfe der`psdImage.getImageResources()` Methode. Dann iterieren wir durch dieses Array, um die spezifische`BorderInformationResource` . Der`instanceof` Operator prüft, ob die aktuelle Ressource tatsächlich eine Randinformationsressource ist. Wenn eine Übereinstimmung gefunden wird, speichern wir sie im`borderInfoResource` variabel, bereit zur Änderung.

## Schritt 4: Rahmeneigenschaften ändern

Mit der uns zur Verfügung stehenden Rahmeninformationsressource können wir endlich ihre Eigenschaften optimieren! So passen Sie die Breite des Rahmens an:

```java
if (borderInfoResource != null) {
    borderInfoResource.setWidth(0.1);
    borderInfoResource.setUnit(PhysicalUnit.Inches);
}
```

## Schritt 5: Speichern der geänderten PSD

Nachdem wir nun unsere Änderungen vorgenommen haben, ist es an der Zeit, die geänderte PSD-Datei zu speichern:

```java
try {
    psdImage.save(outPsdFilePath);
} finally {
    psdImage.dispose();
}
```

-  Speichern des Bildes: Wir verwenden die`psdImage.save()` Methode, um das geänderte PSD-Bild im angegebenen Ausgabedateipfad zu speichern.
-  Entsorgung von Ressourcen: Es ist wichtig, die`psdImage` Objekt mit dem`dispose()` Methode, um Systemressourcen freizugeben. Dies geschieht in einem`finally` -Block, um sicherzustellen, dass dies auch dann geschieht, wenn eine Ausnahme auftritt.

## Abschluss

Aspose.PSD für Java hat sich als leistungsstarkes Tool zur mühelosen Bearbeitung von Rahmeninformationen in PSD-Dateien erwiesen. Wenn Sie die in diesem Handbuch beschriebenen Schritte befolgen, können Sie Rahmeneigenschaften wie Breite und Einheiten präzise ändern. Denken Sie daran, dies ist nur die Spitze des Eisbergs. Aspose.PSD bietet eine Vielzahl von Funktionen für die Arbeit mit PSD-Bildern. Zögern Sie also nicht, die Dokumentation nach weiteren Verbesserungen zu durchsuchen. Lassen Sie Ihrer Kreativität freien Lauf und erstellen Sie atemberaubende Grafiken mit programmgesteuerter Kontrolle über Ihre Ränder! 

## Häufig gestellte Fragen

### Kann ich außer der Breite auch andere Rahmeneigenschaften ändern?

 Absolut! Die`BorderInformationResource` Die Klasse bietet verschiedene Eigenschaften zur Steuerung verschiedener Aspekte von Rahmen, wie Farbe, Stil und mehr. Eine vollständige Liste der verfügbaren Eigenschaften finden Sie in der Aspose.PSD-Dokumentation.

### Welche anderen Ressourcentypen kann ich in einer PSD-Datei bearbeiten?

Aspose.PSD unterstützt die Arbeit mit einer Vielzahl von Bildressourcen über Grenzen hinweg. Sie können mit den entsprechenden Klassen und Methoden auf Ebenen, Kanäle, Farbprofile und andere Elemente in einer PSD-Datei zugreifen und diese ändern.

### Kann ich neue Informationsressourcen zu Grenzen erstellen?

 Während sich das aktuelle Beispiel auf die Änderung vorhandener Grenzen konzentriert, können Sie mit Aspose.PSD auch neue Ressourcen für Randinformationen von Grund auf erstellen. Sie können eine`BorderInformationResource` Objekt und fügen Sie es der Ressourcensammlung des PSD-Bildes hinzu.

### Gibt es beim Arbeiten mit großen PSD-Dateien Leistungsaspekte?

Aspose.PSD ist auf Leistung optimiert, aber die Verarbeitung großer PSD-Dateien kann zusätzliche Aufmerksamkeit erfordern. Erwägen Sie Techniken wie das Laden von Bildern in Blöcken oder die Verwendung asynchroner Vorgänge, um die Verarbeitungszeit zu verbessern.

### Wo finde ich weitere Informationen und Unterstützung?

Die Aspose.PSD-Dokumentation für Java ist eine hervorragende Quelle für ausführliche Informationen zur API und ihren Funktionen. Sie können auch die Aspose-Foren besuchen, um Hilfe zu erhalten und mit anderen Entwicklern zu interagieren. 