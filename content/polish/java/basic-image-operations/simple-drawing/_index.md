---
title: Wykonaj proste rysowanie za pomocą Aspose.PSD dla Java
linktitle: Wykonaj prosty rysunek
second_title: Aspose.PSD API Java
description: Dowiedz się, jak rysować kształty w plikach PSD przy użyciu Aspose.PSD dla Java. Ten przewodnik krok po kroku opisuje tworzenie, dodawanie warstw i rysowanie za pomocą przykładów kodu.
type: docs
weight: 10
url: /pl/java/basic-image-operations/simple-drawing/
---
## Wstęp

Witamy w tym przewodniku krok po kroku dotyczącym wykonywania prostego rysowania przy użyciu Aspose.PSD dla Java! W tym samouczku omówimy podstawy tworzenia nowego dokumentu PSD, dodawania warstw i rysowania kształtów w różnych kolorach. Aspose.PSD dla Java to potężna biblioteka, która umożliwia programową manipulację plikami PSD, zapewniając szeroką funkcjonalność do zadań związanych z projektowaniem graficznym.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Zestaw Java Development Kit (JDK) zainstalowany na komputerze.
-  Aspose.PSD dla biblioteki Java. Można go pobrać z[Aspose.PSD dla dokumentacji Java](https://reference.aspose.com/psd/java/).

## Importuj pakiety

Aby rozpocząć, zaimportuj niezbędne pakiety do swojego projektu Java. Dołącz następujący kod na początku pliku Java:

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

Zacznijmy od utworzenia nowego dokumentu PSD o określonej szerokości i wysokości:

```java
//ExStart: Utwórz dokument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//Rozwiń: Utwórz dokument
```

## Krok 2: Dodaj warstwę

Dodajmy teraz warstwę do dokumentu za pomocą konstruktora bezargumentowego:

```java
//ExStart:Dodaj warstwę
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//Rozwiń:Dodaj warstwę
```

## Krok 3: Narysuj kształty

tym kroku wykorzystamy klasę Graphics do narysowania kształtów na utworzonej warstwie:

### Narysuj prostokąt żółtym kolorem

```java
//ExStart:RysujProstokątŻółty
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//Rozwiń:NarysujProstokątŻółty
```

### Narysuj czerwony prostokąt

```java
//ExStart: Narysuj czerwony prostokąt
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//Rozwiń:NarysujRedRectangle
```

### Narysuj niebieski prostokąt

```java
//ExStart: DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd: DrawBlueRectangle
```

## Krok 4: Zapisz zmiany

Na koniec zapisz kopię załadowanego pliku PSD wraz ze zmianami:

```java
//ExStart: Zapisz zmiany
image.save(outPsdFilePath);
//Rozwiń: Zapisz zmiany
```

## Wniosek

Gratulacje! Pomyślnie wykonałeś prosty rysunek przy użyciu Aspose.PSD dla Java. W tym samouczku omówiono tworzenie nowego dokumentu, dodawanie warstw i rysowanie prostokątów w różnych kolorach. Zachęcamy do zapoznania się z bardziej zaawansowanymi funkcjami oferowanymi przez bibliotekę na potrzeby projektowania graficznego.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.PSD dla Java do manipulowania istniejącymi plikami PSD?

O1: Tak, Aspose.PSD dla Java zapewnia rozbudowaną funkcjonalność do edycji i manipulowania istniejącymi plikami PSD.

### P2: Gdzie mogę znaleźć wsparcie dla Aspose.PSD dla Java?

 A2: Możesz odwiedzić[Aspose.PSD dla forum Java](https://forum.aspose.com/c/psd/34) w przypadku jakichkolwiek pytań związanych ze wsparciem.

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla Java?

 Odpowiedź 3: Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej.[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę kupić licencję na Aspose.PSD dla Java?

 A4: Możesz kupić licencję w witrynie[Strona zakupu Aspose.PSD](https://purchase.aspose.com/buy).

### P5: Czy dostępne są licencje tymczasowe dla Aspose.PSD dla Java?

 Odpowiedź 5: Tak, możesz uzyskać licencję tymczasową od[Tutaj](https://purchase.aspose.com/temporary-license/).