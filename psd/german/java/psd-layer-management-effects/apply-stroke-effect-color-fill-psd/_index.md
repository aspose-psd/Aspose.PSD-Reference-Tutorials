---
title: Stricheffekt mit Farbfüllung in PSD anwenden – Java
linktitle: Stricheffekt mit Farbfüllung in PSD anwenden – Java
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java einen Stricheffekt mit Farbfüllung auf Ihre PSD-Dateien anwenden. Folgen Sie dieser Schritt-für-Schritt-Anleitung, um Ihre Bilder mühelos zu verbessern.
weight: 21
url: /de/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stricheffekt mit Farbfüllung in PSD anwenden – Java

## Einführung

In dieser Anleitung führen wir Sie durch den Prozess zum Anwenden eines Stricheffekts mit Farbfüllung auf Ihre PSD-Dateien mit Aspose.PSD für Java. Egal, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, dieses Schritt-für-Schritt-Tutorial wird Ihnen die Arbeit leicht machen. Wir behandeln alles, vom Einrichten Ihrer Umgebung bis zum Speichern des endgültigen Bilds mit den angewendeten Effekten.

## Voraussetzungen

Bevor wir beginnen, stellen wir sicher, dass Sie alles haben, was Sie brauchen, um diesem Tutorial folgen zu können:

1. Java Development Kit (JDK) installiert: Stellen Sie sicher, dass JDK 8 oder höher auf Ihrem System installiert ist.
2.  Aspose.PSD für Java-Bibliothek: Sie benötigen die Aspose.PSD für Java-Bibliothek. Sie können sie herunterladen von der[Webseite](https://releases.aspose.com/psd/java/).
3. Integrierte Entwicklungsumgebung (IDE): Eine IDE wie IntelliJ IDEA, Eclipse oder eine andere Ihrer Wahl.
4. Beispiel-PSD-Datei: Eine Beispiel-PSD-Datei, auf die Sie den Stricheffekt anwenden können. Wenn Sie keine haben, können Sie eine einfache PSD-Datei in Photoshop erstellen oder eine aus dem Internet herunterladen.
5. Grundlegende Kenntnisse in Java: Obwohl dieses Tutorial anfängerfreundlich ist, sind einige grundlegende Kenntnisse in Java von Vorteil.

Sobald diese Voraussetzungen erfüllt sind, können Sie mit der Anwendung des Stricheffekts mit Farbfüllung auf Ihre PSD-Dateien beginnen.

## Pakete importieren

Um mit Aspose.PSD für Java arbeiten zu können, müssen Sie die erforderlichen Pakete in Ihr Java-Projekt importieren. So können Sie das tun:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Diese Importe bringen alle notwendigen Klassen mit, die Sie zum Arbeiten mit PSD-Dateien, Anwenden von Effekten und Speichern der Bilder im gewünschten Format benötigen.

## Schritt 1: Laden Sie die PSD-Datei

 Der erste Schritt in unserem Prozess ist das Laden der PSD-Datei, die Sie ändern möchten. Aspose.PSD für Java macht dies unglaublich einfach mit seinem`PsdImage` Klasse. So können Sie es machen:

### 1.1 Verzeichnispfad festlegen

Definieren Sie zunächst den Verzeichnispfad, in dem Ihre PSD-Dateien gespeichert sind:

```java
String dataDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` durch den tatsächlichen Pfad, in dem sich Ihre PSD-Datei befindet.

### 1.2 Laden Sie das PSD-Bild

 Laden Sie nun die PSD-Datei mit dem`PsdLoadOptions` Und`PsdImage` Klassen:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

 Hier die`PsdLoadOptions`ist so konfiguriert, dass die Effektressourcen geladen werden. Dadurch wird sichergestellt, dass auf alle vorhandenen Effekte im PSD zugegriffen werden kann.

## Schritt 2: Stricheffekt mit Farbfüllung anwenden

Nachdem die PSD-Datei geladen wurde, besteht der nächste Schritt darin, den Stricheffekt auf die Bildebenen anzuwenden. Hier geschieht die wahre Magie.

Jede PSD-Datei kann mehrere Ebenen enthalten und Sie müssen den Effekt auf jede davon anwenden. So geht's:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

In dieser Schleife:

- `im.getLayers()`: Ruft alle Ebenen in der PSD-Datei ab.
- `StrokeEffect effect`: Extrahiert den auf die Ebene angewendeten Stricheffekt.
- `ColorFillSettings settings`: Ändert die Fülleinstellungen für den Stricheffekt.
- `settings.setColor(Color.getDeepPink())`: Legt die Strichfarbe auf Dunkelrosa fest. Sie können diese Farbe in jede gewünschte Farbe ändern.

## Schritt 3: Speichern Sie die geänderte PSD-Datei und exportieren Sie sie als PNG

Nachdem Sie den Stricheffekt angewendet haben, ist es an der Zeit, die Änderungen zu speichern und das Bild zu exportieren.

### 3.1 Speichern der PSD-Datei

Um die geänderte PSD-Datei zu speichern, verwenden Sie den folgenden Code:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

Dadurch wird die Datei mit dem angewendeten Stricheffekt im angegebenen Pfad gespeichert.

### 3.2 Als PNG exportieren

Um das Bild leichter zugänglich zu machen, können Sie es als PNG-Datei exportieren. So geht's:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

Dieser Codeausschnitt speichert das Bild als PNG mit Echtfarben und Alpha-Transparenz und macht es so bereit für die Verwendung in Webanwendungen oder anderen Plattformen.

## Abschluss

Das Anwenden eines Stricheffekts mit Farbfüllung auf Ihre PSD-Dateien mit Aspose.PSD für Java ist nicht nur unkompliziert, sondern auch unglaublich leistungsstark. Mit nur wenigen Codezeilen können Sie komplexe Bildverarbeitungsaufgaben automatisieren und so Zeit und Mühe sparen.

Egal, ob Sie an einer großen Menge an Bildern arbeiten oder nur ein paar Dateien optimieren müssen, diese Methode bietet eine flexible und effiziente Lösung. Nachdem Sie nun die Grundlagen beherrschen, können Sie mit verschiedenen Effekten und Anpassungen experimentieren, um Ihre Bilder wirklich hervorzuheben.

Bereit, es auszuprobieren? Schnappen Sie sich Ihre PSD-Beispieldatei und beginnen Sie noch heute damit, diese atemberaubenden Effekte hinzuzufügen!

## Häufig gestellte Fragen

### Kann ich mit Aspose.PSD für Java mehrere Effekte auf eine einzelne Ebene anwenden?
Ja, Sie können mehrere Effekte auf eine einzelne Ebene anwenden, indem Sie auf die Fülloptionen der Ebene zugreifen und die gewünschten Effekte hinzufügen.

### Ist es möglich, den Vorgang für einen Stapel PSD-Dateien zu automatisieren?
Auf jeden Fall! Sie können ein Verzeichnis mit PSD-Dateien durchsuchen, den Stricheffekt anwenden und die Ergebnisse automatisch speichern.

### Wie kann ich mit Aspose.PSD für Java an einer PSD-Datei vorgenommene Änderungen rückgängig machen?
Um Änderungen rückgängig zu machen, müssen Sie die ursprüngliche PSD-Datei neu laden, bevor Sie Änderungen speichern. In Aspose.PSD gibt es keine direkte Rückgängig-Funktion.

### Kann ich die Strichstärke und -position anpassen?
 Ja, Aspose.PSD für Java ermöglicht Ihnen die Anpassung der Strichstärke, Position und anderer Eigenschaften über die`StrokeEffect` Klasse.

### Ist die Nutzung der Aspose.PSD-Bibliothek für Java kostenlos?
 Aspose.PSD für Java bietet eine kostenlose Testversion, aber für den vollen Zugriff auf alle Funktionen müssen Sie eine Lizenz erwerben. Sie können die[Kaufoptionen](https://purchase.aspose.com/buy)auf ihrer Website.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
