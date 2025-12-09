---
date: 2025-12-01
description: Erfahren Sie, wie Sie in Java mit dem Bicubic‑Resampler von Aspose.PSD
  eine hochwertige Bildskalierung erreichen. Folgen Sie unserer Schritt‑für‑Schritt‑Anleitung
  für erstklassige Ergebnisse.
linktitle: Implement Bicubic Resampler
second_title: Aspose.PSD Java API
title: Hochqualitative Bildskalierung mit bikubischem Resampler in Aspose.PSD für
  Java
url: /de/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hochqualitative Bildskalierung mit dem Bicubic Resampler in Aspose.PSD für Java

## Einführung

Hochqualitative Bildskalierung ist ein häufiges Bedürfnis, wenn Sie Grafiken ohne Verlust der visuellen Treue verkleinern oder vergrößern müssen. Aspose.PSD für Java bietet einen **Bicubic Resampler**, der für PSD‑Dateien und andere unterstützte Formate glatte, scharfe Ergebnisse liefert. In diesem Tutorial lernen Sie Schritt für Schritt, wie Sie den Bicubic Resampler implementieren, sodass Sie noch heute hochqualitative Bildskalierung in Ihre Java‑Anwendungen integrieren können.

## Schnellantworten
- **Was macht der Bicubic Resampler?** Er wendet einen ausgefeilten Interpolationsalgorithmus an, der beim Skalieren von Bildern Details bewahrt.  
- **Welche ResizeType‑Werte stehen zur Verfügung?** `CubicConvolution` und `Bell` sind die beiden Bicubic‑Optionen, die von Aspose.PSD bereitgestellt werden.  
- **Benötige ich eine Lizenz, um den Code auszuführen?** Eine temporäre Lizenz reicht für die Evaluierung; für den Produktionseinsatz ist eine Voll‑Lizenz erforderlich.  
- **Welche Java‑Version wird benötigt?** Jede Java‑8+ Runtime ist mit der neuesten Aspose.PSD‑Bibliothek kompatibel.  
- **Kann ich andere Formate (PNG, JPEG) mit derselben API skalieren?** Ja, Aspose.PSD unterstützt mehrere Bildtypen, obwohl sich die Beispiele auf PSD konzentrieren.

## Was ist hochqualitative Bildskalierung?

Hochqualitative Bildskalierung bedeutet, ein Bild zu verändern, während scharfe Kanten, sanfte Verläufe und eine akkurate Farbdarstellung erhalten bleiben. Der Bicubic Resampler erreicht dies, indem er die Werte benachbarter Pixel (unter Verwendung von Cubic Convolution oder dem Bell‑Algorithmus) berücksichtigt, um jedes neue Pixel zu berechnen. Das Ergebnis wirkt natürlicher als bei Methoden wie Nearest‑Neighbor oder Bilinear.

## Warum den Bicubic Resampler für hochqualitative Bildskalierung verwenden?

- **Bewahrt Details:** Feine Texturen und Linien bleiben auch nach erheblichen Größenänderungen klar erkennbar.  
- **Reduziert Artefakte:** Minimiert Ringing und Unschärfe, die bei einfacheren Algorithmen häufig auftreten.  
- **Einfache Integration:** Der einzeilige Methodenaufruf (`image.resize`) ermöglicht den Wechsel zwischen Algorithmen, ohne Code neu schreiben zu müssen.  

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.PSD für Java** – laden Sie die neueste JAR von der [Aspose.PSD für Java Dokumentation](https://reference.aspose.com/psd/java/) herunter.  
- **Java Development Kit** – JDK 8 oder neuer installiert und konfiguriert.  
- **Beispiel‑PSD‑Datei** – ein Testbild (z. B. `sample_bicubic.psd`) in einem bekannten Verzeichnis abgelegt.

## Pakete importieren

Fügen Sie die erforderlichen Importe zu Ihrer Java‑Klasse hinzu. Diese bringen die Kernklassen von Aspose.PSD und die Aufzählung `ResizeType` ein.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Schritt 1: Bild laden

Laden Sie zunächst die Quell‑PSD‑Datei, die Sie skalieren möchten. Ersetzen Sie `Your Document Directory` durch den tatsächlichen Pfad auf Ihrem Rechner.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

## Schritt 2: Skalieren mit Cubic Convolution (hohe Qualität)

Wenden Sie nun den **Cubic Convolution**‑Algorithmus an, eine der beiden Bicubic‑Optionen, die hochqualitative Bildskalierung liefert. Das Beispiel skaliert das Bild auf 300 × 300 Pixel.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

## Schritt 3: Skalieren mit Bell‑Algorithmus (alternative hohe Qualität)

Falls Sie den **Bell**‑Algorithmus bevorzugen, der einen leicht anderen Glättungseffekt bietet, können Sie ihn auf dieselbe Weise verwenden. Beachten Sie, dass wir das Originalbild erneut laden, um einen fairen Vergleich zu ermöglichen.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

Experimentieren Sie gern mit anderen Abmessungen oder Dateiformaten – passen Sie einfach die Parameter an.

## Häufige Stolperfallen & Tipps

- **Falscher Pfad:** Stellen Sie sicher, dass `dataDir` mit einem Dateiseparator (`/` oder `\`) endet, der zu Ihrem Betriebssystem passt.  
- **Lizenz‑Ausnahmen:** Das Ausführen ohne gültige Lizenz kann ein Wasserzeichen zum Ausgabebild hinzufügen.  
- **Speicherverbrauch:** Große PSD‑Dateien können erheblichen Speicher beanspruchen; erwägen Sie, Bilder nach dem Speichern zu entsorgen (`image.dispose()`).

## Häufig gestellte Fragen

**F: Kann ich Aspose.PSD für Java mit anderen Bildformaten verwenden?**  
A: Ja, die Bibliothek unterstützt PSD, PNG, JPEG, TIFF, BMP und viele weitere.

**F: Gibt es eine temporäre Lizenz für Aspose.PSD für Java?**  
A: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**F: Wo finde ich Support für Aspose.PSD für Java?**  
A: Besuchen Sie das Aspose.PSD‑Forum [hier](https://forum.aspose.com/c/psd/34) für supportbezogene Anfragen.

**F: Kann ich die Aspose.PSD‑Bibliothek für Java herunterladen?**  
A: Ja, laden Sie die Bibliothek von der Release‑Seite [hier](https://releases.aspose.com/psd/java/) herunter.

**F: Wie kann ich Aspose.PSD für Java erwerben?**  
A: Sie können Aspose.PSD für Java über die Kaufseite [hier](https://purchase.aspose.com/buy) erwerben.

---

**Zuletzt aktualisiert:** 2025-12-01  
**Getestet mit:** Aspose.PSD für Java 24.11 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}