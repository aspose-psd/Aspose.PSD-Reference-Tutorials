---
date: 2026-01-17
description: Dowiedz się, jak w Javie rysować łuki przy użyciu Aspose.PSD for Java.
  Samouczek krok po kroku z przykładami kodu dla aplikacji graficznych.
linktitle: Java Graphics Draw Arc with Aspose.PSD
second_title: Aspose.PSD Java API
title: Java Graphics – rysowanie łuku z Aspose.PSD – przewodnik krok po kroku
url: /pl/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Graphics Draw Arc with Aspose.PSD

## Introduction
W tym samouczku dowiesz się, jak **java graphics draw arc** przy użyciu biblioteki Aspose.PSD for Java. Rysowanie łuków programowo jest przydatne przy tworzeniu własnych komponentów UI, wizualizacji danych lub dowolnej grafiki wymagającej precyzyjnej kontroli krzywej. Przeprowadzimy Cię przez każdy krok — od konfiguracji projektu po renderowanie łuku i zapis wyniku — abyś mógł od razu dodać tę funkcjonalność do swoich aplikacji Java.

## Quick Answers
- **Which library lets Java draw arcs easily?** Aspose.PSD for Java.  
- **Do I need a license for development?** A free trial works for testing; a license is required for production.  
- **What output formats are supported?** BMP, PNG, JPEG, TIFF, GIF, and more.  
- **Can I change arc thickness or color?** Yes—adjust the `Pen` object properties.  
- **Is the code compatible with Java 8+?** Absolutely, the API targets Java 8 and newer.

## What is “java graphics draw arc”?
Wyrażenie odnosi się do użycia kodu Java do renderowania zakrzywionego odcinka (łuku) na płótnie graficznym. Dzięki Aspose.PSD zyskujesz wysokopoziomową klasę `Graphics`, która upraszcza operacje rysowania, zarządzanie kolorami, antyaliasing i eksport plików w tle.

## Why use Aspose.PSD for arc drawing?
- **Full PSD support** – Twórz lub edytuj pliki Photoshop bez zainstalowanego Photoshopa.  
- **Rich drawing API** – Metody takie jak `drawArc` pozwalają określić rozmiar, kąty i styl w jednym wywołaniu.  
- **Cross‑format export** – Zapisz swój łuk do BMP, PNG, JPEG itp. za pomocą kilku linii kodu.  
- **Performance‑focused** – Optymalizowane pod kątem dużych obrazów i przetwarzania wsadowego.

## Prerequisites
1. **Java Development Environment** – Zainstaluj Java (JDK 8 lub nowszy). Pobierz ją ze [strony Oracle](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java** – Pobierz bibliotekę ze [strony pobierania](https://releases.aspose.com/psd/java/) i dodaj plik JAR do classpath projektu.

## Import Packages
Najpierw zaimportuj wymagane klasy Aspose.PSD:

```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

Te importy dają dostęp do definicji kolorów, narzędzi rysunkowych, kontenerów obrazu oraz opcji zapisu plików.

## Step‑by‑Step Guide

### Step 1: Set Up Your Java Project
Utwórz nowy projekt Maven lub Gradle, dodaj JAR Aspose.PSD i sprawdź, czy IDE poprawnie rozpoznaje importy.

### Step 2: Initialize Image and Graphics Objects
Stwórz pusty obiekt `PsdImage` i instancję `Graphics`, na której będziesz rysować:

```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```

Zastąp `"Your Document Directory"` folderem, w którym ma zostać zapisany plik wyjściowy.

### Step 3: Define Arc Parameters
Określ wymiary i kąty definiujące łuk:

```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```

Śmiało modyfikuj te liczby, aby dopasować styl wizualny do własnych potrzeb.

### Step 4: Draw and Save the Arc
Użyj metody `drawArc`, a następnie wyeksportuj obraz:

```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

Kod rysuje czarny łuk na żółtym tle i zapisuje wynik do `Arc.bmp`. Zmien `outputPath` oraz `BmpOptions`, jeśli wolisz inny format lub jakość.

## Common Issues & Solutions
- **File not found error** – Upewnij się, że `dataDir` kończy się separatorem ścieżki (`/` lub `\\`) i że katalog istnieje.  
- **Arc appears as a line** – Sprawdź, czy `width` i `height` są większe od zera oraz czy `sweepAngle` nie jest wielokrotnością 360° (co spowodowałoby pełną elipsę).  
- **Color not applied** – Użyj `new Pen(Color.getRed())` lub ustaw `pen.setWidth(2)`, aby efekt był wyraźniejszy.

## Frequently Asked Questions

**Q: Can Aspose.PSD for Java handle other shapes besides arcs?**  
A: Yes, it supports rectangles, ellipses, lines, and custom paths via the same `Graphics` API.

**Q: How do I change the arc’s thickness or color?**  
A: Create a `Pen` with the desired `Color` and `Width` (e.g., `new Pen(Color.getBlue(), 3)`) and pass it to `drawArc`.

**Q: Is it possible to export the arc to formats other than BMP?**  
A: Absolutely. Use `PngOptions`, `JpegOptions`, `TiffOptions`, etc., instead of `BmpOptions`.

**Q: Where can I find more examples and support?**  
A: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community help, official documentation, and code samples.

## Conclusion
Masz teraz kompletny, gotowy do produkcji przykład, jak **java graphics draw arc** przy użyciu Aspose.PSD for Java. Dostosowując parametry, ustawienia pióra i opcje wyjściowe, możesz wprowadzić własne łuki do dowolnego przepływu pracy graficznego opartego na Javie.

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}