---
date: 2026-06-13
description: Dowiedz się, jak narysować prostokąt w plikach PSD przy użyciu Aspose.PSD
  for Java. Ten przewodnik pokazuje kod krok po kroku, dodawanie warstw, przetwarzanie
  obrazów po stronie serwera oraz rysowanie kształtów.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Wykonaj proste rysowanie
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Jak narysować prostokąt w PSD przy użyciu Aspose.PSD for Java
url: /pl/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak narysować prostokąt w PSD przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

W tym samouczku odkryjesz **how to draw rectangle** kształty wewnątrz pliku Photoshop PSD przy użyciu czystej biblioteki Java Aspose.PSD. Niezależnie od tego, czy budujesz serwerowy potok zasobów, automatyzujesz tworzenie miniatur, czy dodajesz dynamiczną grafikę do istniejących projektów, poniższe kroki zapewnią kompletną, gotową do produkcji rozwiązanie. Omówimy tworzenie nowego dokumentu PSD, dodawanie warstwy, czyszczenie tła oraz ostateczne rysowanie zarówno czerwonych, jak i niebieskich prostokątów — wszystko bez uruchamiania Photoshopa.

## Szybkie odpowiedzi
- **Jaka jest podstawowa klasa do tworzenia pliku PSD?** `PsdImage`
- **Która metoda czyści kolor tła warstwy?** `Graphics.clear(Color)`
- **Jak narysować czerwony prostokąt?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna działa do testów; licencja jest wymagana w produkcji.
- **Czy mogę manipulować istniejącymi plikami PSD przy użyciu tego samego API?** Tak, Aspose.PSD obsługuje pełną edycję PSD.

## Co oznacza rysowanie czerwonego prostokąta w pliku PSD?

Rysowanie czerwonego prostokąta oznacza użycie obiektu `Graphics` do renderowania prostokątnego kształtu wypełnionego lub obrysowanego kolorem czerwonym na określonej warstwie obrazu PSD. Operacja ta jest powszechna przy podświetlaniu obszarów, tworzeniu symboli zastępczych lub dodawaniu prostych grafik programowo.

## Dlaczego warto używać Aspose.PSD dla Javy do manipulacji plikami PSD?

Aspose.PSD dla Javy obsługuje **ponad 50 formatów wejścia i wyjścia**, może przetwarzać wielostronicowe pliki PSD bez ładowania całego pliku do pamięci i działa na każdej platformie wspierającej Java 8 lub wyższą. Jego serwerowy silnik przetwarzania obrazów eliminuje potrzebę Photoshopa, zmniejsza koszty licencjonowania i umożliwia zautomatyzowane przepływy pracy obsługujące do **10 GB** danych obrazowych na godzinę na skromnej maszynie wirtualnej.

## Wymagania wstępne

- Zainstalowany Java Development Kit (JDK) 8 lub nowszy na Twoim komputerze.  
- Biblioteka Aspose.PSD dla Javy. Możesz ją pobrać z [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Importowanie pakietów

Instrukcje `import` wprowadzają wymagane klasy do zakresu, abyś mógł pracować z obrazami PSD, warstwami, kolorami i grafiką.

Klasa `PsdImage` jest głównym obiektem Aspose.PSD reprezentującym pojedynczy plik PSD w pamięci.  
`Graphics` udostępnia prymitywy rysunkowe, takie jak linie, prostokąty i elipsy.  
`Color` i `Pen` pozwalają określić kolory obrysu i ich grubość.  
Klasa `Layer` reprezentuje pojedynczą warstwę obrazu w dokumencie PSD.  
Klasa `Rectangle` definiuje pozycję i rozmiar prostokątnego obszaru używanego w operacjach rysowania.  
Klasa `SolidBrush` wypełnia kształty jednolitym kolorem.

## Jaki jest pierwszy krok do utworzenia dokumentu PSD?

Instancjujesz `PsdImage`, podając szerokość i wysokość płótna w pikselach, co tworzy pustą strukturę pliku PSD. Po skonfigurowaniu początkowych warstw lub tła, wywołujesz metodę `save` z ścieżką pliku, aby zapisać dokument na dysku. To przygotowuje obraz do kolejnych operacji edycyjnych.

## Krok 1: Utwórz nowy dokument

Najpierw utwórz nowy dokument PSD o żądanym rozmiarze płótna. Dokument będzie hostował warstwę, na której będziemy rysować.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Jak dodać nową pustą warstwę do obrazu PSD?

Najpierw utwórz nową instancję `Layer` o tej samej szerokości i wysokości co nadrzędny `PsdImage`. Następnie dodaj tę warstwę do kolekcji `Layers` obrazu przy użyciu metody `add`. Gdy warstwa stanie się częścią obrazu, pobierz jej obiekt `Graphics`, aby wykonać operacje rysunkowe; bez tego kroku rysunki nie będą widoczne.

## Krok 2: Dodaj warstwę

Następnie dodaj nową pustą warstwę obejmującą pełną szerokość i wysokość obrazu. Warstwy są niezbędne do oddzielenia operacji rysunkowych.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Jaki jest cel czyszczenia koloru tła warstwy?

Wywołanie `Graphics.clear` z określonym `Color` wypełnia całą warstwę tym kolorem, efektywnie resetując wszystkie dane pikseli. Zapewnia to usunięcie wszelkiej wcześniejszej zawartości i rozpoczęcie od znanego tła, co zapobiega nieoczekiwanej przezroczystości lub mieszaniu kolorów po otwarciu lub edycji PSD w Photoshopie.

## Krok 3: Rysowanie kształtów

Użyjemy klasy `Graphics` do manipulacji danymi pikseli warstwy. Poniżej trzy przykłady ilustrujące czyszczenie tła oraz rysowanie prostokątów w różnych kolorach.

### Wyczyść kolor warstwy (ustaw tło na żółte)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Narysuj czerwony prostokąt (główny cel)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Narysuj niebieski prostokąt (dodatkowy przykład)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Jak zapisać zmodyfikowany plik PSD na dysku?

Użyj metody `save` na obiekcie `PsdImage`, podając pełną ścieżkę pliku i opcjonalnie określając żądany format obrazu (domyślnie PSD). To zapisuje wszystkie warstwy, maski i polecenia rysunkowe w jednym pliku PSD zgodnym ze specyfikacją Photoshopa, umożliwiając jego otwarcie bez ostrzeżeń.

## Krok 4: Zapisz zmiany

Na koniec zapisz zmodyfikowany obraz PSD na dysku. Plik będzie zawierał nową warstwę i narysowane kształty.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Typowe problemy i rozwiązania

- **Warstwa niewidoczna po rysowaniu:** Upewnij się, że warstwa została dodana do obrazu **przed** utworzeniem obiektu `Graphics`. Powierzchnia rysunkowa musi być podłączona do prawidłowej warstwy.
- **Kolory wyglądają niepoprawnie:** Sprawdź, czy używasz `Color.getRed()` (lub `Color.getBlue()`), a nie tworzysz własną wartość RGB przekraczającą zakres 0‑255.
- **Plik nie został zapisany:** Zweryfikuj, czy ścieżka `outputDir` istnieje i aplikacja ma uprawnienia do zapisu. W systemie Linux może być konieczne dostosowanie własności folderu lub użycie `Files.createDirectories`.
- **Spowolnienie wydajności przy dużych plikach:** Skorzystaj z `setLoadOptions` klasy `PsdImage`, aby wczytać tylko wymagane kanały, zmniejszając zużycie pamięci przy PSD większych niż 200 MB.

## Najczęściej zadawane pytania

**Q1: Czy mogę używać Aspose.PSD dla Javy do manipulacji istniejącymi plikami PSD?**  
A1: Tak, Aspose.PSD dla Javy zapewnia rozbudowaną funkcjonalność edycji i manipulacji istniejącymi plikami PSD, w tym zmianę kolejności warstw, modyfikację masek i rysowanie wektorowe.

**Q2: Gdzie mogę znaleźć wsparcie dla Aspose.PSD dla Javy?**  
A2: Odwiedź [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) w celu uzyskania pomocy od społeczności i oficjalnych odpowiedzi Aspose.

**Q3: Czy dostępna jest darmowa wersja próbna Aspose.PSD dla Javy?**  
A3: Tak, wersję próbną możesz pobrać [tutaj](https://releases.aspose.com/). Próba zawiera wszystkie funkcje, ale dodaje znak wodny do zapisywanych plików.

**Q4: Jak mogę zakupić licencję na Aspose.PSD dla Javy?**  
A4: Licencję można nabyć na [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy). Opcje licencjonowania obejmują licencje wieczyste, subskrypcyjne oraz licencje sieciowe.

**Q5: Czy dostępne są licencje tymczasowe dla Aspose.PSD dla Javy?**  
A5: Tak, tymczasową licencję można uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

## Dodatkowe często zadawane pytania

**Q: Czy mogę rysować inne kształty oprócz prostokątów?**  
A: Tak, klasa `Graphics` obsługuje także rysowanie elips, linii oraz własnych ścieżek za pomocą metody `drawPath`.

**Q: Czy Aspose.PSD obsługuje przezroczystość w rysowanych kształtach?**  
A: Oczywiście; możesz użyć `SolidBrush` z kolorem ARGB, aby uwzględnić przezroczystość alfa, co umożliwia półprzezroczyste nakładki.

**Q: Czy można edytować krycie (opacity) warstwy?**  
A: Tak, każdy obiekt `Layer` posiada metodę `setOpacity`, przyjmującą wartość od 0 do 255, co pozwala na precyzyjną kontrolę przezroczystości warstwy.

**Q: Jak wczytać istniejący plik PSD zamiast tworzyć nowy?**  
A: Użyj `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` przed manipulacją warstwami. Wczytany obraz zachowuje wszystkie oryginalne warstwy i maski.

## Podsumowanie

Teraz opanowałeś **how to draw rectangle** kształty i manipulację warstwami w pliku PSD przy użyciu Aspose.PSD dla Javy. Tworząc dokument, dodając warstwę, czyszcząc jej tło i rysując przy pomocy API `Graphics`, możesz automatyzować niezliczone zadania graficzne po stronie serwera. Eksperymentuj z różnymi piórami, pędzlami i efektami warstw, aby rozwinąć tę bazę w pełnoprawne potoki generowania obrazów.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Jak rysować kształty w Javie – Podstawowe operacje na obrazach](/psd/java/basic-image-operations/)
- [Proste skalowanie z Aspose.PSD – Biblioteka do manipulacji obrazami w Javie](/psd/java/basic-image-operations/simple-resizing/)
- [Przycinanie obrazu prostokątem w Aspose.PSD dla Javy](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Ostatnia aktualizacja:** 2026-06-13  
**Testowano z:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose