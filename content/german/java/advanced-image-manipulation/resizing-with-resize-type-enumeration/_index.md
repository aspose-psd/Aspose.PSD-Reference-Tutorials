---
title: Größenänderung mit Resize Type Enumeration in Aspose.PSD für Java
linktitle: Größenänderung mit Resize Type Enumeration
second_title: Aspose.PSD Java-API
description: Master-Bildgrößenänderung in Java mit Aspose.PSD. Schritt-für-Schritt-Anleitung zur Verwendung der Größenaufzählung.
type: docs
weight: 18
url: /de/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## Einführung

In der sich ständig weiterentwickelnden Landschaft der Java-Entwicklung ist eine effiziente Bildverarbeitung ein entscheidender Aspekt, mit dem sich Entwickler häufig auseinandersetzen. Aspose.PSD für Java erweist sich als leistungsstarke Lösung, die ein nahtloses Erlebnis bei der Größenänderung von Bildern mit dem zusätzlichen Vorteil der Resize Type Enumeration bietet. In diesem Tutorial befassen wir uns mit den Feinheiten der Größenänderung von Bildern mit Aspose.PSD für Java und schlüsseln jeden Schritt auf, um ein umfassendes Verständnis zu gewährleisten.

## Voraussetzungen

Bevor Sie mit diesem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine Java-Entwicklungsumgebung eingerichtet ist.

2. Aspose.PSD-Bibliothek: Laden Sie die Aspose.PSD-Bibliothek von herunter und installieren Sie sie[Webseite](https://releases.aspose.com/psd/java/).

3.  Beispiel-PSD-Datei: Halten Sie eine Beispiel-PSD-Datei zum Experimentieren bereit. Du kannst den ... benutzen[„sample.psd“ (Ihr Dokumentverzeichnis/sample.psd) für dieses Tutorial.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Schritt 1: Laden Sie das Bild

 Laden Sie zunächst ein vorhandenes Bild in eine Instanz von`RasterImage` Klasse. Verwenden Sie den folgenden Codeausschnitt:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
Image image = Image.load(sourceFile);
```

## Schritt 2: Ändern Sie die Größe des Bildes

Ändern Sie nun die Größe des geladenen Bildes mithilfe der Resize Type Enumeration. In diesem Beispiel verwenden wir die Lanczos-Resample-Methode:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Schritt 3: Speichern Sie das in der Größe geänderte Bild

Speichern Sie das Bild nach der Größenänderung mit den angegebenen Abmessungen und dem gewählten Größenänderungstyp. Hier speichern wir es als JPEG-Datei:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

Und da haben Sie es! Sie haben die Größe eines Bildes mithilfe der Resize Type Enumeration in Aspose.PSD für Java erfolgreich geändert.

Zusammenfassend lässt sich sagen, dass Aspose.PSD für Java eine robuste Plattform für die Bildbearbeitung bietet und die Resize Type Enumeration diesem Prozess eine zusätzliche Ebene an Flexibilität verleiht. Egal, ob Sie an einem kleinen Projekt oder einer großen Anwendung arbeiten: Wenn Sie diese Schritte beherrschen, können Sie die Bildgröße nahtlos ändern.

## FAQs

### F1: Ist Aspose.PSD für Java sowohl für kleine als auch für große Projekte geeignet?

A1: Auf jeden Fall! Aspose.PSD für Java ist für Projekte jeder Größe konzipiert und bietet Skalierbarkeit und Effizienz.

### F2: Kann ich einen anderen Größenänderungstyp als Lanczos Resample verwenden?

A2: Ja, Aspose.PSD für Java bietet verschiedene Größenänderungstypen, wie „Nearest Neighbour“, „Bikubisch“ und mehr. Eine umfassende Liste finden Sie in der Dokumentation.

### F3: Wo finde ich zusätzliche Unterstützung für Aspose.PSD für Java?

 A3: Bei Fragen oder Hilfe besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34).

### F4: Gibt es eine kostenlose Testversion für Aspose.PSD für Java?

 A4: Ja, Sie können auf eine kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F5: Wie kann ich eine temporäre Lizenz für Aspose.PSD für Java erhalten?

 A5: Um eine temporäre Lizenz zu erhalten, besuchen Sie[dieser Link](https://purchase.aspose.com/temporary-license/).