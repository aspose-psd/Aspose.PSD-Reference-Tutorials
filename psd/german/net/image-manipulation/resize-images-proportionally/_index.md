---
title: Proportionale Größenanpassung von Bildern in Aspose.PSD für .NET
linktitle: Proportionale Größenanpassung von Bildern
second_title: Aspose.PSD .NET API
description: Entdecken Sie die nahtlose Größenanpassung von Bildern mit Aspose.PSD für .NET. Laden Sie die Bibliothek herunter, folgen Sie unserem Tutorial und verbessern Sie Ihre Bildverarbeitungsfunktionen.
weight: 14
url: /de/net/image-manipulation/resize-images-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Proportionale Größenanpassung von Bildern in Aspose.PSD für .NET

Im Bereich der Bildbearbeitung sticht Aspose.PSD für .NET als leistungsstarkes Toolkit hervor, das Entwicklern die Möglichkeit bietet, Bilder problemlos proportional zu skalieren. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess der Größenänderung von Bildern mit Aspose.PSD für .NET und stellen sicher, dass Ihre Bilder ihre Proportionen einwandfrei beibehalten.

## Einführung

Die proportionale Größenanpassung von Bildern ist in vielen Anwendungen eine gängige Aufgabe, und Aspose.PSD für .NET vereinfacht diesen Vorgang für Entwickler. Egal, ob Sie an einer Webanwendung, Desktop-Software oder mobilen App arbeiten: Um die visuelle Attraktivität und Konsistenz zu wahren, ist es entscheidend, zu wissen, wie Sie die Größe von Bildern unter Beibehaltung ihres Seitenverhältnisses anpassen.

## Voraussetzungen

Bevor Sie sich in die Größenänderungsmagie mit Aspose.PSD für .NET stürzen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.PSD für .NET-Bibliothek installiert haben. Sie können sie von der[Aspose.PSD für .NET-Versionen](https://releases.aspose.com/psd/net/) Seite.

2. Dokumentverzeichnis: Erstellen Sie ein Verzeichnis zum Speichern Ihrer Dokumente und ersetzen Sie „Ihr Dokumentverzeichnis“ im bereitgestellten Code durch den tatsächlichen Pfad zu diesem Verzeichnis.

Nachdem Sie nun die Voraussetzungen geschaffen haben, können wir mit der Schritt-für-Schritt-Anleitung beginnen.

## Namespaces importieren

```csharp
using Aspose.PSD.ImageOptions;
```

Importieren Sie die erforderlichen Namespaces, um auf die erforderlichen Klassen und Methoden zuzugreifen.

## Schritt 1: Laden Sie das Bild

```csharp
// Der Pfad zum Dokumentverzeichnis.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Die restlichen Schritte finden Sie hier
}
```

 Laden Sie das Quellbild mit dem`Image.Load` Verfahren.

## Schritt 2: Breite und Höhe festlegen

```csharp
// Breite und Höhe festlegen
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Bestimmen Sie die neue Breite und Höhe für das skalierte Bild. In diesem Beispiel werden Breite und Höhe halbiert, Sie können diese Werte jedoch Ihren Anforderungen entsprechend anpassen.

## Schritt 3: Speichern Sie das skalierte Bild

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Speichern Sie das skalierte Bild mit dem`Save` Methode mit angegebenen Optionen. In diesem Fall speichern wir es als PNG-Datei.

## Abschluss

Die proportionale Größenanpassung von Bildern in Aspose.PSD für .NET ist ein unkomplizierter Vorgang, der Ihren Bildverarbeitungs-Workflow aufwertet. Dieser Leitfaden hat Ihnen das Wissen vermittelt, diese Funktionalität nahtlos in Ihre Anwendungen zu integrieren.

## Häufig gestellte Fragen

### F1: Kann ich die Größe von Bildern auf bestimmte Abmessungen ändern?

A1: Ja, Sie können die neue Breite und Höhe im Code Ihren Anforderungen entsprechend anpassen.

### F2: Ist Aspose.PSD für .NET für die Stapelgrößenänderung von Bildern geeignet?

A2: Absolut! Sie können diese Schritte in eine Schleife zur Stapelverarbeitung mehrerer Bilder integrieren.

### F3: Gibt es in Aspose.PSD für .NET andere Bildbearbeitungsfunktionen?

A3: Ja, Aspose.PSD für .NET bietet eine breite Palette an Funktionen, darunter Zuschneiden, Drehen und Anwenden von Filtern auf Bilder.

### F4: Gibt es eine kostenlose Testversion für Aspose.PSD für .NET?

 A4: Ja, Sie können die Funktionen von Aspose.PSD für .NET mit einer kostenlosen Testversion erkunden. Besuchen Sie[Hier](https://releases.aspose.com/) um loszulegen.

### F5: Wo finde ich Unterstützung für Aspose.PSD für .NET?

 A5: Besuchen Sie die[Aspose.PSD für .NET-Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
