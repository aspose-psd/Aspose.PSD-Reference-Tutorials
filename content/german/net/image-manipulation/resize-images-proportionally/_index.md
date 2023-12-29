---
title: Proportionale Größenänderung von Bildern in Aspose.PSD für .NET
linktitle: Proportionale Größenänderung von Bildern
second_title: Aspose.PSD .NET-API
description: Entdecken Sie die nahtlose Größenänderung von Bildern mit Aspose.PSD für .NET. Laden Sie die Bibliothek herunter, folgen Sie unserem Tutorial und erweitern Sie Ihre Bildverarbeitungsfunktionen.
type: docs
weight: 14
url: /de/net/image-manipulation/resize-images-proportionally/
---
Im Bereich der Bildbearbeitung sticht Aspose.PSD für .NET als leistungsstarkes Toolkit hervor, das Entwicklern die Möglichkeit bietet, die Größe von Bildern problemlos proportional zu ändern. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess der Größenänderung von Bildern mit Aspose.PSD für .NET und stellen so sicher, dass Ihre Bilder ihre Proportionen einwandfrei beibehalten.

## Einführung

Die proportionale Größenänderung von Bildern ist in vielen Anwendungen eine häufige Aufgabe, und Aspose.PSD für .NET vereinfacht diesen Prozess für Entwickler. Unabhängig davon, ob Sie an einer Webanwendung, einer Desktop-Software oder einer mobilen App arbeiten, ist es für die Aufrechterhaltung der visuellen Attraktivität und Konsistenz von entscheidender Bedeutung, zu wissen, wie man die Größe von Bildern ändert und gleichzeitig ihr Seitenverhältnis beibehält.

## Voraussetzungen

Bevor Sie mit Aspose.PSD für .NET in die Magie der Größenänderung eintauchen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.PSD für .NET-Bibliothek installiert haben. Sie können es hier herunterladen[Aspose.PSD für .NET-Versionen](https://releases.aspose.com/psd/net/) Seite.

2. Dokumentenverzeichnis: Erstellen Sie ein Verzeichnis zum Speichern Ihrer Dokumente und ersetzen Sie „Ihr Dokumentenverzeichnis“ im bereitgestellten Code durch den tatsächlichen Pfad zu diesem Verzeichnis.

Nachdem Sie nun die Voraussetzungen geschaffen haben, beginnen wir mit der Schritt-für-Schritt-Anleitung.

## Namespaces importieren

```csharp
using Aspose.PSD.ImageOptions;
```

Importieren Sie die erforderlichen Namespaces, um auf die erforderlichen Klassen und Methoden zuzugreifen.

## Schritt 1: Laden Sie das Bild

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Die restlichen Schritte gehen hierher
}
```

 Laden Sie das Quellbild mit`Image.Load` Methode.

## Schritt 2: Breite und Höhe angeben

```csharp
// Breite und Höhe angeben
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Bestimmen Sie die neue Breite und Höhe für das in der Größe geänderte Bild. In diesem Beispiel werden Breite und Höhe halbiert, Sie können diese Werte jedoch entsprechend Ihren Anforderungen anpassen.

## Schritt 3: Speichern Sie das in der Größe geänderte Bild

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Speichern Sie das verkleinerte Bild mit`Save` Methode mit angegebenen Optionen. In diesem Fall speichern wir es als PNG-Datei.

## Abschluss

Die proportionale Größenänderung von Bildern in Aspose.PSD für .NET ist ein unkomplizierter Prozess, der Ihren Bildverarbeitungsworkflow aufwertet. Dieser Leitfaden vermittelt Ihnen das Wissen, diese Funktionalität nahtlos in Ihre Anwendungen zu integrieren.

## FAQs

### F1: Kann ich die Größe von Bildern auf bestimmte Abmessungen ändern?

A1: Ja, Sie können die neue Breite und Höhe entsprechend Ihren Anforderungen im Code anpassen.

### F2: Ist Aspose.PSD für .NET für die Größenänderung von Batch-Bildern geeignet?

A2: Auf jeden Fall! Sie können diese Schritte in eine Schleife zur Stapelverarbeitung mehrerer Bilder integrieren.

### F3: Gibt es in Aspose.PSD für .NET weitere Bildbearbeitungsfunktionen?

A3: Ja, Aspose.PSD für .NET bietet eine Vielzahl von Funktionen, einschließlich Zuschneiden, Drehen und Anwenden von Filtern auf Bilder.

### F4: Gibt es eine kostenlose Testversion für Aspose.PSD für .NET?

 A4: Ja, Sie können die Funktionen von Aspose.PSD für .NET mit einer kostenlosen Testversion erkunden. Besuchen[Hier](https://releases.aspose.com/) um loszulegen.

### F5: Wo finde ich Unterstützung für Aspose.PSD für .NET?

 A5: Besuchen Sie die[Aspose.PSD für .NET-Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.