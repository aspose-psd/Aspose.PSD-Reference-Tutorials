---
date: 2025-12-27
description: Naucz się rysować czerwony prostokąt i inne kształty w plikach PSD przy
  użyciu Aspose.PSD dla Javy. Ten przewodnik krok po kroku obejmuje tworzenie dokumentów,
  dodawanie warstw oraz rysowanie z przykładami kodu.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Rysuj czerwony prostokąt przy użyciu Aspose.PSD dla Javy
url: /pl/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Narysuj czerwony prostokąt przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

Witamy w tym przewodniku krok po kroku, jak **narysować czerwony prostokąt** przy użyciu Aspose.PSD dla Javy! W tym tutorialu przeprowadzimy Cię przez tworzenie nowego dokumentu PSD, dodawanie warstwy oraz rysowanie kształtów w niestandardowych kolorach. Niezależnie od tego, czy automatyzujesz zasoby graficzne, czy budujesz backend narzędzia do projektowania, ten tutorial dostarczy Ci niezbędnych elementów budujących.

## Szybkie odpowiedzi
- **Jaka jest podstawowa klasa do tworzenia pliku PSD?** `PsdImage`
- **Która metoda czyści kolor tła warstwy?** `Graphics.clear(Color)`
- **Jak narysować czerwony prostokąt?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna wystarczy do testów; licencja jest wymagana w produkcji.
- **Czy mogę manipulować istniejącymi plikami PSD przy użyciu tego samego API?** Tak, Aspose.PSD obsługuje pełną edycję PSD.

## Co oznacza rysowanie czerwonego prostokąta w pliku PSD?
Rysowanie czerwonego prostokąta oznacza użycie obiektu `Graphics` do wyrenderowania prostokątnego kształtu wypełnionego lub obrysowanego kolorem czerwonym na określonej warstwie obrazu PSD. Operacja ta jest powszechna przy podświetlaniu obszarów, tworzeniu placeholderów lub dodawaniu prostych grafik programowo.

## Dlaczego używać Aspose.PSD dla Javy do manipulacji plikami PSD?
Aspose.PSD dostarcza czysto‑Java API, które pozwala odczytywać, edytować i zapisywać pliki Photoshop PSD bez konieczności instalacji Photoshopa. Obsługuje zarządzanie warstwami, manipulację kolorami oraz rysowanie wektorowe, co czyni go idealnym rozwiązaniem do przetwarzania obrazów po stronie serwera, zautomatyzowanych potoków zasobów i generowania niestandardowych grafik.

## Wymagania wstępne

- Java Development Kit (JDK) zainstalowany na twoim komputerze.  
- Biblioteka Aspose.PSD dla Javy. Możesz ją pobrać z [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Importowanie pakietów

Aby rozpocząć, zaimportuj wymagane klasy do swojego projektu Java:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Krok 1: Utwórz nowy dokument

Najpierw utwórz nowy dokument PSD o żądanym rozmiarze płótna. Dokument ten będzie hostował warstwę, na której będziemy rysować.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Krok 2: Dodaj warstwę

Następnie dodaj nową pustą warstwę, która obejmuje pełną szerokość i wysokość obrazu. Warstwy są niezbędne do oddzielenia operacji rysowania.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Krok 3: Rysuj kształty

Użyjemy klasy `Graphics` do manipulacji danymi pikseli warstwy. Poniżej znajdują się trzy przykłady ilustrujące czyszczenie tła i rysowanie prostokątów w różnych kolorach.

### Wyczyść kolor warstwy (ustaw tło na żółte)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Narysuj czerwony prostokąt (główny cel)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Narysuj niebieski prostokąt (dodatkowy przykład)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Krok 4: Zapisz zmiany

Na koniec zapisz zmodyfikowany obraz PSD na dysku. Plik będzie zawierał nową warstwę oraz narysowane kształty.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Typowe problemy i rozwiązania

- **Warstwa niewidoczna po rysowaniu:** Upewnij się, że warstwa została dodana do obrazu **przed** utworzeniem obiektu `Graphics`.
- **Kolory wyglądają niepoprawnie:** Sprawdź, czy używasz `Color.getRed()` (lub innych metod statycznych), a nie własnych wartości RGB, które mogą być poza zakresem.
- **Plik nie został zapisany:** Potwierdź, że ścieżka `outputDir` istnieje i aplikacja ma uprawnienia do zapisu.

## Najczęściej zadawane pytania

### Q1: Czy mogę używać Aspose.PSD dla Javy do manipulacji istniejącymi plikami PSD?

A1: Tak, Aspose.PSD dla Javy zapewnia rozbudowaną funkcjonalność umożliwiającą edycję i manipulację istniejącymi plikami PSD.

### Q2: Gdzie mogę znaleźć wsparcie dla Aspose.PSD dla Javy?

A2: Możesz odwiedzić [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) w celu uzyskania pomocy związanej z wsparciem.

### Q3: Czy dostępna jest darmowa wersja próbna Aspose.PSD dla Javy?

A3: Tak, wersję próbną możesz pobrać [tutaj](https://releases.aspose.com/).

### Q4: Jak mogę zakupić licencję na Aspose.PSD dla Javy?

A4: Licencję możesz nabyć na [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy).

### Q5: Czy dostępne są licencje tymczasowe dla Aspose.PSD dla Javy?

A5: Tak, tymczasową licencję można uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

## Dodatkowe często zadawane pytania

**Q: Czy mogę rysować inne kształty oprócz prostokątów?**  
A: Tak, klasa `Graphics` obsługuje także rysowanie elips, linii i niestandardowych ścieżek.

**Q: Czy Aspose.PSD obsługuje przezroczystość w rysowanych kształtach?**  
A: Oczywiście; możesz użyć `SolidBrush` z kolorem ARGB, aby uwzględnić przezroczystość alfa.

**Q: Czy można edytować krycie (opacity) warstwy?**  
A: Tak, każdy obiekt `Layer` posiada metodę `setOpacity`, która przyjmuje wartość od 0 do 255.

**Q: Jak załadować istniejący plik PSD zamiast tworzyć nowy?**  
A: Użyj `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` przed manipulacją warstwami.

## Zakończenie

Teraz wiesz, jak **narysować czerwony prostokąt** oraz inne podstawowe kształty w pliku PSD przy użyciu Aspose.PSD dla Javy. Tworząc dokument, dodając warstwę, czyszcząc jej tło i rysując przy użyciu API `Graphics`, możesz zautomatyzować wiele zadań projektowania graficznego. Eksperymentuj dalej, testując różne pędzle, efekty warstw i formaty plików.

---

**Last Updated:** 2025-12-27  
**Testowano z:** Aspose.PSD for Java 24.12 (najnowsza w momencie pisania)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}