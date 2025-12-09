---
date: 2025-12-02
description: Erfahren Sie, wie Sie ein Bild auf einer Leinwand zeichnen und eine Signatur
  in Java mit Aspose.PSD überlagern. Folgen Sie diesem Schritt‑für‑Schritt‑Java‑Bildverarbeitungs‑Tutorial
  und speichern Sie das Ergebnis als PNG.
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: Bild auf Canvas zeichnen – Signatur hinzufügen mit Aspose.PSD für Java
url: /de/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bild auf Canvas zeichnen – Signatur hinzufügen mit Aspose.PSD für Java

## Einführung

Das Hinzufügen einer handschriftlichen oder digitalen Signatur zu einem Bild ist ein häufiges Bedürfnis bei Verträgen, Rechnungen oder anderen Dokumenten, die einen Authentizitätsnachweis erfordern. Mit **Aspose.PSD für Java** können Sie **ein Bild auf Canvas zeichnen** und die Signatur wie jede andere Überlagerungsschicht behandeln. In diesem **Java‑Bildverarbeitungs‑Tutorial** gehen wir den gesamten Workflow durch – vom Laden des Basisbildes und der Signaturdatei, über die Initialisierung der Grafik, das Zeichnen der Überlagerung bis hin zum **Speichern des Bildes im PNG‑Format**.

## Schnelle Antworten
- **Was bedeutet „ein Bild auf Canvas zeichnen“?** Es bezeichnet das Rendern eines Bildes auf ein anderes mithilfe der `Graphics`‑Klasse.  
- **Wie füge ich in Java eine Signatur hinzu?** Laden Sie die Signaturdatei als `Image` und verwenden Sie `Graphics.drawImage`.  
- **Welche Aspose.PSD‑Version wird benötigt?** Jede aktuelle 24.x‑Version; der Code funktioniert mit der neuesten Bibliothek.  
- **Kann ich mehrere Bilder überlagern?** Ja – wiederholen Sie den Aufruf von `drawImage` mit unterschiedlichen Quellen.  
- **Benötige ich eine Lizenz?** Eine Testversion reicht für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.

## Was bedeutet „Bild auf Canvas zeichnen“?
In der Terminologie von Aspose.PSD bedeutet das Zeichnen eines Bildes auf einem Canvas, ein `Image`‑Objekt auf ein anderes mithilfe eines `Graphics`‑Kontexts zu malen. Dieser Vorgang ist das Rückgrat von **Overlay‑Techniken in Java** wie dem Hinzufügen von Wasserzeichen, Logos oder Signaturen.

## Warum Aspose.PSD für das Überlagern einer Signatur verwenden?
- **Vollständige PSD‑Unterstützung** – funktioniert mit Ebenen, Masken und Transparenz.  
- **Keine nativen OS‑Abhängigkeiten** – reines Java, ideal für serverseitige Verarbeitung.  
- **Hochleistungs‑Rendering** – optimiert für große Dateien und komplexe Kompositionen.  

## Voraussetzungen
- Java Development Kit (JDK) 8 oder höher.  
- Aspose.PSD für Java‑JAR in den Klassenpfad Ihres Projekts eingebunden.  
- Zwei Bilddateien: ein Basisbild (z. B. `layers.psd`) und eine Signaturgrafik (`sample.psd`).  

## Pakete importieren

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Schritt 1: Primäres und sekundäres Bild laden

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro‑Tipp:** Halten Sie beide Bilder im gleichen Farbmodus (RGB), um unerwartete Farbverschiebungen beim Zeichnen zu vermeiden.

## Schritt 2: Grafik initialisieren (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

Das `Graphics`‑Objekt wirkt wie ein Pinsel, mit dem Sie **ein Bild auf Canvas zeichnen** können. Durch die Initialisierung mit dem primären `Image` werden alle nachfolgenden Zeichenbefehle auf dieses Canvas bezogen.

## Schritt 3: Signatur zum Bild hinzufügen (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

In diesem Snippet **überlagern wir Bilder in Java**, indem wir die Signatur in der rechten unteren Ecke platzieren. Passen Sie die `Point`‑Werte an, falls Sie eine andere Position wünschen.

## Häufige Probleme & Lösungen
| Symptom | Ursache | Lösung |
|---------|---------|--------|
| Signatur erscheint verzerrt | Unterschiedliche DPI zwischen Canvas und Signatur | Verwenden Sie `signature.resize` vor dem Zeichnen oder stellen Sie sicher, dass beide Dateien dieselbe DPI besitzen. |
| Ausgabedatei ist sehr groß | Speichern ohne Kompression | Übergeben Sie ein konfiguriertes `PngOptions` mit einem höheren `CompressionLevel`. |
| Nichts wird gezeichnet | Grafik nicht freigegeben | Rufen Sie nach dem Zeichnen `graphics.dispose()` auf (optional, aber empfehlenswert). |

## Fazit

Durch die Befolgung dieser Schritte haben Sie gelernt, **wie man ein Bild auf Canvas zeichnet** und nahtlos **eine Signatur hinzufügt** mit Aspose.PSD für Java. Diese Technik lässt sich leicht auf Wasserzeichen, Logos oder andere Überlagerungs‑Grafiken ausweiten und verleiht Ihren Java‑Anwendungen leistungsstarke **Java‑Bildverarbeitungs‑Funktionen**.

## FAQ

### Q1: Kann ich mehrere Signaturen zu einem Bild hinzufügen?

A1: Ja, Sie können mehrere Signaturen hinzufügen, indem Sie die Schritte mit unterschiedlichen Signatur‑Bildern wiederholen.

### Q2: Unterstützt Aspose.PSD weitere Bildformate?

A2: Ja, Aspose.PSD unterstützt ein breites Spektrum an Bildformaten und bietet damit Flexibilität bei der Bildverarbeitung.

### Q3: Wird für die Nutzung von Aspose.PSD für Java eine Lizenz benötigt?

A3: Ja, für die Verwendung von Aspose.PSD benötigen Sie eine gültige Lizenz. Weitere Informationen finden Sie unter [Aspose.PSD kaufen](https://purchase.aspose.com/buy).

### Q4: Wie erhalte ich Support für Aspose.PSD?

A4: Besuchen Sie das [Aspose.PSD‑Forum](https://forum.aspose.com/c/psd/34) für Community‑Support und Diskussionen.

### Q5: Kann ich Aspose.PSD für Java vor dem Kauf testen?

A5: Ja, Sie können eine [kostenlose Testversion](https://releases.aspose.com/) erhalten, um die Funktionen vor dem Kauf zu prüfen.

## Weitere häufig gestellte Fragen

**F: Wie ändere ich die Deckkraft der Signatur?**  
A: Verwenden Sie `graphics.setOpacity(float opacity)` vor dem Aufruf von `drawImage`. Werte liegen zwischen 0,0 (transparent) und 1,0 (undurchsichtig).

**F: Ist es möglich, die Signatur zu drehen?**  
A: Ja – wenden Sie vor dem Zeichnen eine Transformationsmatrix über `graphics.rotateTransform(angle)` an.

**F: Kann ich die Signatur auf ein JPEG statt auf ein PNG zeichnen?**  
A: Absolut. Ersetzen Sie `PngOptions` durch `JpegOptions` und geben Sie das gewünschte Qualitätsniveau an.

---

**Zuletzt aktualisiert:** 2025-12-02  
**Getestet mit:** Aspose.PSD für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}