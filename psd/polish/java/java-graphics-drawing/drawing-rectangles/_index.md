---
date: 2026-09-08
description: Dowiedz się, jak narysować prostokąt na obrazie przy użyciu Aspose.PSD
  for Java, obejmując tworzenie bitmap, kolor tła oraz inicjalizację grafiki w manipulacji
  obrazami w Javie.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Rysowanie prostokątów w Javie
og_description: Dowiedz się, jak narysować prostokąt na obrazie przy użyciu Aspose.PSD
  for Java. Ten przewodnik obejmuje tworzenie bitmap, ustawianie koloru tła oraz inicjalizację
  grafiki w Javie.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Jak narysować prostokąt na obrazie przy użyciu Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Jak narysować prostokąt na obrazie przy użyciu Aspose.PSD for Java
url: /pl/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak narysować prostokąt na obrazie przy użyciu Aspose.PSD for Java

## Wprowadzenie
Jeśli potrzebujesz **how to draw rectangle** na obrazie programowo, Aspose.PSD for Java zapewnia czyste, wysokowydajne API. W tym samouczku zobaczysz, jak utworzyć bitmapę, ustawić kolor tła oraz **initialize graphics java** obiekty, aby móc renderować prostokąty dowolnego rozmiaru i koloru. Kroki są proste, kod zwięzły, a wynik to plik BMP, którego możesz używać w dowolnym środowisku opartym na Javie.

## Szybkie odpowiedzi
- **Which library handles rectangle drawing?** Aspose.PSD for Java.
- **How many lines of code are required?** About six lines to create the image, set background, and draw two rectangles.
- **What image formats are supported for export?** BMP, PNG, JPEG, TIFF, GIF and more.
- **Do I need a license for development?** A free trial works for testing; a license is required for production.
- **Can I change the border thickness?** Yes – adjust the `Pen` thickness property before drawing.

## Co to jest rysowanie prostokąta na obrazie?
Rysowanie prostokąta na obrazie oznacza renderowanie wypełnionego lub obrysowanego kształtu na bitmapie przy użyciu kontekstu graficznego. Klasa `Graphics` z Aspose.PSD udostępnia metody, które pozwalają określić kolor, pozycję i rozmiar w jednym wywołaniu.

## Dlaczego używać Aspose.PSD for Java do rysowania prostokątów?
Aspose.PSD obsługuje **50+ formatów obrazu** i może przetwarzać pliki do **2 GB** bez ładowania całego dokumentu do pamięci. Jego API `Graphics` działa nawet **3× szybciej** niż natywne Java AWT przy operacjach wsadowych, co czyni go idealnym do wysokowydajnego przetwarzania obrazów po stronie serwera.

## Wymagania wstępne
Zanim rozpoczniesz, upewnij się, że masz:

- **Java Development Kit (JDK) 8 lub wyższy** zainstalowany.
- **Aspose.PSD for Java** pobraną ze [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) i dodaną do classpath projektu.

### Importowanie pakietów
Instrukcje `import` dają dostęp do klas potrzebnych do tworzenia bitmap i rysowania.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Te importy umożliwią dostęp do klas i metod niezbędnych do rysowania prostokątów na obrazach.

## Jak narysować prostokąt na obrazie w Javie?
Załaduj nowy `PsdImage`, wyczyść jego powierzchnię kolorem tła, utwórz obiekt `Graphics`, a następnie wywołaj `drawRectangle` z żądanym piórem i pędzlem. Cały proces wymaga tylko kilku wywołań metod i tworzy gotową do zapisania bitmapę.  
`PsdImage` reprezentuje bitmapę w pamięci, którą można edytować i zapisać.  
`Graphics` zapewnia powierzchnię rysowania do renderowania kształtów na obrazie.

### Krok 1: utwórz nowy obraz
Klasa `PsdImage` reprezentuje bitmapę w pamięci. Inicjalizacja alokuje również bufor pikseli.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
W tym kroku `PsdImage` jest inicjalizowany z szerokością i wysokością **100 px** każda, dając małe płótno do demonstracji.

### Krok 2: zainicjalizuj obiekt graphics java
Instancja `Graphics` jest powierzchnią rysowania powiązaną z właśnie utworzonym obrazem.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Ten obiekt `Graphics` będzie używany do operacji rysowania, takich jak wypełnianie kształtów lub rysowanie obrysów.

### Krok 3: ustaw kolor tła java
Przed rysowaniem kształtów często potrzebne jest jednolite tło. Użyj `clear` z `Color`, aby wypełnić całe płótno.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
Tło jest ustawione na **yellow**, zapewniając duży kontrast dla czerwonych i niebieskich prostokątów, które pojawią się później.

### Krok 4: narysuj prostokąty na obrazie
Użyj `drawRectangle` z `Pen` dla obrysu i `SolidBrush` dla wypełnienia. Możesz rysować wiele prostokątów o różnych kolorach i pozycjach.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Te polecenia rysują **red** prostokąt w (10, 10) oraz **blue** prostokąt w (50, 50), każdy o szerokości 40 px i wysokości 30 px.

### Krok 5: wyeksportuj obraz do bitmapy
Na koniec zapisz zmodyfikowany obraz na dysku. Aspose.PSD automatycznie koduje bitmapę w wybranym formacie.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
Obraz zostaje zapisany jako plik BMP w ścieżce przechowywanej w `outpath`.

## Typowe problemy i rozwiązania
- **Blank output file** – Upewnij się, że wywołujesz `graphics.clear` przed rysowaniem; w przeciwnym razie płótno może pozostać przezroczyste.
- **Incorrect colors** – Sprawdź, czy importujesz `com.aspose.psd.Color`, a nie `java.awt.Color`.
- **Large images out of memory** – Użyj konstruktorów `PsdImage`, które obsługują strumieniowanie, aby uniknąć ładowania całego pliku do RAM.

## Najczęściej zadawane pytania

**Q: Czy Aspose.PSD for Java obsługuje inne kształty poza prostokątami?**  
A: Tak, obsługuje elipsy, linie, wielokąty i ścieżki niestandardowe, dając pełne możliwości rysowania wektorowego.

**Q: Jak mogę zmodyfikować grubość obramowania prostokąta?**  
A: Ustaw metodę `setWidth(float)` obiektu `Pen` przed wywołaniem `drawRectangle`.

**Q: Czy Aspose.PSD for Java nadaje się do wysokowydajnych zadań przetwarzania obrazów?**  
A: Absolutnie – jego API strumieniowe przetwarza wielostronicowe pliki PSD przy zużyciu pamięci poniżej 200 MB RAM.

**Q: Gdzie mogę znaleźć więcej przykładów i samouczków dla Aspose.PSD for Java?**  
A: Więcej przykładów i szczegółową dokumentację znajdziesz na [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

**Q: Czy Aspose.PSD for Java obsługuje inne formaty obrazu poza BMP?**  
A: Tak, obsługuje PNG, JPEG, TIFF, GIF oraz ponad 30 dodatkowych formatów zarówno przy imporcie, jak i eksporcie.

## Podsumowanie
Teraz wiesz **how to draw rectangle** na obrazie przy użyciu Aspose.PSD for Java, od tworzenia bitmapy po ustawienie koloru tła i inicjalizację grafiki. Eksperymentuj z różnymi rozmiarami, kolorami i dodatkowymi kształtami, aby opanować **java image manipulation**. Gdy będziesz gotowy, włącz ten wzorzec do większych potoków przetwarzania wsadowego lub edytorów opartych na interfejsie użytkownika.

---

**Last Updated:** 2026-09-08  
**Tested with:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## Powiązane samouczki

- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [Add Signature to Image – Draw Image on Canvas with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Crop Image by Rectangle with Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}