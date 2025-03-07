---
title: Zuschneiden von Bildern durch Verschiebungen in Aspose.PSD für .NET
linktitle: Zuschneiden von Bildern durch Verschiebungen
second_title: Aspose.PSD .NET API
description: Lernen Sie, Bilder mühelos mit Aspose.PSD für .NET zuzuschneiden. Folgen Sie unserer Schritt-für-Schritt-Anleitung für präzise Bildanpassungen.
weight: 12
url: /de/net/image-manipulation/crop-image-shifts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zuschneiden von Bildern durch Verschiebungen in Aspose.PSD für .NET

## Einführung

Im Bereich der .NET-Entwicklung sticht Aspose.PSD als leistungsstarkes Toolkit für Bildverarbeitungsaufgaben hervor. Eine seiner bemerkenswerten Funktionen ist die Möglichkeit, Bilder dank der Funktion „Zuschneiden durch Verschiebungen“ präzise zuzuschneiden. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess des nahtlosen Zuschneidens von Bildern mit Aspose.PSD für .NET.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Bibliothek installiert haben. Wenn nicht, können Sie sie von der[Veröffentlichungsseite](https://releases.aspose.com/psd/net/).

- .NET-Umgebung: Stellen Sie sicher, dass auf Ihrem Computer eine .NET-Entwicklungsumgebung eingerichtet ist.

- Beispielbild: Bereiten Sie ein Beispielbild im PSD-Format vor, mit dem Sie arbeiten möchten.

## Namespaces importieren

Importieren Sie zunächst die erforderlichen Namespaces in Ihr .NET-Projekt. Diese Namespaces bieten Zugriff auf die Aspose.PSD-Klassen und -Methoden, die zum Zuschneiden von Bildern erforderlich sind.

```csharp
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Definieren Sie Ihr Dokumentverzeichnis

Legen Sie den Pfad zu Ihrem Dokumentverzeichnis fest, in dem die Quell- und Zieldateien gespeichert werden.

```csharp
string dataDir = "Your Document Directory";
```

## Schritt 2: Laden Sie das Quellbild

Laden Sie das PSD-Bild, das Sie zuschneiden möchten. Ersetzen Sie unbedingt „sample.psd“ durch den Namen Ihrer Quelldatei.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Schritt 3: Bilddaten zwischenspeichern für bessere Leistung

Vor dem Zuschneiden empfiehlt es sich, die Bilddaten zur Leistungsverbesserung zwischenzuspeichern.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Schritt 4: Verschiebungswerte für das Zuschneiden festlegen

Geben Sie die Verschiebungswerte für die linke, rechte, obere und untere Seite des Bildes an. Passen Sie diese Werte Ihren Zuschneideanforderungen entsprechend an.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Schritt 5: Zuschneiden anwenden und Ergebnisse speichern

 Nutzen Sie die`Crop` Methode, um die angegebenen Verschiebungen anzuwenden und das zugeschnittene Bild in der Zieldatei zu speichern.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Abschluss

Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, wie Sie Bilder mit Aspose.PSD für .NET durch Verschiebungen zuschneiden. Diese leistungsstarke Funktion bietet Ihnen die Präzision und Kontrolle, die Sie für verschiedene Bildverarbeitungsaufgaben benötigen.

## Häufig gestellte Fragen

### F1: Kann ich Bilder verschiedener Formate zuschneiden, nicht nur PSD?

A1: Ja, Aspose.PSD unterstützt verschiedene Bildformate, sodass Sie Bilder in Formaten wie JPEG, PNG und mehr zuschneiden können.

### F2: Gibt es vor dem Kauf von Aspose.PSD für .NET eine Testversion?

 A2: Natürlich! Sie können das Toolkit mit einer kostenlosen Testversion erkunden.[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD für .NET?

 A3: Sie können zu Testzwecken eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).

### F4: Wo finde ich zusätzliche Unterstützung und Diskussionen zu Aspose.PSD?

 A4: Besuchen Sie die[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) für die Unterstützung und anregenden Diskussionen.

### F5: Kann ich Aspose.PSD für .NET direkt von der Website kaufen?

 A5: Ja, Sie können die Bibliothek sicher erwerben bei[Kaufseite](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
