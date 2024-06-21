---
title: Rysowanie prostokątów w Javie
linktitle: Rysowanie prostokątów w Javie
second_title: Aspose.PSD API Java
description: Naucz się rysować prostokąty na obrazach za pomocą Aspose.PSD dla Java. Ten samouczek prowadzi programistów Java krok po kroku. Idealny do zadań związanych z manipulacją obrazami.
type: docs
weight: 17
url: /pl/java/java-graphics-drawing/drawing-rectangles/
---
## Wstęp
W świecie programowania w języku Java programowe manipulowanie i generowanie obrazów jest powszechnym wymogiem w różnych aplikacjach. Jednym z takich często spotykanych zadań jest rysowanie na obrazach kształtów przypominających prostokąty. Aspose.PSD dla Java zapewnia solidny zestaw narzędzi i funkcjonalności pozwalających efektywnie to osiągnąć. Ten samouczek poprowadzi Cię krok po kroku przez proces rysowania prostokątów na obrazie przy użyciu Aspose.PSD dla Java.
## Warunki wstępne
Zanim przejdziesz do samouczka, upewnij się, że masz skonfigurowane następujące wymagania wstępne:
### Środowisko programistyczne Java
Upewnij się, że masz zainstalowany zestaw Java Development Kit (JDK) w swoim systemie, najlepiej JDK 8 lub nowszy.
### Aspose.PSD dla Javy
 Musisz mieć bibliotekę Aspose.PSD dla Java. Można go pobrać z[Strona pobierania Aspose.PSD dla Java](https://releases.aspose.com/psd/java/) i postępuj zgodnie z instrukcjami instalacji zawartymi w ich dokumentacji.
## Importuj pakiety
Aby rozpocząć, zaimportuj niezbędne pakiety Aspose.PSD for Java do pliku Java:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Importy te umożliwią dostęp do klas i metod potrzebnych do rysowania prostokątów na obrazach.
## Krok 1: Utwórz nowy obraz
 Najpierw utwórz nową instancję pliku`PsdImage` klasa o określonej szerokości i wysokości.
```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Utwórz instancję BmpOptions i ustaw jej właściwości
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Utwórz instancję PsdImage o określonych wymiarach
Image image = new PsdImage(100, 100);
```
 Na tym etapie`PsdImage` jest inicjowany z szerokością i wysokością 100 pikseli każdy.
## Krok 2: Zainicjuj obiekt graficzny
 Następnie zainicjuj a`Graphics` obiekt za pomocą`image` utworzony w poprzednim kroku.
```java
// Zainicjuj obiekt graficzny
Graphics graphic = new Graphics(image);
```
 Ten`Graphics`obiekt będzie używany do wykonywania operacji rysowania na obrazie.
## Krok 3: Wyczyść powierzchnię graficzną
Wyczyść powierzchnię graficzną obrazu, używając określonego koloru.
```java
// Przezroczysta powierzchnia graficzna w kolorze żółtym
graphic.clear(Color.YELLOW);
```
Spowoduje to ustawienie tła obrazu na żółte.
## Krok 4: Narysuj prostokąty
Teraz narysuj prostokąty na obrazie, używając różnych kolorów i wymiarów.
```java
// Narysuj czerwony prostokąt
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Narysuj niebieski prostokąt
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Polecenia te rysują prostokąty o określonych kolorach (czerwonym i niebieskim) i położeniu na obrazie.
## Krok 5: Eksportuj obraz
Na koniec zapisz zmodyfikowany obraz w formacie pliku BMP.
```java
// Eksportuj obraz do formatu pliku BMP
image.save(outpath, saveOptions);
```
 Spowoduje to zapisanie obrazu z narysowanymi prostokątami do pliku BMP określonego przez`outpath`.

## Wniosek
Programowe rysowanie prostokątów na obrazach w Javie przy użyciu Aspose.PSD dla Java jest proste przy użyciu odpowiednich narzędzi i bibliotek. Wykonując ten samouczek, nauczyłeś się inicjować obraz, manipulować obiektami graficznymi, rysować kształty i zapisywać zmodyfikowany obraz do pliku. Eksperymentowanie z różnymi kształtami, kolorami i wymiarami jeszcze bardziej poszerzy wiedzę na temat manipulacji obrazami w Javie.
## Często zadawane pytania
### Czy Aspose.PSD dla Java obsługuje inne kształty oprócz prostokątów?
Aspose.PSD dla Java obsługuje oprócz prostokątów rysowanie różnych kształtów, takich jak elipsy, linie i wielokąty.
### Jak mogę zmodyfikować grubość obramowania prostokąta?
 Grubość obramowania prostokąta można dostosować, ustawiając opcję`Pen` właściwość grubości.
### Czy Aspose.PSD dla Java nadaje się do zadań przetwarzania obrazu o wysokiej wydajności?
Tak, Aspose.PSD dla Java jest przeznaczony do wysokowydajnego przetwarzania obrazów z rozbudowanymi funkcjami zarówno dla prostych, jak i złożonych operacji.
### Gdzie mogę znaleźć więcej przykładów i samouczków dla Aspose.PSD dla Java?
 Więcej przykładów i szczegółową dokumentację można znaleźć na stronie[Aspose.PSD dla dokumentacji Java](https://reference.aspose.com/psd/java/).
### Czy Aspose.PSD dla Java obsługuje inne formaty obrazów oprócz BMP?
Tak, Aspose.PSD dla Java obsługuje szeroką gamę formatów obrazów, w tym PNG, JPEG, TIFF i GIF.