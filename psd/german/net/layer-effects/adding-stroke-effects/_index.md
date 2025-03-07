---
title: Hinzufügen von Stricheffekten zu Ebenen in Aspose.PSD für .NET
linktitle: Stricheffekte zu Ebenen hinzufügen
second_title: Aspose.PSD .NET API
description: Verbessern Sie die Bildästhetik mit Aspose.PSD für .NET. Erfahren Sie Schritt für Schritt, wie Sie Stricheffekte hinzufügen. Jetzt herunterladen, kaufen oder die kostenlose Testversion ausprobieren.
weight: 10
url: /de/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hinzufügen von Stricheffekten zu Ebenen in Aspose.PSD für .NET

## Einführung

Willkommen zu diesem Schritt-für-Schritt-Tutorial zum Hinzufügen von Stricheffekten zu Ebenen in Aspose.PSD für .NET. Mit dem Stricheffekt ist es ein Kinderspiel, die visuelle Attraktivität Ihrer Bilder zu verbessern, und Aspose.PSD macht es für .NET-Entwickler nahtlos. In dieser Anleitung führen wir Sie durch den Prozess und bieten klare Schritte und Beispiele, die Ihnen helfen, diese leistungsstarke Funktion zu beherrschen.

## Voraussetzungen

Bevor wir mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.PSD für .NET: Laden Sie die Aspose.PSD-Bibliothek herunter und installieren Sie sie vom[Webseite](https://releases.aspose.com/psd/net/).

- Dokumentverzeichnis: Bereiten Sie ein Verzeichnis vor, das das PSD-Dokument enthält, auf das Sie Stricheffekte anwenden möchten.

- Ausgabeverzeichnis: Verwenden Sie ein separates Verzeichnis zum Speichern der Ausgabebilder mit Stricheffekten.

- Visual Studio: Stellen Sie sicher, dass Sie Visual Studio oder eine andere bevorzugte .NET-Entwicklungsumgebung eingerichtet haben.

## Namespaces importieren

Fügen Sie in Ihr .NET-Projekt die erforderlichen Namespaces ein, um die Aspose.PSD-Funktionalität zu nutzen:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Laden Sie das PSD-Dokument

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Ihr Code zum Laden des PSD-Dokuments kommt hier rein
}
```

## Schritt 2: Farbstricheffekt hinzufügen

```csharp
// Fügt Farbfüllung an der Position „Innen“ hinzu
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Schritt 3: Außenposition

```csharp
// Fügt Farbfüllung an der Position „Außen“ hinzu
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Schritt 4: Mittelposition

```csharp
// Fügt Farbfüllung an der Position „Mitte“ hinzu
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Wiederholen Sie ähnliche Schritte für Farbverlaufs- und Musterfüllungen und passen Sie die Einstellungen entsprechend an.

## Abschluss

Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.PSD für .NET Stricheffekte zu Ebenen hinzufügen. Experimentieren Sie mit verschiedenen Einstellungen, um die gewünschte visuelle Wirkung in Ihren Bildern zu erzielen.

## Häufig gestellte Fragen

### F1: Kann ich Stricheffekte nur auf bestimmte Ebenen anwenden?

A1: Ja, Sie können bestimmte Ebenen ansprechen, indem Sie den Ebenenindex im Code anpassen.

### F2: Ist Aspose.PSD mit dem neuesten .NET-Framework kompatibel?

A2: Auf jeden Fall! Aspose.PSD ist für die nahtlose Integration mit den neuesten .NET-Frameworks konzipiert.

### F3: Wie kann ich die Strichfarbe anpassen?

 A3: Ändern Sie einfach die`Color` -Eigenschaft im Code, um die gewünschte Strichfarbe zu erzielen.

### F4: Unterstützt Aspose.PSD die Stapelverarbeitung für mehrere PSD-Dateien?

A4: Ja, Sie können mehrere PSD-Dateien durchlaufen und den Stricheffekt mit einem ähnlichen Ansatz anwenden.

### F5: Kann ich die Testversion verwenden, bevor ich Aspose.PSD kaufe?

 A5: Natürlich! Schnapp dir die[Kostenlose Testversion](https://releases.aspose.com/) um die Funktionen von Aspose.PSD zu erkunden, bevor Sie einen Kauf tätigen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
