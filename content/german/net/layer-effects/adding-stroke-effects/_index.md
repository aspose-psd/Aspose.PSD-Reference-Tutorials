---
title: Hinzufügen von Stricheffekten zu Ebenen in Aspose.PSD für .NET
linktitle: Hinzufügen von Stricheffekten zu Ebenen
second_title: Aspose.PSD .NET-API
description: Verbessern Sie die Bildästhetik mit Aspose.PSD für .NET. Erfahren Sie Schritt für Schritt, wie Sie Stricheffekte hinzufügen. Laden Sie die kostenlose Testversion jetzt herunter, kaufen Sie sie oder testen Sie sie.
type: docs
weight: 10
url: /de/net/layer-effects/adding-stroke-effects/
---
## Einführung

Willkommen zu dieser Schritt-für-Schritt-Anleitung zum Hinzufügen von Stricheffekten zu Ebenen in Aspose.PSD für .NET. Mit dem Stricheffekt ist es ein Kinderspiel, die visuelle Attraktivität Ihrer Bilder zu verbessern, und Aspose.PSD macht es für .NET-Entwickler nahtlos. In diesem Leitfaden führen wir Sie durch den Prozess und stellen klare Schritte und Beispiele bereit, die Ihnen helfen, diese leistungsstarke Funktion zu beherrschen.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET: Laden Sie die Aspose.PSD-Bibliothek von herunter und installieren Sie sie[Webseite](https://releases.aspose.com/psd/net/).

- Dokumentverzeichnis: Bereiten Sie ein Verzeichnis mit dem PSD-Dokument vor, auf das Sie Stricheffekte anwenden möchten.

- Ausgabeverzeichnis: Es gibt ein separates Verzeichnis zum Speichern der Ausgabebilder mit Stricheffekten.

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
    // Hier finden Sie Ihren Code zum Laden des PSD-Dokuments
}
```

## Schritt 2: Farbstricheffekt hinzufügen

```csharp
// Fügt eine Farbfüllung an der Position „Innen“ hinzu
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Schritt 3: Außenposition

```csharp
// Fügt eine Farbfüllung an der Position „Außen“ hinzu
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Schritt 4: Mittelposition

```csharp
// Fügt eine Farbfüllung an der Position Mitte hinzu
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Wiederholen Sie ähnliche Schritte für Verlaufs- und Musterfüllungen und passen Sie die Einstellungen entsprechend an.

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.PSD für .NET Stricheffekte zu Ebenen hinzufügen. Experimentieren Sie mit verschiedenen Einstellungen, um die gewünschte visuelle Wirkung in Ihren Bildern zu erzielen.

## FAQs

### F1: Kann ich Stricheffekte nur auf bestimmte Ebenen anwenden?

A1: Ja, Sie können auf bestimmte Ebenen abzielen, indem Sie den Ebenenindex im Code anpassen.

### F2: Ist Aspose.PSD mit dem neuesten .NET Framework kompatibel?

A2: Auf jeden Fall! Aspose.PSD ist für die nahtlose Integration in die neuesten .NET-Frameworks konzipiert.

### F3: Wie kann ich die Strichfarbe anpassen?

 A3: Ändern Sie einfach die`Color` Eigenschaft im Code, um die gewünschte Strichfarbe zu erreichen.

### F4: Unterstützt Aspose.PSD die Stapelverarbeitung für mehrere PSD-Dateien?

A4: Ja, Sie können mehrere PSD-Dateien durchlaufen und den Stricheffekt mit einem ähnlichen Ansatz anwenden.

### F5: Kann ich die Testversion verwenden, bevor ich Aspose.PSD kaufe?

 A5: Auf jeden Fall! Packe die[Kostenlose Testphase](https://releases.aspose.com/) um die Möglichkeiten von Aspose.PSD zu erkunden, bevor Sie einen Kauf tätigen.