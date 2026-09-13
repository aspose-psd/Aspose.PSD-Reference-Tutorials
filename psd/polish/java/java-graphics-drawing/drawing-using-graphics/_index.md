---
date: 2026-09-13
description: Dowiedz się, jak narysować elipsę i inne kształty w Javie z Aspose.PSD.
  Ten szczegółowy samouczek grafiki w Javie pokazuje gradient fills, polygon fills
  i image export.
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: Rysowanie przy użyciu Graphics w Javie
og_description: Dowiedz się, jak narysować elipsę w Javie przy użyciu Aspose.PSD.
  Ten samouczek grafiki w Javie obejmuje shape drawing, gradient fills, polygon filling
  oraz exporting images.
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: Jak narysować elipsę przy użyciu grafiki w Javie z Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: Jak narysować elipsę przy użyciu grafiki w Javie z Aspose.PSD
url: /pl/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak narysować elipsę przy użyciu grafiki w Javie z Aspose.PSD

## Wprowadzenie
W tym samouczku dotyczącym grafiki w Javie odkryjesz **jak narysować elipsę** oraz inne kształty programowo, korzystając z Aspose.PSD for Java. Niezależnie od tego, czy potrzebujesz generować dynamiczne miniatury, tworzyć własne elementy UI, czy automatyzować przepływy pracy projektowej, opanowanie rysowania elips i wypełnień gradientowych daje precyzyjną kontrolę wizualną. Poniższe kroki przeprowadzą Cię przez inicjalizację grafiki, konfigurowanie piór i pędzli oraz eksport wyniku do popularnych formatów obrazów.

## Szybkie odpowiedzi
- **Jakiej biblioteki wymaga?** Aspose.PSD for Java (pobierz ze strony oficjalnej).  
- **Na jakim kształcie koncentruje się samouczek?** Rysowanie elipsy i wypełnianie wielokąta.  
- **Czy mogę eksportować do formatów innych niż BMP?** Tak – obsługiwane są PNG, JPEG, TIFF i inne.  
- **Czy potrzebna jest licencja do rozwoju?** Tymczasowa darmowa licencja działa w testach; pełna licencja jest wymagana w produkcji.  
- **Czy API nadaje się do dużych obrazów?** Aspose.PSD przetwarza pliki do 500 MB bez ładowania całego bitmapa do pamięci.

## Jak narysować elipsę w Javie?
Wczytaj `PsdImage` o żądanej szerokości i wysokości, utwórz obiekt `Graphics`, ustaw `Pen` i wywołaj `drawEllipse` z prostokątem ograniczającym. Cała operacja wymaga tylko kilku wywołań metod i trwa poniżej sekundy dla typowych obrazów 800×600 na nowoczesnym sprzęcie.

## Co to jest Aspose.PSD dla Javy?
Aspose.PSD for Java to **czysto‑Java biblioteka, która zapewnia ponad 50 konwersji formatów obrazów oraz pełne możliwości edycji PSD** bez potrzeby Adobe Photoshop. Może renderować, modyfikować i eksportować wielowarstwowe pliki przy niskim zużyciu pamięci, co czyni ją idealną do generowania grafiki po stronie serwera.

## Dlaczego używać Aspose.PSD do rysowania kształtów?
Aspose.PSD oferuje wysoką wydajność, szerokie wsparcie formatów i precyzyjne renderowanie, co czyni ją idealną do generowania grafiki po stronie serwera i rysowania złożonych kształtów.

- **Wydajność:** Obsługuje obrazy do 500 MB przy zużyciu pamięci heap poniżej 150 MB (≈30 % mniej niż konkurencyjne biblioteki).  
- **Wsparcie formatów:** Ponad 50 formatów wejścia i wyjścia, w tym BMP, PNG, JPEG, TIFF i PSD.  
- **Precyzja:** Renderowanie sub‑pikselowe zapewnia ostre elipsy i płynne gradienty na wyświetlaczach wysokiej rozdzielczości.

## Wymagania wstępne
- Podstawowa znajomość programowania w Javie.  
- Zainstalowany Java Development Kit (JDK).  
- IDE, takie jak IntelliJ IDEA lub Eclipse.  
- Biblioteka Aspose.PSD for Java. Możesz ją pobrać z [pobranie Aspose.PSD Java](https://releases.aspose.com/psd/java/).

## Importowanie pakietów
Aby rozpocząć, zaimportuj niezbędne klasy Aspose.PSD oraz standardowe utilitety Javy. Poniższe klasy dostarczają prymitywy rysunkowe i obsługę kolorów:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Krok 1: utwórz obiekt obrazu
`PsdImage` reprezentuje w‑pamięci płótno rastrowe, na które można rysować i które można zapisać w różnych formatach.
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Krok 2: zainicjalizuj obiekt grafiki
`Graphics` to powierzchnia rysunkowa powiązana z `PsdImage`, umożliwiająca operacje wektorowe, takie jak rysowanie kształtów.
```java
Graphics graphics = new Graphics(image);
```

## Krok 3: wyczyść powierzchnię obrazu
`clear` wypełnia całe płótno jednym kolorem tła.
```java
graphics.clear(Color.getWhite());
```

## Krok 4: utwórz i skonfiguruj obiekt pióra
`Pen` definiuje kolor obrysu, szerokość i styl używany przy rysowaniu konturów.
```java
Pen pen = new Pen(Color.getBlue());
```

## Krok 5: rysuj kształty
`drawEllipse` renderuje elipsę, która mieści się w podanym prostokącie, używając bieżącego pióra.
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Krok 6: użyj pędzli do wypełniania
`LinearGradientBrush` tworzy wypełnienie gradientowe, które przechodzi między dwoma kolorami w określonym obszarze.
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Krok 7: zapisz zmodyfikowany obraz
`save` zapisuje `PsdImage` na dysku w wybranym formacie, takim jak BMP lub PNG.
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Typowe pułapki i rozwiązywanie problemów
- **NullPointerException przy grafice:** Upewnij się, że `PsdImage` jest w pełni zainicjowany przed utworzeniem obiektu `Graphics`.  
- **Nieprawidłowe kolory:** Użyj `Color.fromArgb`, aby określić dokładne wartości ARGB, gdy domyślna paleta nie spełnia oczekiwań.  
- **Spowolnienie przy dużych obrazach:** Włącz `PsdImageOptions` z `compression = CompressionType.Rle`, aby zmniejszyć obciążenie pamięci.

## Najczęściej zadawane pytania

**Q: Czy Aspose.PSD radzi sobie z zaawansowanymi manipulacjami obrazami?**  
A: Tak, obsługuje łączenie warstw, korekcję kanałów, renderowanie tekstu oraz zaawansowane maskowanie oprócz rysowania kształtów.

**Q: Czy Aspose.PSD jest odpowiedni dla aplikacji wysokiej wydajności?**  
A: Absolutnie; biblioteka jest zoptymalizowana pod kątem szybkości i może przetworzyć obraz 10 MP w mniej niż 2 sekundy na typowym serwerze.

**Q: Gdzie mogę znaleźć więcej przykładów i dokumentacji?**  
A: Odwiedź [dokumentację Aspose.PSD Java](https://reference.aspose.com/psd/java/) po kompleksowe przewodniki i referencje API.

**Q: Czy Aspose.PSD obsługuje wiele formatów obrazu przy eksporcie?**  
A: Tak, możesz eksportować do BMP, PNG, JPEG, TIFF, GIF oraz PSD i innych.

**Q: Jak mogę uzyskać wsparcie lub pomoc w razie problemów?**  
A: Skontaktuj się ze społecznością Aspose.PSD na [forum wsparcia](https://forum.aspose.com/c/psd/34) lub rozważ [tymczasową licencję](https://purchase.aspose.com/temporary-license/) dla priorytetowej pomocy.

---

**Ostatnia aktualizacja:** 2026-09-13  
**Testowano z:** Aspose.PSD for Java 24.10  
**Autor:** Aspose

## Powiązane samouczki

- [Zmienianie rozmiaru obrazu przy użyciu Aspose.PSD dla Javy – Rysowanie kształtów i podstawowe operacje na obrazie](/psd/java/basic-image-operations/)
- [Rysowanie i zapisywanie prostokąta w PSD przy użyciu Aspose.PSD dla Javy](/psd/java/basic-image-operations/simple-drawing/)
- [Dodaj podpis do obrazu – Rysuj obraz na płótnie z Aspose.PSD dla Javy](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}